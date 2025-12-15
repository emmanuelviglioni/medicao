# Plano de Experimento – Scoping e Planejamento

**Tema:** Comparação de Desempenho entre Algoritmos de Controle de Semáforos: Deep Reinforcement Learning Adaptativo x Sistema de Tempo Fixo em Ambiente de Simulação Urbana

## 1. Identificação Básica

### 1.1 Título do Experimento

Avaliação do Impacto de um Algoritmo Adaptativo Baseado em Deep Reinforcement Learning na Redução de Tempo de Espera e Tempo de Viagem em Comparação com um Sistema de Semáforo de Tempo Fixo em Ambiente de Simulação de Tráfego Urbano.

### 1.2 ID / Código

EXP-TSC-DRL-2025

### 1.3 Versão do Documento e Histórico de Revisão

| Versão | Data | Descrição |
|--------|------|-----------|
| v1.0 | 03/12/2025 | Versão inicial do documento |
| v1.1 | 08/12/2025 | Atualização do documento |
| v1.2 | 08/12/2025 | Adição de mais cruzamentos |
| v1.3 | 08/12/2025 | Melhorias na seção 20 |
| v1.4 | 15/12/2025 | Melhorias sugeridas pelo professor |

### 1.4 Datas

Criação do plano: 03/12/2025
Última atualização: 08/12/2025

### 1.5 Autores

Nome: Emmanuel Viglioni
Área: Engenharia de Software / Inteligência Artificial
Contato: emmanuelviglioni0@gmail.com

### 1.6 Responsável Principal

Emmanuel Viglioni

### 1.7 Projeto / Produto / Iniciativa Relacionada

Trabalho de Conclusão de Curso, relacionado a comparação e implementação de algoritmos de controle de semáforos.

---

## 2. Contexto e Problema

### 2.1 Descrição do Problema / Oportunidade

Sistemas de controle de semáforos com tempo fixo são amplamente utilizados em cidades brasileiras, mas apresentam limitações significativas. Esses sistemas não se adaptam às flutuações do tráfego em tempo real, resultando em congestionamentos desnecessários, aumento do tempo de viagem dos veículos e, consequentemente, maior consumo de combustível e emissões de poluentes. A oportunidade reside na aplicação de técnicas de Inteligência Artificial, especificamente Deep Reinforcement Learning (DRL), para criar um sistema de controle adaptativo capaz de tomar decisões em tempo real baseadas nas condições atuais do tráfego.

Este experimento busca analisar o impacto de um algoritmo adaptativo (DRL) em comparação com a abordagem tradicional de tempo fixo, medindo a redução no tempo de espera e no tempo total de viagem em um ambiente de simulação controlado.

### 2.2 Contexto Organizacional e Técnico

O experimento será conduzido em um contexto acadêmico, no âmbito de uma disciplina de Medição e Experimentação em Engenharia de Software. O ambiente técnico utiliza o software SUMO (Simulation of Urban Mobility), uma ferramenta de código aberto para simulação de tráfego. O algoritmo adaptativo será implementado em Python, utilizando técnicas de Deep Reinforcement Learning. A coleta de dados será automatizada através da interface TraCI (Traffic Control Interface), que permite a comunicação entre os scripts de controle e a simulação.

### 2.3 Trabalhos e Evidências Prévias

A literatura científica demonstra que sistemas de controle de tráfego adaptativos podem reduzir significativamente o tempo de espera e as emissões veiculares. Estudos anteriores indicam que algoritmos de aprendizado por reforço aplicados ao controle de semáforos apresentam melhorias de desempenho em relação aos sistemas de tempo fixo, com reduções de até 30% no tempo de viagem em cenários de simulação.

### 2.4 Referencial Teórico e Empírico Essencial

Este experimento se apoia em três pilares principais: Engenharia de Software Experimental, com foco em metodologia de medição e comparação de soluções; Inteligência Artificial, especificamente em Aprendizado por Reforço Profundo (Deep Reinforcement Learning) e Processos de Decisão de Markov (MDP); e Engenharia de Tráfego, considerando modelos de fluxo veicular e métricas de desempenho de redes viárias. A base teórica fundamenta a expectativa de que um sistema adaptativo, capaz de aprender e responder dinamicamente às condições de tráfego, será mais eficiente que um sistema rígido de tempo fixo.

---

## 3. Objetivos e Questões (Goal / Question / Metric)

### 3.1 Objetivo Geral

Analisar o impacto de um algoritmo adaptativo baseado em Deep Reinforcement Learning no desempenho de um sistema de controle de semáforos, avaliando a redução no tempo de espera e no tempo total de viagem em comparação com um sistema tradicional de tempo fixo, em um ambiente de simulação de tráfego urbano.

### 3.2 Objetivos Específicos

**3.2.1 Objetivo Específico 1 – Redução de Tempo de Espera**

Mensurar a redução no tempo médio de espera dos veículos nas interseções ao utilizar o algoritmo adaptativo (DRL) em comparação com o sistema de tempo fixo.

**3.2.2 Objetivo Específico 2 – Redução de Tempo de Viagem**

Avaliar a redução no tempo médio total de viagem dos veículos ao utilizar o algoritmo adaptativo (DRL) em comparação com o sistema de tempo fixo.

**3.2.3 Objetivo Específico 3 – Eficiência Relativa**

Comparar a eficiência dos dois algoritmos em diferentes cenários de tráfego (baixo volume, volume normal e hora de pico).

**3.2.4 Objetivo Específico 4 – Análise de Robustez e Estabilidade**

Verificar a estabilidade e a robustez do algoritmo DRL, analisando a consistência de seu desempenho e sua capacidade de evitar condições indesejadas, como o bloqueio prolongado de uma via (starvation).

