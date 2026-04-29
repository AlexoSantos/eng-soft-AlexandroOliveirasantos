# 📐 Exercícios de Revisão — Semana 10
**Engenharia de Software** | Prof. Gaio B. Oliveira | 28/04/2026

> Modelos de Contexto e Interação (Sommerville) — Identificação de fronteiras e interação entre atores.

---

## Cenário 1 — Logística de E-commerce Global
**Diagrama Sugerido: Diagrama de Contexto**

### Análise
O **Sistema de Logística** é a caixa preta central. Tudo fora dele é entidade externa:
- **Estoque Interno** — fornece dados de disponibilidade de mercadoria
- **Transportadora** — responde com status de entrega
- **Receita Federal** — recebe dados e emite a Nota Fiscal

A fronteira deixa claro que o sistema *não controla* o estoque nem a transportadora — ele apenas se comunica com eles via interfaces definidas.

```mermaid
graph LR
    EI["📦 Estoque Interno"]
    TR["🚚 Transportadora"]
    RF["🏛️ Receita Federal"]

    subgraph SISTEMA["🖥️  Sistema de Logística E-commerce"]
        CORE["Gerenciamento\nde Despacho"]
    end

    EI -->|"Dados de disponibilidade"| CORE
    CORE -->|"Consulta status de entrega"| TR
    TR -->|"Retorna status"| CORE
    CORE -->|"Envia dados da mercadoria"| RF
    RF -->|"Nota Fiscal emitida"| CORE
```

---

## Cenário 2 — Totem de Autoatendimento em Fast-Food
**Diagrama Sugerido: Diagrama de Casos de Uso**

### Análise
Os **atores** são quem interage com o sistema — diretamente (Cliente, Cozinheiro) ou indiretamente (sistemas externos como Pagamento e Fidelidade). Os **casos de uso** representam as funcionalidades de valor entregues a cada ator.

| Ator | Valor recebido |
|---|---|
| 👤 Cliente | Autonomia para pedir e pagar sem fila |
| 👨‍🍳 Cozinheiro | Visualiza pedidos automaticamente |
| 💳 Gateway de Pagamento | Processa transações do totem |
| ⭐ Sist. Fidelidade | Recebe atualização de pontos |

```mermaid
graph LR
    CLI(["👤 Cliente"])
    COZ(["👨‍🍳 Cozinheiro"])
    PAG_EXT(["💳 Gateway de\nPagamento"])
    FID(["⭐ Sist. Fidelidade"])

    subgraph SISTEMA["🖥️  Totem de Autoatendimento"]
        UC1(["Fazer Pedido"])
        UC2(["Realizar Pagamento"])
        UC3(["Visualizar Pedido\nna Cozinha"])
        UC4(["Atualizar Pontos\nde Fidelidade"])
    end

    CLI --> UC1
    CLI --> UC2
    COZ --> UC3
    UC1 -->|"<<include>>"| UC3
    UC2 --> PAG_EXT
    UC2 -->|"<<include>>"| UC4
    UC4 --> FID
```

---

## Cenário 3 — Sistema de Telemedicina (Monitoramento)
**Diagrama Sugerido: Diagrama de Sequência**

### Análise
O foco é na **ordem cronológica das mensagens**. Usamos um bloco `alt` para representar o desvio condicional: só há consulta ao histórico e alerta ao médico **se** uma alteração for detectada. Caso contrário, o app apenas registra a leitura normal.

Participantes identificados:
1. 🫀 **Sensor Cardíaco** — origem dos dados
2. 📱 **App Mobile** — analisa e intermedia
3. 🖥️ **Servidor** — armazena histórico e dispara alertas
4. 👨‍⚕️ **Tablet do Médico** — destino do alerta

```mermaid
sequenceDiagram
    participant S as 🫀 Sensor Cardíaco
    participant A as 📱 App Mobile
    participant SRV as 🖥️ Servidor
    participant M as 👨‍⚕️ Tablet do Médico

    S->>A: Envia dados cardíacos (batimentos, ritmo)
    A->>A: Analisa os dados recebidos

    alt Alteração detectada
        A->>SRV: Solicita histórico do paciente
        SRV-->>A: Retorna histórico clínico
        A->>SRV: Reporta alteração crítica
        SRV->>M: Dispara alerta imediato
        M-->>SRV: Confirma recebimento do alerta
    else Dados dentro da normalidade
        A->>A: Registra leitura como normal
    end
```

