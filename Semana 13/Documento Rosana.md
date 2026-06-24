# Projeto de Pesquisa e Extensão
## Sistema de Alerta Inteligente (SAI)
### Documento de Visão
**Versão:** 0.1.0  
**Data:** 23/06/2026  

---

### 1. Introdução

#### 1.1 Finalidade
Este documento apresenta a visão geral do projeto do **Sistema de Alerta Inteligente (SAI)**, abordando objetivos, escopo, funcionalidades e usuários envolvidos. Serve como referência para o alinhamento institucional e técnico da equipe responsável pelo desenvolvimento e implantação da solução.

#### 1.2 Escopo
O sistema consiste em uma plataforma digital unificada voltada para o monitoramento ambiental, prevenção de riscos e emissão de alertas em tempo real para o IFSP - Câmpus São João da Boa Vista, Defesa Civil e parceiros. O foco é a consolidação de dados e consulta pública de alertas, sem envolvimento direto com a gestão interna de equipes de campo. 

O sistema abrange todos os tipos de público, contando com acessibilidade rigorosa para pessoas com necessidades especiais de acordo com as normas W3C e WCAG. Cada alerta, dado climático ou evento de risco mapeado será proveniente de sistemas e APIs integrados à plataforma que liberam informações públicas, utilizando métodos como:
* Consulta a informações internas e raspagem de dados (*data scraping*) dos sites e sensores das instituições parceiras.

As principais informações serão exibidas em um painel web de forma responsiva através de um mapa interativo e banners de alerta urgentes , além de uma seção adaptada com acessibilidade para pessoas com necessidades especiais.Para que o sistema alcance o público-alvo de forma eficaz, serão desenvolvidas estratégias de Marketing de Utilidade Pública segmentadas por público e gravidade do risco. Campanhas personalizadas em datas sazonais críticas (ex: períodos de alta estiagem ou fortes chuvas) serão criadas para ampliar o engajamento e a prevenção, acompanhadas de análises contínuas de resultados para a evolução das estratégias.

#### 1.3 Definições, Acrogramas e Abreviaturas
* **SAI:** Sistema de Alerta Inteligente.
* **IFSP:** Instituto Federal de Educação, Ciência e Tecnologia de São Paulo.
* **W3C:** *World Wide Web Consortium* (Organização internacional que desenvolve padrões e diretrizes para a web, garantindo seu crescimento a longo prazo).
* **WCAG:** *Web Content Accessibility Guidelines* (Diretrizes de Acessibilidade para Conteúdo Web).
* **PCD:** Pessoa com Deficiência.

---

### 2. Posicionamento

#### 2.1 Descrição do Problema
* **O problema:** Falta de um projeto integrador com a Defesa Civil, órgãos municipais e o Instituto Federal de São Paulo que vise o monitoramento ambiental e a propagação ágil de alertas de risco para a comunidade. Há dificuldade na divulgação centralizada das ocorrências e dados preventivos, agravada pela ausência de critérios de acessibilidade digital, o que gera exclusão de parte da comunidade.Os sistemas das organizações associadas operam de forma isolada como sistemas legados, dificultando a interoperabilidade e a distribuição fluida da informação. Além disso, nota-se a falta de estratégias de comunicação e marketing direcionadas a identificar e atingir o público de risco de forma dinâmica e sazonal.
* **Afeta:** Alunos, servidores, comunidade externa, moradores de áreas de risco, parceiros institucionais, pessoas com necessidades especiais e órgãos de monitoramento com escassez de dados integrados.
* **O seu impacto é:** Baixa visibilidade de riscos iminentes, pouca participação em simulações preventivas, falta de organização das ações emergenciais, exclusão de PCDs de avisos vitais e desconhecimento geral das ferramentas de segurança disponíveis.
* **A solução ideal seria:** Uma plataforma digital que reúna, organize e permita consultar alertas e dados ambientais promovidos pelo ecossistema do projeto. A solução será construída através da integração de sistemas em uma única aplicação web, realizando a interoperabilidade entre aplicações (incluindo sistemas legado) por meio de uma API de raspagem de dados públicos. Deve contar com estratégias de comunicação segmentadas por públicos e períodos sazonais estratégicos. Para garantir a inclusão, a plataforma deve ser totalmente acessível (normas W3C e WCAG) com filtros específicos informando as adaptações oferecidas (abrangendo Altas Habilidades, Transtornos Globais do Desenvolvimento e do Aprendizado). No cadastro, o usuário indicará sua necessidade especial para que o sistema recomende automaticamente o formato de alerta ideal para suas especificidades.

