# Gemini e Python: crie seu chatbot com IA generativa

## Integrando a API com o Front-End - Apresentação

<video class="elasticMedia" frameborder="0" controls="" controlslist="nodownload" style="box-sizing: inherit; margin: 0px; padding: 0px; top: 0px; left: 0px; width: 820px; height: 461.25px; border: 0px;"></video>

**Boas-vindas!** Meu nome é **André Santana**, sou instrutor na Alura, e irei te acompanhar ao longo dessa jornada no curso sobre **inteligência artificial** utilizando o ***Gemini***.

> **Audiodescrição:** André se descreve como um homem branco, de cabelo curto liso castanho-escuro, barba castanho-escura, e olhos pretos. Ele usa óculos de armação arredondada preta, veste uma camiseta cinza, e está no estúdio da Alura, com uma parede clara iluminada em degradê azul e roxo ao fundo, e uma estante preta à sua esquerda, contendo enfeites, quadros e pontos de iluminação amarela.

## O que vamos aprender?

Neste curso, aprenderemos a **desenvolver um \*chatbot\***, abordando uma série de temas diferentes.

Começaremos trabalhando com uma interface que envolve o uso de ***JavaScript*** e ***Flask***, que será a parte da **aplicação \*web\*** do chatbot. Além disso, aprenderemos a **integrar uma API do Gemini**, para que ele possa responder às mensagens de pessoas usuárias.

Também vamos entender como **configurar o chatbot** para fornecer mais **contexto** e, eventualmente, selecionar **personas** que nos ajudem a responder às pessoas usuárias de forma mais adequada, considerando que, às vezes, ele trará mensagens positivas, negativas, ou neutras.

Além disso, como trabalharemos com um chatbot, iremos verificar como **gerenciar o histórico**, de modo que o chat consiga lembrar de mensagens passadas.

Por fim, entenderemos como **enviar artefatos diferentes**, como **imagens** para interpretar dados de problemas que as pessoas usuárias encontrarem, ou até **textos** associados a esse tipo de imagem.

Abordaremos tudo isso em um projeto de chatbot que trata do **atendimento de clientes** em um ***e-commerce\* de instrumentos musicais**.

## Para quem é este curso?

Este curso é destinado a pessoas que gostam de ***Python*** e desejam **desenvolver um chatbot utilizando tecnologias**, como o Gemini, para responder às perguntas de uma pessoa usuária.

> Recomendamos **acessar os cursos anteriores da formação** antes de iniciar este novo conteúdo.