### 3.3 Questões de Pesquisa

As questões de pesquisa são formuladas para serem respondidas através da análise dos dados coletados:

- **Q1:** O algoritmo adaptativo (DRL) reduz significativamente o tempo médio de espera em comparação com o sistema de tempo fixo?
- **Q2:** O algoritmo adaptativo (DRL) reduz significativamente o tempo médio de viagem em comparação com o sistema de tempo fixo?
- **Q3:** A magnitude da melhoria do algoritmo adaptativo varia significativamente entre diferentes cenários de tráfego?

### 3.4 Tabela GQM – Objetivos, Perguntas e Métricas

| Objetivo Específico | Perguntas de Pesquisa | Métricas Associadas |
|---|---|---|
| **O1: Redução de Tempo de Espera** | Q1.1: O algoritmo DRL reduz o tempo médio de espera em comparação com o sistema de tempo fixo? | M1, M2 |
| | Q1.2: Qual é a magnitude da redução do tempo de espera em cada cenário de tráfego? | M7, M9 |
| | Q1.3: O DRL consegue diminuir o tempo máximo que um veículo fica parado na fila? | M11, M12 |
| **O2: Redução de Tempo de Viagem** | Q2.1: O algoritmo DRL diminui o tempo médio de viagem dos veículos na rede? | M3, M4 |
| | Q2.2: A variabilidade (desvio padrão) do tempo de viagem é menor com o DRL, indicando maior previsibilidade? | M8, M10 |
| | Q2.3: Como o tempo de viagem se comporta nos diferentes cenários de tráfego para cada algoritmo? | M3, M4 |
| **O3: Eficiência Relativa e Vazão** | Q3.1: O algoritmo DRL aumenta a vazão de veículos (carros por hora) na rede? | M5, M6 |
| | Q3.2: Em qual cenário de tráfego (baixo, normal, pico) o ganho de desempenho do DRL é mais pronunciado? | M7, M8 |
| | Q3.3: O DRL é mais eficiente em reduzir o comprimento médio das filas? | M9, M2 |
| **O4: Análise de Robustez e Estabilidade** | Q4.1: O tempo de decisão do agente DRL é baixo o suficiente para operação em tempo real? | M10, M1 |
| | Q4.2: O algoritmo DRL evita o "starvation" (deixar uma via com sinal vermelho por tempo excessivo)? | M12, M2 |
| | Q4.3: O desempenho do DRL se mantém estável ao longo de toda a duração da simulação? | M10, M11 |

### Tabela Geral de Métricas

| ID | Métrica | Descrição | Unidade |
|---|---|---|---|
| M1 | Tempo Médio de Espera (DRL) | Tempo médio que um veículo permanece parado em um semáforo sob o controle do algoritmo DRL. | Segundos (s) |
| M2 | Tempo Médio de Espera (Tempo Fixo) | Tempo médio que um veículo permanece parado em um semáforo sob o controle do algoritmo de tempo fixo. | Segundos (s) |
| M3 | Tempo Médio de Viagem (DRL) | Tempo médio total que um veículo leva para atravessar a rede de 4 cruzamentos com o controle DRL. | Segundos (s) |
| M4 | Tempo Médio de Viagem (Tempo Fixo) | Tempo médio total que um veículo leva para atravessar a rede de 4 cruzamentos com o controle de tempo fixo. | Segundos (s) |
| M5 | Vazão da Rede (DRL) | Número total de veículos que completaram suas rotas na rede durante o período de simulação com o controle DRL. | Veículos/hora |
| M6 | Vazão da Rede (Tempo Fixo) | Número total de veículos que completaram suas rotas na rede durante o período de simulação com o controle de tempo fixo. | Veículos/hora |
| M7 | Redução Percentual de Espera | Ganho de desempenho do DRL em relação ao tempo fixo para a métrica de tempo de espera. Calculado como `((M2 - M1) / M2) * 100`. | Percentual (%) |
| M8 | Redução Percentual de Viagem | Ganho de desempenho do DRL em relação ao tempo fixo para a métrica de tempo de viagem. Calculado como `((M4 - M3) / M4) * 100`. | Percentual (%) |
| M9 | Comprimento Médio da Fila | Número médio de veículos parados em uma fila de semáforo em um determinado instante. | Veículos |
| M10 | Desvio Padrão do Tempo de Viagem | Medida da variabilidade ou consistência do tempo de viagem entre os veículos. Um valor menor indica maior previsibilidade. | Segundos (s) |
| M11 | Tempo Máximo de Espera | O maior tempo de espera individual registrado para um único veículo. | Segundos (s) |
| M12 | Tempo Máximo de Sinal Vermelho | O maior período contínuo de tempo que qualquer via ficou com o sinal vermelho, usado para verificar "starvation". | Segundos (s) |

---

## 4. Escopo do Experimento