#### 2.2 Sentença de Posição do Produto
* **Para:** Membros da comunidade acadêmica, moradores de São João da Boa Vista e região, incluindo pessoas com necessidades especiais e áreas sob monitoramento de risco.
* **Quem:** Desejam consultar alertas ambientais, riscos climáticos e eventos de emergência de maneira acessível, ágil e organizada.
* **O Produto:** O Sistema de Alerta Inteligente (SAI).
* **Que:** É um sistema unificado de monitoramento preventivo e consulta digital de riscos e alertas.
* **Diferentemente dos:** Meios dispersos, informais ou atrasados de divulgação de incidentes e boletins meteorológicos.
* **Nosso produto:** Proporciona acesso centralizado, filtros de pesquisa por localidade/risco, interoperabilidade com sistemas legados e acessibilidade digital estrita.

---

### 3. Descrições dos Envolvidos e Usuários

#### 3.1 Resumo dos Envolvidos (Stakeholders)

| Nome | Descrição | Responsabilidades |
| :--- | :--- | :--- |
| **Instituto Federal de São Paulo (IFSP)** | Campus SJBV, alunos e pesquisadores interessados no funcionamento do sistema. | Idealizador, gestor, mantenedor e desenvolvedor da plataforma técnica de alertas. |
| **Defesa Civil / Órgãos Parceiros** | Órgão municipal e entidades parceiras interessadas na implementação dos alertas. | Fornecer a demanda de riscos, dados ambientais locais e validar as informações técnicas. |
| **Equipe Técnica e Docente do IFSP** | Professores e técnicos administrativos orientadores do projeto. | Produção, supervisão técnica, validação científica e atualização das regras do sistema. |
| **População Sanjoanense e Região** | População geral, incluindo PCDs, pessoas com superdotação ou necessidades tecnológicas específicas. | Usufruir da consulta de alertas, receber notificações preventivas e participar das ações coordenadas. |
| **API de Raspagem de Dados** | Módulo automatizado integrado ao ecossistema do projeto. | Desenvolver uma API separada do sistema principal para realizar consultas automáticas e raspagem em bases de dados públicas parceiras. |

#### 3.2 Resumo dos Usuários

| Nome | Descrição/Atitude | Grau de Poder | Grau de Interesse | Positivos | Negativos |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Usuário Público Geral** | Cidadão interessado em monitorar riscos e receber alertas na sua região. | Baixo  | Alto  | Sim  |Não  |
| **Docente / Técnico Operador** | Responsável por validar, cadastrar e emitir os alertas ou gerenciar dados. | Médio  | Alto  | Sim | Não  |
| **Administrador do Sistema** | Gerencia a infraestrutura, permissões de acesso e suporte técnico das integrações. | Alto  | Médio  | Sim  | Não  |
| **PCDs ou Necessidades Específicas** | Usuários que necessitam de alertas em formatos acessíveis e customizados. | Baixo  | Alto  | Sim  | Não  |

#### 3.3 Necessidades Principais dos Envolvidos ou Usuários

