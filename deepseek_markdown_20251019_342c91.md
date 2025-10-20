# Preparação para Entrevista - Especialista de Software | Itaú Unibanco

## 📋 Competências Avaliadas
- Documentação
- Papos técnicos com o time
- Comunicação com grupos reduzidos, coordenação e squads
- Trabalho em equipe
- Habilidade de influenciar
- Habilidade de pesquisa
- Adaptabilidade e flexibilidade a nível de squad
- Tomada de decisões e pensamentos críticos
- Iniciativas
- Habilidade analítica e negócios
- Pensamento inovador

---

## 🎯 Cases Estruturados no Modelo STAR

### 1. Maior Case/Projeto da Carreira - Modernização

#### **S (Situação)**
No Sispag, sistema crítico de pagamentos do Itaú, enfrentávamos altas taxas de divergência de status nas transações de Pix e TED, o que gerava insegurança operacional e insatisfação do cliente. Além disso, tínhamos falta de visibilidade completa do fluxo transacional, dificultando a identificação e resolução de problemas.

#### **T (Tarefa)**
Minha tarefa, como desenvolvedor pleno atuando com mentalidade de especialista, era liderar a iniciativa de aumentar a confiabilidade do sistema. Os objetivos eram: reduzir drasticamente as divergências, implementar um sistema robusto de observabilidade para monitorar a máquina de estados das transações e criar alarmes proativos.

#### **A (Ação)**
- **Habilidade Analítica e de Pesquisa**: Iniciei um _deep dive_ nos logs e na base de dados para mapear todos os pontos de falha e entender o ciclo de vida completo de uma transação. Apresentei esses dados em papos técnicos com o time para alinharmos a visão do problema.

- **Iniciativa e Pensamento Inovador**: Propus e liderei a implementação de uma camada de observabilidade para monitorar a máquina de estados, latências e taxas de erro. Isso era algo novo para o squad na época.

- **Trabalho em Equipe e Comunicação**: Coordenei esforços com os squads, estabelecendo contratos claros e padrões de retentativa. Também atuei em conjunto com a área de dados na democratização das bases, garantindo que as informações fossem acessíveis e confiáveis para toda a organização.

- **Tomada de Decisão**: Defini, em conjunto com o time, os pontos críticos para a criação de alarmes comportamentais, priorizando os que impactavam diretamente a experiência do cliente final.

#### **R (Resultado)**
- Redução de **mais de 80% nas divergências de status** no primeiro trimestre
- Implementação da observabilidade proporcionou **visibilidade em tempo real**, permitindo identificar gargalos e evitar falhas em cascata
- Alarmes proativos permitiam **agir antes que os problemas impactassem os clientes** massivamente
- Trabalho se tornou **referência para outros squads** e foi fundamental na modernização da aplicação

---

### 2. Case de Influência para Descartar uma Solução - Rejeições AB03

#### **S (Situação)**
Em uma _war room_, foi proposta uma solução para implementar repiques automáticos para transações rejeitadas com o código AB03 (instituição destinatária fora do ar). A ideia era aumentar a taxa de sucesso dos pagamentos.

#### **T (Tarefa)**
Minha tarefa era analisar tecnicamente a proposta e seus impactos. Rapidamente percebi que, embora bem-intencionada, a solução poderia gerar um risco sistêmico para o banco.

#### **A (Ação)**
- **Habilidade Analítica e de Pesquisa**: Simulei cenários de crise: e se um ou dois grandes bancos ficassem fora do ar por horas? A volumetria de repiques seria massiva, sobrecarregando nossos sistemas e, potencialmente, afetando outras integrações.

- **Pensamento Crítico**: Argumentei que, ao assumir a responsabilidade pelo repique, o Itaú poderia se tornar o "garantidor" da transação em cenários prolongados, criando um passivo operacional e de imagem.

- **Habilidade de Influência e Comunicação**: Marquei uma reunião com o time de negócios e a coordenação. Em vez de apenas criticar, apresentei dados mostrando a projeção da rajada de repiques em um cenário de crise. Expliquei os riscos de forma clara, conectando o problema técnico ao impacto no negócio ("colateral nas demais integrações").

- **Adaptabilidade e Pensamento Inovador**: Não fui apenas contra. Apresentei uma contraproposta: um mecanismo de _Circuit Breaker_. Expliquei que, ao detectar uma alta taxa de rejeição AB03 para um determinado banco, poderíamos "abrir o circuito" para aquele destino, evitando repiques desnecessários e poupando recursos.

#### **R (Resultado)**
- A arquitetura inicial foi **descartada** após minha apresentação
- A proposta do _Circuit Breaker_ foi **aprovada e incorporada** ao planejamento
- Resultou em uma **arquitetura mais resiliente** e preparada para cenários de crise
- Consolidou minha **credibilidade como profissional** que antecipa riscos e protege o negócio

