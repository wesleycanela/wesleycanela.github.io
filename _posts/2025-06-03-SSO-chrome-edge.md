---
title: Configuração de SSO no Chrome e Edge no Linux
description: Configurar a autenticação integrada (SSO) nos navegadores Google Chrome e Microsoft Edge no Linux.
author: wesley
date: 25-04-02 14:11
categories: [HowTo]
tags: [linux]
---
### Configuração de SSO no Chrome e Edge

Este tutorial descreve os passos para configurar a autenticação integrada (SSO) nos navegadores Google Chrome e Microsoft Edge utilizando arquivos de políticas gerenciadas no Linux.

As políticas do Chrome e Edge podem ser definidas via arquivos JSON localizados nos diretórios:

- **Chrome**: `/etc/opt/chrome/policies/managed/`
- **Edge**: `/etc/opt/edge/policies/managed/`

Crie ou edite os arquivos `conf.json` com o seguinte conteúdo para ambos os navegadores:

```json
{
  "AuthServerAllowlist": "*.domain.com",
  "DisableAuthNegotiateCnameLookup": true
}
```

**Explicação das Chaves**

- **AuthServerAllowlist**: Especifica os domínios permitidos para envio automático de credenciais. Neste caso, qualquer subdomínio do domínio `domain.com` está autorizado.

- **DisableAuthNegotiateCnameLookup**: Impede que o navegador tente resolver CNAMEs para autenticação Negotiate. Isso pode melhorar a segurança e evitar falhas em alguns ambientes Kerberos.

#### Passo a Passo

1. Criar o diretório de políticas, se ainda não existir

##### Chrome:
```bash
sudo mkdir -p /etc/opt/chrome/policies/managed
```

##### Edge:
```bash
sudo mkdir -p /etc/opt/edge/policies/managed
```

2. Criar o arquivo de política

Chrome:
```bash
sudo tee /etc/opt/chrome/policies/managed/policie.json > /dev/null <<EOF
{
  "AuthServerAllowlist": "*.domain.com",
  "DisableAuthNegotiateCnameLookup": true
}
EOF
```

Edge:
```bash
sudo tee /etc/opt/edge/policies/managed/policie.json > /dev/null <<EOF
{
  "AuthServerAllowlist": "*.domain.com",
  "DisableAuthNegotiateCnameLookup": true
}
EOF
```

3. Reiniciar os navegadores

Após salvar os arquivos de política, **feche e reabra o Chrome e o Edge** para que as novas configurações entrem em vigor.

4. Validação

Para validar se a política foi aplicada corretamente:

1. Acesse `chrome://policy` no Chrome ou `edge://policy` no Edge.
2. Clique em “**Reload Policies**” (Recarregar Políticas).
3. Verifique se as políticas `AuthServerAllowlist` e `DisableAuthNegotiateCnameLookup` estão listadas com os valores corretos.
