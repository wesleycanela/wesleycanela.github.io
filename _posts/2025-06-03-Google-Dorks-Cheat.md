---
title: Google Dorks Cheat para OSINT
description: Guia rápido de comandos Google Dorks para investigações OSINT.
author: wesleycanela
date: 25-04-03 06:11
categories: [OSINT]
tags: [dork, google, cheat]
---
# Google Dorks Cheat para OSINT

## Operadores Básicos de Busca

### Busca por Frase Exata

- `"frase exata"` - Busca pela frase exata entre aspas
- `"João Silva" AND "Brasilia"` - Encontra páginas que contenham ambas as frases exatas

### Wildcard e Proximidade

- `*` - Wildcard para palavras desconhecidas
- `AROUND(X)` - Encontre termos dentro de X palavras um do outro
- `"cyber * attack"` - Encontre variações como "cyber security attack"

### Operadores Booleanos

- `AND` / `+` - Ambos os termos devem estar presentes
- `OR` / `|` - Qualquer um dos termos pode estar presente
- `NOT` / `-` - Exclui termos específicos
- `()` -  Agrupa termos para consultas complexas

## Operadores Avançados Específicos de Site

### Direcionamento de Site

- `site:example.com` - Busca dentro de um domínio específico
- `site:*.gov` -  Busca em todos os sites governamentais
- `site:linkedin.com "João Silva"` - Encontra perfis no LinkedIn
- `site:reddit.com` - Busca posts e comentários no Reddit

### Buscas por Tipo de Arquivo

- `filetype:pdf` - Encontra documentos PDF
- `filetype:doc` - Encontra documentos do Word
- `filetype:xls` - Encontra planilhas do Excel
- `filetype:ppt` - Encontra apresentações do PowerPoint
- `filetype:txt` - Encontra arquivos de texto
- `filetype:log` - Encontra arquivos de log
- `ext:sql` - Sintaxe alternativa para extensões de arquivo

### URL Structure Searches

- `inurl:admin` - Encontra URLs que contenham "admin"
- `inurl:login` - Encontra páginas de login
- `inurl:config` - Encontra arquivos de configuração
- `allinurl:admin panel` - Todos os termos devem estar na URL

### Title and Text Searches

- `intitle:confidential` - Encontra páginas com "confidencial" no título
- `allintitle:secret document` - Todos os termos devem estar no título
- `intext:password` - Encontra páginas que contenham "password" no texto
- `allintext:classified information` - Todos os termos devem estar no texto da página

## Técnicas Específicas de OSINT

### Inteligência de Pessoas (PEOPINT)

- `"João Silva" site:linkedin.com` - Encontra perfis no LinkedIn
- `"João Silva" + "email" + "@gmail.com"` - Encontra endereços de e-mail
- `"João Silva" + "phone" + "062"` - Encontra números de telefone
- `"João Silva" site:facebook.com` - Encontra perfis no Facebook
- `"João Silva" site:twitter.com` - Encontra perfis no Twitter
- `"João Silva" + "curriculo" filetype:pdf` - Encontra currículos

### Company Intelligence

- `site:empresa.com filetype:pdf` - Encontra documentos da empresa
- `"Nome da Empresa" + "employee" + "email"` -  Encontra e-mails de funcionários
- `"Nome da Empresa" + "org chart" OR "organizational chart"` - Encontra organogramas
- `"Nome da Empresa" + "annual report" filetype:pdf` - Encontra relatórios anuais
- `site:empresa.com inurl:careers` - Encontra vagas de emprego

### Location Intelligence (GEOINT)

- `"address" + "city, state" + "zip code"` - Encontra endereços específicos
- `"GPS coordinates" + "latitude longitude"` - Encontra dados de GPS
- `site:maps.google.com "location name"` - Encontra dados no Google Maps
- `"street view" + "address"` - Encontra imagens do Street View

### Inteligência Técnica (TECHINT)

- `site:github.com "nome da empresa"` - Encontra repositórios da empresa
- `"API key" + "nome da empresa"` - Encontra chaves de API expostas
- `"database" + "nome da empresa" + "leak"` -  Encontra vazamentos de dados
- `"config" + "password" + "database"` - Encontra arquivos de configuração