| Necessidade | Prioridade | Preocupações | Solução Atual | Soluções Propostas |
| :--- | :--- | :--- | :--- | :--- |
| [cite_start]Acesso centralizado aos alertas e dados de risco[cite: 81]. | [cite_start]Alta [cite: 81] | [cite_start]Baixa visibilidade de riscos e incidentes em tempo real[cite: 81]. | [cite_start]Divulgação de forma isolada por múltiplos órgãos[cite: 81]. | [cite_start]Plataforma digital integrada e centralizada[cite: 81]. |
| [cite_start]Consulta de riscos por filtros específicos (ex: bairro, tipo de evento)[cite: 81]. | [cite_start]Alta [cite: 81] | [cite_start]Dificuldade de busca rápida em momentos de urgência[cite: 81]. | [cite_start]Não aplicável[cite: 81]. | [cite_start]Painel com filtros avançados de pesquisa[cite: 81]. |
| [cite_start]Atualização constante e automatizada do conteúdo[cite: 81]. | [cite_start]Média [cite: 81] | [cite_start]Informações desatualizadas comprometendo a segurança pública[cite: 81]. | [cite_start]Atualização e digitação manual[cite: 81]. | [cite_start]Cadastro simplificado e raspagem via sistema[cite: 81]. |
| [cite_start]Acessibilidade total no recebimento de notificações[cite: 81, 88]. | [cite_start]Alta [cite: 88] | [cite_start]Dificuldade de navegação e exclusão de PCDs em emergências[cite: 88, 99]. | [cite_start]Nenhuma acessibilidade estruturada[cite: 88]. | [cite_start]Layout acessível baseado nas diretrizes WCAG e W3C[cite: 88, 120]. |
| [cite_start]Painel de Moderação e Validação de Alertas[cite: 88]. | [cite_start]Alta [cite: 88] | [cite_start]Informações erradas, alarmistas ou alarmes falsos[cite: 88]. | [cite_start]Nenhuma[cite: 88]. | [cite_start]Painel administrativo de moderação para incluir, alterar ou excluir alertas[cite: 88]. |
| [cite_start]Canal de Comunicação e Suporte[cite: 88]. | [cite_start]Média [cite: 88] | [cite_start]Dúvidas da população sobre os procedimentos de segurança[cite: 88]. | [cite_start]Nenhuma[cite: 88]. | [cite_start]Campo de envio de mensagens e respostas diretas dos responsáveis técnicos[cite: 88]. |
| [cite_start]Planejamento de campanhas segmentadas de prevenção[cite: 88]. | [cite_start]Alta [cite: 88] | [cite_start]Divulgação preventiva pouco eficaz ou ignorada[cite: 88]. | [cite_start]Nenhuma[cite: 88]. | [cite_start]Estratégias de Marketing Digital e Avisos segmentados por categoria de risco e público[cite: 88]. |
| [cite_start]Aproveitamento de períodos sazonais para alertas preventivos[cite: 88]. | [cite_start]Alta [cite: 88] | [cite_start]Perda de janelas críticas de prevenção (ex: estiagem/queimadas)[cite: 88]. | [cite_start]Nenhuma[cite: 88]. | [cite_start]Disparar avisos estruturados e alinhados a datas e climas sazonais estratégicos[cite: 88]. |
| [cite_start]Integração automática com calendários externos[cite: 140]. | [cite_start]Média [cite: 127] | [cite_start]Esquecimento de simulações de evacuação ou vistorias por falta de anotação [cite: 130-135]. | [cite_start]Nenhuma[cite: 136]. | [cite_start]Integração direta do sistema com a API do Google Calendar[cite: 140]. |
| [cite_start]Interoperabilidade com sensores e sistemas parceiros [cite: 145-148]. | [cite_start]Alta [cite: 149] | [cite_start]Falta de disponibilidade imediata dos dados ambientais brutos [cite: 150-153]. | [cite_start]Nenhuma[cite: 154]. | [cite_start]Criação de fluxos automatizados e APIs de raspagem contínua de dados legados [cite: 156-158]. |

---

### 4. Visão Geral do Produto

