---
title: "Windows Software: Gerenciador de Pacotes WinGet"
date_created: 2026-08-17
tags:
  - windows/gerenciador-pacotes
---

# 📦 Windows Software: Gerenciador de Pacotes WinGet

> [!info] Comandos para pesquisa, instalação e atualização em lote de softwares com o utilitário nativo WinGet.

---

### 📦 Gerenciamento do WinGet
```shell
winget search <nome>
winget list
winget install <pacote>
winget uninstall <pacote>
winget upgrade
winget upgrade --all
```

#### 🔄 Reparar fontes e atualizações
```shell
winget source reset --force
winget source update
winget upgrade --all --accept-source-agreements
```

> #### 🔗 Fontes de consulta
> - <https://winstall.app>
> - <https://winget.run>
> - <https://youtu.be/OYF0hWHAicc>

### ⚙️ Aplicativos essenciais
```shell
winget install --id=Microsoft.PowerShell -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.WindowsTerminal -e --accept-package-agreements --accept-source-agreements
winget install --id=7zip.7zip -e --accept-package-agreements --accept-source-agreements
winget install --id=Mozilla.Firefox -e --accept-package-agreements --accept-source-agreements
winget install --id=Foxit.FoxitReader -e --accept-package-agreements --accept-source-agreements
winget install --id=Google.Chrome -e --accept-package-agreements --accept-source-agreements
winget install --id=TheDocumentFoundation.LibreOffice.LTS -e --accept-package-agreements --accept-source-agreements
winget install --id=Skillbrains.Lightshot -e --accept-package-agreements --accept-source-agreements
winget install --id=RustDesk.RustDesk -e --accept-package-agreements --accept-source-agreements
winget install --id=VideoLAN.VLC -e --accept-package-agreements --accept-source-agreements
winget install --id=Adobe.Acrobat.Reader.64-bit -e --accept-package-agreements --accept-source-agreements
winget install --id=AnyDeskSoftwareGmbH.AnyDesk -e --accept-package-agreements --accept-source-agreements
winget install --id=ByteDance.CapCut -e --accept-package-agreements --accept-source-agreements
winget install --id=Dropbox.Dropbox -e --accept-package-agreements --accept-source-agreements
winget install --id=GlavSoft.TightVNC -e --accept-package-agreements --accept-source-agreements
winget install --id=MiniTool.PartitionWizard.Free -e --accept-package-agreements --accept-source-agreements
winget install --id=OBSProject.OBSStudio -e --accept-package-agreements --accept-source-agreements
winget install --id=Oracle.VirtualBox -e --accept-package-agreements --accept-source-agreements
winget install --id=Flameshot.Flameshot -e --accept-package-agreements --accept-source-agreements
winget install --id=ShareX.ShareX -e --accept-package-agreements --accept-source-agreements
winget install --id=RealVNC.VNCViewer -e --accept-package-agreements --accept-source-agreements
winget install --id=Rufus.Rufus -e --accept-package-agreements --accept-source-agreements
winget install --id=TeamViewer.TeamViewer -e --accept-package-agreements --accept-source-agreements
winget install --id=Transmission.Transmission -e --accept-package-agreements --accept-source-agreements
winget install --id=uGetdm.uGet -e --accept-package-agreements --accept-source-agreements
winget install --id=Valve.Steam -e --accept-package-agreements --accept-source-agreements
winget install --id=WinSCP.WinSCP -e --accept-package-agreements --accept-source-agreements
```

### ⚙️ Runtimes
```shell
winget install --id=Microsoft.DotNet.Framework.DeveloperPack_4 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.DotNet.Framework.DeveloperPack.4.5 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.DotNet.Runtime.5 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.DotNet.Runtime.6 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.DotNet.Runtime.7 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.DotNet.Runtime.8 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2005.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2005.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2008.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2008.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2010.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2010.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2012.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2012.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2013.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2013.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2015+.x86 -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VCRedist.2015+.x64 -e --accept-package-agreements --accept-source-agreements
winget install --id=Oracle.JavaRuntimeEnvironment -e --accept-package-agreements --accept-source-agreements
```

### ⚙️ Ferramentas de desenvolvimento (Dev)
```shell
winget install --id=Microsoft.VisualStudioCode -e --accept-package-agreements --accept-source-agreements
winget install --id=Microsoft.VisualStudio.2022.Community -e --accept-package-agreements --accept-source-agreements
winget install --id=Git.Git -e --accept-package-agreements --accept-source-agreements
winget install --id=Google.AndroidStudio -e --accept-package-agreements --accept-source-agreements
winget install --id=ApacheFriends.Xampp.8.1 -e --accept-package-agreements --accept-source-agreements
winget install --id=ApacheFriends.Xampp.7.4 -e --accept-package-agreements --accept-source-agreements
winget install --id=Notepad++.Notepad++ -e --accept-package-agreements --accept-source-agreements
```

### ⚙️ Comunicação (chat)
```shell
winget install --id=Discord.Discord -e --accept-package-agreements --accept-source-agreements
winget install --id=Telegram.TelegramDesktop -e --accept-package-agreements --accept-source-agreements
winget install --id=BeeBEEP.BeeBEEP -e --accept-package-agreements --accept-source-agreements
```

## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
- [Windows Software: Gerenciador de Pacotes Chocolatey](18_chocolatey.md) — Uso do gerenciador de pacotes comunitário Chocolatey.
