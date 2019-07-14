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

So you should end up with a foundational file selection like this:

1. `LICENSE.md`
2. `README.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>The basic repository structure</i></p>

  


### Choosing a license <a name="License"></a>

Choosing an appropriate license is what will differentiate your Open Source repository from publicly available software. While you are not obliged to choose a license, doing so guarantees that others will be able to modify, share, re-use, and build upon your project within a legal framework.

To start with, you want to check [Choose A License](https://choosealicense.com/) to find a license that best suits your intentions for the repository.

The three primary ones to choose from are:

* **MIT License**: A permissive license that lets people do whatever they want with your code as long as they provide appropriate attribution to you, and do not hold you liable.
* **Apache License 2.0**: Similar permissions to the MIT License, but also provides an express grant of patent rights from contributors to users.
* **GNU General Public License (GPL) v3**: A [copyleft](https://en.wikipedia.org/wiki/Copyleft) license that requires anyone who redistributes your code, or a derivative work, to make the source available under the same terms as the original license; also provides an express grant of patent rights from contributors to users.

Thankfully, when you start a new repository on GitHub, you are given the option to select an existing license from a drop-down menu. You should always (with very few exceptions) use an existing license, since this is what potential users and contributors will see before they choose to use or contribute to your software.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Choosing an example license</i></p>

  


If they don't have one you want, you can add one you like manually. To do this, simply click 'Create new file' in the repository, and copy and paste an existing license text in. Name the file something like `LICENSE.txt` or `LICENSE.md` to make it clear, and keep it in the main repository folder (i.e., the root). Make sure to add a clean commit message, and you're done!

> **Helping hand**: This MOOC uses a different combination of licenses for code content and non-code content. Here you can find an example of the [MIT License](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) that we apply for all code and software generated as part of the MOOC production.

  


### Creating a README file <a name="Readme"></a>

When you initialise your new repository, there should be an option to do so with a `README` file. Just like Alice in Wonderland, these do exactly what they say - provide key information about the project. These are typically the first thing outside contributors will see when they come to your repository, so making them informative and welcoming is key.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Part of the README file for this module</i></p>

  


The file will originally be in markdown (`.md`) format. This is a lightweight markup language with a plain text format. To learn some basic markdown, see [this cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). But for now, we can just use plain text.

There are several things you will want to include in your `README` file:

* What is this project about and what does it do.
* Why should people care, and why is it useful.
* How can someone get started contributing to the project.
* Who can be contacted in case someone needs help.
* A link to the license, contributing guidelines, and code of conduct.
* A description of the project structure.
* Who is involved, and what are their roles.
* The current status of the project.

> **Pro-tip**: Later on as your project develops, you might want to add FAQs based on community feedback, or a tutorial to help users understand how your project works.

Remember that not everyone coming to your project will be an expert, or understand what it is you are doing and why. Having a well-documented `README` file will enhance the user experience for people with a range of prior knowledge.

When the `README` file is included in the root directory, GitHub will automatically display this on the homepage of your repository. This means it is the first thing people will often see, so make it count!

> **Helping hand**: Here, you can find the `README` file used for this [MOOC module](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). This includes information on the status, rationale, learning outcomes, development team, key documents, and license to help. You can copy and adapt this structure for your own projects as needed.

  


### Creating contributing guidelines <a name="Contributing"></a>

Contributing guidelines are designed to communicate to potential contributors a short guide on how to engage with your project and community. You want to make sure to be welcoming, and indicate that you are eager for participants to engage with your project. Whenever a participant opens a new pull request or creates a new issue, they will see a link to your contribution file.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Part of the `CONTRIBUTING` guidelines for this module</i></p>

  


Sticking with the all caps file names, the next step is to create a `CONTRIBUTING` file. Click 'Create new file', and make sure to save it in markdown format as before. This file will tell other users how they can engage with and participate in your project. This is the first step towards establishing a community around your project, so make it engaging, concise, and informative.

The `CONTRIBUTING` file should include information on:

* What sort of contributions you are looking for.
* How to suggest updates or new features.
* How to interact with the project using GitHub's functions (e.g., the pull request protocol).
* How to file a bug report or create an issue.
* The ultimate goal, vision, or roadmap for the project.
* How to contact those in charge of the project.
* Links to any external documentation or websites.

> **Pro-tip**: Consider starting off with a short thank you note for people taking the time to consider contributing - they have clicked on the file to learn more after all! If there are other methods of recognition that you have in mind, make sure to include them in here too.

Here, you are essentially trying to encourage people to volunteer their time to advance your project. Make sure to be welcoming and friendly, and be precise about how people can engage. When writing this, make sure to think about it from the user perspective - how can you make their life easier when submitting pull requests and opening issues to make the whole project run more smoothly.

> **Helping hand**: The [Contributing guidelines](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) for this MOOC module include some very specific things: an introduction to using Git and GitHub, tips for getting started, contact information, how to alter the content and repor issues, a link to the `README` file, and information on the preferred content and code styles. Feel free to copy and adapt this for your own project as needed.

  


### Creating a Code of Conduct <a name="Conduct"></a>

A code of conduct is important for setting the ground rules for expected behaviour and participation for project contributors, and is an easily referenced document for showing that your project team takes constructive dialogues seriously. Therefore, it is a critical element for creating and maintaining a healthy community that engages in a constructive and productive manner within a positive social atmosphere.

A code of conduct not only provides expectations of behaviour, but also describes who those expectations apply to, when they apply, what to do should a violation of the code occur, and what the action items for this will be. As such, points of contact need to be made clear in the code of conduct. Typically, this should be in a private way such as an email address.

> **Pro-tip**: In case a violation needs to be reported about the person who receives those reports, make sure to include an option to contact a secondary party.

To add a code of conduct, you can create your own from scratch by adding a new markdown file, or use existing templates such as the [Contributor Covenant](https://contributor-covenant.org/). Name your file `CODE_OF_CONDUCT.md`, and make sure it is visible in the `README` file.

> **Helping hand**: This MOOC also has a [Code of Conduct](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) based on the Contributor Covenant. As you can see, it includes information on expected standards of behaviour, responsibilities of those in the community, and enforcement of the CoC including contact details. Feel free again to re-use and adapt this to your project as you see fit.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Part of the CODE OF CONDUCT file for this module, based on the Contributor Covenant</i></p>

  


Making sure to enforce the code of conduct is important, as it shows that not only do you value the code, but you respect the influence that it has on your community. It is important to treat each member of the community with the respect, courtesy, and importance that they deserve. Should a violation occur, or a repeat offender makes consistent violations, it is best to refer to the [Open Source Guide](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) to see how to enforce the code of conduct.

  


### Making your code citable <a name="Citation"></a>

If you want to make your code citable from the start, you should store the metadata needed for a citation from the start, by creating a `[codemeta.json](https://codemeta.github.io)` file or a `[CITATION.cff](https://citation-file-format.github.io)` file. Both will allow tooling that is currently being developed to automatically create citation information, rather than asking you to type it in a form later.

If you're interested, [cite.research-software.org](https://cite.research-software.org) provides further background information about software citation in academia.

  


## Keeping your issues up to date <a name="Issues"></a>

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