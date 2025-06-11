---
title: Criar um Usuário Local Durante a Instalação do Windows
author: wesley
date: 25-06-11 03:17
categories: [HowTo]
tags: [windows, howto]
---
Com as versões mais recentes do Windows 11, a Microsoft dificulta a criação de contas locais durante a instalação, forçando o uso de uma conta Microsoft online. No entanto, existem métodos eficazes e atualizados para contornar essa exigência e criar um usuário local, garantindo mais privacidade e controle sobre o sistema. Veja o passo a passo detalhado:

### 1. **Inicie a Instalação do Windows 11**
Prossiga normalmente até chegar à tela **"Vamos conectá-lo a uma rede"** (Let's connect you to a network).
Se possível, já inicie a instalação sem nenhum cabo de rede conectado e não conecte ao Wi-Fi.

### 2. **Abra o Prompt de Comando**
Pressione as teclas **Shift + F10** ao mesmo tempo. Isso abrirá uma janela do Prompt de Comando (CMD).

### 3. **Execute o Comando de Bypass**
No Prompt de Comando, digite:
```
start ms-cxh:localonly
```

### 4. Conta Local
Uma janela **"Conta da Microsoft"** será aberta, escolha a opção para criar uma conta local.

### 5. Usuário e Senha
Siga as instruções para definir um nome de usuário e senha.

### 6. Finalizar 
Continue a instalação normalmente até concluir a configuração do Windows 11.

### **Dica Extra**
**Rufus:** Se for criar um pendrive bootável, o Rufus possui uma opção para remover o requisito de conta online da Microsoft durante a criação da mídia, facilitando ainda mais o processo.
