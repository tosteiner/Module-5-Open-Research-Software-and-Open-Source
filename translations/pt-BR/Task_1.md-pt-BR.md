---
output:
  html_document: default
  pdf_document: default
---

# Tarefa 1: Como configurar um repositório no GitHub

Esta tarefa é projetada para estudantes e pesquisadores que desejam criar seu primeiro projeto Open Source (seja software ou não) no GitHub. O GitHub é um lugar para você conhecer, testar e experimentar novos fluxos de trabalho da pesquisa, inclusive este é apenas o começo para ajudá-lo(a) a preparar o terreno para seus próprios caminhos e ideias.

Não se esqueça de que você pode participar das discussões no nosso fórum aberto no [** canal do Slack **](https://osmooc.herokuapp.com/). Por favor, apresente-se no #módulo5opensource e conte-nos um pouco sobre quem você é, qual a sua formação e como chegou aqui!

**OBSERVE** que uma gravação de tela para esta tarefa também está disponível via [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&).

Tempo estimado para conclusão: 30 a 45 minutos.

Estimativa de economia de tempo após a conclusão: Inimaginável ..

## Sumário

* [Primeiros Passos](#Getting_started) 
  * [Configurando um perfil do GitHub](#Profile)
  * [O idioma do GitHub](#Language)
  * [Criando um novo repositório](#Create_new)
* [Os passos fundamentais](#Foundation) 
  * [Escolhendo uma licença](#License)
  * [Criando um arquivo README](#Readme)
  * [Criando diretrizes de contribuição](#Contributing)
  * [Criando um código de conduta](#Conduct)
  * [Tornando seu código citável](#Citation)
* [Mantendo suas questões atualizadas](#Issues)
* [Lista de verificação para iniciar seu projeto](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Task 1 workflow" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>O fluxo de trabalho da Tarefa 1. Mantenha isso acessível e ao seu alcance enquanto executa a tarefa!</i></p>

  


## Primeiros Passos<a name="Getting_started"></a>

Um 'repositório' é realmente apenas um nome sofisticado para um projeto no GitHub. O GitHub é um local on-line onde você pode gerenciar projetos, armazenar arquivos e colaborar abertamente com outras pessoas. Tudo isso é possível graças ao uso do controle de versão para acompanhar os projetos à medida em que eles progridem. Como tal, o GitHub é uma ferramenta poderosa para projetos de programas e mesmo os que não são um software.

Uma das coisas mais importantes a considerar neste estágio inicial é pensar em como você deseja que a comunidade mais ampla interaja com seu projeto. Como se está trabalhando de maneira aberta, você deve se certificar de que os outros se sentem à vontade para acessar, visualizar e interagir com seu trabalho. Configurar um repositório de forma a reduzir as barreiras de acesso, assim como o medo de ser um "outsider" (forasteiro/estranho), constitui o primeiro passo para manter um projeto bem sucedido.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, a pequena mascote do GitHub</i></p>

  


### Configurando um perfil do GitHub <a name="Profile"></a>

Para configurar um perfil do GitHub, simplesmente vá para a página principal e clique em [Sign Up for GitHub](https://github.com/join). Aqui, você pode criar sua conta pessoal, com nome de usuário, e-mail e senha como padrão.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Cadastre-se no GitHub</i></p>

  


O próximo passo é a criação de uma conta pessoal. Por enquanto, basta selecionar o plano 'Repositórios públicos ilimitados gratuitamente', a menos que você esteja preocupado com a privacidade, nesse caso, selecione o plano privado. Se você pretende criar um projeto para uma organização, também poderá selecionar essa opção.

  


### O idioma GitHub <a name="Language"></a>

Este é possivelmente o aspecto mais confuso e desconcertante do GitHub. Aqui estão alguns dos termos mais usados e suas definições:

* **Initialise (Inicialização)**: Criar um repositório vazio.
* **Checkout**: Criar uma cópia de trabalho de um repositório local.
* **Clone**: Copiar o repositório para um diretório local no seu computador.
* **Fork**: Criar um desdobramento pessoal de um repositório para trabalhar em paralelo.
* **Branch**: Uma versão independente e paralela de um repositório. As alterações não afetam o ramo principal.
* **Master**: A ramificação principal e padrão de um repositório.
* **Clean**: Nenhum commit pendente no branch.
* **Stage**: Adicionar atualizações prontas para serem confirmadas em uma ramificação.
* **Commit**: Uma revisão para um repositório, como uma função 'save' (salvar) com controle de versão.
* **Mensagem de commit**: Uma descrição das alterações que acompanham um commit.
* **Check**: Uma verificação de status.
* **Fetch**: Nada a ver com cães. Refere-se a obter as últimas alterações de um repositório on-line sem mesclá-las.
* **Index**: A 'árvore' que atua como uma área de preparação.
* **Working Directory (Diretório de Trabalho)**: A 'árvore' onde os arquivos são mantidos.
* **Head**: The 'tree' which indicates the last commits made.
* **Push**: Adicionar alterações confirmadas à Head do seu repositório remoto.
* **Merge (Mesclar)**: Combinar as alterações feitas em um branch com a master branch após a conclusão.
* **Pull**: Atualizar seu repositório buscando [fetch] e mesclando [merge] os commits mais recentes.
* **Pull request**: Um pedido para mesclar um branch atualizado no master branch.
* **Issue**: Sugestões de melhorias, tarefas ou perguntas relacionadas a um repositório.

Ufa! Não se preocupe em memorizar *todos esses termos* por enquanto. Como qualquer nova habilidade, a familiaridade vem com a experiência.

Provavelmente, é possível ver como algumas dessas funções são semelhantes a outras conhecidas, tais como salvar, copiar, colar, ou seja, tratam-se de operações de um fluxo de trabalho padrão, porém, adaptadas para um processo de gerenciamento de software. Para saber mais, também há um [glossário](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html), mas isto deve servir para começar.

Se você estiver interessado, a maioria desses termos vem basicamente do [Git system](https://git-scm.com). O Git foi construído para permitir que desenvolvedores gerenciem versões diferentes do código-fonte de maneira distribuída, o que é ótimo. Tem muitos recursos e a capacidade de fazer muitas coisas complexas, escritas por um [ cara muito inteligente](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). No entanto, a interface de usuário [não foi projetada para usuários novos iniciantes ](https://xkcd.com/1597/), por isso pode ser difícil de aprender.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Guia imbatível para usar o Git. (Fonte: XKCD)</i></p>

  


### Criando um novo repositório <a name="Create_new"></a>

No seu perfil do GitHub, clique em "Create new repository" (Criar novo repositório). O primeiro passo é criar um nome como marca para o seu projeto. De preferência, deve ser fácil de memorizar e dar alguma indicação sobre o que se trata o projeto.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Criar um novo repositório</i></p>

  


Certifique-se de não duplicar nomes, infringir outras marcas registradas ou nomeá-las como algo que possa ser considerado ofensivo.

  


## Os passos fundamentais <a name="Foundation"></a>

Qualquer repositório GitHub requer 4 elementos chave para ser iniciado e começar a desenvolver uma comunidade acolhedora:

1. Licenças de código aberto
2. Um arquivo `README`;
3. Diretrizes de contribuição; e
4. Um Código de Conduta

Estes são aspectos críticos e as melhores práticas de qualquer projeto para que os usuários entendam seus direitos legais, suas expectativas, o propósito do projeto e para melhorar a experiência geral do usuário.

Todos esses quatro arquivos devem ser mantidos no diretório raiz do seu repositório de projetos. É conveniente usar formatos de arquivo markdown (`.md`) para a maioria desses arquivos (embora o arquivo de licença seja, na maioria das vezes, texto simples (`.txt`)) e capitalize todos os nomes de arquivo. Ao invés de espaços em nomes de arquivos, certifique-se de usar sublinhados `_` .

Então você deve se deparar com uma seleção de arquivos fundamentais como esta:

1. `LICENÇA.md`
2. `README.md`
3. `CONTRIBUIÇÃO.md`
4. `CÓDIGO_DE_CONDUTA.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>A estrutura básica do repositório</i></p>

  


### Escolhendo uma licença <a name="License"></a>

Escolher uma licença apropriada é o que diferencia seu repositório Open Source do software disponível publicamente. Embora você não seja obrigado a escolher uma licença, isso garante que outras pessoas poderão modificar, compartilhar, reutilizar e desenvolver seu projeto dentro de uma estrutura legal.

Para começar, você quer verificar [Escolha uma Licença](https://choosealicense.com/) para encontrar uma licença que melhor se encaixa em suas intenções para o repositório.

Os três principais para escolher são:

* **Licença MIT (MIT License)**: Uma licença de permissão que possibilita que as pessoas façam o que quiserem com o seu código, desde que forneçam a atribuição adequada para você e não o responsabilizem.
* **Licença Apache 2.0**: Tem permissões semelhantes à Licença MIT, mas também fornece uma concessão expressa de direitos de patentes de colaboradores para usuários.
* **GNU General Public License (GPL) v3**: A [copyleft](https://en.wikipedia.org/wiki/Copyleft) licença que requer a qualquer pessoa a redistribuição do seu código, ou uma obra derivada, para tornar a fonte disponível sob os mesmos termos que a licença original; além disso, fornece uma concessão expressa de direitos de patente dos colaboradores aos usuários.

Felizmente, quando você inicia um novo repositório no GitHub, você tem a opção de selecionar uma licença existente em um menu suspenso. Você deve sempre (com pouquíssimas exceções) usar uma licença existente, pois é isso que os usuários e colaboradores em potencial poderão ver antes de optarem por usar ou contribuir com seu software.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Escolhendo uma licença de exemplo</i></p>

  


Se não há uma licença como você quer, é possível adicionar uma nova manualmente conforme a sua necessidade. Para fazer isso, basta clicar em "Criar novo arquivo" no repositório, copiar e colar um texto de licença existente nele. Nomeie o arquivo, por exemplo, como `LICENSE.txt` ou `LICENSE.md` para torná-lo claro e mantê-lo na pasta principal do repositório (ou seja, a raiz). Certifique-se de adicionar uma mensagem de confirmação (commit message) clara e está pronto!

> **Mão amiga**: Este curso usa uma combinação diferente de licenças para o conteúdo de código e para o conteúdo que não é código. Aqui você pode encontrar um exemplo da licença [MIT](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) que aplicamos para todos os códigos e software gerados como parte da produção deste curso.

  


### Criando um arquivo README <a name="Readme"></a>

Quando você iniciar seu novo repositório, deve haver uma opção para fazê-lo com um arquivo `README`. Assim como Alice no País das Maravilhas, eles fazem exatamente o que dizem - fornecem informações importantes sobre o projeto. Essas são normalmente a primeira coisa que os colaboradores externos verão quando chegam ao seu repositório, portanto, torná-las informativas e receptivas é essencial.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Parte do arquivo README para este módulo</i></p>

  


O arquivo estará originalmente no formato markdown (`.md`). Esta é uma linguagem de marcação leve em formato de texto simples. Para aprender o básico em markdown, veja [este folheto](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Mas por enquanto, podemos apenas usar texto simples.

Há várias coisas que você vai precisar incluir no seu arquivo `README` :

* Do que se trata este projeto e o que faz.
* Por que as pessoas deveriam se importar e por que isso é útil.
* Como alguém pode começar a contribuir com o projeto.
* Quem pode ser contatado no caso de alguém precisar de ajuda.
* Um link para a licença, diretrizes de contribuição e código de conduta.
* Uma descrição da estrutura do projeto.
* Quem está envolvido e quais são os papéis desempenhados.
* O status atual do projeto.

> **Sugestão**: Mais tarde, à medida em que o projeto for sendo desenvolvido, você poderá adicionar perguntas frequentes com base no feedback da comunidade ou um tutorial para ajudar os usuários a entender como o seu projeto funciona.

Lembre-se de que nem todos que chegam ao seu projeto serão especialistas ou entenderão o que você está fazendo e por quê. Ter um arquivo `README` bem documentado aprimorará a experiência do usuário para pessoas com vários conhecimentos prévios.

Quando o arquivo `README` estiver incluído no diretório raiz, o GitHub exibirá automaticamente isso na página inicial do seu repositório. Isso significa que é a primeira coisa que as pessoas costumam ver, então faça valer a pena!

> **Mão amiga**: Aqui, você pode encontrar o arquivo `README` usado para este módulo [MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Isso inclui informações sobre o status, a lógica, os resultados do aprendizado, a equipe de desenvolvimento, os principais documentos e a licença para ajudar. Você pode copiar e adaptar essa estrutura para seus próprios projetos, conforme necessário.

  


### Criando diretrizes de contribuição <a name="Contributing"></a>

As diretrizes de contribuição são projetadas para comunicar aos possíveis colaboradores um breve guia sobre como se engajar com o projeto e a comunidade. Se você quer ter certeza de que está sendo receptivo, pode indicar o quanto anseia que os participantes se envolvam com o seu projeto. Sempre que um participante abrir um novo pull request (solicitação) ou cria uma nova questão (issue), eles verão um link para o seu arquivo de contribuição.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Parte das diretrizes de "CONTRIBUIÇÃO" para este módulo</i></p>

  


Mantendo os nomes dos arquivos em letras maiúsculas, o próximo passo é criar um arquivo e nomeá-lo como `CONTRIBUIÇÃO`. Clique em "Create new file" (Criar novo arquivo) e salve-o no formato de marcação conforme o que foi explicado anteriormente. Esse arquivo informará a outros usuários como eles podem se envolver e participar do seu projeto. Este é o primeiro passo para estabelecer uma comunidade em torno do seu projeto, para torná-lo envolvente, conciso e informativo.

O arquivo `CONTRIBUIÇÃO` deve incluir informações sobre:

* Que tipo de contribuições você está procurando?
* Como sugerir atualizações ou novos recursos.
* Como interagir com o projeto usando as funções do GitHub (por exemplo, o protocolo pull request).
* Como arquivar um relatório de bug ou criar uma questão (issue).
* O objetivo final, visão ou o roteiro para o projeto.
* Como contatar os responsáveis pelo projeto.
* Links para qualquer documentação ou sites externos.

> **Dica**: Considere começar com uma breve nota de agradecimento para as pessoas que estão pensando em contribuir - assim, depois de clicarem no arquivo vão aprender mais no fim das contas! Se houver outros métodos de reconhecimento que você tenha em mente, inclua-os aqui também.

Aqui, você está essencialmente tentando incentivar as pessoas a se oferecerem voluntariamente para fazer avançar seu projeto. Certifique-se de ser acolhedor e amigável, além de ser preciso sobre como as pessoas podem se engajar. Ao escrever isso, certifique-se de pensar sobre o assunto a partir da perspectiva do usuário - como você pode tornar sua vida mais fácil ao enviar solicitações (pull requests) e abertura de questões (issues) para fazer todo o projeto ser executado de forma mais eficiente.

> **Dica**: O item [Diretrizes de contribuição](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) para este módulo MOOC incluem algumas coisas muito específicas: uma introdução ao uso do Git e do GitHub, dicas para começar, informações de contato, como alterar o conteúdo e relatar problemas, um link para o `Arquivo README` e informações sobre o conteúdo preferido e os estilos de código. Sinta-se à vontade para copiar e adaptar isso para o seu próprio projeto, conforme necessário.

  


### Criando um Código de Conduta <a name="Conduct"></a>

Um código de conduta é importante para definir as regras básicas para o comportamento esperado e a participação dos contribuidores do projeto, e é um documento de fácil referência para mostrar que a equipe do projeto leva a sério diálogos construtivos. Portanto, é um elemento fundamental para criar e manter uma comunidade saudável que se envolve de forma construtiva e produtiva dentro de uma atmosfera social positiva.

Um código de conduta não só fornece expectativas de comportamento, mas também descreve a quem e quando estas se aplicam, além de indicar o que fazer caso ocorra uma violação do código e quais serão os itens de ação para tal. Por conseguinte, os pontos de contato precisam ser claramente explicitados no código de conduta. Normalmente, isso deve ser feito de maneira particular, como um endereço de e-mail.

> **Sugestão**: No caso de uma violação precisar ser relatada sobre a pessoa que recebe essas denúncias, certifique-se de incluir uma opção para contatar uma parte secundária.

Para adicionar um código de conduta, você pode criar o seu próprio do zero, adicionando um novo arquivo em markdown, ou pode usar modelos existentes, como o [Contributor Covenant (Convênio de colaboradores)](https://contributor-covenant.org/). Nomeie seu arquivo `CODE_OF_CONDUCT.md` e verifique se ele está visível no arquivo `README`.

> **Dica**: Este curso também tem um [Código de Conduta](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) baseado no Convênio de Colaboradores. Como você pode ver, inclui informações sobre os padrões de comportamento esperados, as responsabilidades das pessoas na comunidade e a aplicação do Código de Conduta, incluindo detalhes de contato. Novamente, sinta-se livre para reutilizar e adaptar isso ao seu projeto como preferir.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Parte do arquivo CÓDIGO DE CONDUTA para este módulo, com base no Convênio de Colaboradores.</i></p>

  


Certificar-se de aplicar o código de conduta é importante, pois mostra que você não apenas valoriza o código, mas respeita a influência que ele tem em sua comunidade. É importante tratar cada membro da comunidade com o devido respeito, cortesia e a importância que merecem. Caso ocorra uma infração ou um reincidente cometa violações sistemáticas, é melhor se referir ao seguinte [Guia de código aberto](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) para ver como aplicar o código de conduta.

  


### Tornando seu código citável <a name="Citation"></a>

Se você quiser tornar seu código passível de ser citado, desde o início você deve armazenar os metadados necessários para uma citação, criando um arquivo `[codemeta.json](https://codemeta.github.io)` ou um `[CITATION.cff](https: //citation-file-format.github.io)` arquivo. Ambos permitirão que as ferramentas em desenvolvimento atualmente criem automaticamente informações de citação, sem a necessidade de solicitar que você as digite em um formulário mais tarde.

Se você estiver interessado, o [cite.research-software.org](https://cite.research-software.org) fornece mais informações básicas sobre a citação de software na academia.

  


## Mantendo suas questões atualizadas <a name="Issues"></a>

Issues are not necessarily problems with a project, but also suggestions for improvement, things to develop in the future, and comments and feedback about the project to work through. They can be openly shared and discussed with contributors as needed, sort of like a forum.

If you are a project lead, it is important to maintain a list of issues that make it clear to contributors what aspects of the project need attention. It is also important to engage with as many issues as possible from others in a positive manner, to show that you take their contributions seriously.

Key elements for issues include:

* An informative title and description;
* Coloud-coded labels/tags to help categorise and filter;
* Milestones to associate issues with specific features or project phases;
* Assignees indicate who is responsible for working on an issue;
* Comments for providing feedback.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>The issue tracker for the Open Scholarship Strategy project</i></p>

  


Within issues it is possible to use @ mentions to notify other contirbutors about the issue, and to get the right people engaged in an effective manner. GitHub has an internal system of notifications, just like Facebook or Twitter, and can also send emails to people who are mentioned in the issue tracker. This can all be customised for individuals within the user settings.

  


## Checklist for launching your project <a name="Checklist"></a>

So now you are ready to launch your project, begin advertising it, and getting contributions! Before continuing, make sure that you have:

* [ ] Project has a memorable and informative name
* [ ] Project has a `LICENSE` file that is an exact copy of an Open Source license
* [ ] Complete documentation including a `README`, `CONTRIBUTING`, and `CODE_OF_CONDUCT` files
* [ ] Project has at least one clearly labelled issue
* [ ] Any code included at this stage is clearly structured and annotated

**CONGRATULATIONS!**

You have now launched an Open Source research project! Hopefully, from here on out, your work will act to benefit the wider community, forge new collaborations, and create new and fantastic opportunities for you all. Try and think about ways in which these skills can be applied to future projects, and how they might also have helped with some in the past.

From now on, it is all up to you! Some advice is to:

* Write clean code;
* Have a well-structured project;
* Make frequent commits with clean messages;
* Keep projects well-documented;
* Have clear contributing guidelines;
* Make use of the description and tag functions;
* Don't fork someone else's repository unless you intend to work on them;
* Make sure to contribute to other people's projects too.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)