| Seção | Descrição |
|---|---|
| **O que está DENTRO do escopo?** | |
| Foco do Experimento | Comparação de desempenho entre dois algoritmos de controle de semáforos: um de tempo fixo (baseline) e um adaptativo (DRL). |
| Ambiente | O experimento será conduzido exclusivamente em um ambiente de simulação utilizando o software SUMO. |
| Rede Viária | A análise será realizada em uma rede urbana simulada composta por uma malha 2x2, totalizando 4 cruzamentos. |
| Cenários de Tráfego | Serão avaliados três cenários distintos de densidade de tráfego: baixo, normal e pico. |
| Métricas Coletadas | As métricas primárias de análise são: tempo médio de espera por veículo e tempo médio de viagem total. Métricas secundárias como tamanho da fila e vazão também serão coletadas. |
| Análise | A análise dos dados será puramente quantitativa, com foco em testes de hipóteses estatísticas para comparar o desempenho dos algoritmos. |
| **O que está FORA do escopo?** | |
| Validação em Ambiente Real | O experimento não incluirá testes de campo ou validação em cruzamentos reais. Os resultados são restritos ao ambiente de simulação. |
| Outros Algoritmos de IA | A comparação se limita ao algoritmo DRL especificado. Outras técnicas de IA (e.g., redes neurais, lógica fuzzy, outros algoritmos de RL) não serão avaliadas. |
| Redes Complexas | A análise não será estendida para redes viárias de grande porte ou com topologias complexas (e.g., rotatórias, vias expressas). |
| Métricas de Impacto Ambiental | O escopo não inclui a medição de consumo de combustível, emissões de CO2 ou outros poluentes. |
| Fatores Humanos e Eventos Não Previstos | O experimento não modelará comportamentos de direção imprudentes, acidentes, obras na via ou outras anomalias que afetam o tráfego real. |
| Otimização de Parâmetros | O foco é na comparação dos algoritmos já treinados/configurados, não na otimização fina de seus hiperparâmetros. |

---

## 5. Instrumentação e Materiais

O experimento utiliza os seguintes instrumentos e materiais:

**Ferramentas de Simulação:**
- **SUMO (Simulation of Urban MObility):** Software de código aberto para simulação de tráfego, responsável pela geração do cenário viário, simulação do comportamento dos veículos e cálculo das métricas de desempenho.
- **TraCI (Traffic Control Interface):** Interface que permite a comunicação entre scripts Python e a simulação SUMO, permitindo a implementação dos algoritmos de controle e coleta de dados em tempo real.

**Linguagem e Bibliotecas:**
- **Python 3.8+:** Linguagem de programação para implementação dos algoritmos.
- **Bibliotecas:** NumPy e Pandas para manipulação de dados; Matplotlib para visualização; SciPy para análise estatística.

**Armazenamento de Dados:**
- **Arquivos CSV:** Para armazenar os resultados de cada execução da simulação, contendo as métricas coletadas.

**Ambiente:**
- Computador pessoal com sistema operacional Linux ou Windows com WSL2, com capacidade de processamento adequada para executar as simulações.

---

## 6. Procedimentos Operacionais

O experimento será executado seguindo um protocolo estruturado em etapas:

**Etapa 1: Preparação do Ambiente**

Inicialmente, o ambiente SUMO será configurado com a definição da rede viária (um cruzamento urbano simples), os padrões de geração de veículos para cada cenário de tráfego, e as características dos veículos simulados (velocidade máxima, aceleração, etc.). Os dois algoritmos de controle (Tempo Fixo e DRL) serão implementados em Python e integrados à simulação através da interface TraCI.

**Etapa 2: Execução das Simulações**

Para cada um dos três cenários de tráfego (baixo volume, volume normal, hora de pico), serão realizadas múltiplas execuções (réplicas) de simulação. Cada execução será designada aleatoriamente para um dos dois algoritmos de controle. O número de réplicas por algoritmo e por cenário será de 30, totalizando 180 execuções de simulação (30 réplicas × 2 algoritmos × 3 cenários).

Cada execução seguirá o seguinte procedimento:
1. Inicializar a simulação SUMO com o cenário de tráfego selecionado e uma semente aleatória única.
2. Aplicar o algoritmo de controle designado (Tempo Fixo ou DRL).
3. Executar a simulação por um período de tempo predefinido (por exemplo, 1 hora de tempo simulado).
4. Coletar as métricas de desempenho (tempo de espera e tempo de viagem) através da interface TraCI.
5. Registrar os resultados em um arquivo CSV, associando-os ao algoritmo, cenário e réplica.

**Etapa 3: Coleta e Consolidação de Dados**

Ao término de cada série de execuções para um cenário, os dados coletados serão consolidados e validados para garantir integridade e ausência de registros duplicados. Os dados serão preparados para a análise estatística posterior.

---

## 7. Modelo Conceitual e Hipóteses

### 7.1 Modelo Conceitual

O modelo conceitual postula que o **método de controle de semáforos** (variável independente) influencia diretamente a **eficiência do fluxo de tráfego** (variáveis dependentes). Acredita-se que um algoritmo adaptativo, capaz de aprender e responder dinamicamente às condições de tráfego em tempo real, será mais eficiente que um algoritmo rígido de tempo fixo. Essa adaptabilidade resultará em redução do tempo de espera nas interseções, o que, por sua vez, reduzirá o tempo total de viagem dos veículos.

**Diagrama Conceitual (Mermaid)**
<img width="2048" height="4772" alt="diagrama_conceitual" src="https://github.com/emmanuelviglioni/medicao/blob/main/refs/diagrama_conceitual.png" />

### 7.2 Hipóteses Formais

**Hipóteses relacionadas ao Objetivo O1 – Tempo de Espera**

- **H0_1:** Não há diferença significativa no tempo médio de espera entre o algoritmo adaptativo (DRL) e o sistema de tempo fixo.
- **H1_1:** O tempo médio de espera com o algoritmo adaptativo (DRL) é significativamente menor do que com o sistema de tempo fixo.

**Hipóteses relacionadas ao Objetivo O2 – Tempo de Viagem**

- **H0_2:** Não há diferença significativa no tempo médio de viagem entre o algoritmo adaptativo (DRL) e o sistema de tempo fixo.
- **H1_2:** O tempo médio de viagem com o algoritmo adaptativo (DRL) é significativamente menor do que com o sistema de tempo fixo.

**Hipóteses relacionadas ao Objetivo O3 – Eficiência Relativa**

