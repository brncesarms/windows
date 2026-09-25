---
title: "Windows Serviços: Spooler de Impressão"
date_created: 2026-08-17
tags:
  - windows/servicos
  - windows/manutencao
---

# 🛠️ Windows Serviços: Spooler de Impressão

> [!info] Procedimento rápido para reiniciar o Spooler de Impressão e limpar arquivos de fila travada no Windows.

---

> [!info] Use este procedimento quando a impressora ficar "presa" ou com fila de impressão travada.

### 🔌 Parar o serviço de spooler de impressão
```powershell
Stop-Service -Name Spooler -Force
```

### 🧹 Limpar arquivos da fila de impressão
```powershell
Remove-Item -Path "$env:SystemRoot\System32\spool\PRINTERS\*.*"
```

### 🔌 Iniciar o serviço de spooler de impressão
```powershell
Start-Service -Name Spooler
```

> [!tip] Em um único passo (reiniciar)
> ```powershell
> Restart-Service -Name Spooler -Force
> ```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
