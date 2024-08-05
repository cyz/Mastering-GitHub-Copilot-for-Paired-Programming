<header>

# Usando o GitHub Copilot com JavaScript

Neste módulo, continuaremos explorando as capacidades do GitHub Copilot e aprenderemos como utilizá-lo para aprimorar sua experiência de codificação. Imagine escrever código mais rapidamente e com menos esforço—o GitHub Copilot torna isso uma realidade ao gerar sugestões com base no contexto dos seus comentários e código.

Como desenvolvedor em busca de maior produtividade, você embarcará em uma jornada para dominar as capacidades do GitHub Copilot, com foco em sua aplicação em JavaScript. Ao final do módulo, você ganhará experiência em criar prompts que geram sugestões valiosas usando a extensão GitHub Copilot no Visual Studio Code. Eleve suas habilidades de codificação enquanto usa o GitHub Copilot para aprimorar um projeto em JavaScript, vivenciando em primeira mão como este programador em par baseado em IA oferece sugestões no estilo de autocompletar, transformando seu fluxo de desenvolvimento.

Ao dominar o GitHub Copilot, você não apenas configurará repositórios em Codespaces, mas também utilizará eficientemente essa ferramenta de IA para melhorar seus projetos de codificação. Prepare-se para revolucionar sua experiência de codificação e aumentar sua produtividade nesta dinâmica aventura de aprendizado!

</header>


