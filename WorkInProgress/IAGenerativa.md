[Skip to content](https://www.ibm.com/br-pt/think/topics/generative-ai#main-content)



















[Think](https://www.ibm.com/br-pt/think)

- [Inteligência artificial](https://www.ibm.com/br-pt/think/artificial-intelligence)
- [Nuvem](https://www.ibm.com/br-pt/think/cloud)
- [Segurança](https://www.ibm.com/br-pt/think/security)
- [Notícias](https://www.ibm.com/br-pt/think/news)
- 
- 
- 
- 
- 

Inscreva-se

# O que é a IA generativa? 

Machine learning

- [Boas-vindas](https://www.ibm.com/br-pt/think/machine-learning#605511093)
- Introdução
- Ciência de dados para aprendizado de máquina
- Engenharia de funcionalidades
- Aprendizado supervisionado
- Aprendizado não supervisionado
- Aprendizado semissupervisionado
- Aprendizado por reforço
- Deep learning
- IA generativa
  - [Visão geral](https://www.ibm.com/br-pt/think/topics/generative-ai#257779831)
  - [Modelo generativo](https://www.ibm.com/br-pt/think/topics/generative-model#257779832)
  - [IA generativa versus IA preditiva](https://www.ibm.com/br-pt/think/topics/generative-ai-vs-predictive-ai-whats-the-difference#257779833)
  - Grandes modelos de linguagem (LLMs)
  - Geração de imagens por IA
  - IA multimodal
  - Geração aumentada de recuperação (RAG)
  - Geração de código de IA
  - Agentes de IA
- Treinamento de modelo
- Bibliotecas de aprendizado de máquina
- MLOps
- Processamento de linguagem natural
- Visão computacional

## O que é IA generativa?



A IA generativa, às vezes chamada de *IA gen,* é a [inteligência artificial](https://www.ibm.com/br-pt/think/topics/artificial-intelligence) (IA) que pode criar conteúdo original, como texto, imagens, vídeo, áudio ou código de software, em resposta a um prompt ou solicitação do usuário.

A IA generativa depende de modelos sofisticados de [aprendizado de máquina](https://www.ibm.com/br-pt/think/topics/machine-learning) chamados modelos de *[deep learning,](https://www.ibm.com/br-pt/think/topics/deep-learning)* que simulam os processos de aprendizado e tomada de decisão do cérebro humano. Esses modelos funcionam identificando e codificando os padrões e relacionamentos em grandes quantidades de dados e, em seguida, usando essas informações para entender as solicitações ou perguntas de linguagem natural dos usuários e responder com novo conteúdo relevante.

A IA tem sido um tema tecnológico importante na última década, mas a IA generativa, e especificamente a chegada do ChatGPT em 2022, colocaram a IA nas manchetes mundiais e lançaram uma onda sem precedentes de inovação e adoção da IA. A IA generativa oferece enormes benefícios de produtividade para pessoas físicas e jurídicas e, embora também apresente desafios e riscos muito reais, as empresas estão avançando, explorando como a tecnologia pode melhorar seus fluxos de trabalho internos e enriquecer seus produtos e serviços. De acordo com uma pesquisa da empresa de consultoria de gerenciamento McKinsey, um terço das organizações já utiliza a IA generativa regularmente em pelo menos uma função empresarial.¹ O analista do setor Gartner projeta que mais de 80% das organizações terão implantado aplicativos de IA generativa ou usado interfaces de programação de aplicativos (APIs) de IA generativa até 2026.2

A ascensão da IA generativa no mundo dos negócios (14:44 min)

## Como funciona a IA generativa



Na maioria das vezes, a IA generativa opera em três fases: 

- **Treinamento**, para criar um modelo de base que possa servir como base para várias aplicações de IA generativa.

  

- **Ajuste**, para adaptar o modelo de base a uma aplicação específica de IA generativa.

  

- **Geração**, **avaliação e reajuste***,* para avaliar a produção da aplicação de IA generativa e melhorar continuamente sua qualidade e precisão.

### Treinamento

A IA generativa começa com um modelo de base, um modelo de deep learning que serve de base para vários tipos diferentes de aplicações de IA generativa. Os modelos de base mais comuns atualmente são [grandes modelos de linguagem (LLMs)](https://www.ibm.com/br-pt/think/topics/large-language-models), criados para aplicações de geração de texto, mas também há modelos de base para geração de imagens, geração de vídeo, geração de som e música, bem como modelos de base multimodais, compatíveis com vários tipos de geração de conteúdo.

Para criar um modelo de base, os profissionais treinam um algoritmo de deep learning em grandes volumes de dados brutos, não estruturados e não rotulados — por exemplo, terabytes de dados retirados da internet ou de alguma outra fonte de dados enorme. Durante o treinamento, o algoritmo executa e avalia milhões de exercícios de "preencher o espaço em branco", tentando prever o próximo elemento em uma sequência (por exemplo, a próxima palavra em uma frase, o próximo elemento em uma imagem, o próximo comando em uma linha de código) e se ajustando continuamente para minimizar a diferença entre suas previsões e os dados reais (ou resultado "correto").

O resultado desse treinamento é uma [rede neural](https://www.ibm.com/br-pt/think/topics/neural-networks) de *parâmetros* (representações codificadas das entidades, padrões e relacionamentos nos dados) que podem gerar conteúdo de forma autônoma em resposta a entradas, ou prompts.

Esse processo de treinamento tem um uso intenso de computação, é demorado e caro: requer milhares de unidades de processamento gráfico em clusters (GPUs) e semanas de processamento, o que custa milhões de dólares. Projetos de modelo de base de código aberto, como o Llama-2 da Meta, permitem que os desenvolvedores de IA generativa evitem essa etapa e seus custos.

### Ajuste

Metaforicamente falando, um modelo de base é generalista: ele sabe muito sobre muitos tipos de conteúdo, mas muitas vezes não consegue gerar tipos específicos de produção com a precisão ou fidelidade desejada. Para isso, o modelo deve ser ajustado para uma tarefa específica de geração de conteúdo. Isso pode ser feito de várias maneiras.

#### Ajuste fino

O [ajuste fino](https://www.ibm.com/br-pt/think/topics/fine-tuning) envolve alimentar o modelo com dados específicos da aplicação de geração de conteúdo — perguntas ou prompts que a aplicação provavelmente receberá e as respostas corretas correspondentes no formato desejado. Por exemplo, se uma equipe de desenvolvimento estiver tentando criar um chatbot para atendimento ao cliente, ela criará centenas ou milhares de documentos contendo perguntas rotuladas de atendimento ao cliente e respostas corretas e, em seguida, alimentará o modelo com esses documentos.

O ajuste fino é trabalhoso. Os desenvolvedores geralmente terceirizam a tarefa para empresas com grandes forças de trabalho de rotulagem de dados.

#### Aprendizado por reforço com feedback humano (RLHF)

No [RLHF](https://www.ibm.com/br-pt/think/topics/rlhf), os usuários humanos respondem ao conteúdo gerado com avaliações que o modelo pode usar para atualizar o modelo para maior precisão ou relevância. Muitas vezes, o RLHF envolve pessoas "pontuando" diferentes saídas em resposta ao mesmo prompt. Mas pode ser tão simples quanto fazer com que as pessoas digitem ou conversem com um chatbot ou assistente virtual, corrigindo sua saída.

### Geração, avaliação, mais ajuste

Desenvolvedores e usuários avaliam continuamente as saídas de seus aplicativos de IA generativa e ajustam ainda mais o modelo (até uma vez por semana) para obter maior precisão ou relevância. (Ao contrário, o modelo de base em si é atualizado com muito menos frequência, talvez a cada 12 ou 18 meses).

Outra opção para melhorar o desempenho de um aplicativo de IA generativa é a *geração aumentada de recuperação* (RAG). A RAG é um framework para estender o modelo de base para usar fontes relevantes fora dos dados de treinamento, para complementar e refinar os parâmetros ou representações no modelo original. A RAG pode garantir que um aplicativo de IA generativa sempre tenha acesso às informações mais atuais. Como bônus, as fontes adicionais acessadas por meio da RAG são transparentes para os usuários de uma forma que o conhecimento no modelo de base original não é.

O que é geração aumentada de recuperação (RAG)? (6:32 min)

## Arquiteturas de modelos de IA generativa e como elas evoluíram



Modelos verdadeiramente de IA generativa (modelos de deep learning que podem criar conteúdo sob demanda de forma autônoma) evoluíram nos últimos 10 ou 12 anos. As arquiteturas de modelos de destaque durante esse período incluem

- **Autocodificadores variacionais (VAEs),** que geraram avanços no reconhecimento de imagens, processamento de linguagem natural e detecção de anomalias.
   
- **Redes adversárias generativas (GANs)** e **modelos de difusão**, que melhoraram a precisão de aplicações anteriores e permitiram algumas das primeiras soluções de IA para geração de imagens fotorrealistas.
   
- **Transformadores**, a arquitetura do modelo de deep learning por trás dos principais modelos de base e soluções de IA generativa da atualidade.

### Autocodificadores variacionais (VAEs)

Um [autocodificador](https://www.ibm.com/br-pt/think/topics/autoencoder) é um modelo de deep learning que compreende duas redes neurais conectadas: uma que codifica (ou comprime) uma enorme quantidade de dados de treinamento não estruturados e não rotulados em parâmetros, e outra que decodifica esses parâmetros para reconstruir o conteúdo. Tecnicamente, os autocodificadores podem gerar novo conteúdo, mas são mais úteis para compactar dados para armazenamento ou transferência e descompactá-los para uso do que para geração de conteúdo de alta qualidade.

Lançados em 2013, os autocodificadores variacionais (VAEs) podem codificar dados como um autocodificador, mas *decodificar várias novas variações do conteúdo*. Ao treinar um VAE para gerar variações em direção a um objetivo específico, ele pode "zerar" um conteúdo mais preciso e de maior fidelidade ao longo do tempo. As primeiras aplicações de VAE incluíam detecção de anomalias (por exemplo, análise de imagens médicas) e geração de linguagem natural.

### Redes adversárias generativas (GANs)

As GANs, lançadas em 2014, também são compostas por duas redes neurais: um gerador, que gera novo conteúdo, e um discriminador, que avalia a precisão e a qualidade dos dados gerados. Esses algoritmos adversários incentivam o modelo a gerar produções de qualidade cada vez mais alta.

As GANs são comumente usadas para geração de imagens e vídeo, mas podem gerar conteúdo realista e de alta qualidade em vários domínios. Elas se mostraram particularmente bem-sucedidas em tarefas como *transferência de estilo* (alterar o estilo de uma imagem de, digamos, uma foto para um esboço a lápis) e *aumento de dados* (criar novos dados sintéticos para aumentar o tamanho e a diversidade de um conjunto de dados de treinamento).

### Modelos de difusão

Lançados também em 2014, os modelos de difusão funcionam primeiro adicionando ruído aos dados de treinamento até que sejam aleatórios e irreconhecíveis e, em seguida, treinando o algoritmo para difundir iterativamente o ruído para revelar uma produção desejada.

Os modelos de difusão levam mais tempo para serem treinados do que os VAEs ou GANs, mas, em última análise, oferecem um controle mais refinado sobre a produção, particularmente para ferramentas de geração de imagem de alta qualidade. O DALL-E, ferramenta de geração de imagens da Open AI, é impulsionada por um modelo de difusão.

### Transformadores

Documentados pela primeira vez em um artigo de 2017 publicado por Ashish Vaswani e outros, os [transformadores](https://www.ibm.com/br-pt/think/topics/transformer-model) evoluem o paradigma codificador-decodificador para permitir um grande avanço na forma como os modelos de base são treinados e na qualidade e variedade do conteúdo que podem produzir. Esses modelos estão no centro da maioria das ferramentas de IA generativa atuais, incluindo o ChatGPT e GPT-4, Copilot, BERT, Bard e Midjourney, para citar algumas.

Os transformadores usam um conceito chamado *atenção*, determinando e se concentrando no que é mais importante sobre os dados em uma sequência, para

- processar sequências inteiras de dados (por exemplo, frases em vez de palavras individuais) simultaneamente;
   
- capturar o contexto dos dados dentro da sequência;
   
- codificar os dados de treinamento em *incorporações* (também chamadas de *hiperparâmetros*) que representam os dados e seu contexto.

Além de permitir um treinamento mais rápido, os transformadores se destacam no processamento de linguagem natural (PNL) e na Natural Language Understanding (NLU), e podem gerar sequências mais longas de dados (por exemplo, não apenas respostas a perguntas, mas poemas, artigos ou documentos) com maior precisão e qualidade superior a outros modelos de IA generativa profunda. Os modelos de transformadores também podem ser treinados ou ajustados para usar ferramentas (por exemplo, uma aplicação de planilha, HTML, um programa de desenho) para produzir conteúdo em um formato específico.

Modelos generativos explicados (8:30 min)

## O que a IA generativa pode criar



A IA generativa pode criar muitos tipos de conteúdo em vários domínios diferentes. 



Texto

Modelos generativos, especialmente aqueles baseados em transformadores, podem gerar textos coerentes e contextualmente relevantes — tudo, desde instruções e documentação até folhetos, e-mails, cópias de sites, blogs, artigos, relatórios, documentos e até mesmo redação criativa. Eles também podem realizar tarefas de redação repetitivas ou tediosas (por exemplo, redigir resumos de documentos ou meta descrições de páginas da web), liberando o tempo dos redatores para trabalhos mais criativos e de maior valor.



Imagens e vídeo

A geração de imagens, como DALL-E, Midjourney e Stable Diffusion, pode criar imagens realistas ou arte original e pode realizar transferência de estilo, tradução de imagem para imagem e outras tarefas de edição ou aprimoramento de imagem. As ferramentas emergentes de vídeo de IA generativa podem criar animações a partir de prompts de texto e aplicar efeitos especiais ao vídeo existente de forma mais rápida e econômica do que outros métodos.



Som, fala e música

Os modelos generativos podem sintetizar fala natural e conteúdo de áudio para chatbots IA habilitados para voz e assistentes digitais, narração de audiobook e outras aplicações. A mesma tecnologia pode gerar músicas originais que imitam a estrutura e o som de composições profissionais.



Código de software

A IA generativa pode gerar código original, autocompletar trechos de código, traduzir entre linguagens de programação e resumir a funcionalidade do código. Ela permite que os desenvolvedores criem protótipos, refatorem e depurem aplicações rapidamente, oferecendo uma interface de linguagem natural para tarefas de codificação.



Design e arte

Os modelos de IA generativa podem gerar obras de arte e design exclusivas ou ajudar no design gráfico. As aplicações incluem geração dinâmica de ambientes, personagens ou avatares e efeitos especiais para simulações virtuais e videogames.



Simulações e dados sintéticos

Os modelos de IA generativa podem ser treinados para gerar [dados sintéticos](https://www.ibm.com/br-pt/think/topics/synthetic-data) ou estruturas sintéticas baseadas em dados reais ou sintéticos. Por exemplo, a IA generativa é aplicada na descoberta de medicamentos para gerar estruturas moleculares com propriedades desejadas, auxiliando no design de novos compostos farmacêuticos.

## Benefícios da IA generativa



O benefício óbvio e abrangente da IA generativa é a **maior \**e\**ficiência**. Como pode gerar conteúdo e respostas sob demanda, a IA generativa tem o potencial de acelerar ou automatizar tarefas que exigem muito trabalho, reduzir custos e liberar o tempo dos funcionários para trabalhos de maior valor.

Mas a IA generativa oferece vários outros benefícios para indivíduos e organizações.

### Aumento da criatividade

As ferramentas de IA generativa podem inspirar a criatividade por meio de brainstorming automatizado, gerando várias novas versões de conteúdo. Essas variações também podem servir como pontos de partida ou referências que ajudam escritores, artistas, designers e outros criadores a superar bloqueios criativos.

### Tomada de decisões aprimorada (e mais rápida)

A IA generativa é excelente na análise de grandes conjuntos de dados, identificando padrões e extraindo insights significativos e, em seguida, gerando hipóteses e recomendações com base nesses insights para apoiar executivos, analistas, pesquisadores e outros profissionais na tomada de decisões mais inteligentes e baseadas em dados.

### Personalização dinâmica

Em aplicações como sistemas de recomendação e criação de conteúdo, a IA generativa pode analisar as preferências e o histórico do usuário e gerar conteúdo personalizado em tempo real, levando a uma experiência do usuário mais personalizada e envolvente.

### Disponibilidade constante

A IA generativa opera continuamente sem fadiga, fornecendo disponibilidade ininterrupta para tarefas como [chatbots](https://www.ibm.com/br-pt/think/topics/chatbots) para atendimento ao cliente e respostas automatizadas.

AI Academy

### A ascensão da IA generativa para negócios

Saiba mais sobre a ascensão histórica da IA generativa e o que isso significa para os negócios.



[Acessar o episódio ](https://www.ibm.com/br-pt/think/videos/ai-academy/generative-ai-for-business)

## Casos de uso para IA generativa



Veja a seguir apenas alguns casos de uso de IA generativa para empresas. À medida que a tecnologia se desenvolve e as organizações incorporam essas ferramentas a seus fluxos de trabalho, podemos esperar ver muitos outros. 



Experiência do cliente

As organizações de marketing podem economizar tempo e aumentar a produção de conteúdo usando ferramentas de IA generativa para redigir textos para blogs, páginas da web, materiais de apoio, e-mails e muito mais. Mas as soluções de IA generativa também podem produzir textos de marketing e visuais altamente personalizados em tempo real com base em quando, onde e para quem o anúncio é entregue. E impulsionará chatbots e [agentes virtuais](https://www.ibm.com/br-pt/think/topics/virtual-agent) de próxima geração, que podem dar respostas personalizadas e até mesmo iniciar ações em nome do cliente — um avanço significativo em comparação com a geração anterior de modelos de IA conversacional, treinados em dados mais limitados para tarefas muito específicas.



Desenvolvimento de software e modernização de aplicações

As ferramentas de geração de código podem automatizar e acelerar o processo de escrever novo código. A geração de código também tem o potencial de acelerar drasticamente a [modernização de aplicações](https://www.ibm.com/br-pt/think/topics/application-modernization) ao automatizar grande parte da codificação repetitiva necessária para modernizar aplicações legadas para ambientes de nuvem híbrida.



Mão de obra digital

A IA generativa pode elaborar ou revisar rapidamente contratos, faturas, contas e outras "papeladas" digitais ou físicas, para que os funcionários que a utilizam ou gerenciam possam se concentrar em tarefas de nível superior. Isso pode acelerar os [fluxos de trabalho](https://www.ibm.com/br-pt/think/topics/workflow) em praticamente todas as áreas da empresa, incluindo recursos humanos, jurídico, compras e finanças.



Ciência, engenharia e pesquisa

Os modelos de IA generativa podem ajudar cientistas e engenheiros a propor novas soluções para problemas complexos. Na área da saúde, por exemplo, modelos generativos podem ser aplicados para sintetizar imagens médicas para treinamento e testes de sistemas de imagens médicas.

## IA generativa, agentes de IA e IA agêntica



Um [agente de IA](https://www.ibm.com/br-pt/think/topics/ai-agents) é um programa de IA autônomo. Ele pode realizar tarefas e atingir metas em nome de um usuário ou de outro sistema sem intervenção humana, projetando seu próprio fluxo de trabalho e usando as ferramentas disponíveis (outras aplicações ou serviços). A [IA agêntica](https://www.ibm.com/br-pt/think/topics/agentic-ai) é um sistema de múltiplos agentes de IA, cujos esforços são coordenados, ou orquestrados, para realizar uma tarefa mais complexa ou um objetivo maior do que qualquer agente único no sistema poderia alcançar.

Ao contrário dos chatbots e outros modelos de IA, que operam dentro de restrições predefinidas e requerem intervenção humana, os agentes de IA e a IA agêntica exibem autonomia, comportamento orientado por objetivos e adaptabilidade a circunstâncias em mudança. Os termos "agente" e "agêntico" se referem à *agência* desses modelos ou à capacidade deles de agir de forma independente e proposital.

Uma maneira de pensar em agentes de IA é como um próximo passo natural após a IA generativa. Os modelos de IA generativa se concentram na criação de conteúdo com base em padrões aprendidos; os agentes usam esse conteúdo para interagir uns com os outros e com outras ferramentas para tomar decisões, resolver problemas e concluir tarefas. Por exemplo, um aplicativo de IA generativa pode ser capaz de informar o melhor momento para escalar o Monte Everest considerando seu horário de trabalho, mas um agente pode lhe dizer isso e, em seguida, usar um serviço de viagens online para reservar o melhor voo e um quarto no hotel mais conveniente no Nepal.

[Explore nosso guia de 2025 para agentes de IA ](https://www.ibm.com/br-pt/think/ai-agents)

## Desafios, limitações e riscos



A IA generativa obteve avanços notáveis em um período relativamente curto, mas ainda apresenta desafios e riscos significativos para desenvolvedores, usuários e o público em geral. Veja abaixo alguns dos problemas mais sérios e como eles estão sendo tratados. 

### "Alucinações" e outras produções imprecisas

Uma [alucinação de IA](https://www.ibm.com/br-pt/think/topics/ai-hallucinations) é uma saída de IA generativa absurda ou completamente imprecisa — mas, muitas vezes, parece totalmente plausível. O exemplo clássico é quando um advogado usou uma ferramenta de IA generativa para pesquisa em preparação para um caso de alta visibilidade, e [a ferramenta "produziu" vários casos de exemplo, completos com citações e atribuições, que eram inteiramente ficcionais](https://www.legaldive.com/news/chatgpt-fake-legal-cases-generative-ai-hallucinations/651557/).

Alguns profissionais veem as alucinações como uma consequência inevitável do equilíbrio entre a precisão de um modelo e seus recursos criativos. Mas os desenvolvedores podem implementar medidas preventivas, chamadas de *proteções*, que restringem o modelo a fontes de dados relevantes ou confiáveis. A avaliação e o ajuste contínuos também podem ajudar a reduzir alucinações e imprecisões.

### Produções inconsistentes

Devido à natureza variacional ou probabilística dos modelos de IA generativa, as mesmas entradas podem resultar em saídas ligeiramente ou significativamente diferentes. Isso pode ser indesejável em determinadas aplicações, como chatbots para atendimento ao cliente, onde saídas consistentes são esperadas ou desejadas. Por meio da [engenharia de prompts](https://www.ibm.com/br-pt/think/topics/prompt-engineering) (refinando ou compondo prompts iterativamente), os usuários podem chegar a prompts que fornecem consistentemente os resultados desejados de suas aplicações de IA generativa.

### Viés

Os modelos generativos podem aprender vieses sociais presentes nos dados de treinamento (ou nos dados rotulados, fontes de dados externas ou avaliadores humanos usados para ajustar o modelo) e gerar conteúdo com viés, injusto ou ofensivo como resultado. Para evitar saídas com viés de seus modelos, os desenvolvedores devem garantir dados de treinamento diversos, estabelecer diretrizes para evitar vieses durante o treinamento e o ajuste e avaliar continuamente as saídas do modelo quanto a vieses e precisão.

### Falta de explicabilidade e métricas

Muitos modelos de IA generativa são modelos de “[black box AI](https://www.ibm.com/br-pt/think/topics/black-box-ai)“, o que significa que pode ser desafiador ou impossível entender seus processos de tomada de decisões; até mesmo os engenheiros ou cientistas de dados que criam o algoritmo subjacente podem entender ou explicar o que exatamente está acontecendo dentro dele e como chega a um resultado específico. Práticas e técnicas de [IA explicável](https://www.ibm.com/br-pt/think/topics/explainable-ai) podem ajudar profissionais e usuários a entender e confiar nos processos e produções dos modelos generativos.

Avaliar e comparar a qualidade do conteúdo gerado também pode ser um desafio. As métricas de avaliação tradicionais podem não captar os aspectos sutis de criatividade, coerência ou relevância. O desenvolvimento de métodos de avaliação robustos e confiáveis para a IA generativa continua sendo uma área ativa de pesquisa.

### Ameaças à segurança, privacidade e propriedade intelectual

Modelos de IA generativa podem ser explorados para gerar e-mails de [phishing](https://www.ibm.com/br-pt/think/topics/phishing) convincentes, identidades falsas ou outros conteúdos maliciosos que podem induzir os usuários a tomarem medidas que comprometam a segurança e a privacidade dos dados. Desenvolvedores e usuários precisam ter cuidado para que os dados inseridos no modelo (durante o ajuste ou como parte de um prompt) não exponham sua própria propriedade intelectual (IP) ou qualquer informação protegida como IP por outras organizações. E precisam monitorar as produções de novos conteúdos que exponham sua própria propriedade intelectual ou que violem as proteções de propriedade intelectual de terceiros.

### Deepfakes

Deepfakes são imagens, vídeo ou áudio gerados ou manipulados por IA para convencer as pessoas de que estão vendo, assistindo ou ouvindo alguém fazer ou dizer algo que nunca fizeram ou disseram. Eles estão entre os exemplos mais assustadores de como o poder da IA generativa pode ser aplicado com intenção maliciosa.

A maioria das pessoas está familiarizada com deepfakes criados para prejudicar reputações ou espalhar informações erradas. Mais recentemente, os cibercriminosos implementaram deepfakes como parte de ataques cibernéticos (por exemplo, vozes falsas em golpes de phishing de voz) ou esquemas de fraude financeira.

Os pesquisadores estão trabalhando arduamente em modelos de IA que possam detectar deepfakes com maior precisão. Enquanto isso, a educação dos usuários e as melhores práticas (por exemplo, não compartilhar material controverso não verificado ou não examinado) podem ajudar a limitar os danos que os deepfakes podem causar.

## Um breve histórico da IA generativa



O termo "IA generativa" explodiu na consciência pública na década de 2020, mas a IA generativa faz parte de nossas vidas há décadas, e a tecnologia de IA generativa de hoje se baseia em avanços de aprendizado de máquina desde o início do século 20. Um histórico representativo não exaustivo da IA generativa pode incluir algumas das seguintes datas

- **1964:** o cientista da computação do MIT Joseph Weizenbaum desenvolve o ELIZA, uma aplicação de processamento de linguagem natural baseado em texto. Essencialmente o primeiro chatbot (chamado de "chatterbot" na época), o ELIZA usou scripts de correspondência de padrões para responder a inputs de linguagem natural digitadas com respostas de texto empáticas.
   
- **1999:** a Nvidia lança a GeoForce, a primeira unidade de processamento gráfico. Originalmente desenvolvidas para fornecer gráficos de movimento suave para videogames, as GPUs se tornaram a plataforma de fato para o desenvolvimento de modelos de IA e mineração de criptomoedas.
   
- **2004:** o preenchimento automático do Google aparece pela primeira vez, gerando possíveis próximas palavras ou frases à medida que os usuários inserem seus termos de pesquisa. O exemplo relativamente moderno da IA generativa é baseado na Cadeia de Markov, um modelo matemático desenvolvido em 1906.
   
- **2013:** aparecem os primeiros autocodificadores variacionais (VAEs).
   
- **2014:** surgem as primeiras redes adversárias generativas (GANs) e modelos de difusão.
   
- **2017**: Ashish Vaswani, uma equipe do Google Brain, e um grupo da University of Toronto publicam "Attention is All You Need", um artigo que documenta os princípios dos modelos de transformadores, amplamente reconhecido por permitir os modelos de base mais poderosos e as ferramentas de IA generativa que estão sendo desenvolvidos atualmente.
   
- **2019-2020**: a OpenAI lança seus grandes modelos de linguagem GPT (Generative Pretraining Transformer), GPT-2 e GPT-3.
   
- **2022:** a OpenAI apresenta o ChatGPT, um front-end para o GPT-3 que gera frases complexas, coerentes e contextuais e conteúdo longo em resposta aos prompts do usuário final.

Com a notoriedade e popularidade do ChatGTP abrindo efetivamente as comportas, desenvolvimentos de IA generativa e lançamentos de produtos vieram em um ritmo furioso, incluindo lançamentos do Google Bard (agora Gemini), Microsoft Copilot, IBM [watsonx.ai](https://www.ibm.com/br-pt/think/topics/transformer-model) e o grande modelo de linguagem de código aberto Llama-2 da Meta.











Ebook

Tenha acesso ao poder da IA generativa + ML



Saiba como incorporar com confiança a IA generativa e o aprendizado de máquina em sua empresa.



[Leia o e-book](https://www.ibm.com/account/reg/signup?formid=urx-52356)

## Recursos

Carousel





Guia

Guia do CEO sobre IA generativa



Aprenda como os CEOs podem equilibrar o valor que a IA generativa pode criar com o investimento que ela exige e os riscos que ela introduz.



[Leia o guia](https://www.ibm.com/thought-leadership/institute-business-value/report/ceo-generative-ai)





Treinamento

Leve suas habilidades de IA generativa para o próximo nível



Aprenda conceitos fundamentais e desenvolva suas habilidades com laboratórios práticos, cursos, projetos guiados, avaliações e muito mais.



[Aprenda IA generativa](https://developer.ibm.com/get-started/generative-ai/?cm_sp=ibmdev-_-developer-_-getstarted-_-genai)





Ebook

Tenha acesso ao poder da IA generativa + ML



Saiba como incorporar com confiança a IA generativa e o aprendizado de máquina em sua empresa.



[Leia o e-book](https://www.ibm.com/account/reg/signup?formid=urx-52356)





Guia

Coloque a IA para trabalhar: como gerar ROI com a IA generativa



Quer ter mais retorno sobre seus investimentos em IA? Saiba como o dimensionamento da IA generativa em áreas importantes promove mudanças, ajudando suas melhores mentes a criar e oferecer soluções novas e inovadoras.



[Leia o guia](https://www.ibm.com/account/reg/signup?formid=urx-53137)

























1 / 2

Slide 1 of 2. Showing 4 items.



Soluções relacionadas



IBM watsonx.ai

Treine, valide, ajuste e implemente recursos de IA generativa, modelos de base e recursos de aprendizado de máquina com o IBM watsonx.ai, um estúdio empresarial de última geração para construtores de IA. Crie aplicações de IA em uma fração do tempo com uma fração dos dados.

[Conheça o watsonx.ai ](https://www.ibm.com/br-pt/products/watsonx-ai)



Soluções de inteligência artificial

Use a IA a serviço de sua empresa com a experiência e o portfólio de soluções líder do setor da IBM à sua disposição.

[Explore as soluções de IA ](https://www.ibm.com/br-pt/artificial-intelligence)



Serviços de IA

Reinvente os fluxos de trabalho e operações críticos adicionando IA para maximizar experiências, tomadas de decisão em tempo real e valor de negócios.

[Explore os serviços de IA ](https://www.ibm.com/br-pt/consulting/artificial-intelligence)



Dê o próximo passo

Obtenha acesso completo aos recursos que abrangem o ciclo de vida do desenvolvimento da IA. Produza soluções poderosas de IA com interfaces fáceis de usar, fluxos de trabalhos e acesso a APIs e SDKs padrão do setor.

[Explore o watsonx.ai](https://www.ibm.com/br-pt/products/watsonx-ai)[Agende uma demonstração em tempo real](https://www.ibm.com/br-pt/forms/mkt-demo-dataaiwatsonxai)





- ## Conheça


   

  ## Seguir


   

  ## Conectar


   

  ## Sobre

- 

- 

[Fale com a IBM](https://www.ibm.com/br-pt/contact)[Privacidade](https://www.ibm.com/br-pt/privacy)[Termos de uso](https://www.ibm.com/br-pt/legal/terms?lnk=flg-tous-usen)[Acessibilidade](https://www.ibm.com/able/?lnk=flg-acce-usen)Preferências de Cookies























A janela de bate-papo foi encerrada