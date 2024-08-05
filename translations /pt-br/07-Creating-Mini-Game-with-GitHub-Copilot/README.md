<header>

# Criando um Mini Jogo com o GitHub Copilot

Nosso foco neste módulo é aproveitar o poder do GitHub Copilot para criar um minijogo clássico de pedra, papel e tesoura. Esta experiência prática não só aprimorará suas habilidades de programação, mas também aumentará sua capacidade de desenvolver aplicativos de console em Python. A melhor parte? Estaremos utilizando o GitHub Codespaces, eliminando o incômodo de configurar seu ambiente de desenvolvimento. Com o GitHub Copilot como seu programador parceiro de IA, você pode se concentrar no desenvolvimento de aplicativos enquanto colabora perfeitamente com seu assistente de código.

</header>


- **Para quem é**: Desenvolvedores, Engenheiros DevOps, Gerentes de desenvolvimento de software, Testadores.
- **O que você aprenderá**: Aproveitar o GitHub Copilot para criar código e adicionar comentários ao seu trabalho.
- **O que você construirá**: Arquivos Python que terão código gerado pela IA do Copilot para sugestões de código e comentários.
- **Pré-requisitos**: Para usar o GitHub Copilot, você deve ter uma assinatura ativa do GitHub Copilot. Inscreva-se para 30 dias grátis Copilot.
- **Tempo**: Este curso pode ser concluído em menos de uma hora.

Ao final deste módulo, você adquirirá as habilidades para:

- Experimentar o GitHub Codespaces como um ambiente de desenvolvimento.
- Desenvolver rotinas de entrada e saída em um aplicativo de console Python.
- Usar o GitHub Copilot como assistente.

## Leitura pré-requisito:
- [Introdução à engenharia de prompts com o GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Projeto de desafio - Construa um minijogo com o GitHub Copilot e Python](https://learn.microsoft.com/training/modules/challenge-project-create-mini-game-with-copilot/?WT.mc_id=academic-113596-abartolo)
- Learn Live: Construa um aplicativo de console de minijogo com o GitHub Copilot (Vídeo abaixo)
- [![Learn Live: Construa um aplicativo de console de minijogo com o GitHub Copilot](https://mediusimg.event.microsoft.com/video-53275/b508053c0b/thumbnail.jpg?sv=2018-03-28&sr=c&sig=k6NthrPwnvBfDPNAEBQaYaVzlJavZ8pnWuP6OcKm4Bs%3D&se=2028-11-18T05%3A23%3A52Z&sp=r)](https://ignite.microsoft.com/sessions/aeaf1e85-65e2-497d-aaf5-724d85213aa1?WT.mc_id=academic-113596-abartolo)


## Requisitos

- Habilite seu serviço [GitHub Copilot](https://github.com/github-copilot/signup)

## 💪🏽 Exercício

**Clique com o botão direito no botão "Iniciar Curso" para abrir seu Codespace em uma nova aba**
 
[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=copilot-codespaces-vscode&owner=%40me&name=skills-copilot-codespaces-vscode&description=My+clone+repository&visibility=public)

Você já aprendeu um pouco sobre o GitHub Codespaces e o GitHub Copilot e como eles funcionam. Neste exercício de desafio, seu objetivo é desenvolver um minijogo em Python usando o GitHub Copilot.

#### Testando seu GitHub Codespace

1. Acesse seus Codespaces e crie um novo arquivo chamado *app.py* no Visual Studio Code.

   **Nota:** Você pode precisar instalar a Extensão Python no Visual Studio Code se ela não estiver instalada atualmente.

2. Digite o seguinte comentário:


   ```python
   # escreva 'hello world' no console
   ```
      
3. O GitHub Copilot deve completar o código para você e fornecer o seguinte resultado:

   ```python
   # escreva 'hello world' no console
   print('hello world')
   ```

4. Execute o aplicativo com o comando *python app.py* no terminal e verifique se o resultado é semelhante à seguinte mensagem no console:

   ```bash
   hello world
   ```
   
### Criando a lógica do jogo

Agora que você verificou que o Codespaces está funcionando com o GitHub Copilot, seu próximo passo é desenvolver a lógica do minijogo em Python com a ajuda do GitHub Copilot com base nas seguintes especificações:

O vencedor do jogo é determinado por três regras simples:

- **Pedra** vence tesoura.
- **Tesoura** vence papel.
- **Papel** vence pedra.

#### Considerações sobre a interação do jogo

O computador será seu oponente e pode escolher aleatoriamente um dos elementos (**pedra**, **papel** ou **tesoura**). Sua interação com o jogo será através do console (Terminal).

- O jogador pode escolher uma das três opções: pedra, papel ou tesoura e deve ser avisado se inserir uma opção inválida.
- Em cada rodada, o jogador deve inserir uma das opções da lista e ser informado se ganhou, perdeu ou empatou com o oponente.
- Ao final de cada rodada, o jogador pode escolher se deseja jogar novamente.
- Exibir a pontuação do jogador ao final do jogo.
- O minijogo deve lidar com entradas do usuário, colocando-as em minúsculas e informando ao usuário se a opção é inválida.

No seu GitHub Codespaces, siga as instruções fornecidas para configurar prompts que o GitHub Copilot possa entender e usar para ajudá-lo a construir o minijogo. Lembre-se de que o GitHub Copilot depende de comentários para entender o contexto e fornecer sugestões úteis enquanto você trabalha no seu projeto.

#### Verifique seu trabalho

1. Execute o minijogo no console com o comando *python app.py*.
2. No prompt, digite uma das opções do jogo: *pedra*, *papel* ou *tesoura*.
3. O minijogo deve informar ao jogador se ele ganhou, perdeu ou empatou com o oponente.
4. Escolha continuar jogando.
5. No prompt, digite *screen*.
6. O minijogo deve informar ao jogador se a opção inserida é inválida.
7. Repita os passos 2 e 4 para jogar algumas rodadas e escolha não continuar jogando.
8. Verifique se o minijogo é encerrado e se exibe sua pontuação, informando o número de vitórias e rodadas.

Parabéns por completar este exercício de desafio! Você criou um minijogo de console em Python usando o GitHub Copilot.