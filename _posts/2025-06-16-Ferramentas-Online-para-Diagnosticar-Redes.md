---
title: Ferramentas Online para Diagnosticar Problemas de Rede
author: wesley
date: 25-06-16 03:11
categories: [Security, SOC]
tags: [SOC, blueTeam, diagnostico]
---
Em determinados cenários é preciso **agir com rapidez e eficácia** para avaliar incidentes, excluir hipóteses e focar nas ameaças reais.

Se um **alerta é gerado**, um **domínio passa a apresentar comportamento suspeito**, o **certificado de um serviço expira**, o **e-mail não é entregue** ou determinados **portos estão expostos**, o analista de segurança precisa de fontes de informação **confiáveis e fáceis de usar** para dar uma **resposta ágil**.

Neste artigo compartilhamos uma **série de sites gratuitos**, práticos e eficientes que você pode usar como ponto de apoio nas suas atividades de **triagem**, **análise forense**, **network diagnostics**, **certificados**, **DNS**, **port scanning**, **e-mail delivery** e muito mais.

## 1. httpstat.us

* **URL:** [https://httpstat.us/](https://httpstat.us/)
* Por que usar: ele responde exatamente o **código de status que você quer**, sendo particularmente útil para **simular diferentes cenários de erro**. Por exemplo:

  * [https://httpstat.us/200](https://httpstat.us/200) → responde 200 OK
  * [https://httpstat.us/500](https://httpstat.us/500) → responde 500 Internal Server Error
  * [https://httpstat.us/200?sleep=5000](https://httpstat.us/200?sleep=5000) → faz um delay de 5 segundos antes de responder

## 2. example.com e example.org

* **URLs:** [https://example.com/](https://example.com/) | [https://example.org/](https://example.org/)
* Por que usar: são domínios reservados pelo IANA para **documentação e teste**, sendo **sempre ativos e confiáveis**. Uma saída simples para dar um **curl**, health check ou teste básico de DNS.

## 3. HackerTarget

* **URL:** [https://hackertarget.com/](https://hackertarget.com/)
* Por que usar: proporciona uma **série de ferramentas online**, como:

  * Port scan
  * Trace route
  * DNS lookup
  * Reverse IP
  * Banner grabbing
    Isso torna o HackerTarget particularmente útil tanto para **network engineers** quanto para **analistas de TI** que precisam de um conjunto de diagnósticos centralizado.

## 4. Ping-Test

* **URL:** [https://www.ping-test.net/](https://www.ping-test.net/)
* Por que usar: uma alternativa simples para:

  * Fazer pings
  * Medir velocidade da internet
  * Analisar o trajeto da rede (traceroute)
    Isso fortalece o **diagnóstico de problemas de conectividade** de forma rápida e intuitiva.

## 5. YouGetSignal

* **URL:** [https://www.yougetsignal.com/tools/open-ports/](https://www.yougetsignal.com/tools/open-ports/)
* Por que usar: saída simples para **saber se determinados portos estão abertos**, auxiliando no **troubleshooting de redes**, firewall e port-forward.

## 6. DNS Checker

* **URL:** [https://dnschecker.org/](https://dnschecker.org/)
* Por que usar: verifica a **propagação de DNS pelo mundo**, mostrando de diferentes localidades se o nome de um serviço resolve para o IP correto. Útil depois de **mudar o DNS de um serviço** e quer saber se ele já propagou para todos.

## 7. SSL Labs (SSL-Test)

* **URL:** [https://www.ssllabs.com/ssltest/](https://www.ssllabs.com/ssltest/)
* Por que usar: faz uma avaliação detalhada da **configuração SSL/TLS de um site**, mostrando:

  * Rating de A a F
  * Cifras habilitadas
  * Vulnerabilidades presentes (Heartbleed, POODLE etc.)
    Isso fortalece a **segurança da sua aplicação**.

## 8. Traceroute Online

* **URL:** [https://traceroute-online.com/](https://traceroute-online.com/)
* Por que usar: uma alternativa baseada na **web** para você realizar um **traceroute**, mostrando o caminho que o seu pedido percorre até o destino. Útil para detectar **roteamentos ruins**, **perda de pacotes** ou **pontos de gargalo** na rede.

## 9. MxToolBox

* **URL:** [https://www.mxtoolbox.com/](https://www.mxtoolbox.com/)
* Por que usar: uma suite de ferramentas que cobre:

  * Verificar registros DNS (A, CNAME, MX, TXT).
  * Testar blacklists de e-mail (RBL).
  * Diagnosticar problemas específicos de e-mail, como reverse DNS, PTR, SPF, DKIM e DMARC.
    Isso é particularmente valioso para a administração de e-mail e domínios.

## Outros

* [https://www.speedtest.net/](https://www.speedtest.net/) — verifica velocidade de **conexão**, **ping**, **jitter**, etc.
* [https://www.whatsmydns.net/](https://www.whatsmydns.net/) — verifica **propagação de DNS** pelo planeta.
* [https://www.uptrends.com/tools/uptime](https://www.uptrends.com/tools/uptime) — verifica **uptime**, **resposta** e **certificados**.
* [https://www.sslshopper.com/ssl-checker.html](https://www.sslshopper.com/ssl-checker.html) — verifica **certificados SSL/TLS**.

## Por que usar esses sites?

Com essas alternativas você consegue:

* Simular diferentes cenários de erro.
* Validar a velocidade da sua rede e o tempo de resposta do serviço.
* Monitorar o caminho da sua ligação até o destino (traceroute).
* Diagnosticar problemas específicos de DNS, certificados, blacklists, e-mail, portas e muito mais.