#### 4.1 Perspectiva do Produto
[cite_start]O sistema será acessível via ambiente web com compatibilidade multiplataforma, voltado inteiramente à consulta pública e governamental de dados ambientais e alertas de risco promovidos pelo IFSP, Defesa Civil e parceiros[cite: 162]. [cite_start]Ele consistirá em um site responsivo e integrado com os sistemas legados dos parceiros locais municipais, solucionando em definitivo os problemas de interoperabilidade entre aplicações antigas[cite: 163]. 

[cite_start]A partir dessa automação, o sistema garantirá a disponibilidade e a unificação dos dados climáticos e de risco em tempo real[cite: 164]. [cite_start]Adicionalmente, toda a plataforma será desenvolvida seguindo os padrões internacionais de acessibilidade digital das diretrizes W3C e WCAG, assegurando que pessoas com deficiências de naturezas diversas naveguem e interpretem os avisos com total facilidade e segurança[cite: 165].

#### 4.2 Suposições e Dependências
* [cite_start]Disponibilidade da equipe técnica do projeto para o desenvolvimento e manutenção das rotinas de software[cite: 173];
* [cite_start]Cooperação e engajamento dos docentes e técnicos da Defesa Civil para validação e atualização contínua dos parâmetros de alerta[cite: 174];
* [cite_start]Concessão de acessos aos portais institucionais e sensores físicos municipais para viabilizar as integrações técnicas[cite: 175];
* [cite_start]Acompanhamento contínuo e aplicação prática das estratégias de comunicação e marketing de utilidade pública segmentadas[cite: 176];
* [cite_start]Planejamento de campanhas sazonais alinhadas aos períodos climáticos críticos e eventos de risco locais[cite: 177];
* [cite_start]Compromisso ético e técnico com a implementação rigorosa dos padrões WCAG para inclusão total dos usuários[cite: 178];
* [cite_start]Disponibilização e abertura das bases de dados dos parceiros para execução da raspagem de dados manual ou automatizada[cite: 179].

---

### 5. Recursos do Produto

#### 5.1 Cadastro e Edição de Alertas e Eventos de Risco
[cite_start]Sistema intuitivo voltado para operadores registrarem e atualizarem informações sobre áreas de risco, alertas de tempestades, queimadas ou bloqueios, contendo campos detalhados, mapas de calor e opção de anexar documentos instrutivos de segurança, contando com rigorosa validação dos dados inseridos [cite: 181-183].

#### 5.2 Consulta com Filtros Avançados e Performance
[cite_start]Mecanismo de busca otimizado que permite ao cidadão filtrar os alertas ativos por tipo de risco, nível de gravidade, bairro e proximidade geográfica[cite: 185]. [cite_start]O recurso emprega cache inteligente de dados para impedir lentidão ou travamentos na interface durante as buscas[cite: 186].

#### 5.3 Exportação de Dados e Relatórios Históricos
[cite_start]Opção para exportar dados estatísticos consolidados sobre os incidentes e métricas ambientais nos formatos PDF, CSV e XLSX, facilitando análises técnicas e prestação de contas por parte da Defesa Civil [cite: 192-194].

#### 5.4 Integração em Tempo Real com Páginas Parceiras
[cite_start]Sincronização automatizada com o portal do IFSP e prefeituras associadas, exibindo os alertas vigentes nas páginas principais sem necessidade de retrabalho ou atualizações manuais duplicadas [cite: 195-197].

#### 5.5 Interface Inclusiva Adaptada (W3C/WCAG)
[cite_start]Desenvolvida estritamente em conformidade com as diretrizes WCAG da W3C[cite: 199]. [cite_start]Para PCDs, inclui navegação completa via teclado, suporte avançado para leitores de tela, contrastes dinâmicos e descrições alternativas para mapas e gráficos[cite: 200]. [cite_start]Para usuários com superdotação ou necessidades cognitivas específicas, fornece controle sobre estímulos visuais, ajustes de velocidade e recursos que suportam variados perfis de processamento de informação[cite: 201].