- **H0_3:** A magnitude da melhoria do algoritmo adaptativo (DRL) é equivalente em todos os cenários de tráfego.
- **H1_3:** A magnitude da melhoria do algoritmo adaptativo (DRL) varia significativamente entre os cenários de tráfego, com maior benefício em cenários de alto volume.

### 7.3 Nível de Significância

O nível de significância (α) adotado para todos os testes de hipóteses será de **0,05**. Isso significa que há uma probabilidade de 5% de rejeitar a hipótese nula quando ela é verdadeira (erro do Tipo I).

---

## 8. Variáveis, Fatores, Tratamentos e Objetos de Estudo

### 8.1 Objetos de Estudo

Os objetos de estudo são os **algoritmos de controle de semáforos** implementados e testados no ambiente de simulação. Cada algoritmo representa uma abordagem distinta para a gestão do tráfego em uma rede de múltiplas interseções urbanas. Além disso, são considerados objetos de estudo os **registros de desempenho** gerados pela simulação, contendo as métricas de tempo de espera e tempo de viagem para cada execução. As rotas dos veículos atravessam a rede de 4 cruzamentos, permitindo medir o tempo total de viagem de ponta a ponta.

### 8.2 Sujeitos / Participantes (Visão Geral)

Neste experimento, não há participantes humanos. Os "sujeitos" são as **entidades virtuais** dentro da simulação: os veículos que se movem pela rede e as interseções onde o controle de semáforos é aplicado. O comportamento agregado desses sujeitos virtuais, sob a influência de cada algoritmo de controle, gera os dados para análise.

### 8.3 Tabela de Variáveis do Experimento

| Categoria da Variável | Nome da Variável | Descrição |
|---|---|---|
| **Variável Independente** | Algoritmo de Controle | O método utilizado para gerenciar os semáforos. É o fator principal que será manipulado no experimento. |
| | Cenário de Tráfego | A densidade do fluxo de veículos na simulação. Atua como um fator secundário para análise de adaptabilidade. |
| **Variáveis Dependentes** | Tempo Médio de Espera | O tempo médio que um veículo permanece parado em um semáforo. Mede a eficiência local do cruzamento. |
| | Tempo Médio de Viagem | O tempo médio total que um veículo leva para percorrer sua rota completa na rede. Mede a eficiência global da rede. |
| | Vazão da Rede | O número total de veículos que conseguem completar suas rotas em um determinado intervalo de tempo. Mede a capacidade do sistema. |
| | Comprimento Médio da Fila | O número médio de veículos aguardando em uma fila de semáforo. Indica o nível de congestionamento. |
| **Variáveis de Controle** | Topologia da Rede | A estrutura da malha viária (4 cruzamentos em 2x2), que será mantida idêntica para todos os testes. |
| | Características dos Veículos | Propriedades como velocidade máxima, aceleração e comprimento dos veículos, que serão padronizadas. |
| | Duração da Simulação | Todas as execuções terão a mesma duração de tempo simulado para garantir uma base de comparação justa. |
| **Variáveis de Confusão** | Aleatoriedade da Simulação | Pequenas variações na geração de veículos ou em suas decisões de rota, que podem introduzir ruído nos resultados. |
| | Qualidade do Treinamento do DRL | O desempenho do algoritmo DRL depende da qualidade do seu treinamento prévio. Um modelo mal treinado pode levar a conclusões inválidas. |

### 8.4 Fatores, Tratamentos e Combinações

O experimento possui um desenho fatorial 2x3, combinando os níveis de dois fatores principais para criar os tratamentos.

| Fator | Níveis | Descrição |
|---|---|---|
| **F1: Algoritmo de Controle** | Nível 1: Tempo Fixo | Grupo de controle. Utiliza um plano de semáforos com ciclos e fases pré-definidos e não adaptativos. |
| | Nível 2: DRL | Grupo de tratamento. Utiliza um agente de aprendizado por reforço para ajustar dinamicamente as fases do semáforo. |
| **F2: Cenário de Tráfego** | Nível 1: Baixo | Simula condições de tráfego de baixa demanda (e.g., madrugada), com poucos veículos na rede. |
| | Nível 2: Normal | Simula condições de tráfego moderado, representando o fluxo durante a maior parte do dia. |
| | Nível 3: Pico | Simula condições de tráfego intenso (e.g., horário de rush), com alto volume de veículos e potencial de congestionamento. |

A combinação desses fatores resulta nos seguintes 6 tratamentos (condições experimentais) que serão aplicados:

| Código do Tratamento | F1: Algoritmo de Controle | F2: Cenário de Tráfego |
|---|---|---|
| T1 | Tempo Fixo | Baixo |
| T2 | Tempo Fixo | Normal |
| T3 | Tempo Fixo | Pico |
| T4 | DRL | Baixo |
| T5 | DRL | Normal |
| T6 | DRL | Pico |

### 8.5 Variáveis Dependentes (Respostas)

As principais variáveis de resposta são diretamente associadas às métricas definidas no GQM:

- **Tempo Médio de Espera:** O tempo médio que um veículo permanece parado no semáforo.
- **Tempo Médio de Viagem:** O tempo médio total para um veículo percorrer a rede viária simulada.
- **Redução Percentual:** A percentagem de melhoria do algoritmo adaptativo em relação ao sistema de tempo fixo.

### 8.6 Variáveis de Controle / Bloqueio

Para garantir uma comparação justa entre os tratamentos, os seguintes fatores serão mantidos constantes em todas as execuções:

