# 🚨 Projeto: Sistema de Prevenção e Alerta de Desastres Naturais

Este documento detalha o levantamento de necessidades, a definição de Histórias de Usuário e a base técnica para o desenvolvimento de uma solução focada na proteção da vida e do patrimônio da população de São João da Boa Vista.

---

## 1. Captura de Necessidades 🎯

O projeto nasce para suprir uma lacuna crítica no sistema de ajuda à população, com foco em:
* **Prevenção:** Reduzir danos materiais e físicos causados por desastres naturais.
* **Acessibilidade:** Garantir que o alerta alcance o cidadão **mesmo sem internet** ou sem a necessidade de um aplicativo instalado (ex: via protocolos de rede celular ou rádio).

---

## 2. Histórias de Usuário (Método CARD) 📝

As histórias abaixo foram refinadas para garantir que o desenvolvimento seja focado no valor entregue ao usuário final.

### História 1: Emissão de Alerta Crítico
* **Como:** Agente da Defesa Civil.
* **Eu quero:** Disparar um alerta geolocalizado através da plataforma web.
* **Para que:** A população da região afetada receba o aviso instantaneamente e possa proteger seus bens e sua integridade física.

### História 2: Gerenciamento de Áreas de Risco
* **Como:** Gestor público da Prefeitura de São João da Boa Vista.
* **Eu quero:** Cadastrar e monitorar os bairros com maior incidência de transtornos climáticos.
* **Para que:** As ações de socorro sejam direcionadas de forma eficiente.

### História 3: Acesso à Informação (Cidadão)
* **Como:** Morador de uma área vulnerável.
* **Eu quero:** Receber notificações de emergência de forma passiva (sem depender de busca ativa ou sinal de internet estável).
* **Para que:** Eu tenha tempo hábil de reagir a um desastre natural iminente.

---

## 3. Organização Técnica 🛠️

Para viabilizar as funcionalidades descritas, serão mobilizadas as seguintes competências:

### 🌐 Interface e Dados
* **Tecnologias:** HTML5, CSS3 e JavaScript.
* **Aplicação:** Construção do dashboard de controle para a Defesa Civil e Prefeitura.
* **Intercâmbio:** Uso de **JSON** para comunicação entre o front-end e o servidor de alertas.

### 🐍 Lógica de Servidor (Backend)
* **Linguagem:** Python.
* **Aplicação:** * Processamento lógico dos alertas geolocalizados.
    * Integração com bancos de dados para armazenamento de áreas de risco.
    * Gerenciamento da comunicação com serviços de broadcast (transmissão de mensagens).

---

## 🚀 Próximos Passos
1.  Definição dos Critérios de Aceite para cada História.
2.  Prototipagem da interface de disparo de alertas.
3.  Pesquisa técnica de integração com protocolos de alerta celular (Cell Broadcast).
