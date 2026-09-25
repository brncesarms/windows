---
title: "Windows Manutenção: Comando CHKDSK"
date_created: 2026-08-17
tags:
  - windows/manutencao
---

# 🛠️ Windows Manutenção: Comando CHKDSK

> [!info] Utilização da ferramenta CHKDSK para analisar a integridade física de discos, reparando bad sectors e arquivos órfãos.

---

### 🛠️ CHKDSK
> [!warning] Execute como Administrador. Pode exigir reinicialização para agendar a verificação.
> ```powershell
> chkdsk C: /r
> ```

> [!tip] Alternativa via PowerShell
> ```powershell
> Repair-Volume C -OfflineScanAndFix
> ```

> [!info] `/r` localiza setores defeituosos e recupera informações legíveis, além de corrigir erros lógicos.


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Manutenção: Ferramentas SFC e DISM](10_sfc_dism.md) — Reparo lógico de arquivos corrompidos de sistema com SFC e DISM.
- [Windows Manutenção: Desfragmentação e Otimização](9_desfragmentar.md) — Otimização e desfragmentação manual de discos rígidos e SSDs.