> **Lembre-se!** Além dos vídeos, disponibilizaremos **atividades** no decorrer das aulas, temos um [fórum de apoio](https://cursos.alura.com.br/forum/categoria-inteligencia-artificial/todos), e uma [comunidade do *Discord*](https://discord.com/oauth2/authorize?client_id=1278070632013238334&response_type=code&redirect_uri=https%3A%2F%2Fcursos.alura.com.br%2Fdiscord%2Fcallback&scope=email+identify+guilds.join) para tirar dúvidas.

**Nos encontramos na primeira aula!**

## Integrando a API com o Front-End - Conectando o chatbot com o front-end

<video class="elasticMedia" frameborder="0" controls="" controlslist="nodownload" style="box-sizing: inherit; margin: 0px; padding: 0px; top: 0px; left: 0px; width: 820px; height: 461.25px; border: 0px;"></video>

Dando sequência à **formação em \*Gemini\***, começaremos a desenvolver uma aplicação com um propósito mais específico, utilizando todo o poder que uma **linguagem natural** tem a oferecer.

## Conectando o *chatbot* ao *front-end*

Inicialmente, temos a interface da aplicação associada a um **assistente virtual** para um *e-commerce* de instrumentos musicais: a **MusiMart**. Em geral, o processamento de linguagem natural nos auxilia no processo de **interação entre a pessoa usuária e uma plataforma**, como um *chatbot*.

Neste caso específico, atuamos em uma **loja virtual**. No entanto, quando pensamos em chatbots, não precisamos focar apenas em assistentes que atuam do lado da pessoa usuária que faz uma compra online. Eventualmente, podemos utilizar chatbots para **diferentes propósitos**.

### Em quais cenários podemos utilizar *chatbots*?

Por exemplo: em uma **campanha eleitoral**, podemos criar um chatbot para oferecer **suporte**, onde as pessoas usuárias podem **consultar** quais são os documentos necessários para o dia da votação.

Também podemos utilizar um chatbot para **auxiliar times de vendas** que têm acesso a um grande catálogo de produtos ou serviços, otimizando o processo de vendas.

Por exemplo: em uma indústria específica, podemos usar um chatbot para oferecer informações sobre os **produtos mais indicados** para o pedido de determinada pessoa usuária.

Embora estejamos trabalhando com um assistente para uma loja de instrumentos musicais, a interação de um assistente virtual com a pessoa usuária para **responder perguntas** e **acessar um domínio de conhecimento específico** tem diversas outras aplicações.

> Podemos utilizar chatbots para resolver diversos problemas em um serviço digital.

### Conhecendo a interface da aplicação MusiMart

No navegador, temos a **interface principal** da aplicação aberta, onde é exemplificada no chat a mensagem um assistente virtual da loja MusiMart, que começa perguntando como pode ajudar:

> Olá! Eu sou o assistente virtual da MusiMart ~
>
> Como posso te ajudar?

Na parte inferior, há um **campo de texto** com um `placeholder` escrito "Enviar uma mensagem". Nesse campo, podemos digitar uma nova mensagem, que substituirá a mensagem padrão.

À esquerda desse campo, há um **botão** de `+` para **adicionar anexos**, que, por enquanto, ainda não funciona. Além disso, à direita, temos um **botão de envio** para submeter uma mensagem.

Por enquanto, temos apenas a interface **visual** do chatbot, implementada com um conjunto de tecnologias que entenderemos como estão orquestradas. Sendo assim, se enviarmos uma mensagem agora, não receberemos nenhuma resposta, pois temos apenas o ***front-end***.

```plaintext
Olá
```

> ***Not Found***
>
> *The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.*

Vamos acessar o *Visual Studio* para entender como isso está implementado?

### Acessando o projeto no *Visual Studio*

No menu lateral esquerdo, no diretório do projeto, temos algumas **pastas** e **arquivos** escritos em diferentes linguagens. É importante realizar todo o processo de **instalação inicial** e **configuração da aplicação** para que ela funcione adequadamente, então atente-se ao processo de instalação das **bibliotecas** necessárias. Feito isso, teremos o ***script\* principal** no arquivo `app.py`.

> *`app.py`:*

```py
from flask import Flask, render_template, request, Response
import google.generativeai as genai
from dotenv import load_dotenv
import os

load_dotenv()

CHAVE_API_GOOGLE = os.getenv("GEMINI_API_KEY")
MODELO_ESCOLHIDO = "gemini-1.5-flash"   
genai.configure(api_key=CHAVE_API_GOOGLE)

app = Flask(__name__)
app.secret_key = 'alura'

@app.route("/")
def home():
    return render_template("index.html")
if __name__ == "__main__":
    app.run(debug = True)
```

### Entendendo o código do arquivo `app.py`

No início do código, utilizamos uma estrutura para desenhar a **parte visual do front-end** com *Python*, usando a biblioteca ***Flask*** (`flask`). Além disso, temos acesso direto à **chave de API** (`CHAVE_API_GOOGLE`), configurada nas **variáveis de ambiente**.

> **Importante!** Devemos ter uma chave de acesso de API.

Nesse caso, utilizamos o modelo mais básico do Gemini, o ***Gemini 1.5 Flash*** (`gemini-1.5-flash`), e configuramos a chave logo abaixo, com `genai.configure(api_key=CHAVE_API_GOOGLE)`.

Na sequência, temos o `app` do `Flask()` e algumas **rotas** — ou *endpoints* — que utilizaremos. O principal deles (`@app.route("/")`), ao subir a aplicação, **renderiza a página principal** no arquivo `index.html` através do renderizador de *template* (`render_template()`).

> Basicamente, o Python, junto à biblioteca Flask, sugere renderizar a página `index.html`, que nos fornece o **front-end** exibido anteriormente na aplicação no navegador.

### Entendendo o código do arquivo `index.html`

Na pasta "templates", conseguimos acessar o arquivo `index.html`.

> *`index.html`:*

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoMart</title>
    <link rel="stylesheet" href="{{ url_for('static', filename='css/index.css') }}">
</head>
<body>
   <header class="cabecalho container">
        <img src="{{ url_for('static', filename='img/logo-chatbot.svg') }}" alt="Logo Chatbot">
        <div class="cabecalho__acoes">

        </div>
   </header> 
   <main class="main">
        <section class="chat container" id="chat">
            <p class="chat__bolha chat__bolha--bot">
                Olá! Eu sou o assistente virtual da EcoMart ~<br/><br/>
                Como posso te ajudar?
            </p>
        </section>
        <section class="entrada container">
            <div class="entrada__container">
                <button id="mais_arquivo" aria-label="Botão de mais opções">
                    <i class="icone icone--mais-opcoes"></i>
                </button>
                <input type="text" class="entrada__input" placeholder="Enviar uma mensagem" id="input">
                <button aria-label="Botão de enviar" id="botao-enviar">
                    <img class="icone icone--enviar-mensagem"></>
                </button>
            </div>
        </section>
   </main>
</body>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="{{ url_for('static', filename='js/index.js') }}"></script>
</html>
```

Trata-se de uma **página HTML** desenhada com caracteres em português (`<html lang="pt-br">`). Na tag `head`, temos uma **folha de estilo CSS** (`stylesheet`) para estilizar os componentes.

Abaixo, na tag `body`, há um **cabeçalho** principal (`header`) contendo o **logotipo do Gemini** (`img`), seguido de uma **estrutura principal** (`main`) para observar as mensagens trocadas entre o assistente e a pessoa usuária, e outros elementos de interação.

Entre esses elementos, há um **botão** (`button`) para enviar arquivos, um **campo de texto** (`input`) para a pessoa usuária enviar mensagens ao assistente, e **outro botão** para enviar a mensagem.

### Entendendo o código do arquivo `index.js`

Além disso, como trabalhamos com uma aplicação web, toda a parte de **gerenciamento do \*back-end\***, que se comunica com os elementos visuais da interface, é orquestrada pelo *script* `index.js`.

Para acessá-lo, vamos até a pasta "*static*", que contém os **elementos estáticos**, onde temos acesso aos **elementos de estilo** na pasta "css" e ao arquivo `index.js` na pasta "js".

Este script escrito na linguagem ***JavaScript*** é muito importante, pois ele orquestra o fluxo de informações do front-end para o Flask, que, por sua vez, submete os dados à API e devolve a resposta para ser exibida. Portanto, toda a gestão do que será construído é feita pelo JavaScript.

Nas três primeiras linhas, buscamos alguns elementos utilizando o **método** `querySelector()`. Nesse caso, buscamos elementos com os **IDs** `#chat`, `#input` e `#botao-enviar`, armazenando-os nas **variáveis** `chat`, `input` e `botaoEnviar`, respectivamente. Observe abaixo:

> *`index.js`:*

```js
let chat = document.querySelector('#chat');
let input = document.querySelector('#input');
let botaoEnviar = document.querySelector('#botao-enviar');

// código omitido
```

Na sequência, declaramos uma **função** em JavaScript chamada `enviarMensagem()`, que é **assíncrona** (`async`), ou seja, não precisamos esperar ela ser concluída para ser chamada e processada.

```js
// código omitido

async function enviarMensagem() {
    if(input.value == "" || input.value == null) return;
    let mensagem = input.value;
    input.value = "";

    let novaBolha = criaBolhaUsuario();
    novaBolha.innerHTML = mensagem;
    chat.appendChild(novaBolha);

    let novaBolhaBot = criaBolhaBot();
    chat.appendChild(novaBolhaBot);
    vaiParaFinalDoChat();
    novaBolhaBot.innerHTML = "Analisando ..."

    // Envia requisição com a mensagem para a API do ChatBot
    const resposta = await fetch("http://127.0.0.1:5000/chat", {
        method: "POST",
        headers: {
        "Content-Type": "application/json",
        },
        body: JSON.stringify({'msg':mensagem}),
    });
    const textoDaResposta = await resposta.text();
    console.log(textoDaResposta);
    novaBolhaBot.innerHTML = textoDaResposta.replace(/\n/g, '<br>');
    vaiParaFinalDoChat();
}

// código omitido
```

Nessa função, verificamos em um bloco `if` se os *inputs* possuem algum **valor vazio**, e a partir disso, começamos o processo de **criação da nova mensagem**, realizado sempre em pares:

> - Uma mensagem exibida ao **enviar** algo para o chatbot;
> - E outra mensagem na **resposta** devolvida pela API do Gemini.

Portanto, inicialmente, criamos a bolha de mensagem da **pessoa usuária** (`novaBolha`), buscamos a informação digitada durante o envio, utilizamos essa mensagem para **preencher o conteúdo** da `novaBolha`, e depois a adicionamos como **elemento filho** (`appendChild()`) do `chat`.

Na sequência, fazemos o mesmo para o chatbot: criamos a variável `novaBolhaBot`; adicionamos como elemento filho; pedimos para ir ao final do chat (`vaiParaFinalDoChat()`); e **atualizamos o conteúdo da mensagem** para "Analisando…". Essa mensagem aguarda a resposta da API do Gemini, que, uma vez construída, substituirá a mensagem com base no que o Gemini devolver.

Logo abaixo, declaramos uma **constante** (`const`) chamada `resposta`, que espera (`await`) uma resposta do Flask em uma rota que será criada, por meio de uma requisição do tipo `POST`.

Feito isso, transformamos a mensagem em texto com `JSON.stringify()` e utilizamos o resultado como texto da nova bolha de chat, declarando a constante `textoDaResposta`.

> Com **bolha**, nos referimos ao balão que mostra a interação entre a pessoa usuária e o chatbot.

Por fim, **substituímos o conteúdo** e vamos ao final do chat novamente.

Mais adiante no código, temos **funções auxiliares** para gestão do HTML com CSS, como a função `criaBolhaUsuario()`, que cria um novo elemento do tipo `p`, adicionando a **classe de estilo** em `bolha.classList` para ficar adequado, e retornando a `bolha` em seguida.

```js
// código omitido

function criaBolhaUsuario() {
    let bolha = document.createElement('p');
    bolha.classList = 'chat__bolha chat__bolha--usuario';
    return bolha;
}

// código omitido
```

O mesmo ocorre para criar a bolha de resposta do chatbot, onde temos a função `criaBolhaBot`. A única diferença é em relação ao **estilo**, posicionando as mensagens da pessoa usuária de um lado da tela e as do chatbot do outro lado. Isso é feito através das **classes do CSS**.

```js
// código omitido

function criaBolhaBot() {
    let bolha = document.createElement('p');
    bolha.classList = 'chat__bolha chat__bolha--bot';
    return bolha;
}

// código omitido
```

Na sequência, temos a função `vaiParaFinalDoChat()`, que rola a informação com `chat.scrollTop = chat.scrollHeight` para deixá-la sempre na **parte inferior da tela**.

```js
// código omitido

function vaiParaFinalDoChat() {
    chat.scrollTop = chat.scrollHeight;
}

// código omitido
```

Por fim, **adicionamos um evento** (`addEventListener()`) ao `botaoEnviar`, que, **ao ser clicado** (`click`), envia uma mensagem (`enviarMensagem`). O mesmo ocorre no `input`, mas o evento é de **tecla** (`keyup`), para que, ao pressionarmos "Enter", a mensagem seja enviada ao chatbot.

```js
// código omitido

botaoEnviar.addEventListener('click', enviarMensagem);
input.addEventListener("keyup", function(event) {
    event.preventDefault();
    if (event.keyCode === 13) {
        botaoEnviar.click();
    }
});

// código omitido
```

> Quem processa tudo isso é o **Flask**, que orquestra a informação, devolvendo ao JavaScript e, eventualmente, enviando novamente ao front-end.

### Configurando a rota `/chat`

Na constante `resposta`, temos uma instrução que solicita ao endereço da aplicação que **consuma o resultado de uma rota de chat** (`await fetch("http://127.0.0.1:5000/chat")`).

Essa rota precisa ser configurada no Flask em Python. Para isso, criaremos uma **nova rota** em `app.py`, que irá se comunicar com a instrução em JavaScript, esperando uma nova mensagem.

Antes de `@app.route("/")`, vamos adicionar outro `@app.route()`, definindo o nome igual ao do JavaScript (`/chat`). Em seguida, especificaremos os **métodos de requisição** (`methods`), com o tipo `POST`. Assim, sempre que acessarmos o endereço `/chat`, ele invocará o método associado.

Feito isso, criaremos o **método em Python** com o comando `def`, optando pelo mesmo nome `chat()`, de modo a facilitar a manutenção do código. No escopo, colocaremos duas instruções:

> 1. A declaração da variável `prompt`, que armazena a **mensagem capturada do input** no front-end pelo JavaScript, trazendo para a rota em Python pelo Flask. Buscaremos isso através da requisição (`request`) feita, acessando o `json` criado no JavaScript e pegando a chave `msg`, especificada em `index.js`;
> 2. A declaração da variável `resposta`, que armazena a **resposta da pessoa usuária**, vinda de um novo método chamado `bot()`, recebendo como parâmetro o `prompt`.

> *`app.py`:*

```py
# código omitido

@app.route("/chat", methods=["POST"])
def chat():
    prompt = request.json["msg"]
    resposta = bot(prompt)

# código omitido
```

## Conclusão

Agora, precisamos **criar o método `bot()`**. Faremos isso no próximo vídeo!

## Integrando a API com o Front-End - Criação do bot

<video class="elasticMedia" frameborder="0" controls="" controlslist="nodownload" style="box-sizing: inherit; margin: 0px; padding: 0px; top: 0px; left: 0px; width: 820px; height: 461.25px; border: 0px;"></video>

Dando sequência à implementação, vamos garantir a **comunicação com a API do \*Gemini\***, para que nosso *chatbot* comece a responder perguntas relacionadas ao *e-commerce* MusiMart.

## Criando o *bot*

### Importando a biblioteca

Primeiramente, no arquivo `app.py`, vamos importar uma **nova biblioteca** para gerenciar tentativas de requisição à API, caso ocorram falhas. Importaremos a função `sleep` da biblioteca `time`.

> *`app.py`:*

```py
from flask import Flask,render_template, request, Response
import google.generativeai as genai
from dotenv import load_dotenv
import os
from time import sleep

# código omitido
```

### Definindo o método `bot()`

Feito isso, podemos começar a **implementação do bot**. Antes da declaração da primeira `@app.route()`, definiremos (`def`) o **método** `bot()` recebendo `prompt` como parâmetro.

```py
# código omitido

def bot(prompt):

# código omitido
```

### Declarando a variável `maximo_tentativas`

A primeira ação será declarar uma **variável** para o **número máximo de tentativas**, caso ocorra alguma exceção na conexão com o Gemini. Sendo assim, no escopo do método, vamos declarar `maximo_tentativas` com o valor inicial de 1, que pode ser ajustado conforme necessário.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1

# código omitido
```

### Declarando a variável `repeticao`

Na sequência, criaremos uma nova **variável** chamada `repeticao`, iniciada em 0, que servirá como **contador** para cada nova tentativa de comunicação com o Gemini.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1
    repeticao = 0

# código omitido
```

### Criando um *loop* `while`

Utilizaremos um ***loop*** `while` com a condição `True` para manter a execução até que uma resposta seja obtida. No escopo do `while`, usaremos um bloco `try` para executar as ações necessárias.

A primeira ação no `try` será **criar um \*prompt\* do sistema**, configurando o chatbot para atuar como assistente de atendimento ao cliente de um e-commerce, sem responder a perguntas fora desse contexto. Para isso, vamos declarar a **variável** `prompt_do_sistema` recebendo uma *f-string*.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1
    repeticao = 0

    while True:
        try:
            prompt_do_sistema = f"""
            Você é um chatbot de atendimento a clientes de um e-commerce. 
            Você não deve responder perguntas que não sejam dados do e-commerce informado!
            """

# código omitido
```

Em seguida, criaremos a **variável** `configuracao_modelo`, que será um **dicionário** com chaves específicas. Inicialmente, definiremos a chave `temperature`, que **controla a criatividade** do assistente ao gerar respostas. Como queremos respostas menos criativas, definiremos como `0.1`.

Além disso, adicionaremos a chave `max_output_tokens` para **limitar a quantidade máxima de \*tokens\*** nas respostas. Nesse caso, definiremos a chave com o valor de `8192`.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1
    repeticao = 0

    while True:
        try:
            prompt_do_sistema = f"""
            Você é um chatbot de atendimento a clientes de um e-commerce. 
            Você não deve responder perguntas que não sejam dados do e-commerce informado!
            """

            configuracao_modelo = {
                "temperature" : 0.1,
                "max_output_tokens" : 8192
            }

# código omitido
```

O próximo passo será iniciar a **comunicação da LLM com a API do Gemini**. Para isso, criaremos a **variável** `llm`, utilizando a biblioteca `genai` para acessar o **construtor** `GenerativeModel()`.

Por padrão, esse construtor espera algumas informações. Entre parênteses, passaremos o **nome do modelo** (`model_name`), definido como uma constante no início do código (`MODELO_ESCOLHIDO`).

Atribuindo esse modelo, utilizaremos o modelo `gemini-1.5-flash`, conforme definido na constante. Esse é o modelo mais em conta, mas de menor qualidade oferecido pelo Gemini.

Além disso, passaremos as seguintes configurações:

> - A **instrução do sistema** (`system_instruction`), definida como `prompt_do_sistema`;
> - E a **configuração do modelo** (`generation_config`), definida como `configuracao_modelo`.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1
    repeticao = 0

    while True:
        try:
            prompt_do_sistema = f"""
            Você é um chatbot de atendimento a clientes de um e-commerce. 
            Você não deve responder perguntas que não sejam dados do e-commerce informado!
            """

            configuracao_modelo = {
                "temperature" : 0.1,
                "max_output_tokens" : 8192
            }

            llm = genai.GenerativeModel(
                model_name=MODELO_ESCOLHIDO,
                system_instruction=prompt_do_sistema,
                generation_config=configuracao_modelo
            )

# código omitido
```

Com a `llm` configurada, podemos **gerar a resposta** a partir da interação com o LLM. Para isso, criaremos a **variável** `resposta` e utilizaremos o **método** `generate_content()` da `llm`, passando o `prompt` como parâmetro. A resposta será retornada no formato de **texto** (`return resposta.text`).

Caso ocorra algum problema, iremos **capturar a exceção** com um bloco `except`, no mesmo nível do bloco `try`, pegando uma exceção genérica (`Exception`) que apelidaremos de `erro`.

Nesse bloco, vamos **incrementar a variável** `repeticao` com `+= 1` e verificar se ela é **maior ou igual ao número máximo de tentativas** (`if repeticao >= maximo_tentativas`).

Se for, trataremos o erro e encerraremos o procedimento (`return "Erro no Gemini: %s" % erro`). Caso contrário, faremos uma pausa de 50 milissegundos (`sleep(50)`) antes de tentar novamente.

```py
# código omitido

def bot(prompt):
    maximo_tentativas = 1
    repeticao = 0

    while True:
        try:
            prompt_do_sistema = f"""
            Você é um chatbot de atendimento a clientes de um e-commerce. 
            Você não deve responder perguntas que não sejam dados do e-commerce informado!
            """

            configuracao_modelo = {
                "temperature" : 0.1,
                "max_output_tokens" : 8192
            }

            llm = genai.GenerativeModel(
                model_name=MODELO_ESCOLHIDO,
                system_instruction=prompt_do_sistema,
                generation_config=configuracao_modelo
            )

            resposta = llm.generate_content(prompt)
            return resposta.text
        except Exception as erro:
            repeticao += 1
            if repeticao >= maximo_tentativas:
                return "Erro no Gemini: %s" % erro
            
            sleep(50)

# código omitido
```

### Enviando a resposta ao *JavaScript*

Por fim, para **enviar a resposta ao \*JavaScript\***, que a exibirá no front-end, retornaremos a `resposta` na rota do chat (`@app.route("/chat")`). Para isso, basta adicionar `return resposta`.

```py
# código omitido

@app.route("/chat", methods=["POST"])
def chat():
    prompt = request.json["msg"]
    resposta = bot(prompt)
    return resposta

# código omitido
```

### Testando o código

Após salvar as alterações, podemos **executar a aplicação**. Ao fazer isso, um endereço será gerado (`http://127.0.0.1:5000`), que pode ser colado no navegador para iniciar a interação com o chatbot.

```plaintext
http://127.0.0.1:5000
```

No navegador, podemos enviar uma mensagem, como, por exemplo:

```plaintext
Olá! Quero comprar uma guitarra!
```

A requisição será feita ao Gemini, que retornará uma resposta padrão em linguagem natural:

> Olá! [Emoji de rosto sorrindo] Que legal! [Emoji de rosto sorrindo] Adoro guitarras! [Emoji de rosto sorrindo com estrelas nos olhos] Para te ajudar a encontrar a guitarra perfeita, preciso de algumas informações. [Emoji de guitarra] Você poderia me dizer:
>
> - **Qual o seu nível de experiência?** (Iniciante, Intermediário, Avançado)
> - **Qual o estilo musical que você toca ou gostaria de tocar?** (Rock, Blues, Jazz, Clássico, etc.)
> - **Qual o seu orçamento?**
> - **Você prefere uma guitarra acústica ou elétrica?**
>
> Com essas informações, posso te indicar os melhores modelos para você! [Emoji de rosto sorrindo e piscando um olho]

## Conclusão

Nosso próximo passo será garantir que o chatbot ofereça **respostas mais contextualizadas**, melhorando a **experiência da pessoa usuária** no e-commerce MusiMart.

Nos encontramos na próxima aula!

## Sobre o curso Gemini e Python: crie seu chatbot com IA generativa

O [curso Gemini e Python: crie seu chatbot com IA generativa ](https://www.alura.com.br/curso-online-python-gemini-crie-chatbot-ia-generativa)possui **116 minutos de vídeos**, em um total de **45 atividades**. Gostou? Conheça nossos outros **[cursos de IA para Programação](https://www.alura.com.br/cursos-online-inteligencia-artificial/ia-para-programacao)** em **[Inteligência Artificial](https://www.alura.com.br/cursos-online-inteligencia-artificial)**, ou leia nossos [artigos de Inteligência Artificial](https://www.alura.com.br/artigos/inteligencia-artificial).

Matricule-se e comece a estudar com a gente hoje! Conheça outros tópicos abordados durante o curso:

- Integrando a API com o Front-End
- Refinando o contexto de um chatbot
- Gerenciando o histórico da conversa
- Enviando imagens pelo chat
- Refinando o chatbot

## 