- **Topologia da Rede Viária:** A estrutura da rede com 4 cruzamentos (malha 2x2) será idêntica para todos os testes.
- **Características dos Veículos:** Velocidade máxima, aceleração, comprimento e comportamento dos motoristas serão os mesmos.
- **Padrões de Geração de Veículos:** Para cada cenário de tráfego, o volume e a distribuição temporal de veículos serão mantidos consistentes.
- **Duração da Simulação:** Todas as execuções terão a mesma duração de tempo simulado.
- **Rotas dos Veículos:** As rotas serão pré-definidas, com veículos entrando em um ponto da rede e saindo em outro, atravessando múltiplos cruzamentos.

### 8.7 Possíveis Variáveis de Confusão Conhecidas

São reconhecidas como potenciais variáveis de confusão:

- **Aleatoriedade da Simulação:** Pequenas variações na geração de veículos ou em suas decisões de rota podem introduzir ruído nos resultados.
- **Qualidade do Treinamento do DRL:** O desempenho do algoritmo adaptativo depende da qualidade do treinamento prévio. Um treinamento inadequado pode resultar em desempenho inferior.
- **Parâmetros de Configuração:** Diferentes valores de parâmetros (por exemplo, duração dos ciclos de semáforo) podem influenciar os resultados.

Essas variáveis serão monitoradas e, quando possível, documentadas para posterior discussão na análise de ameaças à validade.

---

## 9. Desenho Experimental

### 9.1 Tipo de Desenho

O desenho experimental adotado é um **estudo controlado com dois grupos paralelos**, um grupo controle (Tempo Fixo) e um grupo tratamento (DRL). O experimento utiliza um design **completamente randomizado**, onde cada execução da simulação é aleatoriamente designada para um dos dois grupos. Essa abordagem garante que a única diferença sistemática entre os grupos seja o algoritmo de controle utilizado, permitindo uma comparação direta e imparcial dos efeitos de cada tratamento sobre as variáveis dependentes.

### 9.2 Randomização e Alocação

A randomização será implementada no nível das execuções da simulação. Para cada cenário de tráfego a ser testado, serão realizadas múltiplas execuções. A alocação de cada execução a um dos dois tratamentos (Tempo Fixo ou DRL) será determinada por um processo de sorteio computacional. Além disso, cada execução utilizará uma semente aleatória diferente para a geração de veículos, capturando a variabilidade natural do tráfego.

### 9.3 Balanceamento e Contrabalanço

O **balanceamento** será garantido assegurando que cada um dos dois tratamentos seja executado o mesmo número de vezes para cada cenário. Por exemplo, se forem planejadas 60 execuções para um determinado cenário de tráfego, cada tratamento será aplicado em 30 dessas execuções. O **contrabalanço** não é aplicável neste desenho experimental, pois não há participantes humanos que possam sofrer efeitos de ordem ou aprendizagem entre as sessões. Cada execução da simulação é um evento independente.

### 9.4 Número de Grupos e Execuções

O experimento considera dois grupos de tratamento: Tempo Fixo e DRL. Serão testados três cenários de tráfego distintos. Para cada combinação de cenário e tratamento, serão realizadas 30 execuções (réplicas), totalizando 180 execuções de simulação (30 réplicas × 2 tratamentos × 3 cenários).

---

## 10. População, Sujeitos e Amostragem

A **população-alvo** deste experimento é composta por **fluxos de tráfego em redes urbanas de pequeno porte** (2-4 cruzamentos) em cidades brasileiras de médio porte. O objetivo é que os resultados possam ser generalizados para contextos urbanos com características similares de infraestrutura viária e padrões de congestionamento em malhas urbanas simples.

A **amostra** do experimento é composta por 180 execuções de simulação, distribuídas conforme descrito na seção anterior. Cada execução representa uma observação independente do desempenho de um algoritmo de controle sob um cenário específico de tráfego.

O método de seleção dos cenários de tráfego utiliza uma **amostragem estratificada**, onde os três estratos (baixo volume, volume normal, hora de pico) representam diferentes condições de operação de um cruzamento urbano típico. Essa abordagem garante que a amostra seja representativa das variações de tráfego que ocorrem ao longo de um dia.

---

## 11. Fluxograma do Experimento

O fluxograma a seguir apresenta uma visão geral de todos os passos operacionais do experimento, desde a preparação do ambiente até a análise final dos dados. O fluxograma detalha as decisões críticas, os loops de execução e os pontos de validação.

<img alt="diagrama_conceitual" src="https://github.com/emmanuelviglioni/medicao/blob/main/refs/fluxograma_experimento_v2.png" />

**Descrição das Fases:**

**Fase 1 – Preparação do Ambiente:** Instalação de ferramentas, configuração da rede viária, definição de cenários de tráfego, implementação dos algoritmos e realização de um teste piloto para validação.

**Fase 2 – Execução Principal:** Loop principal de simulações, onde cada combinação de cenário e algoritmo é executada 30 vezes. Durante cada execução, as métricas são coletadas automaticamente via TraCI e armazenadas em arquivos CSV.

**Fase 3 – Consolidação de Dados:** Validação da integridade dos dados, remoção de duplicatas e cálculo de estatísticas descritivas básicas.

**Fase 4 – Análise Estatística:** Verificação de normalidade dos dados e aplicação de testes de hipóteses apropriados (paramétricos ou não paramétricos). Cálculo de ganhos percentuais de desempenho.

**Fase 5 – Interpretação e Conclusão:** Interpretação dos resultados, geração de visualizações, documentação de ameaças à validade e escrita do relatório final.

---

## 12. Instrumentação e Protocolo Operacional

### 12.1 Instrumentos de Coleta

Os instrumentos de coleta de dados serão primariamente digitais e automatizados:

