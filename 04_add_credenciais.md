---
title: "Windows Segurança: Adicionar Credenciais de Rede"
date_created: 2026-08-17
author: "Bruno César / Antigravity"
privacy: public
tags:
  - publico
  - windows/seguranca
  - windows/gerenciamento
---

# 🔑 Windows Segurança: Adicionar Credenciais de Rede

> [!info] Procedimento via terminal cmdkey para salvar senhas e credenciais de rede de forma persistente no cofre do Windows.

---

> [!warning] Exemplo didático
> Substitua os valores de exemplo por **suas credenciais reais**. Não utilize senhas em texto plano em scripts versionados.

### 🔌 Salvar credencial de rede
```powershell
# Substitua pelos seus valores reais
$username = "SEU_USUARIO"
$password = "SUA_SENHA"
$servidor = "192.168.0.34"

cmdkey /add:$servidor /user:$username /pass:$password
```

> [!tip] Alternativa segura
> Para evitar senha em texto plano, use o prompt interativo:
> ```powershell
> cmdkey /add:192.168.0.34 /user:SEU_USUARIO
> ```
> O `cmdkey` solicitará a senha de forma oculta.

### 🔍 Excluir credencial salva
```powershell
cmdkey /delete:192.168.0.34
```


## 🔗 Notas Relacionadas
- [Windows: Guia Principal de Referência de Conhecimento](README.md) — Índice principal de tópicos de Windows.
