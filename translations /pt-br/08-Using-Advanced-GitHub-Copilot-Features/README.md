<header>

# Usando Recursos Avançados do GitHub Copilot

O GitHub Copilot oferece mais do que sugestões de código. Como Engenheiro de Software, você frequentemente se encontrará tentando entender o código existente e aprimorá-lo com documentação, testes e automação.

Neste módulo, você usará os recursos avançados do GitHub Copilot que permitirão trabalhar interativamente com seu código e aplicar sugestões e conhecimentos de forma eficiente.

Você usará uma API HTTP existente baseada em Python para fazer alterações, correções de bugs, documentação e testes para um novo endpoint que você implementará.

</header>


- **Para quem é**: Desenvolvedores, Engenheiros DevOps, Gerentes de desenvolvimento de software, Testadores.
- **O que você aprenderá**: Usar recursos avançados do GitHub Copilot para testar, documentar e trabalhar com código.
- **O que você construirá**: Uma nova rota de API HTTP, juntamente com documentação e testes para verificar sua correção.
- **Pré-requisitos**: Para usar o GitHub Copilot, você deve ter uma assinatura ativa do GitHub Copilot. Inscreva-se para 30 dias grátis Copilot.
- **Tempo**: Este módulo pode ser concluído em menos de uma hora.

Ao final deste módulo, você adquirirá as habilidades para:

- Usar recursos avançados do GitHub Copilot, como chat inline, comandos de barra e agentes.
- Interagir com o GitHub Copilot com um contexto mais profundo sobre seu projeto e fazer perguntas sobre ele.

## Leitura pré-requisito:
- [Introdução à engenharia de prompts com o GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Usando recursos avançados do GitHub Copilot](https://learn.microsoft.com/training/modules/advanced-github-copilot/?WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilite seu serviço [GitHub Copilot](https://github.com/github-copilot/signup)
1. Abra [este repositório com Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-advanced-copilot)

## 💪🏽 Exercício

**Clique com o botão direito no botão Codespaces abaixo para abrir seu Codespace em uma nova aba**
 
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

A API atual não está expondo country/{country}, que precisa ser implementado para listar cidades. A rota deve permitir apenas solicitações HTTP GET com uma resposta JSON fornecendo informações sobre os máximos e mínimos históricos para aquele país, cidade e mês específico.

Como em qualquer implementação, essa adição deve incluir pelo menos uma função de teste para funcionar com o pytest runner e o framework de testes.


### 🛠 Step 1: Add a new route 
On our first exercise we will create a new route in our API. Go to the main.py file, and by using the inline chat with the following command `ctrl` + `i` (on Windows) or  `cmd` + `i`(on Mac) ask GitHub Copilot to help you create a new API that shows you the cities of a country. 

Use the following prompt in inline-chat:

```
Create a new route that exposes the cities of a country.
```

This prompt should give you something similar like this:


```python
# Create a new route that exposes the cities of a country:
@app.get('/countries/{country}')
def cities(country: str):
    return list(data[country].keys())

```

> [!NOTE]
> Try your new route and refine your prompt until the result is as desired.

### 🔎 Step 2: Create a test
Now that you have created a new route, let's create a test with Copilot Chat for this route that uses Spain as the country. Remember to select your code and ask Copilot Chat to help you with this specific API that we just have created.

Use the following prompt with GitHub Copilot Chat:

```
/tests help me to create a new test for this route that uses Spain as the country.
```

![Copilot Chat image example](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-advanced-copilot/main/images/ideascopilot.png)


Once Copilot has helped you to create your test, try it. If this is not functioning as expected, feel free to share those details with Copilot in the chat. For example:

```
This test is not quite right, it is not including cities that doesn't exist. Only Seville is part of the API.
```

It should give you another solution. Keep trying until you achieve the desired result.

### 🐍 Step 3: Use an agent to write the project
During this step we will be using an agent (workspace) to write the project documentation on how to run this project. In the GitHub Copilot Chat, we will try the following prompt:

`> @workspace help me to use an agent to write the project documentation on how to run it .`

Finally, verify the new endpoint is working by trying it out by going to the `/docs` endpoint and confirming that the endpoint shows up.


### 💡 Step 4: Using Slash Commands

Now that you've used GitHub Copilot to generate and explain code, you can also explore some other alternative approaches to perform developer tasks. These extra challenges will help you dive deeper into other GitHub Copilot features in addition to the ones you already know. For these extra challenges, you will use the Chat interface. Click on the GitHub Copilot Chat icon on the left sidebar if you don't have it open yet.

🚀 Congratulations, through the exercise, you have used GitHub Copilot with many different features that will allow you to work better with different projects. You interactively used some features to write tests, documentation, and find more about existing code..

## Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