---

### 3. Contribuição para a Melhoria da Carreira dos Pares

#### **S (Situação)**
Percebi que o conhecimento sobre o domínio do produto e a arquitetura do Sispag estava concentrado em poucas pessoas do squad, o que criava gargalos e limitava o crescimento individual.

#### **T (Tarefa)**
Me propus a ajudar a criar um ambiente de aprendizado contínuo, onde todos pudessem evoluir tecnicamente e em seu entendimento do negócio.

#### **A (Ação)**
- **Comunicação e Feedback**: Adotei a prática de dar feedbacks informais imediatos após _pair programming_ ou revisões de código, sempre de forma construtiva. Durante almoços ou _coffee breaks_, puxava assuntos sobre arquitetura ou regras de negócio complexas.

- **Habilidade de Influência**: Conversava individualmente com meus pares para entender suas vontades de evolução técnica. Se alguém queria aprender mais sobre Kafka, por exemplo, eu garantia que essa pessoa fosse a principal responsável pela próxima tarefa relacionada ao tópico, com meu suporte.

- **Adaptabilidade e Trabalho em Equipe**: Ficava atento ao momento de cada pessoa. Se notava alguém com baixa produtividade ou desmotivado, em vez de julgar, procurava conversar, entender se era um problema pessoal ou de falta de desafio.

#### **R (Resultado)**
- Membros do time se sentiram **mais confiantes e apoiados**, assumindo tarefas mais complexas
- Criação de uma **cultura de compartilhamento de conhecimento** mais forte dentro do squad
- **Redução dos pontos únicos de falha** (SPOFs de conhecimento)
- Contribuiu diretamente para a **retenção de talentos** e clima de trabalho mais colaborativo

---

### 4. Pior Case/Projeto da Carreira - A Maratona do Pix Identificado

#### **S (Situação)**
Enfrentávamos uma data muro crítica, proveniente de uma demanda de segurança e compliance: era necessário rastrear e amarrar com 100% de confiabilidade as consultas de chaves no DICT às transações de Pix efetivadas. O objetivo era cruzar os dados para criar um "termômetro" de comportamento, identificando possíveis agentes atuando de má-fé através de varreduras massivas de chaves.

#### **T (Tarefa)**
A tarefa era dupla: 
1. Implementar a solução de amarração para atender a data muro urgente de segurança
2. Viabilizar a democratização desses dados para que as áreas de analytics e segurança pudessem consumi-los e gerar indicadores de fraude

#### **A (Ação)**
- **Arquitetura da Solução (trade-off)**: Para atender ao prazo apertado, a estratégia adotada foi criar desfunções no fluxo transacional principal. Paralelamente, atuei no desenvolvimento de um _building block_ com outros especialistas para capturar e estruturar dados para democratização.

- **O Dilema do Especialista**: Naquele momento, concentrei-me em fazer a solução funcionar. A entrega do _building block_ e a democratização dos dados para combate a fraude eram objetivos tão nobres que ofuscaram os malefícios da desfunção no _core_.

- **Foco no Valor de Negócio Imediato**: A decisão foi tomada com base no altíssimo valor de negócio da democratização dos dados para o combate a fraudes. Aceitamos o trade-off conscientemente, mas subestimamos o custo de manutenção a longo prazo.

#### **R (Resultado)**
- **Sucesso de Negócio**: Entregamos dentro do prazo. O _building block_ foi um sucesso e a democratização dos dados funcionou perfeitamente, permitindo detectar comportamentos suspeitos.

- **Dívida Técnica**: O preço pago foi a **desfunção no ambiente transacional**. O fluxo principal ficou mais complexo, frágil e difícil de manter.

- **Aprendizados**:
  1. **Não existem soluções apenas técnicas** - toda decisão é um trade-off
  2. **Papel do Especialista é iluminar trade-offs** - apresentar opções claras com seus custos e benefícios
  3. **Um "sucesso" pode ser um "pior case"** se a maturidade arquitetural foi comprometida

---

## 💡 Dicas para a Entrevista

### Prática Recomendada
- **Cronometre** cada resposta (2-3 minutos por case)
- **Pratique em voz alta** sozinho ou com um amigo
- **Use números** para quantificar resultados sempre que possível
- **Conecte** ações técnicas a impactos no negócio

### Durante a Entrevista
- Mantenha as respostas **focadas e estruturadas**
- Destaque **competências específicas** em cada case
- Mostre **autocrítica e aprendizado** nos casos desafiadores
- Demonstre **visão de negócio** além do técnico

---

*Documento preparado para entrevista de Especialista de Software no Itaú Unibanco*
*Última atualização: [INSERIR DATA]*
