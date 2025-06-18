---
title: 50 Casos de Uso SIEM no Windows que Você Precisa Monitorar 
author: wesley
date: 25-06-18 02:27
categories: [Security, SIEM]
tags: [logs,windows,siem,monitoramento]
---
Monitorar eventos críticos do Windows é fundamental para antecipar ameaças, detectar ataques em tempo real e garantir a conformidade. Abaixo estão 50 casos de uso essenciais para configurar alertas e dashboards no seu SIEM.

| #  | Caso de Uso                                           | Event ID(s)                    | Observação                        |
|----|-------------------------------------------------------|---------------------------------|-----------------------------------|
| 1  | Tentativas de login falhas                            | 4625                            |                                   |
| 2  | Contas bloqueadas                                     | 4740                            |                                   |
| 3  | Login fora do horário comercial                       | 4624                            |                                   |
| 4  | Criação de novo usuário                               | 4720                            |                                   |
| 5  | Uso de conta privilegiada                             | 4672                            |                                   |
| 6  | Alterações em contas de usuário                       | 4722, 4723, 4724, 4725, 4726    |                                   |
| 7  | Logon de locais incomuns                              | 4624                            | com geolocalização                |
| 8  | Trocas de senha                                       | 4723, 4724                      | 4723 (tentativa), 4724 (reset)    |
| 9  | Alterações de grupo                                   | 4727, 4731, 4735, 4737          |                                   |
| 10 | Padrões de logon suspeitos                            | 4624                            |                                   |
| 11 | Falhas excessivas de logon                            | 4625                            |                                   |
| 12 | Atividade de conta desativada                         | 4725                            |                                   |
| 13 | Uso de conta dormente                                 | 4624                            |                                   |
| 14 | Atividade de conta de serviço                         | 4624, 4672                      |                                   |
| 15 | Monitoramento de acesso RDP                           | 4624                            | com filtro RDP                    |
| 16 | Movimento lateral                                     | 4648                            |                                   |
| 17 | Acesso a arquivos e pastas                            | 4663                            |                                   |
| 18 | Compartilhamento não autorizado de arquivos           | 5140, 5145                      |                                   |
| 19 | Alterações no registro                                | 4657                            |                                   |
| 20 | Instalação/remoção de aplicativos                     | 11707, 1033                     |                                   |
| 21 | Uso de dispositivos USB                               | 20001, 20003                    |                                   |
| 22 | Mudanças no firewall                                  | 4946, 4947, 4950, 4951          |                                   |
| 23 | Criação de tarefa agendada                            | 4698                            |                                   |
| 24 | Execução de processos                                 | 4688                            |                                   |
| 25 | Reinício/desligamento do sistema                      | 6005, 6006, 1074                |                                   |
| 26 | Limpeza de logs                                       | 1102                            |                                   |
| 27 | Execução de malware                                   | 4688, 1116                      |                                   |
| 28 | Alterações no Active Directory                        | 5136, 5141                      |                                   |
| 29 | Exclusão de Shadow Copies                             | 524                             |                                   |
| 30 | Mudanças de rede                                      | 4254, 4255, 10400               |                                   |
| 31 | Execução de scripts suspeitos                         | 4688                            |                                   |
| 32 | Instalação/modificação de serviços                    | 4697                            |                                   |
| 33 | Limpeza de logs de auditoria                          | 1102                            |                                   |
| 34 | Violação de política de software                      | 865                             |                                   |
| 35 | Enumeração excessiva de contas                        | 4625, 4776                      |                                   |
| 36 | Tentativas de acesso a arquivos sensíveis             | 4663                            |                                   |
| 37 | Injeção de processo incomum                           | 4688                            | com Sysmon/EDR                    |
| 38 | Instalação de driver                                  | 7045                            |                                   |
| 39 | Modificação de tarefas agendadas                      | 4699                            |                                   |
| 40 | Alterações não autorizadas em GPO                     | 5136                            |                                   |
| 41 | Atividade suspeita no PowerShell                      | 4104                            |                                   |
| 42 | Conexões de rede incomuns                             | 5156                            |                                   |
| 43 | Acesso não autorizado a arquivos compartilhados       | 5145                            |                                   |
| 44 | Consultas DNS maliciosas                              | 5158                            |                                   |
| 45 | Abuso de pesquisa LDAP                                | 4662                            |                                   |
| 46 | Encerramento de processo                              | 4689                            |                                   |
| 47 | Falha ao iniciar serviço                              | 7041                            |                                   |
| 48 | Alterações na política de auditoria                   | 4719, 1102                      |                                   |
| 49 | Monitoramento de mudanças de horário                  | 4616, 520                       |                                   |
| 50 | Alterações na chave do BitLocker                      | 5379                            |                                   |

---

Adote esses casos de uso como base para fortalecer o monitoramento de ambientes Windows em seu SIEM. A personalização desses alertas, de acordo com o perfil da sua organização, aumenta drasticamente a capacidade de detecção e resposta a incidentes.