- **Para quem é**: Desenvolvedores, Engenheiros DevOps, Gerentes de desenvolvimento de software, Testadores.
- **O que você aprenderá**: Usar o GitHub Copilot para criar código e adicionar comentários ao seu trabalho.
- **O que você construirá**: Arquivos JavaScript que terão código gerado pela IA do Copilot para sugestões de código e comentários.
- **Pré-requisitos**: Para usar o GitHub Copilot, você deve ter uma assinatura ativa do GitHub Copilot. Inscreva-se para 30 dias grátis [Copilot](https://github.com/settings/copilot).
- **Tempo**: Este módulo pode ser concluído em menos de uma hora.

Ao final deste módulo, você adquirirá as habilidades para:

- Criar prompts para gerar sugestões do GitHub Copilot.
- Aplicar o GitHub Copilot para melhorar seus projetos.

## Leitura pré-requisito:
- [Introdução à engenharia de prompts com GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot/?WT.mc_id=academic-113596-abartolo)
- [Usando GitHub Copilot com JavaScript](https://learn.microsoft.com/training/modules/introduction-copilot-javascript/?WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilite seu [serviço GitHub Copilot](https://github.com/github-copilot/signup).
1. Abra [este repositório com Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-javascript?quickstart=1).


## 💪🏽 Exercício

**Clique com o botão direito no botão Codespaces a seguir para abrir seu Codespace em uma nova aba**

[![Abrir no GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682619)

Neste portfólio modelo, temos um aplicativo web baseado em React pronto para você personalizar e implantar facilmente usando apenas seu navegador.

**Nota:** Por favor, desconsidere as instruções fornecidas dentro do GitHub Codespace. Para este laboratório, certifique-se de seguir as instruções encontradas aqui.

### 🛠 Passo 1: Personalize o aplicativo web

Personalize o portfólio com seus próprios links. Vá para `src/App.jsx` e atualize o `siteProps` com suas informações. A variável `siteProps` é um objeto JavaScript que contém pares de chave e valor usados para personalizar o site, deve parecer com isto:

```javascript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
```
### 📖 Passo 2: Explique o código

Agora vamos usar o comando de barra para explicar o que uma parte do código faz. Selecione o seguinte código:

```javascript
};

const primaryColor = "#4E567E";
const secondaryColor = "#D2F1E4";

const App = () => {
  return (
    <div id="main">
      <Header />
      <Home name={siteProps.name} title={siteProps.title} />
      <About />
      <Portfolio />
      <Footer {...siteProps} primaryColor={primaryColor} secondaryColor={secondaryColor} />
    </div>
  );
};
```
Depois de selecionar, pressione Ctrl + I (Windows) ou Cmd + I (Mac) e digite **/explain**. Você deve receber uma resposta na janela do Copilot Chat semelhante a esta:

```
Este código JavaScript é escrito em React, uma biblioteca popular para construir interfaces de usuário. O código define um componente funcional chamado App. O componente App é o componente raiz da sua aplicação. É onde todos os outros componentes (Header, Home, About, Portfolio, Footer) são chamados e renderizados. O componente App retorna uma estrutura JSX (JavaScript XML), que se parece com HTML. Essa estrutura JSX define o que o componente App deve renderizar na tela. No JSX, há um div com um id de "main". Dentro desse div, vários componentes estão sendo renderizados: Header, Home, About, Portfolio e Footer. O componente Home está recebendo duas props: name e title, ambas propriedades do objeto siteProps. O componente Footer está recebendo várias props. A sintaxe ...siteProps está usando o operador spread do JavaScript para passar todas as propriedades de siteProps como props separadas. Além de siteProps, duas props adicionais estão sendo passadas: primaryColor e secondaryColor. Estas são definidas como constantes no topo do arquivo. Lembre-se, props (abreviação de propriedades) no React são a forma como os componentes se comunicam. Se você pensar nos componentes como funções, então as props são os argumentos dessas funções. Elas são passadas do componente pai (neste caso, App) para os componentes filhos (Header, Home, About, Portfolio, Footer).
```

Vamos aprofundar um pouco mais. Note como o Copilot Chat agora fornece uma sugestão de pergunta para você fazer. Clique na pergunta sugerida pelo GitHub Copilot encontrada na parte inferior da janela, geralmente começando com "Qual é o propósito..." e revise a resposta fornecida. Como exemplo, se a pergunta fornecida pelo GitHub Copilot for a seguinte:

Qual é o propósito de usar props em componentes React?

Você deve obter uma resposta semelhante a esta:

```
Props (abreviação de propriedades) no React são usadas para passar dados de um componente para outro, assim como argumentos de função. Elas são somente leitura e ajudam a tornar os componentes reutilizáveis e dinâmicos. No seu código, por exemplo, o componente Home recebe name e title como props. Isso significa que o componente Home pode usar esses valores para exibir conteúdo dinâmico. O componente Footer também recebe várias props, incluindo todas as propriedades de siteProps e as constantes primaryColor e secondaryColor. Aqui está uma analogia: pense em um componente como um elemento HTML personalizado e props como os atributos desse elemento. Assim como você pode passar diferentes atributos para um elemento HTML (como <img src="image.jpg" alt="Uma imagem">), você pode passar diferentes props para um componente React (como <Home name="John" title="Developer" />). Isso torna seus componentes mais flexíveis e reutilizáveis. Por exemplo, você poderia usar o mesmo componente Home com diferentes props para exibir conteúdo diferente.
```

Você notou que depois de clicar na pergunta sugerida na janela do Copilot Chat, ele usou um comando semelhante ao seguinte para fazer a pergunta:
```
@workspace /explain What is the purpose of using props in React components?
```

O agente @workspace, assim como o Copilot, preenche os detalhes ausentes, ajudando quando os humanos esquecem ou não descrevem completamente tudo o que veem. Quando solicitado, o Copilot adota uma abordagem diferente. Em vez de responder imediatamente, ele primeiro examina os arquivos e pastas no workspace em etapas:

1. Ele verifica os nomes dos arquivos/pastas para ver quais podem ser relevantes.
2. Ele lê o conteúdo dos arquivos, às vezes na íntegra, às vezes parcialmente devido a limites de memória.
3. Ele cria um contexto a partir das informações coletadas.
4. Ele responde, usando tanto o contexto do prompt quanto as informações que reuniu.


### 🔎 Step 3: Animate the social media icons with a prompt

Uma animação pode tornar a seção de redes sociais mais atraente. Peça a ajuda do Copilot para animar os ícones. Vá até o final do arquivo e escreva o seguinte prompt no arquivo `src/styles.css`:

```css
/* add an amazing animation to the social icons */
```

A sugestão do Copilot deve ser semelhante à seguinte:

```css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```

### 🚀 Step 4: Find out how to run the app

Abra o chat do GitHub Copilot clicando no ícone de chat na barra lateral esquerda e use a seção de entrada para perguntar o seguinte:

```
@workspace I want to understand how can I run this React application
```

O prompt utiliza `@workspace`, que é um recurso especial do GitHub Copilot chat que permite incluir mais contexto para uma resposta mais completa. Experimente outras consultas usando o painel de chat para um fluxo de trabalho mais interativo.

### Conclusão

Seu site já deve estar em execução no seu Codespace, e a alteração será recarregada automaticamente na página. Para ver as mudanças, passe o cursor sobre um dos ícones de redes sociais no rodapé para ver a mágica!

**Nota:** Atualize a janela do navegador do Codespace se os efeitos de hover não funcionarem.

Parabéns, através do exercício, você usou o GitHub Copilot para gerar código e também fez isso de uma maneira interativa e divertida! Você pode usar o GitHub Copilot não apenas para gerar código, mas também para escrever documentação, testar suas aplicações e muito mais.