- **SUMO:** Ferramenta principal para a simulação do tráfego e geração dos dados brutos.
- **TraCI (Traffic Control Interface):** Interface que permite a comunicação entre os scripts Python e a simulação SUMO, utilizada para aplicar os diferentes tratamentos e coletar dados em tempo real.
- **Scripts Python:** Implementação dos algoritmos de controle (Tempo Fixo e DRL) e orquestração das execuções das simulações.
- **Arquivos CSV:** Armazenamento estruturado dos resultados de cada execução, contendo as métricas de interesse.

### 12.2 Materiais de Suporte

Os materiais de suporte incluem:

- **Documentação do Código:** Comentários detalhados nos scripts Python explicando a implementação dos algoritmos e do protocolo experimental.
- **Arquivo README:** Guia passo a passo para configurar o ambiente, instalar dependências e executar o experimento.
- **Arquivos de Configuração:** Definições do cenário viário, padrões de tráfego e parâmetros da simulação em formato estruturado (XML ou JSON).

### 12.3 Procedimento Experimental (Protocolo – Visão Passo a Passo)

O protocolo experimental será executado de forma automatizada por um script principal:

1. **Inicialização:** O script carrega a configuração do cenário de tráfego (baixo volume, volume normal ou hora de pico).
2. **Seleção do Tratamento:** O script seleciona aleatoriamente um dos dois tratamentos (Tempo Fixo ou DRL) para a próxima execução.
3. **Execução da Simulação:** O SUMO é iniciado com a configuração do cenário e o tratamento selecionado. A simulação roda por um período de tempo predefinido (por exemplo, 1 hora de tempo simulado).
4. **Coleta de Dados:** Durante a simulação, o script coleta as métricas de desempenho através da interface TraCI.
5. **Registro de Resultados:** Ao final da simulação, os dados agregados (tempo médio de espera, tempo médio de viagem, etc.) são salvos em um arquivo CSV.
6. **Repetição:** Os passos 2 a 5 são repetidos para cada tratamento, um número pré-definido de vezes (30 vezes), utilizando diferentes sementes aleatórias para cada execução.
7. **Finalização:** Após todas as execuções para um cenário serem concluídas, o script finaliza e os dados consolidados estão prontos para a análise.

---

## 13. Plano de Análise de Dados (Pré-Execução)

A análise dos dados será conduzida em três etapas principais:

### 13.1 Etapa 1: Preparação dos Dados

Inicialmente, será realizada a limpeza e normalização dos dados coletados. Os registros do arquivo CSV serão importados em um ambiente de análise (Python com bibliotecas Pandas e NumPy), onde serão verificadas inconsistências, valores faltantes e outliers. Outliers serão investigados para determinar se representam erros de coleta ou comportamentos legítimos da simulação.

### 13.2 Etapa 2: Análise Descritiva

Para cada tratamento e cenário de tráfego, serão calculadas estatísticas descritivas:

- Média e mediana do tempo de espera e tempo de viagem.
- Desvio padrão e intervalo interquartil.
- Valores mínimo e máximo.

Gráficos de box plot e histogramas serão gerados para visualizar a distribuição dos dados e comparar os grupos experimentalmente.

### 13.3 Etapa 3: Análise Inferencial

Para comparar as médias dos dois grupos (Tempo Fixo vs. DRL), será utilizado o **Teste t de Student independente**. Antes, o teste de **Shapiro-Wilk** será usado para verificar se os dados seguem uma distribuição normal. Se a normalidade não for atendida, o teste não paramétrico de **Mann-Whitney U** será usado como alternativa.

Para avaliar se a magnitude da melhoria varia entre os cenários, será utilizada uma **ANOVA de duas vias** (ou seu equivalente não paramétrico, Kruskal-Wallis) com fatores: Algoritmo (Tempo Fixo vs. DRL) e Cenário (Baixo Volume, Volume Normal, Hora de Pico).

Cada hipótese definida previamente em H0/H1 será avaliada considerando um nível de significância de 5% (α = 0,05).

---

## 14. Avaliação da Validade

Nesta seção, identificamos e abordamos as principais ameaças à validade do experimento, garantindo que as conclusões sobre o impacto do algoritmo adaptativo sejam robustas e bem fundamentadas.

### 14.1 Validade de Conclusão

A validade de conclusão se concentra em garantir que as inferências estatísticas entre o tratamento (DRL) e os resultados observados sejam corretas.

**Principais Ameaças:**

- **Tamanho Reduzido da Amostra:** O número de 30 réplicas por tratamento e cenário, embora razoável, pode ser limitado para detectar efeitos pequenos.
- **Ruído da Simulação:** Variações de desempenho da simulação podem introduzir ruído nas medições, reduzindo a precisão das estimativas.

**Estratégias de Mitigação:**

- Realização de análise de poder estatístico para validar o tamanho da amostra.
- Uso de múltiplas réplicas com diferentes sementes aleatórias para diluir o efeito do acaso.
- Aplicação de testes estatísticos robustos (não paramétricos) quando apropriado.

### 14.2 Validade Interna

A validade interna se refere à confiança de que as mudanças observadas nas variáveis dependentes foram causadas pela manipulação da variável independente (algoritmo de controle).

**Principais Ameaças:**

- **Aleatoriedade da Simulação:** Pequenas variações na geração de veículos podem confundir os resultados.
- **Qualidade do Treinamento do DRL:** Um algoritmo mal treinado pode não representar adequadamente o potencial da abordagem de DRL.

**Estratégias de Mitigação:**

- Randomização na alocação dos tratamentos e uso de múltiplas réplicas com diferentes sementes.
- Garantir que o algoritmo DRL seja adequadamente treinado antes do experimento, validando sua convergência.
- Manutenção de variáveis de controle constantes entre os grupos.

### 14.3 Validade de Constructo

A validade de constructo refere-se ao grau em que as medidas utilizadas no estudo representam os conceitos teóricos de interesse.

