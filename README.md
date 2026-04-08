# eng-soft-AlexandroOliveiraSantos
Engenharia de Software
Portfólio de Engenharia de Software

**Dev:** [Alexandro Oliveira dos Santos]  
**Disciplina:** Engenharia de Software - Sistemas para Internet  

Relatório de Gestão de Projetos e Maturidade de Software
Este repositório contém a análise técnica para a recuperação do projeto de IA subaquática e o diagnóstico de maturidade organizacional da Chaos-IT, fundamentados nos frameworks de Sommerville e CMMI.

Parte 1: O Labirinto de Boehm (Modelo Espiral)
A Defesa do Modelo Espiral
A queda dos drones de IA subaquática não foi uma falha apenas de hardware, mas de gestão de incertezas. Segundo Ian Sommerville, o Modelo Espiral de Boehm é orientado a riscos. No modelo de cascata tradicional, os riscos só aparecem na fase de testes (tarde demais).

Na Espiral, a Análise de Riscos ocorre em cada iteração. Ela teria evitado a queda dos drones ao identificar:

Riscos Ambientais: Pressão e salinidade afetando a IA antes da construção do protótipo final.

Riscos de Algoritmo: Simulações de visão computacional em águas turvas antes do lançamento em campo.

Ciclo de Desenvolvimento (IA Subaquática)
Para o próximo ciclo do projeto, cada quadrante da espiral focará em:

Objetivos (Definição): Definir os requisitos de autonomia da IA e os limites de profundidade suportados.

Avaliação e Redução de Riscos: Realizar testes de estresse em câmara hiperbárica e simulações de perda de sinal. Se o risco de perda do drone for > 10%, o design deve ser revisado.

Desenvolvimento e Validação: Implementar o código de navegação e realizar testes em piscina controlada (prototipagem rápida).

Planejamento: Revisar os resultados com os stakeholders e planejar a próxima volta da espiral (testes em mar aberto).

Parte 2: O Diagnóstico CMMI
Análise da Chaos-IT
Com base na descrição do cenário (processos reativos, falta de padronização e dependência de "heróis" individuais), a empresa encontra-se no:

Nível de Maturidade 1: Inicial (Initial)

Características Observadas: O sucesso depende do esforço individual. Não há repetição de processos. O ambiente é instável e o cronograma é frequentemente negligenciado frente a crises.

Diagnóstico: A Chaos-IT "apaga incêndios" em vez de gerir projetos.

O Caminho para o Nível 2 (Gerenciado)
Para subir de nível, a Chaos-IT precisa institucionalizar a gestão. O que falta:

Gestão de Requisitos: Estabelecer um processo formal para aceitar e mudar requisitos, evitando o "scope creep".

Planejamento de Projeto: Criar estimativas baseadas em dados históricos, não em intuição.

Monitoramento e Controle: Implementar métricas para acompanhar o progresso real versus o planejado.

Gestão de Configuração: Garantir que o código e a documentação estejam versionados e seguros.
