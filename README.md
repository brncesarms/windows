---
title: "Windows Systems Engineering & Administration Runbooks"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows
  - powershell
  - devops
  - sysadmin
---

# 🪟 Windows Systems Engineering & Administration Runbooks

[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20%7C%20Server-0078D6?logo=windows&logoColor=white)](#)
[![Shell](https://img.shields.io/badge/Shell-PowerShell%207%2B%20%7C%20WindowsPowerShell-5391FE?logo=powershell&logoColor=white)](#)
[![Package Manager](https://img.shields.io/badge/Package%20Manager-WinGet%20%7C%20Chocolatey-blue)](#)
[![Access](https://img.shields.io/badge/Remote%20Access-OpenSSH%20Server-4EAA25)](#)
[![Obsidian](https://img.shields.io/badge/Knowledge%20Base-Obsidian-483699?logo=obsidian&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](#)

> [!NOTE]
> **Repositório Oficial de Engenharia de Sistemas Windows**  
> Runbooks determinísticos, automações PowerShell, gerenciamento declarativo de pacotes, procedimentos de hardening, diagnóstico aprofundado e administração remota via OpenSSH nativo.

---

## 🎯 Visão Geral & Filosofia

Este repositório consolida as melhores práticas de administração e engenharia para ambientes Windows (Workstations e Servidores). O foco é transformar procedimentos manuais repetitivos em **runbooks previsíveis, scripts reutilizáveis e configurações declarativas**, reduzindo o tempo de setup pós-formatação de horas para poucos minutos.

### Principais Pilares
1. **Automação First**: Instalação e atualização de softwares via gerenciadores de pacotes CLI (`winget`, `choco`).
2. **Gerenciamento Remoto Headless**: Configuração completa e diagnóstico de máquinas via **OpenSSH + PowerShell Remoting**.
3. **Hardening & Otimização**: Remoção de bloatware, desativação de telemetria invasiva e otimização de energia para estações de alta demanda.
4. **Resiliência & Diagnóstico**: Rotinas preventivas e corretivas de integridade do sistema operacional (`SFC`, `DISM`, `CHKDSK`).

---

## 📚 Índice Temático dos Runbooks

### 🚀 1. Automação, Scripting & Gerenciadores de Pacote
| Runbook | Descrição | Ferramentas |
| :--- | :--- | :--- |
| [**01. Habilitar Execução de Scripts**](01_habilitar_execucao_scripts_powershell.md) | Configuração segura de `ExecutionPolicy` no PowerShell (`RemoteSigned`). | `Set-ExecutionPolicy` |
| [**17. Gerenciador de Pacotes WinGet**](17_winget.md) | Guia completo de instalação e atualização em lote com WinGet CLI. | `winget` |
| [**18. Gerenciador de Pacotes Chocolatey**](18_chocolatey.md) | Provisionamento automatizado de utilitários de TI e dependências com Chocolatey. | `choco` |
| [**19. Script de Desbloat Win11Debloat**](19_win11debloat.md) | Hardening e limpeza profunda de bloatware, telemetria e widgets do Win 11. | `Win11Debloat`, `PowerShell` |

### 🛡️ 2. Segurança, Identidade & Gerenciamento Remoto
| Runbook | Descrição | Ferramentas |
| :--- | :--- | :--- |
| [**20. Configuração Remota via SSH**](20_ssh_remoto_configuracao.md) | Setup completo pós-formatação com OpenSSH Server nativo e PowerShell Core. | `sshd`, `ssh-copy-id`, `Win32-OpenSSH` |
| [**02. Exibir Hostname e Contas**](02_exibir_nome_computador_e_usuarios.md) | Identificação rápida do host, build do OS e inventário de usuários ativos. | `hostname`, `net user`, `whoami` |
| [**04. Adicionar Credenciais de Rede**](04_add_credenciais.md) | Gestão segura de credenciais de compartilhamento SMB e servidores no cofre Windows. | `cmdkey` |
| [**05. Habilitar Usuário Administrador**](05_habilitar_usuario_administrador.md) | Ativação controlada da conta local interna de Administrador para suporte. | `net user administrator` |
| [**06. Gerenciar Usuários Locais**](06_gerenciar_usuarios.md) | Criação, alteração de credenciais e inclusão em grupos administrativos. | `net user`, `net localgroup` |
| [**11. Atualizar Políticas de Grupo (GPUpdate)**](11_atualizar_politica_de_usuario.md) | Forçar replicação imediata de políticas locais e de domínio sem reinicialização. | `gpupdate /force` |

### 🩺 3. Manutenção, Diagnóstico & Reparo de Sistema
| Runbook | Descrição | Ferramentas |
| :--- | :--- | :--- |
| [**10. Ferramentas SFC e DISM**](10_sfc_dism.md) | Verificação e recuperação do repositório de componentes (`WinSxS`) e arquivos corrompidos. | `DISM`, `sfc /scannow` |
| [**08. Diagnóstico de Disco com CHKDSK**](08_chkdsk.md) | Análise de integridade de volumes NTFS/ReFS e reparo de setores lógicos defeituosos. | `chkdsk` |
| [**09. Otimização e Desfragmentação de Disco**](09_desfragmentar.md) | Execução de TRIM em SSDs e desfragmentação controlada de unidades magnéticas. | `defrag` |
| [**12. Manutenção do Spooler de Impressão**](12_print_spooler_service.md) | Resolução determinística de fila presa e redefinição do serviço Spooler. | `Stop-Service`, `spoolsv` |

### ⚡ 4. Otimização, Desempenho & Telemetria
| Runbook | Descrição | Ferramentas |
| :--- | :--- | :--- |
| [**03. Otimização de Energia da CPU**](03_desativar_gerenciador_de_energia.md) | Prevenção de throttling de CPU e ativação do plano de Alto Desempenho. | `powercfg` |
| [**15. Desativar Histórico de Atividades**](15_desativar_historico_atividades_do_windows.md) | Hardening de privacidade contra rastreamento de uso e timeline da Microsoft. | `Registry`, `GPO` |
| [**16. Desativar Aplicativos em Segundo Plano**](16_desativar_aplicativos_em_segundo_plano.md) | Redução de overhead de memória RAM e ciclos ociosos de CPU por apps UWP. | `Settings`, `PowerShell` |
| [**14. Ativar Tema Escuro**](14_ativar_tema_escuro.md) | Padronização de interface escura em sistema e aplicativos via registro. | `reg.exe` |

### 🌐 5. Redes & Configuração do Host
| Runbook | Descrição | Ferramentas |
| :--- | :--- | :--- |
| [**07. Renomear Computador**](07_renomear_computador.md) | Alteração padronizada do hostname da máquina para alinhamento em rede/AD. | `Rename-Computer` |
| [**13. Atualizar Interface de Rede**](13_atualizar_interface_de_rede.md) | Renovação de concessão DHCP, flush de cache DNS e redefinição de adaptadores. | `ipconfig /flushdns`, `netsh` |

---

## 🛠️ Como Utilizar este Repositório

### Clonagem Local
```bash
git clone git@github.com:brncesarms/windows.git
cd windows
```

### Visualização Recomendada
- **Obsidian**: Abra este diretório como um vault ou sub-vault do seu cofre técnico para usufruir da navegação por grafo e links bidirecionais.
- **Terminal**: Os blocos de comando podem ser copiados e executados diretamente em uma sessão de terminal com privilégios de Administrador.

---

## 🤝 Conexão com a Caixa de Ferramentas Multiplataforma

Os scripts PowerShell prontos para uso correspondentes a estas rotinas estão disponíveis em nossa toolbox pública de automação:
🔗 **[Repositório brncesarms/scripts (PowerShell)](https://github.com/brncesarms/scripts/tree/main/powershell)**

---

## 👤 Autor

**Bruno César**  
*Engenheiro de Infraestrutura, Redes & Automação*  
- **GitHub**: [@brncesarms](https://github.com/brncesarms)
- **LinkedIn**: [linkedin.com/in/brncesarms](https://linkedin.com/in/brncesarms)
