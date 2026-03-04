[Skip to content](https://blog.nvidia.com.br/blog/tres-passos-chaves-atendimento-ao-cliente-nvidia-ai-blueprint/#content)



- Pesquisar por:

  

- [Home](https://blog.nvidia.com.br/)
- [IA](https://blog.nvidia.com.br/blog/category/deep-learning/)
- [Data Center](https://blog.nvidia.com.br/blog/category/data-center/)
- [Gaming](https://blog.nvidia.com.br/blog/category/gaming/)
- [Gráficos Profissionais](https://blog.nvidia.com.br/blog/category/graficos-profissionais/)
- [Robótica](https://blog.nvidia.com.br/blog/category/robotica/)
- [Startups](https://blog.nvidia.com.br/blog/category/startups/)
- [Podcast](https://blog.nvidia.com.br/vem-ai-podcast/)
- [Casos de Uso](https://blog.nvidia.com.br/blog/tag/cases-de-clientes/)
- [Sala de Imprensa](https://blog.nvidia.com.br/blog/category/sala-de-imprensa/)

# Três Passos Chaves para Criar Assistentes Virtuais de IA para Atendimento ao Cliente com um NVIDIA AI Blueprint

1 de abril de 2025 por [Isabel Hulseman](https://blog.nvidia.com.br/blog/author/ihulseman/)

![img](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/04/ai-virtual-assistant-graphic-1280x720.jpg)

 Compartilhe

- 
- 
- 
- 

 

No ambiente de negócios acelerado de hoje, fornecer um atendimento excepcional ao cliente não é mais apenas uma coisa boa de se ter, é uma necessidade. Seja abordando problemas técnicos, resolvendo questões de cobrança ou fornecendo atualizações de serviço, os clientes esperam respostas rápidas, precisas e personalizadas conforme sua conveniência. No entanto, atingir esse nível de serviço traz desafios significativos.

Abordagens legadas, como scripts estáticos ou processos manuais, geralmente ficam aquém quando se trata de fornecer suporte personalizado e em tempo real. Além disso, muitas operações de atendimento ao cliente dependem de dados confidenciais e fragmentados, que estão sujeitos a rígidos regulamentos de governança e privacidade de dados. Com o surgimento da IA generativa, as empresas pretendem revolucionar o atendimento ao cliente, aumentando a eficiência operacional, cortando custos e maximizando o ROI.

A integração da IA aos sistemas existentes apresenta desafios relacionados à transparência, precisão e segurança, o que pode impedir a adoção e interromper os workflows. Para superar esses obstáculos, as empresas estão aproveitando assistentes virtuais com IA generativa para gerenciar uma ampla gama de tarefas, melhorando os tempos de resposta e liberando recursos.

Esta postagem descreve como os desenvolvedores podem usar o [NVIDIA AI Blueprint para assistentes virtuais de IA](https://build.nvidia.com/nvidia/ai-virtual-assistant-for-customer-service) para dimensionar operações com IA generativa. Ao aproveitar essas informações, incluindo código de amostra, as empresas podem atender às crescentes demandas por atendimento excepcional ao cliente, garantindo a integridade e a governança dos dados. Seja melhorando os sistemas existentes ou criando novos, esse blueprint capacita as equipes a atender às necessidades dos clientes com interações eficientes e significativas.

## **Assistentes Virtuais de IA Mais Inteligentes com um Mecanismo de Consulta de IA Usando Geração Aumentada por Recuperação**

Ao criar um assistente virtual de IA, é importante alinhar-se com os requisitos exclusivos do caso de uso, o conhecimento institucional e as necessidades da empresa. Os bots tradicionais, no entanto, geralmente dependem de frameworks rígidos e métodos desatualizados que lutam para atender às crescentes demandas do cenário atual de atendimento ao cliente.

Em todos os setores, os assistentes baseados em IA podem ser transformadores. Por exemplo, as empresas de telecomunicações e a maioria dos provedores de varejo e serviços podem usar assistentes virtuais de IA para aprimorar a experiência do cliente, oferecendo suporte 24 horas por dia, 7 dias por semana, enquanto lidam com uma ampla variedade de consultas de clientes em vários idiomas e fornecem interações dinâmicas e personalizadas que simplificam a solução de problemas e o gerenciamento de contas. Isso ajuda a reduzir os tempos de espera e garante um serviço consistente em diversas necessidades do cliente.

Outro exemplo é o setor de pagamentos de seguros na área de saúde, onde garantir uma experiência positiva para os membros é fundamental. Os assistentes virtuais aprimoram essa experiência fornecendo suporte personalizado aos membros, abordando suas reivindicações, consultas de cobertura, benefícios e problemas de pagamento, garantindo a conformidade com os regulamentos de saúde. Isso também ajuda a reduzir a carga administrativa sobre os profissionais da área de saúde.

Com a plataforma de IA da NVIDIA, as empresas podem criar um mecanismo de consulta de IA que usa [geração aumentada por recuperação (RAG)](https://www.nvidia.com/en-us/glossary/retrieval-augmented-generation) para conectar aplicações de IA a dados corporativos. O blueprint do assistente virtual de IA permite que os desenvolvedores comecem rapidamente a criar soluções que forneçam experiências aprimoradas ao cliente. Ele é criado usando os seguintes microsserviços [NVIDIA NIM](https://www.nvidia.com/pt-br/ai/):

- NVIDIA NIM para LLM:

   

  Traz o poder dos grandes modelos de linguagem (LLMs) de última geração para aplicações, fornecendo processamento de linguagem natural incomparável com eficiência notável.

  - [Llama 3.1 70B Instruct NIM](https://build.nvidia.com/meta/llama-3_1-70b-instruct): Potencializa conversas complexas com compreensão contextual superior, raciocínio e geração de texto.

- NVIDIA NeMo

   Retriever NIM:

   

  Esta coleção fornece acesso fácil a modelos de última geração que servem como bases fundamentais para pipelines RAG. Esses pipelines, quando integrados a soluções de assistente virtual, permitem acesso contínuo aos dados corporativos, desbloqueando o conhecimento institucional por meio de respostas rápidas, precisas e escaláveis.

  - **NeMo** [Retriever Embedding NIM](https://build.nvidia.com/nvidia/embed-qa-4): Aumenta o desempenho de recuperação de respostas a perguntas de texto, fornecendo incorporações de alta qualidade para o assistente virtual downstream.
  - **NeMo** [Retriever Reranking NIM](https://build.nvidia.com/nvidia/rerank-qa-mistral-4b): Melhora ainda mais o desempenho de recuperação com um reclassificador ajustado, encontrando as passagens mais relevantes para fornecer como contexto ao consultar um LLM.

O projeto foi projetado para se integrar perfeitamente às aplicações de atendimento ao cliente existentes sem quebrar os mandatos de segurança da informação. Graças à portabilidade do NVIDIA NIM, as empresas podem integrar dados onde quer que eles residam. Ao trazer IA generativa para os dados, essa arquitetura permite que os assistentes virtuais de IA forneçam experiências mais personalizadas e personalizadas para cada cliente, aproveitando seus perfis exclusivos, históricos de interação do usuário e outros dados relevantes.

Um blueprint é um ponto de partida que pode ser personalizado para o caso de uso exclusivo de uma empresa. Por exemplo, integre outros microsserviços do NIM, como o [Nemotron 4 Hindi 4B Instruct](https://build.nvidia.com/nvidia/nemotron-4-mini-hindi-4b-instruct), para permitir que um assistente virtual de IA se comunique no idioma local. Outros microsserviços podem habilitar recursos adicionais, como geração de dados sintéticos e ajuste fino de modelos, para se alinhar melhor aos requisitos específicos do caso de uso. Dê ao assistente virtual de IA uma interface semelhante à humana quando conectado ao Blueprint de IA de humano digital.

Com a implementação de um back-end RAG com dados proprietários (perfil da empresa e do usuário e seus dados específicos), o assistente virtual de IA pode se envolver em conversas altamente contextuais, abordando as especificidades das necessidades de cada cliente em tempo real. Além disso, a solução opera com segurança dentro de seus frameworks de governança existentes, garantindo a conformidade com os protocolos de privacidade e segurança, especialmente ao trabalhar com dados confidenciais.

## **Três Bases para Criar Seu Próprio Assistente Virtual de IA**

Como desenvolvedor, você pode criar seu próprio assistente virtual de IA que recupera as informações mais relevantes e atualizadas, em tempo real, com respostas humanas cada vez melhores. A Figura 1 mostra o diagrama de arquitetura do assistente virtual de IA que inclui três componentes funcionais.

![Architecture diagram showing the AI virtual assistant workflow for customer service, with ingest (top), virtual assistant (middle), customer service operations (bottom).](https://developer-blogs.nvidia.com/wp-content/uploads/2024/10/llm-diagram-update-ai-virtual-assistant-dark-35485471.png)*Figura 1. O plano de IA da NVIDIA para assistentes virtuais de IA*

## **1. Pipeline de Ingestão e Recuperação de Dados**

Os administradores de pipeline usam o pipeline de ingestão para carregar dados estruturados e não estruturados nos bancos de dados. Exemplos de dados estruturados incluem perfis de clientes, histórico de pedidos e status do pedido. Os dados não estruturados incluem manuais de produtos, catálogo de produtos e material de apoio, como documentos de perguntas frequentes.

## **2. Agente de IA**

O assistente virtual de IA é o segundo componente funcional. Os usuários interagem com o assistente virtual por meio de uma interface de usuário. Um agente de IA, implementado na estrutura de programação LLM agêntica do LangGraph, planeja como lidar com consultas complexas de clientes e resolve recursivamente. O agente LangGraph usa o recurso de chamada de ferramenta do [Llama 3.1 70B Instruct NIM](https://build.nvidia.com/meta/llama-3_1-70b-instruct) para recuperar informações das fontes de dados não estruturadas e estruturadas e, em seguida, gera uma resposta precisa.

O agente de IA também usa funções de memória de curto e longo prazo para habilitar o histórico de conversas em vários turnos. As consultas e respostas de conversa ativas são inseridas para que possam ser recuperadas posteriormente na conversa como contexto adicional. Isso permite interações mais humanas e elimina a necessidade de os clientes repetirem as informações que já compartilharam com o agente.

Por fim, no final da conversa, o agente de IA resume a discussão junto com uma determinação de sentimento e armazena o histórico da conversa no banco de dados estruturado. As interações subsequentes do mesmo usuário podem ser recuperadas como contexto adicional em conversas futuras. O resumo de chamadas e a recuperação do histórico de conversas podem reduzir o tempo de chamada e melhorar a experiência do cliente. A determinação de sentimentos pode fornecer informações valiosas ao administrador de atendimento ao cliente sobre a eficácia do agente.

## **3. Pipeline de Operações**

O pipeline de operações do cliente é o terceiro componente funcional da solução geral. Esse pipeline fornece informações e insights importantes para os operadores de atendimento ao cliente. Os administradores podem usar o pipeline de operações para revisar o histórico de chat, comentários do usuário, dados de análise de sentimento e resumos de chamadas. O microsserviço de análise, que aproveita o NIM Llama 3.1 70B Instruct, pode ser usado para gerar análises, como tempo médio de chamada, tempo de resolução e satisfação do cliente. As análises também são aproveitadas como feedback do usuário para treinar novamente os modelos LLM para melhorar a precisão.

Você pode encontrar o exemplo completo de como começar a usar este Blueprint no [repositório GitHub do NVIDIA AI Blueprint.](https://github.com/NVIDIA-AI-Blueprints/ai-virtual-assistant)

## **Chegue à Produção com Parceiros NVIDIA**

Os parceiros de consultoria da NVIDIA estão ajudando as empresas a adotar assistentes virtuais de IA de classe mundial criados usando a computação acelerada da NVIDIA e o [software NVIDIA AI Enterprise](https://www.nvidia.com/pt-br/data-center/products/ai-enterprise/), que inclui NeMo, microsserviços NIM e Blueprints de IA.

**Accenture**

[A Accenture AI Refinery](https://newsroom.accenture.com/news/2024/accenture-and-nvidia-lead-enterprises-into-era-of-ai), criada com base na [NVIDIA AI Foundry](https://newsroom.accenture.com/news/2024/accenture-pioneers-custom-llama-llm-models-with-nvidia-ai-foundry), ajuda a projetar interações autônomas e orientadas por intenção com o cliente, permitindo que as empresas adaptem a jornada ao indivíduo por meio de canais inovadores, como humanos digitais ou agentes de interação. Casos de uso específicos podem ser adaptados para atender às necessidades de cada setor, por exemplo, call centers de telecomunicações, consultores de apólices de seguro, agentes farmacêuticos interativos ou agentes de rede de revendedores automotivos.

**Deloitte**

O Deloitte Frontline AI aprimora a experiência de atendimento ao cliente com avatares digitais e agentes LLM criados com NVIDIA AI Blueprints que são acelerados por tecnologias NVIDIA, como NVIDIA ACE, NVIDIA Omniverse, NVIDIA Riva e NIM.

**Wipro**

O Wipro Enterprise Generative AI (WeGA) Studio acelera casos de uso específicos do setor, incluindo agentes de contact center na área de saúde, serviços financeiros, varejo e muito mais.

**Mahindra Tech**

A Tech Mahindra está aproveitando o NVIDIA AI Blueprint para humanos digitais para criar soluções para atendimento ao cliente. Usando RAG e NVIDIA NeMo, a solução oferece a capacidade de um estagiário parar um agente durante uma conversa, levantando a mão para fazer perguntas esclarecedoras. O sistema foi projetado para se conectar a microsserviços no back-end com um sistema de gerenciamento de aprendizado refinado, que pode ser implantado em muitos casos de uso do setor.

**Infosys**

O [Infosys Cortex](https://www.infosys.com/products-and-platforms/cortex.html), parte do [Infosys Topaz](https://www.infosys.com/services/data-ai-topaz.html), é uma plataforma de engajamento do cliente orientada por IA que integra o NVIDIA AI Blueprints e as tecnologias NVIDIA NeMo, Riva e ACE para IA generativa, IA de fala e recursos humanos digitais para fornecer assistência especializada e individualizada, proativa e sob demanda a todos os membros de uma empresa de atendimento ao cliente, consequentemente desempenhando um papel fundamental no aprimoramento da experiência do cliente, melhorando a eficiência operacional e reduzindo custos.

**Tata Consultancy Services**

O agente virtual Tata Consultancy Services (TCS), desenvolvido pela NVIDIA NIM e integrado ao IT Virtual Agent da ServiceNow, foi projetado para otimizar o suporte de IT e RH. Essa solução usa ajuste de prompt e RAG para melhorar os tempos de resposta, a precisão e fornecer recursos de conversação em vários turnos. Os benefícios incluem custos reduzidos de service desk, menos tíquetes de suporte, utilização aprimorada do conhecimento, implantação mais rápida e uma melhor experiência geral do funcionário e do cliente.

**Quantiphi**

A [Quantiphi](https://quantiphi.com/quantiphi-empowers-enterprise-ai-transformation-with-nvidia-nim-agent-blueprints/) está integrando o NVIDIA AI Blueprints em suas soluções de IA conversacional para aprimorar o atendimento ao cliente com avatares digitais realistas. Esses avatares de última geração, impulsionados pelas tecnologias NVIDIA Tokkio e ACE, [microsserviços NVIDIA NIM](https://www.nvidia.com/pt-br/ai/) e [NVIDIA NeMo](https://www.nvidia.com/pt-br/ai-data-science/products/nemo/), integram-se perfeitamente às aplicações corporativas existentes, aprimorando as operações e as experiências do cliente com maior realismo. As implantações de NIM ajustadas para workflows de avatar digital provaram ser altamente econômicas, reduzindo os gastos corporativos com tokens.

**SoftServe**

O [SoftServe Digital Concierge](https://www.softserveinc.com/en-us/our-partners/nvidia/digital-concierge), acelerado por NVIDIA AI Blueprints e microsserviços NVIDIA NIM, usa NVIDIA ACE, NVIDIA Riva e o microsserviço NVIDIA Audio2Face NIM para fornecer um assistente virtual altamente realista. Graças à ferramenta Character Creator, ele oferece fala e expressões faciais com notável precisão e detalhes realistas.

Com os recursos RAG do NVIDIA NeMo Retriever, o SoftServe Digital Concierge pode responder de forma inteligente às consultas dos clientes, referenciando o contexto e fornecendo informações específicas e atualizadas. Ele simplifica consultas complexas em respostas claras e concisas e também pode fornecer explicações detalhadas quando necessário.

**EXL**

A oferta Smart Agent Assist da EXL é uma solução de IA de contact center que aproveita os microsserviços NVIDIA Riva, NVIDIA NeMo e NVIDIA NIM. A EXL planeja aumentar sua solução usando o NVIDIA AI Blueprint para agentes virtuais de IA.

No [NVIDIA AI Summit India](https://blogs.nvidia.com/blog/accelerating-india-ai-adoption), os parceiros de consultoria da NVIDIA anunciaram uma colaboração com a NVIDIA para transformar a Índia em um Front Office para IA. Usando as tecnologias da NVIDIA, esses gigantes da consultoria podem ajudar os clientes a adaptar o projeto do agente de atendimento ao cliente para criar assistentes virtuais exclusivos usando seu modelo de IA preferido, incluindo LLMs soberanos de fabricantes de modelos baseados na Índia, e executá-lo em produção com eficiência na infraestrutura de sua escolha.

## **Começar**

Para experimentar o blueprint gratuitamente e ver os requisitos do sistema, navegue até o [Blueprint Card](https://build.nvidia.com/nvidia/ai-virtual-assistant-for-customer-service).

Para começar a criar aplicações usando esses microsserviços, visite o [catálogo de APIs da NVIDIA](https://build.nvidia.com/explore/discover). Para [entrar](https://build.nvidia.com/explore/discover?signin=true), você será solicitado a inserir um endereço de e-mail pessoal ou comercial para acessar diferentes opções de criação com o NIM. Para obter mais informações, consulte as [Perguntas Frequentes sobre o NVIDIA NIM](https://forums.developer.nvidia.com/t/nim-faq/300317).

Categorias: [IA Generativa](https://blog.nvidia.com.br/blog/category/ia-generativa/)

Tags: [Geração Aumentada por Recuperação (RAG)](https://blog.nvidia.com.br/blog/tag/geracao-aumentada-por-recuperacao-rag/) | [IA Conversacional](https://blog.nvidia.com.br/blog/tag/ia-conversacional/) | [LLM](https://blog.nvidia.com.br/blog/tag/llm/) | [Microserviços NeMo](https://blog.nvidia.com.br/blog/tag/microservicos-nemo/) | [NeMo](https://blog.nvidia.com.br/blog/tag/nemo/) | [NeMo Retriever](https://blog.nvidia.com.br/blog/tag/nemo-retriever/) | [NIM](https://blog.nvidia.com.br/blog/tag/nim/)

### All NVIDIA News

![img](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/11/Python-OpenUSD-960x540.jpg)

[Usando Python para Automatizar Workflows 3D com OpenUSD](https://blog.nvidia.com.br/blog/usando-python-para-automatizar-workflows-3d-com-openusd-2/)

![img](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/11/amazon-featured-1280x680-1-960x510.jpg)

[Amazon Devices & Services Dá um Passo Importante em Direção à Manufatura Sem Toque com NVIDIA AI e Gêmeos Digitais](https://blog.nvidia.com.br/blog/amazon-devices-services-da-um-passo-importante-em-direcao-a-manufatura-sem-toque-com-nvidia-ai-e-gemeos-digitais/)

![Como Renderizar Instantaneamente Cenas do Mundo Real em Simulação Interativa](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/11/31.gif)

[Como Renderizar Instantaneamente Cenas do Mundo Real em Simulação Interativa](https://blog.nvidia.com.br/blog/como-renderizar-instantaneamente-cenas-do-mundo-real-em-simulacao-interativa/)

![img](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/11/isaac-png-960x540.webp)

[Impulsionando o Desenvolvimento de Robótica Alimentada por IA com o NVIDIA Isaac for Healthcare](https://blog.nvidia.com.br/blog/impulsionando-o-desenvolvimento-de-robotica-alimentada-por-ia-com-o-nvidia-isaac-for-healthcare/)

![img](https://blog.nvidia.com.br/wp-content/uploads/sites/12/2025/10/Picture104.jpg)

[NVIDIA disponibiliza software Aerial de código aberto para acelerar o 6G nativo de IA](https://blog.nvidia.com.br/blog/nvidia-disponibiliza-software-aerial-de-codigo-aberto-para-acelerar-o-6g-nativo-de-ia/)

### Informações Corporativas

- [Sobre a NVIDIA](https://www.nvidia.com/pt-br/about-nvidia/)
- [Visão Geral Corporativa](https://www.nvidia.com/pt-br/about-nvidia/ai-computing/)
- [Tecnologias](https://www.nvidia.com/pt-br/technologies/)
- [Pesquisa na NVIDIA](https://www.nvidia.com/pt-br/research/)
- [Investidores](https://investor.nvidia.com/home/default.aspx)
- [Responsabilidade Social](https://www.nvidia.com/pt-br/csr/)
- [Fundação NVIDIA](https://www.nvidia.com/pt-br/foundation/)

### Faça Parte

- [Fóruns](https://www.nvidia.com/pt-br/forums/)
- [Carreiras na NVIDIA](https://www.nvidia.com/pt-br/about-nvidia/careers/)
- [Para Desenvolvedores](http://developer.nvidia.com/)
- [Participe do Programa para Desenvolvedores](http://developer.nvidia.com/developer-program)
- [Rede de Parceiros NVIDIA](https://www.nvidia.com/pt-br/about-nvidia/partners/)
- [NVIDIA Inception](https://www.nvidia.com/pt-br/startups/)
- [Recursos para Investidores de Startups](https://www.nvidia.com/pt-br/startups/venture-capital/)
- [Treinamentos Técnicos](https://www.nvidia.com/pt-br/training/)
- [Treinamento para Profissionais de IT](https://academy.nvidia.com/en/)
- [Serviços Profissionais para Ciência de Dados](https://www.nvidia.com/pt-br/ai-data-science/professional-services/)

### Notícias e Eventos

- [Sala de Imprensa](https://nvidianews.nvidia.com/)
- [Blog da NVIDIA](https://blog.nvidia.com.br/)
- [Webinars](https://www.nvidia.com/pt-br/about-nvidia/webinar-portal/)
- [Fiquei Informado](https://www.nvidia.com/pt-br/preferences/email-signup/)
- [Calendário de Eventos](https://www.nvidia.com/pt-br/events/)
- [NVIDIA GTC](https://www.nvidia.com/en-us/gtc)
- [NVIDIA On-Demand](https://www.nvidia.com/en-us/on-demand/)

EXPLORE NOSSOS BLOGS REGIONAIS E OUTRAS REDES SOCIAIS



- [Política de Privacidade](https://www.nvidia.com/pt-br/about-nvidia/privacy-policy/)
-  
- [Gerenciar Minha Privacidade](https://www.nvidia.com/pt-br/privacy-center/)
- [Gerenciar meus cookies](javascript:void(0);)
-  
- [Legais](https://www.nvidia.com/pt-br/about-nvidia/legal-info/)
-  
- [Acessibilidade](https://www.nvidia.com/pt-br/about-nvidia/accessibility/)
-  
- [Segurança dos Produtos](https://www.nvidia.com/pt-br/product-security/)
-  
- [Fale Conosco](https://www.nvidia.com/pt-br/contact/)

Copyright © 2025 NVIDIA Corporation

[Brasil](https://www.nvidia.com/en-us/location-selector/)