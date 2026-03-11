# eng-soft-AlexandroOliveiraSantos
Engenharia de Software
Portfólio de Engenharia de Software

**Dev:** [Alexandro Oliveira dos Santos]  
**Disciplina:** Engenharia de Software - Sistemas para Internet  

Bem-vindo ao meu repositório! Aqui você encontrará todas as minhas entregas, exercícios e documentações desenvolvidas durante a disciplina.

---

## 🛠️ Minha Stack / Tecnologias
*(Liste aqui as linguagens, ferramentas ou frameworks que você já conhece ou está aprendendo)*
- HTML5, CSS3, JavaScript
- Python
- Cobol

---

## 📂 Índice de Entregas Semanais

Clique nos links abaixo para acessar os arquivos de cada semana:

* 📄 [Semana 01 - Fundamentos e Ética](./semana-01)
* 📄 [Semana 02 - Modelos de Processo](./semana-02)
* 📄 [Semana 03 - (Nome do tópico futuro) ](./semana-03)

# 🌀 Ciclo de Desenvolvimento: Projeto IA Subaquática (Modelo Espiral)

Para garantir a integridade dos drones em ambientes de alta pressão e baixa visibilidade, aplicamos o **Modelo Espiral de Boehm**. Cada volta na espiral é um seguro contra falhas catastróficas.

---

## 📍 Detalhamento de um Ciclo (Iteração de Estabilidade de Navegação)

Abaixo, descrevemos o que ocorre em cada quadrante para o desenvolvimento do módulo de **IA de Desvio de Obstáculos**.



### 1. Determinar Objetivos, Alternativas e Restrições (Q1)
* **Objetivo Central:** Implementar um algoritmo de visão computacional capaz de identificar redes de pesca e rochas em águas turvas.
* **Alternativas:** * Uso de Sensores Lidar (Alto custo/curto alcance).
    * Visão Estereoscópica com IA (Baixo custo/processamento intenso).
* **Restrições:** O drone possui apenas 8GB de RAM disponível para processamento de imagem em tempo real.

### 2. Avaliação e Redução de Riscos (Q2)
> *Este é o quadrante que evita a queda dos drones.*
* **Risco Identificado:** A IA pode falhar ao distinguir uma sombra de uma rocha, causando colisões ou manobras bruscas que drenam a bateria.
* **Ação de Mitigação:** Criação de um **Protótipo de Baixa Fidelidade** em simulador subaquático (Gazebo/Unity) para testar o comportamento do modelo antes de ir para a água real.
* **Análise de Falha:** Teste de "Falso Positivo" para garantir que o drone não pare desnecessariamente em correntes fortes.

### 3. Desenvolvimento e Verificação (Q3)
* **Codificação:** Implementação do modelo de rede neural otimizado para o hardware embarcado.
* **Integração:** Conexão do módulo de IA com o sistema de propulsão do drone.
* **Validação:** Testes em tanque controlado com obstáculos físicos reais e monitoramento de telemetria em tempo real.

### 4. Planejamento do Próximo Ciclo (Q4)
* **Revisão de Desempenho:** A IA atingiu 98% de precisão no desvio de obstáculos?
* **Feedback da Engenharia:** O hardware aqueceu demais durante o processamento?
* **Próximo Passo:** Planejar a integração do módulo de **Comunicação Acústica** para o próximo giro da espiral.

---

> **Nota Crítica:** No Modelo Espiral, o projeto só avança para o Quadrante 3 se o Quadrante 2 (Riscos) der "Luz Verde". Se o risco de colisão for alto, o design é revisado **antes** de gastarmos recursos com a fabricação do drone.