---

## Cenário 4 — Sistema de Controle de Acesso Inteligente
**Diagrama Sugerido: Diagrama de Atividades com Swimlanes**

### Análise
As **raias (swimlanes)** separam as responsabilidades de cada participante, tornando explícito **quem faz o quê** no processo:
- **Usuário** — ação física de aproximar o celular
- **App** — toda a lógica de validação e decisão
- **Hardware** — executa o comando físico de destrancar

O nó de decisão `Tem reserva ativa?` é o coração do fluxo.

```mermaid
flowchart TD
    subgraph USR["👤 Usuário"]
        A([Aproxima o celular\nda fechadura])
        H([Porta destrancada —\nAcesso liberado ✅])
        I([Acesso negado ❌])
    end

    subgraph APP["📱 App / Sistema"]
        B[Detecta aproximação\nvia NFC/Bluetooth]
        C{Tem reserva\nativa agora?}
        E[Envia comando\nDESTRANCAR]
        D[Exibe mensagem:\nSem reserva ativa]
    end

    subgraph HW["🔒 Hardware — Fechadura"]
        F[Aciona mecanismo\nde desbloqueio]
    end

    A --> B
    B --> C
    C -- Sim --> E
    C -- Não --> D
    E --> F
    F --> H
    D --> I
```

---

## Cenário 5 — Marketplace de Serviços Domésticos
**Diagrama Sugerido: Diagrama de Casos de Uso (com extensões)**

### Análise das relações `<<include>>` e `<<extend>>`

| Relação | Entre | Motivo |
|---|---|---|
| `<<include>>` | Buscar Profissional → Filtrar | O filtro **sempre ocorre** ao buscar — é obrigatório |
| `<<include>>` | Realizar Pagamento → Emitir Comprovante | Comprovante **sempre** acompanha o pagamento |
| `<<extend>>` | Avaliar Profissional → Realizar Pagamento | A avaliação é **opcional** — acontece depois do pagamento, mas não é obrigatória |

> 💡 **Decisão de design:** "Avaliar Profissional" é um `<<extend>>` de "Realizar Pagamento" pois a avaliação não é mandatória para completar o fluxo principal. O sistema funciona normalmente mesmo se o cliente não avaliar.

```mermaid
graph LR
    CLI(["👤 Cliente"])
    PRO(["🔧 Profissional"])
    PAG_EXT(["💳 Gateway de\nPagamento"])

    subgraph SISTEMA["🏠 Marketplace de Serviços Domésticos"]
        UC1(["Buscar Profissional"])
        UC2(["Filtrar por Localização\ne Disponibilidade"])
        UC3(["Contratar Serviço"])
        UC4(["Realizar Pagamento"])
        UC5(["Avaliar Profissional"])
        UC6(["Emitir Comprovante"])
    end

    CLI --> UC1
    CLI --> UC3
    CLI --> UC4
    CLI -.->|"<<extend>>"| UC5

    PRO --> UC3

    UC1 -->|"<<include>>"| UC2
    UC4 -->|"<<include>>"| UC6
    UC4 --> PAG_EXT
    UC5 -.->|"pós-pagamento\n(opcional)"| UC4
```

---

## 💬 Resposta à Pergunta Final do Prof.

> *"Qual desses cenários parece o mais desafiador para definir o que está 'fora' do sistema?"*

**Cenário 1 (Logística E-commerce)** é o mais desafiador para definir fronteiras, pois o **Estoque Interno** pode causar ambiguidade: ele é parte *da empresa*, mas não parte do *sistema de logística* em si. A tentação é incluí-lo dentro da fronteira, mas o correto é tratá-lo como entidade externa com a qual o sistema se comunica por interface. Essa distinção entre "sistema da empresa" e "este sistema" é típica de projetos reais e exige clareza sobre o escopo do software.

---

## 📚 Referência

SOMMERVILLE, Ian. *Engenharia de Software*. 10ª ed. Pearson, 2019.
- Cap. 5 — Modelagem de Sistema
- Modelos de Contexto e Modelos de Interação