## Pesquisa de Vulnerabilidades e Segurança

### Arquivos e Diretórios Expostos

- `intitle:"Index of" password` - Encontra listas de diretórios com senhas
- `intitle:"Index of" "backup"` - Encontra diretórios de arquivos de backup
- `intitle:"Index of" "config"` - Encontra diretórios de configuração
- `intitle:"Index of" "log"` - Encontra diretórios de arquivos de log

### Páginas de Login e Painéis de Administração

- `inurl:admin intitle:login` - Encontra páginas de login de administração
- `inurl:wp-admin` - Encontra painéis administrativos do WordPress
- `inurl:phpmyadmin` - Encontra interfaces do phpMyAdmin
- `intitle:"admin panel" OR "control panel"` - Encontra painéis de controle

### Informações de Banco de Dados e Sistema

- `intext:"sql syntax near" OR intext:"syntax error has occurred"` -  Encontra erros de SQL
- `intext:"Warning: mysql_connect()"` - Encontra erros de conexão MySQL
- `intitle:"phpinfo()" "PHP Version"` - Encontra páginas de informações do PHP
- `intext:"Server at" intext:"Apache"` - Encontra informações de servidores Apache

### Credenciais e Dados Sensíveis

- `intext:"username" intext:"password" filetype:log` - Encontra credenciais em arquivos de log
- `"password" filetype:txt site:pastebin.com` - Encontra senhas no Pastebin
- `"BEGIN RSA PRIVATE KEY" filetype:key` - Encontra chaves privadas
- `"api_key" OR "apikey" filetype:json` - Encontra chaves de API em arquivos JSON

## Mídias Sociais e Comunicação

### Perfis em Redes Sociais

- `site:linkedin.com/in/ "João Silva"` - Perfis do LinkedIn
- `site:twitter.com "João Silva"` - Perfis do Twitter
- `site:facebook.com "João Silva"` - Perfis do Facebook
- `site:instagram.com "João Silva"` - Perfis do Instagram

### Fóruns e Comunidades

- `site:reddit.com/r/ "topic"` - Busca em subreddits específicos
- `site:stackoverflow.com "nome da empresa"` - Encontra discussões técnicas
- `"João Silva" site:forum.*` - Encontra postagens de uma pessoa em fóruns

### Plataformas de Comunicação

- `site:discord.com "server name"` - Encontra servidores no Discord
- `site:telegram.me "channel name"` - Encontra canais no Telegram
- `"João Silva" + "Skype" + "username"` - Encontra nomes de usuário do Skype

## Pesquisas por Tempo e Cache

### Conteúdo em Cache e Arquivado

- `cache:example.com` - Visualiza a versão em cache do Google
- `site:archive.org "website.com"` - Encontra versões arquivadas
- `site:web.archive.org "deleted content"` - Encontra conteúdo web excluído

### Pesquisas por Intervalo de Datas

- `after:2023-01-01 before:2023-12-31` - Busca dentro de um intervalo de datas
- `"data breach" after:2024-01-01` - Encontra vazamentos de dados recentes

## Pesquisas Especiais por Arquivos e Conteúdos

### Documentos e Relatórios

- `"quarterly report" filetype:pdf site:sec.gov` - Encontra registros na SEC
- `"incident report" filetype:pdf "nome da empresa"` - Encontra relatórios de incidentes
- `"audit report" filetype:pdf` - Encontra documentos de auditoria
- `"meeting minutes" filetype:pdf` - Encontra registros de reuniões

### E-mails e Informações de Contato

- `"@company.com" + "email"` - Encontra endereços de e-mail da empresa
- `intext:"email" + "contact" + "@"` - Encontra e-mails de contato
- `"john.smith@" + "company.com"` - Encontra padrões específicos de e-mail

### Telefones e Endereços

- `"phone" + "555-123-4567"` - Encontra referências a números de telefone
- `"address" + "123 Main Street"` - Encontra referências a endereços
- `"fax" + "nome da empresa"` - Encontra números de fax

