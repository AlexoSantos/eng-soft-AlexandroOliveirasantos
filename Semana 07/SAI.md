# 🛡️ Sistema de Comando de Crise SJBV - Alerta Inteligente

## 📋 Informações do Projeto
| Campo | Descrição |
| :--- | :--- |
| **Dono do Projeto** | [Alexandro Oliveira dos Santos] |
| **Versão** | 1.0 (MVP 2.0) |
| **Data** | 16 de Abril de 2026 |
| **Status** | Em Desenvolvimento |

---

## 1. Introdução
O objetivo deste documento é descrever os requisitos para o desenvolvimento do **Sistema de Comando de Crise SJBV**. [cite_start]Este sistema foi concebido para transformar dados meteorológicos brutos em decisões logísticas automáticas, garantindo que a Defesa Civil e a população ajam antes do impacto de eventos climáticos severos[cite: 5, 6].

## 2. Escopo
O sistema foca-se na antecipação de desastres naturais com alta precisão e inclui:
* [cite_start]**Motor de Previsão:** Ingestão de dados de satélites e radares[cite: 9].
* [cite_start]**Inteligência Geográfica:** Cruzamento de polígonos de risco com dados demográficos do IBGE[cite: 10].
* [cite_start]**Dashboard de Comando:** Gestão de logística de resgate e alertas via *Cell Broadcast*[cite: 11].

## 3. Requisitos Funcionais

### 3.1 Funcionalidade 1: Motor Preditivo (IA e Clima)
| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 1.1** | [cite_start]Coleta de dados via APIs (Tomorrow.io/INPE) a cada 10 minutos[cite: 14]. |
| **RF 1.2** | [cite_start]Cálculo de probabilidade de eventos severos num horizonte de 60 minutos[cite: 14]. |

### 3.2 Funcionalidade 2: Inteligência Geográfica e Logística
| ID | Descrição do Requisito |
| :--- | :--- |
| **RF 2.1** | [cite_start]Uso da função `ST_Intersects` (PostGIS) para identificar bairros atingidos[cite: 16]. |
| **RF 2.2** | [cite_start]Cálculo automático de efetivo de bombeiros (1 agente por 150 habitantes) e viaturas[cite: 16]. |

## 4. Requisitos Não Funcionais
* [cite_start]**RNF 4.1:** O cruzamento espacial no PostGIS deve ser processado em menos de 2 segundos[cite: 18].
* [cite_start]**RNF 4.2:** A interface deve seguir padrões de acessibilidade e ser responsiva para uso em centros de comando[cite: 19].

## 5. Design da Interface (UI/UX)
* [cite_start]**Padrão Visual:** Estética "Dark Mode" de Centro de Operações, utilizando azul-marinho (`#2c3e50`) e alertas em vermelho (`#c0392b`)[cite: 21].
* [cite_start]**Experiência do Usuário:** Mapa interativo centralizado em SJBV com barra lateral de métricas de resgate automáticas[cite: 22].

## 6. Arquitetura do Sistema
* [cite_start]**Arquitetura:** Padrão Cliente-Servidor com processamento pesado no Backend[cite: 24].
* **Tecnologias:** * **Frontend:** HTML5, CSS3, JavaScript, Leaflet.js.
    * **Backend:** Python (Flask/FastAPI).
    * [cite_start]**Banco de Dados:** PostgreSQL + PostGIS[cite: 25].

## 7. Requisitos de Dados
* [cite_start]**RD 7.1:** Tabela `demografia_bairros` com integração de polígonos GeoJSON do IBGE[cite: 27].
* [cite_start]**RD 7.2:** Armazenamento de histórico de eventos para treinamento futuro da IA[cite: 28].

## 8. Requisitos de Segurança
* [cite_start]**RS 8.1:** Autenticação de dois fatores para disparos de alertas reais à população[cite: 30].
* [cite_start]**RS 8.2:** Criptografia de dados sensíveis e proteção de chaves de API via variáveis de ambiente (`.env`)[cite: 31].

## 9. Requisitos de Desempenho
* [cite_start]**RP 9.1:** Suporte a múltiplos acessos simultâneos durante crises climáticas[cite: 33].
* [cite_start]**RP 9.2:** Otimização de consultas espaciais para baixo consumo de memória no servidor[cite: 34].

## 10. Cronograma (Estimado)
| Tarefa | Status |
| :--- | :--- |
| Levantamento de Requisitos | ✅ Concluído |
| Design e Prototipagem | 🏗️ Em progresso |
| Desenvolvimento Backend (Python/PostGIS) | 📅 Planejado |
| Testes de Integração | 📅 Planejado |

---
[cite_start]*Este documento segue o padrão de Requisitos de Software (SRS) v1.1[cite: 1, 41].*
