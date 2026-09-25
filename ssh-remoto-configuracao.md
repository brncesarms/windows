---
title: "Windows Remoto: Configuração Pós-Formatação via SSH"
date_created: 2026-08-31
tags:
  - windows/ssh
  - windows/remoto
  - infraestrutura
---

# 🖥️ Windows Remoto: Configuração Pós-Formatação via SSH

> [!info] Parceria de trabalho
> O **Bruno formata fisicamente** o computador (Windows 11) e o **agente configura de forma remota via SSH** (OpenSSH Server + PowerShell). Este guia padroniza esse fluxo.

---

## 🔌 Passo 0 — O que o Bruno faz antes (fisicamente)

1. Conecta o PC à **internet/rede local**.
2. Informa ao agente o **IP ou hostname**, o **usuário** e como autenticar (senha ou chave SSH).

> [!tip] Ativar OpenSSH Server (roda localmente no PC antes de desconectar, como admin)
> ```powershell
> Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
> Start-Service sshd
> Set-Service -Name sshd -StartupType 'Automatic'
> ```

---

## 🔗 Passo 1 — Conectar via SSH (a partir do Linux do Bruno)

```bash
ssh usuario@IP_DO_PC
```

- Por padrão o OpenSSH do Windows abre **PowerShell** (em vez de bash). Para garantir:
  ```powershell
  # No PC remoto (uma única vez):
  New-ItemProperty -Path "HKLM:\SOFTWARE\OpenSSH" -Name DefaultShell -Value "C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe" -PropertyType String -Force
  ```
- Execução de comando único:
  ```bash
  ssh usuario@IP "powershell.exe -NoProfile -Command \"Get-ComputerInfo\""
  ssh usuario@IP "cmd /c hostname"
  ```
- Para sessão sem senha a cada vez: `ssh-copy-id usuario@IP` antes.

---

## ✅ Passo 2 — Checklist de configuração pós-formatação

> [!warning] Honestidade
> O agente **nunca diz que fez o que não fez**. Sempre executa o comando, vê a saída real e só então relata.

1. **Identificar o sistema**
   ```powershell
   hostname
   Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion, OsBuildNumber
   Get-NetIPConfiguration | Select-Object InterfaceAlias, IPv4Address
   ```

2. **Windows Update**
   ```powershell
   Start-Service wuauserv
   (New-Object -ComObject Microsoft.Update.AutoUpdate).DetectNow()
   ```

3. **Habilitar execução de scripts PowerShell**
   ```powershell
   Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
   Get-ExecutionPolicy -List
   ```

4. **Gerenciadores de pacote**
   - **Winget** (nativo Win11): `winget --version`
   - **Chocolatey** (se pedido): ver [Chocolatey](./18_chocolatey.md)

5. **Programas essenciais** (exemplos winget)
   ```powershell
   winget install --accept-source-agreements --accept-package-agreements Google.Chrome
   winget install --accept-source-agreements --accept-package-agreements Microsoft.VisualStudioCode
   winget install --accept-source-agreements --accept-package-agreements VideoLAN.VLC
   ```

6. **Privacidade/ajustes** (somente se pedido)
   - Tema escuro: [Ativar tema escuro](./14_ativar_tema_escuro.md)
   - Desativar histórico de atividades: [Desativar histórico](./15_desativar_historico_atividades_do_windows.md)

7. **Verificação/reparo** (se houver problema)
   - `sfc /scannow` e DISM: [SFC & DISM](./10_sfc_dism.md)

---

## ⚠️ Armadilhas

- Windows SSH usa **PowerShell/CMD**, não bash → use `powershell.exe -Command "..."` ou `cmd /c`.
- **Não reinicie o PC remoto sem avisar** o Bruno (perde a sessão).
- Prefira `Set-ExecutionPolicy RemoteSigned` em vez de `Unrestricted`.
- Confirmar conectividade antes de declarar sucesso: `ssh usuario@IP "echo ok"`.

---

## 🔗 Notas Relacionadas
- [Guia Principal de Windows](./README.md)
- [SSH para Ollama/Proxmox](../proxmox/ollama--guia-acesso-ssh.md)
- [T.I. — Mapa de Conteúdo](../README.md)
