---
title: "Windows Software: Gerenciador de Pacotes Chocolatey"
date_created: 2026-08-17
author: "Bruno César / Antigravity"
privacy: public
tags:
  - publico
  - windows/gerenciador-pacotes
---

# 📦 Windows Software: Gerenciador de Pacotes Chocolatey

> [!info] Instalação e gerenciamento ágil de pacotes de software de terceiros a partir da CLI com o Chocolatey.

---

### 📦 Instalar o Chocolatey
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

> #### 🔗 Fontes de consulta
> - <https://community.chocolatey.org/>
> - <https://chocolatey.org/install>
> - <https://youtu.be/SaXqT1fm6Js>

### 📦 Gerenciamento do Chocolatey
```shell
choco search <nome>
choco list
choco install -y vlc
choco upgrade -y vlc
choco upgrade all -y
choco uninstall -y vlc
```

> Instalar uma versão específica:
> ```shell
> choco install typora --version 0.9.75 -y
> ```

### ⚙️ Aplicativos essenciais
```shell
choco install -y 7zip
choco install -y googlechrome
choco install -y vlc
choco install -y libreoffice-still
choco install -y rustdesk
choco install -y adobereader
choco install -y firefox
choco install -y ffmpeg
choco install -y lightshot
```

### ⚙️ Runtimes
```shell
choco install -y jre8
choco install -y dotnetfx
choco install -y dotnet-5.0-runtime
choco install -y dotnet-6.0-runtime
choco install -y dotnet-7.0-runtime
choco install -y vcredist-all
choco install -y vcredist2005
choco install -y vcredist2008
choco install -y vcredist2010
choco install -y vcredist2012
choco install -y vcredist2013
choco install -y vcredist140
```

### ⚙️ Ferramentas de desenvolvimento (Dev)
```shell
choco install -y git
choco install -y vscode
choco install -y dart-sdk
choco install -y flutter
choco install -y androidstudio
choco install -y php
```

## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Software: Gerenciador de Pacotes WinGet](17_winget.md) — Utilização do gerenciador de pacotes nativo WinGet.