**Principais Ameaças:**

- **Representatividade das Métricas:** As métricas de tempo de espera e tempo de viagem podem não capturar completamente a "eficiência do tráfego".

**Estratégias de Mitigação:**

- Uso de múltiplas métricas (tempo de espera e tempo de viagem) para fornecer uma visão mais completa do desempenho.
- Justificação clara de por que essas métricas foram escolhidas como proxies para eficiência.

### 14.4 Validade Externa

A validade externa refere-se à capacidade de generalizar os resultados do estudo para outros contextos.

**Principais Ameaças:**

- **Rede Pequena:** O experimento utiliza uma rede pequena (4 cruzamentos), que pode não representar a complexidade de redes viárias urbanas maiores.
- **Dados Sintéticos:** O uso de dados de simulação pode não capturar todas as nuances do tráfego real.

**Estratégias de Mitigação:**

- Explicitação clara das limitações da validade externa nas conclusões.
- Sugestão de estudos futuros que repliquem o experimento em redes maiores e mais complexas, e, se possível, com dados reais.
- Escolha de parâmetros de simulação baseados em características realistas de cidades brasileiras.
- Documentação clara da topologia da rede utilizada para facilitar futuras replicações em contextos diferentes.

### 14.5 Resumo das Principais Ameaças e Estratégias de Mitigação

| Tipo de Validade | Ameaça Principal | Estratégia de Mitigação |
|---|---|---|
| Conclusão | Tamanho reduzido da amostra | Análise de poder; múltiplas réplicas; testes não paramétricos |
| Interna | Aleatoriedade da simulação | Randomização; múltiplas réplicas; variáveis de controle |
| Constructo | Representatividade das métricas | Múltiplas métricas; justificação clara |
| Externa | Cenário simplificado; dados sintéticos | Explicitação de limitações; sugestão de replicação futura |

---

## 15. Ética, Privacidade e Conformidade

Como o experimento será conduzido inteiramente em um ambiente de simulação, sem a participação de sujeitos humanos ou coleta de dados pessoais, as questões éticas tradicionalmente associadas à pesquisa com pessoas não se aplicam. A pesquisa não envolve a coleta de dados de indivíduos, eliminando preocupações com privacidade e consentimento informado.

Os dados gerados pelo experimento são puramente sintéticos, originados da simulação de tráfego, e não contêm informações que possam identificar indivíduos. Portanto, as regulamentações de proteção de dados, como a LGPD (Lei Geral de Proteção de Dados), não se aplicam diretamente ao conjunto de dados do experimento.

Não é necessária a submissão do projeto a um Comitê de Ética em Pesquisa (CEP), pois a pesquisa não envolve seres humanos.

---

## 16. Recursos e Infraestrutura

### 16.1 Recursos Humanos e Papéis

- **Pesquisador Principal (Estudante):** Responsável pelo planejamento, implementação, execução do experimento, análise dos dados e redação do relatório final.
- **Orientador / Professor:** Responsável pela supervisão científica, revisão do plano experimental e validação dos resultados.

### 16.2 Infraestrutura Técnica Necessária

- **Hardware:** Um computador pessoal (desktop ou notebook) com capacidade de processamento adequada para executar as simulações.
- **Software:**
  - Sistema Operacional: Linux (preferencialmente Ubuntu) ou Windows com WSL2.
  - Simulador de Tráfego: SUMO (código aberto).
  - Linguagem de Programação: Python 3.8+.
  - Bibliotecas Python: NumPy, Pandas, Matplotlib, SciPy (todas de código aberto).

### 16.3 Materiais e Insumos

Todos os materiais necessários são digitais e de código aberto. Não há necessidade de materiais físicos ou licenças de software pagas.

### 16.4 Orçamento e Custos Estimados

O projeto tem um custo direto estimado de **zero**, pois se baseia exclusivamente em ferramentas de software de código aberto e hardware de uso pessoal. Custos indiretos, como o consumo de energia elétrica durante a execução das simulações, são considerados marginais.

---

## 17. Cronograma e Marcos

| Semana | Atividade | Marco |
|--------|-----------|-------|
| 1 | Configuração do ambiente SUMO e implementação do algoritmo de Tempo Fixo | M1 |
| 2 | Implementação do algoritmo DRL e treinamento | M2 |
| 3 | Execução do experimento (coleta de dados) | M3 |
| 4 | Análise dos dados e redação do relatório final | M4 |

---

## 18. Governança do Experimento

### 18.1 Papéis e Responsabilidades Formais

- **Quem Executa (Responsible):** O Pesquisador Principal (Estudante) é responsável por todas as atividades de implementação, execução e análise.
- **Quem Revisa (Consulted):** O Orientador / Professor será consultado em etapas críticas, como a finalização do plano, a validação do algoritmo DRL e a análise dos resultados.
- **Quem Decide (Accountable):** O Orientador / Professor é o responsável final pelas decisões científicas do experimento.

### 18.2 Ritos de Acompanhamento

Serão realizadas **reuniões semanais** entre o Pesquisador Principal e o Orientador para discussão do progresso, solução de dúvidas e revisão de resultados parciais.

### 18.3 Processo de Controle de Mudanças

Qualquer mudança necessária no plano após sua aprovação inicial deverá ser formalmente proposta ao Orientador, incluindo justificativa e análise de impacto. A mudança só será implementada após aprovação explícita.

---

## 19. Plano de Documentação e Reprodutibilidade

### 19.1 Repositórios e Convenções de Nomeação

Todo o código-fonte, scripts, arquivos de configuração e dados serão armazenados em um repositório Git. Será adotada uma convenção clara de nomeação para arquivos e pastas:

