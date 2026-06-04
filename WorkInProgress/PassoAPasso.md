

# ☕💣 Passo 1 — Criar a Documentação do Agente

Use o README que montamos.

Inclua:

- Nome: Bellacosa Mainframe Assistant
- Objetivo
- Público-alvo
- Funcionalidades
- Tecnologias
- Diferenciais

Entregável:

📄 `README.md`

------

# ☕💣 Passo 2 — Criar a Base de Conhecimento

Monte um documento chamado:

📄 `base_conhecimento.md`

Exemplo:

```text
Área COBOL
- Variáveis
- Arquivos VSAM
- Tabelas
- SQL Embedded

Área JCL
- JOB
- EXEC
- DD
- PROCs
- IF/THEN

Área RACF
- Users
- Groups
- Profiles
- Permissions
```

Quanto mais conteúdo, melhor.

------

# ☕💣 Passo 3 — Criar o Prompt Principal

Arquivo:

📄 `prompt_sistema.txt`

Exemplo:

```text
Você é o Bellacosa Mainframe Assistant.

Especialista em:

COBOL
JCL
CICS
DB2
RACF
TSO/ISPF
JES2
z/OS

Responda sempre de forma didática.

Explique conceitos técnicos usando exemplos reais de ambiente corporativo.

Quando possível:
- mostre exemplos
- mostre boas práticas
- explique erros comuns
- apresente curiosidades históricas
```

------

# ☕💣 Passo 4 — Criar a Aplicação

Você pode usar qualquer plataforma.

## Opção mais fácil

### ChatGPT GPTs

Criar um GPT personalizado.

Adicionar:

- Nome
- Instruções
- Conhecimento

Tirar screenshots.

------

## Opção intermediária

### Dify

Criar chatbot.

Adicionar:

- Prompt
- Base de conhecimento

Publicar.

Tirar screenshots.

------

## Opção avançada

### Streamlit

Criar aplicação Python.

Estrutura:

```text
app.py
README.md
prompt_sistema.txt
base_conhecimento.md
```

------

# ☕💣 Passo 5 — Realizar Testes

Faça pelo menos 10 perguntas.

Exemplo:

### Teste 1

Pergunta:

```text
O que é um ABEND?
```

Resposta:

```text
Explicou corretamente.
```

------

### Teste 2

Pergunta:

```text
Diferença entre JES2 e JES3?
```

Resultado:

```text
Correto.
```

------

### Teste 3

Pergunta:

```text
Explique um READ VSAM em COBOL.
```

Resultado:

```text
Correto.
```

Monte uma tabela:

| Teste | Resultado |
| ----- | --------- |
| 1     | OK        |
| 2     | OK        |
| 3     | OK        |
| 4     | OK        |
| 5     | OK        |

------

# ☕💣 Passo 6 — Definir Métricas

Exemplo:

| Métrica     | Valor |
| ----------- | ----- |
| Precisão    | 95%   |
| Clareza     | 93%   |
| Satisfação  | 4,8/5 |
| Tempo Médio | 2s    |

------

# ☕💣 Passo 7 — Criar o Pitch

1 minuto já é suficiente.

### Problema

Falta de profissionais Mainframe.

### Solução

Bellacosa Mainframe Assistant.

### Benefícios

- Aprendizado acelerado
- Respostas rápidas
- Preservação do conhecimento

### Futuro

- Integração com documentação IBM
- Simuladores
- Laboratórios

------

# ☕💣 Passo 8 — Capturas de Tela

Tire screenshots de:

1. Tela do agente
2. Prompt
3. Base de conhecimento
4. Testes realizados
5. Resultado das respostas

------

# ☕💣 Estrutura Final da Entrega

```text
Bellacosa-Mainframe-Assistant/

README.md

base_conhecimento.md

prompt_sistema.txt

testes.pdf

metricas.pdf

pitch.pdf

screenshots/
├── tela_principal.png
├── prompt.png
├── conhecimento.png
├── testes.png
└── resultados.png
```

Com isso você cobre integralmente as 6 etapas do desafio da DIO e ainda apresenta um projeto alinhado à sua especialidade em Mainframe, o que costuma destacar bastante a entrega.