---
title: "Windows Rede: Atualizar Interface de Rede"
date_created: 2026-08-17
author: "Bruno César"
privacy: public
tags:
  - publico
  - windows/rede
  - windows/manutencao
---

# 🔌 Windows Rede: Atualizar Interface de Rede

> [!info] Comandos de redefinição de sockets TCP/IP, liberação/renovação de IP via DHCP e limpeza de cache de DNS.

---

### 🌐 Limpar cache de DNS
```powershell
ipconfig /flushdns
```

### 🌐 Liberar e renovar IP via DHCP
```powershell
ipconfig /release
ipconfig /renew
```

### 📶 Desabilitar Wi-Fi
```powershell
netsh interface set interface name="Wi-Fi" admin=DISABLE
```

### 📶 Habilitar Wi-Fi
```powershell
netsh interface set interface name="Wi-Fi" admin=ENABLE
```

### ⚙️ Desabilitar Ethernet
```powershell
netsh interface set interface name="Ethernet" admin=DISABLE
```

### ⚙️ Habilitar Ethernet
```powershell
netsh interface set interface name="Ethernet" admin=ENABLE
```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