- `/src`: código-fonte dos algoritmos.
- `/sumo`: arquivos de configuração da simulação.
- `/data`: dados brutos e processados.
- `/analysis`: scripts de análise estatística.

### 19.2 Plano de Empacotamento para Replicação Futura

Um "pacote de replicação" será criado contendo:

1. Código-fonte completo e comentado.
2. Todos os arquivos de configuração do SUMO.
3. Arquivo `requirements.txt` listando dependências com versões exatas.
4. Guia detalhado (README.md) explicando como configurar e executar o experimento.
5. Dados brutos gerados, permitindo replicação da análise.

---

## 20. Plano de Comunicação

### 20.1 Públicos e Mensagens-Chave

O principal público é o **Orientador / Professor**, que será comunicado sobre o progresso do trabalho através de reuniões semanais.

### 20.2 Canais e Frequência de Comunicação

- **Canal Principal:** Reuniões semanais (presenciais ou por vídeo).
- **Canal Secundário:** E-mail para comunicações assíncronas.
- **Frequência:** Semanal.

### 20.3 Pontos de Comunicação Obrigatórios

Comunicação formal será obrigatória:

- Após a conclusão do plano de experimento.
- Após a implementação dos algoritmos e validação.
- Após a conclusão da coleta de dados.
- Antes da entrega do relatório final.

---

## 21. Critérios de Prontidão para Execução

### 21.1 Checklist de Prontidão

A execução do experimento somente poderá começar quando todos os itens abaixo estiverem concluídos, revisados e aprovados:

**1. Documentação e Plano Experimental**

- Plano de Experimento finalizado, revisado e aprovado pelo Orientador.
- Modelo conceitual e desenho experimental concluídos e validados.
- Seções de validade, ética, governança, cronograma e orçamento finalizadas.
- Diagrama conceitual do experimento concluído e documentado.

**2. Ambiente Técnico e Infraestrutura**

- Repositório Git criado e acessível para armazenamento do código.
- SUMO instalado e configurado com a rede de 4 cruzamentos (malha 2x2).
- Interface TraCI testada e funcional para comunicação entre Python e SUMO.
- Algoritmo de Tempo Fixo implementado e validado.
- Algoritmo de DRL implementado, treinado e validado.
- Scripts Python para automação das execuções concluídos e testados.
- Sistema de armazenamento de dados (CSV) configurado e testado.
- Scripts de coleta, transformação e consolidação dos dados revisados e testados.

**3. Configuração da Simulação**

- Arquivo de configuração da rede viária (XML do SUMO) finalizado.
- Padrões de geração de veículos para os 3 cenários de tráfego definidos e testados.
- Rotas dos veículos (entrada e saída da rede) pré-definidas e validadas.
- Parâmetros de simulação (velocidade, aceleração, etc.) documentados.

**4. Teste Piloto**

- Execução de um piloto técnico contendo:
  - Simulação de teste com ambos os algoritmos.
  - Coleta automática de métricas no arquivo CSV.
  - Verificação de ponta a ponta do fluxo completo (código → simulação → coleta de dados).
- Validação de que as métricas são coletadas corretamente.
- Documentação de qualquer ajuste necessário com base nos resultados do piloto.

**5. Plano de Análise de Dados**

- Scripts de análise estatística (testes t, Mann-Whitney U, etc.) preparados e testados.
- Ambiente de análise (Python com Pandas, NumPy, SciPy) configurado.
- Procedimentos de limpeza, normalização e tratamento de outliers documentados.

**6. Comunicação e Governança**

- Comunicação prévia enviada ao Orientador com:
  - Objetivos do experimento.
  - Datas previstas para execução.
  - Responsabilidades.
  - Instruções operacionais.
- Confirmação de recebimento e entendimento das instruções pelo Orientador.
- Definição do responsável por acompanhar o experimento.
- Calendário com marcos, checkpoints e reuniões definido.
- Fluxo de controle de mudanças estabelecido.
- Critérios de bloqueio e retomada (go/no-go) documentados.

### 21.2 Aprovações Finais para Iniciar a Operação

Antes do início oficial da execução do experimento, é necessário registrar o aceite formal das seguintes partes:

**1. Pesquisador Responsável (Estudante)**

Confirma que:

- Todo o plano está completo e validado.
- Infraestrutura foi testada e está funcional.
- Riscos foram avaliados e mitigados.
- Ambiente técnico está pronto.
- Teste piloto foi bem-sucedido.

Registro do aceite: Assinatura digital ou formulário de confirmação.

**2. Orientador Acadêmico**

Confirma que:

- Plano de experimento está cientificamente sólido.
- Metodologia é apropriada para responder às questões de pesquisa.
- Riscos e ameaças à validade foram adequadamente considerados.
- Projeto está pronto para execução.

Registro do aceite: Assinatura digital ou e-mail de confirmação.

**3. Apoio Técnico (se aplicável)**

Confirma que:

- Ambiente técnico está funcional e estável.
- SUMO, TraCI e scripts Python foram verificados.
- Sistema de armazenamento de dados está operacional.
- Coleta automática de métricas foi testada.

Registro do aceite: Checklist técnico assinado digitalmente.

Após o registro de todas as aprovações, o experimento está oficialmente **"READY"**, autorizado para início da execução.

---

## Referências

[1] Abdulhai, B., Pringle, R., & Karakoulas, G. (2003). Reinforcement learning for true adaptive traffic signal control. *Journal of Transportation Engineering*, 129(3), 278-285.

[2] Genders, W., & Razavi, S. (2019). Deep reinforcement learning for traffic signal control: A survey. *IEEE Transactions on Intelligent Transportation Systems*, 20(10), 3691-3703.
