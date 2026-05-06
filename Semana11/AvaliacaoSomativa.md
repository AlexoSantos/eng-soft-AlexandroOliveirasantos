# 📘 Sala de Aula Invertida – Padrões de Arquitetura na Web

---

## Slide 1 – Introdução (Base Sommerville)
- Projeto de Arquitetura: organização global do sistema e definição de componentes.  
- Decisões Críticas: impacto em desempenho, segurança e manutenção.  
- Capítulo 6 do Sommerville como referência.  

---

## Slide 2 – Padrão Escolhido: Microsserviços
- Sistema dividido em serviços independentes.  
- Comunicação via APIs.  
- Evolução da arquitetura cliente-servidor e de componentes.  

---

## Slide 3 – Trade-offs dos Microsserviços
- **Desempenho**: escalabilidade alta, mas maior latência de rede.  
- **Segurança**: isolamento facilita proteção, mas aumenta superfície de ataque.  
- **Manutenção**: independência facilita evolução, mas exige coordenação complexa.  

---

## Slide 4 – Exemplo Real
- **Netflix**: utiliza microsserviços para suportar milhões de usuários simultâneos.  
- Escalabilidade e resiliência como pontos fortes.  

---

## Slide 5 – Outros Padrões Modernos
- **Serverless (FaaS)**: execução sob demanda, sem gestão de servidores.  
- **Hexagonal (Ports and Adapters)**: núcleo isolado, fácil teste.  
- **EDA (Orientada a Eventos)**: comunicação assíncrona.  
- **BFF (Backend For Frontend)**: APIs otimizadas para cada frontend.  

---

## Slide 6 – Exemplos Reais
- Serverless → AWS Lambda  
- Hexagonal → Bancos  
- EDA → Uber  
- BFF → Spotify  

---

## Slide 7 – Comparação em Tabela

| Padrão          | Evolução de                  | Vantagem                        | Desvantagem                 | Exemplo   |
|-----------------|------------------------------|---------------------------------|-----------------------------|-----------|
| Microsserviços  | Cliente-servidor / componentes | Escalabilidade e independência   | Latência e complexidade     | Netflix   |
| Serverless      | Orientada a eventos          | Custo sob demanda               | Dependência do provedor     | AWS Lambda|
| Hexagonal       | Arquitetura em camadas       | Núcleo isolado, fácil teste     | Complexidade inicial        | Bancos    |
| EDA             | Processos síncronos          | Escalabilidade assíncrona       | Difícil rastrear fluxo      | Uber      |
| BFF             | Cliente-servidor             | API otimizada para cada frontend| Duplicação de lógica        | Spotify   |

---

## Slide 8 – Rubrica de Avaliação
- **Domínio Técnico**: explicar fluxo de dados.  
- **Conexão Acadêmica**: mostrar evolução dos padrões clássicos.  
- **Análise de Atributos**: detalhar trade-offs.  
- **Qualidade do Material**: diagramas claros e bem estruturados.  
- **Apresentação Oral**: explicação fluida e interativa.  

---