## Técnicas Avançadas de Combinação

### Pesquisas Multi-Plataforma

- `("João Silva" site:linkedin.com) OR ("João Silva" site:twitter.com)` - Busca em várias plataformas
- `"nome da empresa" (site:reddit.com OR site:stackoverflow.com)` - Encontra discussões em diferentes plataformas

### Pesquisas Negativas para Filtragem

- `"João Silva" -site:linkedin.com -site:facebook.com` - Exclui redes sociais
- `"data breach" -news -media` - Exclui artigos de notícias
- `"nome da empresa" -jobs -careers -hiring` - Exclui artigos de notícias

### Consultas Booleanas Complexas

- `("API key" OR "secret key") AND ("nome da empresa") NOT ("example" OR "test")` - Busca complexa por credenciais
- `(inurl:admin OR inurl:login) AND (intext:password OR intext:username)` - Encontra painéis administrativos com credenciais

## Pesquisas Específicas por Setor

### Governo e Militar

- `site:*.gov "classified" -"declassified"` - Encontra referências governamentais classificadas
- `site:*.mil "personnel" filetype:pdf` - Encontra documentos de pessoal militar
- `"FOIA" + "document" + "agency name"` -  Encontra documentos FOIA

### Saúde e Medicina

- `site:*.edu "patient data" OR "medical records"` - Encontra dados de saúde
- `"HIPAA" + "violation" + "hospital name"` - Encontra violações da HIPAA
- `"clinical trial" + filetype:pdf` - Encontra documentos de ensaios clínicos

### Finanças e Bancos

- `site:sec.gov "10-K" "nome da empresa"` - Encontra registros 10-K da SEC
- `"financial statement" filetype:pdf "nome da empresa"` -  Encontra documentos financeiros
- `"audit" + "bank" + "report" filetype:pdf` - Encontra relatórios de auditoria bancária

## Metadados e Informações Ocultas

### Pesquisas de Metadados

- `filetype:pdf "metadata" "author"` - Encontra metadados em PDFs
- `"exif data" + "image" + "location"` - Encontra metadados de imagens
- `"document properties" filetype:doc` - Encontra propriedades de documentos do Word

### Texto Oculto e Comentários

- `intext:"hidden" OR intext:"comment"` - Encontra texto oculto
- `"TODO" OR "FIXME" site:github.com` - Encontra comentários em códigos
- `"password" + "comment" filetype:html` - Encontra senhas em comentários HTML

## Melhores Práticas e Dicas

### Otimização de Consultas
- Use termos específicos em vez de genéricos
- Combine múltiplos operadores para resultados precisos
- Use aspas para frases exatas
- Teste variações das suas consultas

### Considerações Legais e Éticas
- Respeite o robots.txt e os termos de serviço
- Não acesse sistemas não autorizados
- Use as informações de forma responsável
- Siga as leis e regulamentos aplicáveis

### Documentação e Verificação
- Salve as consultas e os resultados das buscas
- Verifique informações em múltiplas fontes
- Documente a data e hora das pesquisas
- Faça capturas de tela de achados importantes
- Padrões Comuns de Busca

## Padrões Comuns de Busca

### Verificação de Identidade

```
"João Silva" + "birthday" + "1985"
"João Silva" + "address" + "city"
"João Silva" + "phone" + "email"
```

### Pesquisa de Empresas

```
site:company.com filetype:pdf
"nome da empresa" + "employee" + "directory"
"nome da empresa" + "leak" + "data"
```

### Investigação de Incidentes

```
"incident" + "date" + "location"
"breach" + "company" + "data"
"hack" + "attack" + "victim"
```

### Descoberta de Ativos

```
"nome da empresa" + "server" + "IP"
"nome da empresa" + "domain" + "subdomain"
"nome da empresa" + "network" + "range"
```

Essa lista de Cheats oferece uma base abrangente para o uso de Google Dorks em investigações OSINT. Lembre-se de sempre atuar dentro dos limites legais e seguir princípios éticos ao conduzir pesquisas.
