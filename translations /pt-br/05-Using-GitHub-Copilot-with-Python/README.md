<header>

# Usando GitHub Copilot com Python

O GitHub Copilot é a primeira ferramenta de desenvolvedor em escala com IA do mundo que acelera significativamente a escrita de código, fornecendo sugestões no estilo de autocomplete enquanto você trabalha. Neste módulo, vamos focar em usar o poder do GitHub Copilot para melhorar a eficiência da codificação em Python.

Como desenvolvedor, seu objetivo é aumentar a produtividade e acelerar os processos de codificação. O GitHub Copilot atua como seu par de programação em IA, oferecendo sugestões com base no contexto e padrões de código. Neste módulo, você usará o GitHub Copilot com Codespaces para gerar e implementar sugestões de código de forma eficaz.

Prepare-se para mergulhar em um cenário real! Você estará modificando um repositório Python usando o GitHub Copilot para criar um formulário HTML interativo e um endpoint de API. Este projeto lhe dará experiência valiosa no desenvolvimento de uma aplicação web Python que serve uma API HTTP, gerando tokens pseudo-aleatórios para fins de identificação.

</header>


- **Para quem é este módulo**: Desenvolvedores, Engenheiros de DevOps, Gerentes de desenvolvimento de software, Testadores.
- **O que você vai aprender**: Usar o GitHub Copilot para criar código e adicionar comentários ao seu trabalho.
- **O que você vai construir**: Arquivos Python que terão código gerado pela IA do Copilot para sugestões de código e comentários.
- **Pré-requisitos**: Para usar o GitHub Copilot, você deve ter uma assinatura ativa do GitHub Copilot. Inscreva-se para um teste gratuito de 30 dias [Copilot](https://github.com/settings/copilot).
- **Duração**: Este módulo pode ser concluído em menos de uma hora.

Ao final deste módulo, você terá as habilidades para:

- Criar prompts para gerar sugestões do GitHub Copilot
- Aplicar o GitHub Copilot para melhorar seus projetos.

## Leitura pré-requisita:
- [Introdução à engenharia de prompts com GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Usando GitHub Copilot com Python](https://learn.microsoft.com/en-us/training/modules/introduction-copilot-python/?WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilite seu [serviço GitHub Copilot](https://github.com/github-copilot/signup).
2. Abra [este repositório com Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python).

## 💪🏽 Exercise

**Clique com o botão direito no seguinte botão Codespaces para abrir seu Codespace em uma nova aba**
 
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

A API já possui um endpoint para gerar um token. Vamos atualizar a API adicionando um novo endpoint que aceite texto e retorne uma lista de tokens.

### 🛠 Step 1: Add a Pydantic model

Vá para o arquivo `main.py`, navegue até o final do código fornecido, selecione **Ctrl + I (PC)** ou **Cmd + I (Mac)** e copie o seguinte para a caixa de chat do GitHub Copilot para que ele possa gerar um modelo `Pydantic` para você:

```
Crie um modelo Pydantic para que eu possa usá-lo em uma nova rota que aceitará JSON com a chave `text`, a qual deve aceitar uma string.
```

O modelo gerado deve ficar assim:

```python
    class TextData(BaseModel):
        text: str
```

> [!NOTE]
> Você pode ver alguns avisos de linter no editor (identificáveis ​​com sublinhados pontilhados vermelhos) que podem ser ignorados. Eles incluem linhas longas ou até mesmo novas linhas que não são necessárias. Sinta-se à vontade para lidar com eles, embora isso não deva afetar a execução correta do seu aplicativo.

### 🔎 Etapa 2: Gere um novo endpoint

Em seguida, gere um novo endpoint com o GitHub Copilot adicionando o comentário na parte inferior do arquivo `main.py` sob a última rota.

```python
# Crie um endpoint FastAPI que aceite uma solicitação POST com um corpo JSON contendo um único campo chamado "text" e retorne um checksum do texto.
```

Você pode receber uma sugestão que usa um módulo ou biblioteca que não foi importado. Se isso acontecer, você pode pedir ajuda ao GitHub Copilot para importar o módulo correto selecionando o código gerado e usando Command+I (MAC) ou Control+I (Windows) e adicionando um prompt para adicionar as importações faltantes. Esse pequeno pop-up é chamado de chat inline e é outra maneira de interagir com o GitHub Copilot.

### 🐍 Passo 3: Explique o código

A rota `generate()` cria um ID de token pseudo-aleatório usando uma única linha que pode ser difícil de entender completamente. Selecione toda a função, clique com o botão direito na seleção, depois selecione o item de menu do Copilot e, em seguida, a opção _"Explain This"_. A interface de chat do GitHub Copilot abrirá à esquerda e fornecerá uma explicação útil que você pode usar para fazer mais perguntas de forma interativa.

Por fim, verifique se o novo endpoint está funcionando testando-o acessando o endpoint `/docs` e confirmando que o endpoint aparece.

🚀 Parabéns, através deste exercício, você não apenas usou o Copilot para gerar código, mas também fez isso de uma maneira interativa e divertida! Você pode usar o GitHub Copilot não apenas para gerar código, mas também para escrever documentação, testar suas aplicações e muito mais.

### 💡 Passo 4: Usando comandos de barra

Agora que você usou o GitHub Copilot para gerar e explicar código, você também pode explorar algumas outras abordagens alternativas para realizar tarefas de desenvolvedor. Esses desafios extras ajudarão você a mergulhar mais fundo em outros recursos do GitHub Copilot, além dos que você já conhece. Para esses desafios extras, você usará a interface de chat. Clique no ícone do GitHub Copilot Chat na barra lateral esquerda, caso ainda não tenha aberto.

**Gerar documentação**

Com o `main.py` aberto, use a interface de chat com o seguinte texto:

```
/docs Preciso documentar as rotas para estas rotas da API. Ajude-me a produzir documentação que eu possa colocar no arquivo README.md deste projeto.
```

A parte `/docs` do prompt é chamada de _"comando de barra"_ e é uma característica específica do GitHub Copilot que permite escrever documentação


**Gerar testes**

O código atual não tem testes. Para este desafio, você usará o comando de barra `/tests`. Com o `main.py` aberto, use a interface de chat com o seguinte prompt:

```
/tests ajude-me a escrever um teste para a rota generate() usando o cliente de teste do FastAPI e o framework Pytest. Ajude-me a entender onde devo colocar o arquivo de teste, como adicionar a dependência do Pytest ao meu projeto e como executar os testes.
```

O comando `/tests` irá guiá-lo na escrita de um novo teste para sua rota e fornecerá tudo o que você precisa para verificar seu trabalho.

**Desafio do Workspace**

Finalmente, você terá a chance de usar um _agente_. Agentes são um recurso especial do GitHub Copilot no Visual Studio Code que permitem que um contexto específico seja compartilhado com o GitHub Copilot. Para este desafio final, você usará o agente `@workspace`, que inclui arquivos do workspace atual para fornecer mais contexto. Você resolverá um problema relacionado a como executar toda a aplicação. Neste caso, você aprimorará o README.md com mais detalhes que abrangem vários arquivos. Usar `@workspace` ajuda a fornecer mais contexto sem precisar abrir muitos arquivos.

Para este desafio final, você não precisa ter nenhum arquivo aberto. Use o seguinte prompt na janela de chat do GitHub Copilot:

```
@workspace Quero fornecer instruções sobre como executar esta aplicação usando o servidor web uvicorn. Também preciso fornecer instruções sobre como instalar as dependências corretamente e quais são algumas características do framework FastAPI. Usarei isso para melhorar o arquivo README.md.
```

O resultado deve ser uma explicação muito boa sobre o FastAPI, como executar a aplicação e como instalar as dependências. Um relatório no topo da resposta pode incluir todas as referências usadas para determinar quais arquivos eram necessários para fornecer o contexto correto para o GitHub Copilot.

## Avisos Legais

A Microsoft e quaisquer colaboradores concedem a você uma licença para a documentação da Microsoft e outros conteúdos
neste repositório sob a Licença Pública Internacional Creative Commons Attribution 4.0,
veja o arquivo LICENSE, e concedem a você uma licença para qualquer código no repositório sob a Licença MIT, veja o
arquivo LICENSE-CODE.

Microsoft, Windows, Microsoft Azure e/ou outros produtos e serviços Microsoft referenciados na documentação
podem ser marcas comerciais ou marcas registradas da Microsoft nos Estados Unidos e/ou em outros países.
As licenças para este projeto não concedem a você direitos de uso de quaisquer nomes, logotipos ou marcas comerciais da Microsoft.
As diretrizes gerais de marcas registradas da Microsoft podem ser encontradas em http://go.microsoft.com/fwlink/?LinkID=254653.

Informações sobre privacidade podem ser encontradas em https://privacy.microsoft.com/en-us/

A Microsoft e quaisquer colaboradores reservam todos os outros direitos, seja sob seus respectivos direitos autorais, patentes,
ou marcas comerciais, seja por implicação, preclusão ou de outra forma.