#### 5.6 Integração de Avisos com API de Calendários
[cite_start]Uso integrado da API do Google Calendar para inserir e notificar automaticamente as datas de simulações de evacuação, treinamentos preventivos da Defesa Civil e vistorias públicas mapeadas no ecossistema de dispositivos dos cidadãos[cite: 202, 203].

#### 5.7 Cadastro Customizado de Necessidades Assistivas
[cite_start]A plataforma conterá um formulário de cadastro adaptado onde o usuário informará suas particularidades físicas ou cognitivas (deficiência visual, auditiva, motora ou superdotação)[cite: 210]. [cite_start]O sistema usará as informações para ativar automaticamente as tecnologias assistivas ideais e personalizar a entrega dos alertas conforme o perfil[cite: 211].

#### 5.8 Sistema de Notificações Pró-Ativas Personalizadas
[cite_start]Permite aos cidadãos se inscreverem para receber alertas críticos urgentes via canais digitais (como e-mail ou push) filtrados estritamente por suas regiões de moradia, trabalho ou interesses cadastrados, fomentando uma cultura proativa de proteção [cite: 212-214].

#### 5.9 Monitoramento e Log de Integração de Dados
[cite_start]Painel exclusivo que exibe em tempo real o status das coletas automatizadas de dados (sucesso, falha ou pendência), indicando a origem da informação, o horário exato da última raspagem (*scraping*) e os códigos de erro detalhados [cite: 215-217]. [cite_start]O painel mantém logs históricos transparentes (volume de dados processados, tempo de execução, fonte de origem), simplificando o diagnóstico e a correção rápida de falhas por parte da equipe técnica[cite: 218].

---

### 6. Benefícios ao Usuário e Recursos de Suporte

| Benefícios ao Usuário | Recursos de Suporte |
| :--- | :--- |
| [cite_start]Acesso rápido, centralizado e facilitado a dados de risco e alertas urgentes na cidade[cite: 219]. | [cite_start]Treinamento técnico e operacional fornecido para usuários internos (docentes e equipe da Defesa Civil)[cite: 219]. |
| [cite_start]Consulta altamente eficiente, ágil e personalizada por geolocalização[cite: 219]. | [cite_start]Disponibilização de documentação de uso completa e guias de segurança[cite: 219]. |
| [cite_start]Histórico consolidado de ocorrências ambientais aberto para toda a comunidade[cite: 223]. | [cite_start]Equipe técnica de suporte dedicada para manutenção e ajustes de infraestrutura[cite: 223]. |
| [cite_start]Recebimento de alertas direcionados conforme o local em que reside ou trabalha[cite: 223]. | [cite_start]Planejamento, gestão e automação de campanhas digitais e comunicados preventivos[cite: 223]. |
| [cite_start]Divulgação otimizada em períodos de pico climático e sazonalidades críticas[cite: 223]. | [cite_start]Equipe técnica encarregada de gerenciar e monitorar as integrações automatizadas sazonais[cite: 223]. |
| [cite_start]Área exclusiva com informações e formatos adaptados para suas exatas necessidades assistivas[cite: 223]. | [cite_start]Facilidade para encontrar diretrizes claras que atendam perfeitamente o perfil de vulnerabilidade do usuário[cite: 223]. |
| [cite_start]Cadastro flexível adaptado que ajusta o comportamento e a acessibilidade da interface de imediato[cite: 223]. | [cite_start]Definição clara e automatizada de quais tecnologias assistivas serão ativadas para cada cidadão[cite: 223]. |
| [cite_start]Conformidade e segurança contínuas com os protocolos WCAG, garantindo personalização a todos de forma inclusiva[cite: 223]. | [cite_start]Equipe técnica de design e acessibilidade focada na auditoria e evolução das normas WCAG do portal[cite: 223]. |
| [cite_start]Notificações proativas e imediatas baseadas em interesses e localização geográfica, elevando a segurança ativa[cite: 223]. | [cite_start]Sistema automatizado de mensageria com filtros configuráveis interligado com o banco de dados principal[cite: 223]. |
