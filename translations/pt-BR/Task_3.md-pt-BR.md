---
output:
  html_document: padrão
  pdf_document: padrão
---

# Tarefa 3: Como integrar o Git ao R Studio

Esta tarefa é projetada para estudantes e pesquisadores que desejam implementar um sistema de controle de versão dentro de um fluxo de trabalho padrão baseado em R. Isto pode ser aplicado a uma série de tarefas de desenvolvimento de software, análise de dados e gestão de projetos. Sua pesquisa futura irá agradecer-lhe a conveniência.

Não se esqueça de que você pode participar das discussões no nosso fórum aberto no [** canal do Slack **](https://osmooc.herokuapp.com/). Por favor, apresente-se no #módulo5opensource e conte-nos um pouco sobre quem você é, qual a sua formação e como chegou aqui!

Tempo estimado para conclusão: 30 minutos

Estimativa de economia de tempo depois de concluída: praticamente infinita

**NOTA** Uma versão guia de vídeo desta tarefa está disponível no [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

## Sumário

* [Como começar](#Começando) 
  * [Git](#Git)
  * [R Studio](#RStudio)
* [Primeiro passo: faça o download de todas as coisas](#um)
* [Segundo passo: Configure o Git dentro do RStudio](#dois)
* [Terceiro passo: Por que eu fiz isso?](#três)
* [Quarto passo: O casamento perfeito entre Git e R](#four)
* [Quinto passo: Obtendo conteúdo com conteúdo](#cinco)
* [Sexto passo: Um esforço corajoso](#seis)
* [Sétimo passo: FORÇA!](#sete)

## Primeiros Passos<a name="Getting_started"></a>

Parabéns por ter chegado tão longe! Se você está lendo isso, você sobreviveu aos pull requests, web-hooks, e, provavelmente pode até nos dizer o que significa o F em FOSS (*não* Frustração ...) Esperamos que você tenha superado qualquer ceticismo ou relutância em relação aos benefícios do GitHub e do Software de Código Aberto, ou seja, você está pronto para dar o próximo passo.

Se você completou [ as tarefas 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [ 2 ](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), nós também temos uma Tarefa BÔNUS</strong> para você, caso queira aperfeiçoar suas habilidades ainda mais.

Esta tarefa ensinará como integrar o software de controle de versão, Git, ao popular ambiente de codificação RStudio. E sim, é Git como em 'gif', não 'Jit', a pronúncia incorreta da palavra.

Se você é um daqueles pesquisadores que pensa que ter seu código espalhado por vários discos rígidos prestes a quebrar, Dropbox, Google Drive ou qualquer outro software não especializado, essa tarefa é exatamente para você. Se você já experimentou o processo mental de ter múltiplas versões 'finais' de um trabalho que circula entre diferentes coautores, isto também é para você.

Todos nós somos culpados por este tipo de situação de vez em quando, no entanto, existem maneiras melhores de fazer isso que serão úteis para o seu futuro e para aqueles que poderão se beneficiar do seu trabalho.

  


### Obtendo o Git <a name="Git"></a>

Então, o que é o Git e como ele é diferente do GitHub? O Git é um sistema de controle de versão, permite salvar e rastrear cópias do seu trabalho durante todo o processo de desenvolvimento. Também funciona com itens que não são de código, como este curso, e, a maioria dos quais foi escrito em markdown no RStudio e integrado a um fluxo de trabalho no Git / GitHub.

Isso é importante, uma vez que toda a investigação passa por mudanças e, frequentemente, queremos saber quais foram as alterações efetuadas. Você excluiu algum texto que agora considera importante? O controle de versão salvará isso para você. Seu código funcionou perfeitamente no passado, mas agora está completamente incompreensível? Controle de versão É uma ótima maneira de evitar esse estado caótico em que você tem várias cópias do mesmo arquivo, mas, sem uma convenção de nomenclatura de arquivos difícil e chata. `FINAL_Revisado_2.2_supervisor_edits_ver1.7_scream.txt` será uma coisa do passado.

O GitHub é a plataforma que permite que você compartilhe código de maneira fácil a partir do seu espaço de trabalho (por exemplo, laptop) para ser hospedado em um espaço online. Então, como a interface pública para o GitHub. As vantagens do Git/GitHub são:

1. Você consegue manter cópias de todo o seu trabalho ao longo do tempo;
2. Você pode comparar o trabalho através de diferentes cópias ao longo do tempo, o que ajuda a detectar falhas ou erros;
3. Outras pessoas podem colaborar abertamente com o seu trabalho;
4. Você tem uma cópia local e online do seu trabalho que permanece em sincronização;
5. É totalmente transparente quanto a quem fez uma contribuição, por que eles fizeram e quando; e
6. Você pode ter várias pessoas trabalhando no mesmo projeto de uma vez em paralelo.

Embora isso tenha sido projetado principalmente para o código-fonte, deve ser imediatamente óbvio como isso se torna uma ferramenta poderosa para praticamente todos os fluxos de trabalho de pesquisa.

  


### RStudio <a name="Rstudio"></a>

O RStudio é um ambiente de codificação popular para pesquisadores que usam a linguagem de programação estatística, R. Ele vem com um editor de texto, para que você não tenha que instalar outro e alternar entre eles. Inclui também uma interface gráfica de usuário (GUI) para Git e GitHub, que nós vamos usar aqui.

Não é bacana quando ferramentas de código aberto geniais se integram perfeitamente como essa? Isso deve ajudar a tornar seu uso diário do Git muito mais simples.

Se em algum momento você precisar instalar novos pacotes para R, simplesmente use o seguinte comando:

`install.packages ("PACKAGE NAME", dependencies = TRUE)`

Substituindo `PACKAGE NAME` pelo nome do pacote er. Alguns exemplos que você pode experimentar que talvez venham a ser úteis incluem: `knitr`, `devtools` ou `ggplot2`.

  


## Primeiro passo: faça o download de todas as coisas <a name="one"></a>

1. Você já deve ter uma conta no GitHub se você seguiu as tarefas anteriores. Se não, [inscreva-se aqui](https://github.com/). Repositórios ilimitados gratuitos para todos!
2. Baixe e instale a versão mais recente do [R](https://www.r-project.org/). Também disponível para [Mac](https://cloud.r-project.org/) e [Linux](https://cloud.r-project.org/bin/linux/).
3. Baixe e instale a versão mais recente do [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop). Oh, Ei, parece que é Código Aberto! Impressionante.
4. Baixe e instale a versão mais recente do [Git](https://gitforwindows.org/). **Certifique-se de selecionar “Usar Git do Prompt de Comando do Windows” durante a instalação.**

> **Dica**: Para atualizar todos os seus pacotes R em um só, simplesmente execute o seguinte código `update.packages(ask = FALSE, checkBuilt = TRUE)`

Por enquanto, basta escolher todas as opções padrão usuais para cada instalação. Dependendo de qual sistema operacional (por exemplo, Mac, Windows, Linux), isso pode ser diferente para cada um de vocês. Por enquanto, e para o restante desta tarefa, continuaremos fazendo as coisas da maneira mais fácil do Windows (mas também forneceremos algumas instruções para usar a linha de comando).

Para usuários Linux ou Debian, simplesmente use o seguinte comando para instalar o Git:

`sudo apt-get install git-core`

Para usuários de Mac, [acesse este link ](http://git-scm.com/download/mac)ou adquira um novo laptop com um sistema operacional diferente.

Se você quiser, também pode baixar a versão [local do GitHub](https://desktop.github.com/) e usá-lo através da GUI simples. Está disponível no Windows, no Mac e no Linux, e pode tornar sua vida um pouco mais fácil, especialmente se você quiser usar uma plataforma diferente para o RStudio.

> **Dica:** Ao instalar o Git, você verá a indicação da frase 'Use Git Bash as shell for Git projects?'. Portanto, esse é o local onde você pode usar a linha de comando para acessar o Git de fora do RStudio. É uma ferramenta poderosa. Tente os dois comandos a seguir para começar:

`git config --global user.name 'SEU NOME DE USUÁRIO'`   
`git config --global user.email 'SEU E-MAIL'`   


## Segundo passo: Configure o Git dentro do RStudio <a name="two"></a>

Certo, essa é a parte fácil. Em seguida, entre no RStudio e acesse as abas no topo, vá para **Tools > Global Options > Git/SVN**. O SVN é apenas outro sistema de controle de versão como o Git, mas não precisamos nos preocupar com isso aqui.

No lugar onde está escrito *Git executable*, adicione o caminho para o arquivo git.exe que você acabou de baixar na etapa anterior. Marque a caixa de seleção abaixo na opção **Enable version control interface for RStudio projects**. Agora, este projeto tem controle de versão vinculado a projetos futuros no RStudio, de forma a viabilizar uma dimensão adicional realmente poderosa ao trabalho colaborativo ou individual.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>A janela de opções globais dentro do RStudio</i></p>

  


Em seguida, pressione o botão nesta janela em que está escrito *Create RSA Key*, esta é uma chave privada que é usada para autenticação entre diferentes sistemas, e evita que você tenha que digitar sua senha várias vezes. Aqui, ele irá abrir uma nova janela com uma chave pública, que você deseja copiar para a área de transferência.

Vá para o GitHub, acesse as configurações do seu perfil e a guia *SSH e GPG keys*. Clique em *New SSH key*. Aqui, cole na chave do RStudio e renomeie como 'RStudio'.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>Dentro do GitHub onde você deseja entrar com a chave que acabou de gerar no RStudio</i></p>

  


Ok, agora mantenham-se firmes, vamos para a linha de comando. Não se preocupe se você nunca usou o shell antes, porque é bastante semelhante ao uso de R ou qualquer outro sistema de codificação. A principal diferença aqui é que em vez de chamar funções como em R, você chama comandos.

Então, volte ao RStudio, vá para **Tools > Shell**, e se abrirá uma janela de notificação de comando. Se você já utilizou o Git Bash anteriormente, então deve ter feito este passo. Digite os dois comandos a seguir:

`git config --global user.name 'SEU NOME DE USUÁRIO'`   
`git config --global user.email 'SEU E-MAIL'`   


Espero que não seja necessário substituir seu nome de usuário e seu e-mail do GitHub aqui. Você pode acessar isso a partir de qualquer ponto apenas encontrando o 'Shell' no Windows. Ou, se você clicar com o botão direito do mouse em qualquer pasta da sua área de trabalho que esteja ligada a um repositório GitHub, poderá abrir o Shell instantaneamente e fazer o Bash de forma instantânea.

O que esse estágio fez foi configurar o Git, que é um software que roda em sua área de trabalho, para o GitHub, que é um site de repositório.

Reinicie o R Studio. Uau, isso foi difícil. Próximo.

  


## Terceiro passo: Por que eu fiz isso? <a name="three"></a>

OK, mantenha sua respiração, vamos fazer uma pausa aqui apenas para aprender alguns comandos básicos do Git. Alguns dos principais comandos que você pode fazer para aprender são:

* **Add (Adicionar)**: É onde você envia os arquivos para a área de preparação antes de ser submetido.

* **Commit** É como 'salvar' seu trabalho criando uma nova versão ou cópia.

* **Push**: É assim que você envia os arquivos do seu projeto local para o repositório online.

* **Pull**: É assim que você obtém os arquivos do seu repositório online para o seu projeto local.

Volte ao RStudio, digite o seguinte no *Terminal*, ou abrindo um novo Shell:

`git add.`

Na verdade, ele não fará nada por enquanto, mas no futuro adicionará todos os arquivos em seu diretório de trabalho atual (isso é o que o `` faz) para a preparação e deixar tudo pronto para executar o comando commit.

  


## Quarto passo: O casamento perfeito entre Git e R <a name="four"></a>

Agora, na Tarefa 1, você deve ter aprendido a construir seu primeiro repositório do GitHub. Se você não fez isso, podemos esperar aqui enquanto você faz isso. Se você já tiver, ou tem um repositório GitHub existente, podemos continuar.

Portanto, você deve ter um repositório no GitHub, completo com um arquivo `README` , um arquivo `LICENSE` e alguns outros arquivos que fazem parte do projeto.

O que vamos fazer agora é integrar esse repositório com o Git. Mantenha-se firme agora.

1. Primeiramente, vá para **Project (Projeto)> Create Project (Criar Projeto)> Version Control (Controle de Versão)> Git**.
2. Volte ao GitHub, você deve procurar onde há uma URL https://. Esse é o link para o seu repositório, e ele dá a opção de cloná-lo em sua área de trabalho. Por enquanto, basta copiar esse link, voltar para o RStudio e colá-lo no 'URL do repositório' (Repository URL), conforme indicado.
3. Dê ao projeto um nome de diretório, como teste, Jim ou o que você quiser.
4. Em seguida, procure o local em sua área de trabalho onde você deseja que este projeto resida, seu subdiretório.
5. Clique em 'Criar Projeto' (Create Project) e deixe a mágica acontecer!

O que você acabou de fazer foi dizer ao RStudio para associar um novo projeto em R com um repositório específico no GitHub.

## **Passo 4: Alternativo**

Se você ainda não construiu seu primeiro repositório no GitHub, podemos fazer algo um pouco diferente aqui. No RStudio, clique em *New project* e, em seguida, em *New Directory*. Atribua o nome que quiser e altere o diretório conforme necessário, certifique-se de marcar a opção *Create a git repository (Criar um repositório git)* e, em seguida, clique em *Create Project*. Isso cria um arquivo `.Rproj` , que você pode gerenciar da maneira usual no RStudio, incluindo a adição de `arquivos README.md`e `LICENSE.md` como discutido na Tarefa 1.

## Quinto passo: Obtendo conteúdo com conteúdo <a name="five"></a>

Lembra-se de que `arquivos README` foram criados há algum tempo? Bem, agora é a hora de escrever isso. Lembrando-nos da Tarefa 1, havia algumas coisas específicas que dissemos fazer parte de um bom arquivo `README`. Você se lembra de quais elementos eram? Apenas para refrescar sua memória, são:

* Sobre o que é este projeto e o que ele faz.
* Por que as pessoas deveriam se importar e por que isso é útil.
* Como alguém pode começar a contribuir com o projeto.
* Quem pode ser contatado no caso de alguém precisar de ajuda.
* Um link para a licença, diretrizes de contribuição e código de conduta.
* Uma descrição da estrutura do projeto.
* Quem está envolvido e quais são os papéis desempenhados.
* O status atual do projeto.

Então, no RStudio, abra esse arquivo e adicione apenas algumas informações em seu projeto. Se você está fazendo isso para um projeto real, tente torná-lo útil. Se você está apenas manipulando neste momento, pode adicionar o que quiser.

Lembre-se de que seu arquivo `README` está no formato markdown (.md). Para aprender o básico em markdown, veja [este folheto](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Captura de tela do que este módulo parece em markdown, durante o desenvolvimento. Meta.</i></p>

  


## Sexto passo: Um esforço corajoso <a name="six"></a>

OK, agora você deve ter um arquivo `README` bem editado. Agora vamos fazer um "commit" disso para o projeto usando o Git. Isso é basicamente o equivalente a salvar essa versão do seu projeto, com um registro de quais alterações foram feitas. Os commits sucessivos produzem um histórico que pode ser examinado posteriormente, permitindo que você trabalhe com confiança.

Existem algumas maneiras de fazer isso.

1. Vá para **Tools (Ferramentas)> Version Control (Controle de Versão)> Commit**
2. No painel de ambiente do RStudio, deve haver uma nova guia 'Git'. Prático
3. Em seu painel de console, deve haver agora um novo 'Terminal', no qual você pode executar as linhas de comando do Git.

Vamos apenas ficar com a segunda opção por enquanto. Este painel Git mostra quais arquivos foram alterados e inclui botões para os comandos Git mais importantes que vimos anteriormente.

Selecione o arquivo `README` na janela do Git, que deve aparecer automaticamente se você tiver feito qualquer edição. Isso adiciona esse arquivo à área de "teste", que é como o espaço de pré-salvamento para o seu trabalho. Clique em "Commit" e uma nova janela deve aparecer.

Aqui, você tem a chance de revisar suas alterações e escrever uma boa mensagem de confirmação. Digite algo breve, mas informativo sobre as alterações que você fez nesta versão ou uma imagem de captura de tela do seu trabalho. Você vai querer que essa informação seja suficiente para que, caso você ou outra pessoa olhe para trás, saiba por que você fez esse commit e as mudanças associadas a ele. Estes são como redes de segurança para o seu projeto, caso você precise voltar por algum motivo.

> **Dica**: Aqui, você verá uma lista de todas as alterações feitas desde o último commit. As linhas removidas mais antigas estão em vermelho e as linhas recém-adicionadas estão em verde. Verifique novamente para garantir que as edições feitas são aquelas que você pretendia fazer. Isso é realmente útil para identificar erros de digitação, edições erradas e quaisquer outros pequenos erros que você possa ter introduzido acidentalmente. Segurança Primeiro

**Nota** Se você é daltônico e não pode ver quais linhas foram adicionadas ou removidas, você pode usar os números de linha nas duas colunas à esquerda da janela como um guia. Aqui, o número na primeira coluna identifica a versão mais antiga e o número na segunda coluna identifica a nova versão.

Agora, quando você clicar em "Commit", outra janela será exibida, informando quantos arquivos você alterou e o número de linhas dentro desse arquivo que você alterou. Feche essa janelinha.

  


## Sétimo passo: FORÇA! <a name="seven"></a>

Clique no botão *Push* no canto superior direito da nova janela. Uma nova janela irá aparecer agora. Isto irá sincronizar os arquivos alterados no seu repositório local com o arquivo `README` para a versão online do projeto no GitHub.

Para fazer isso no Shell, use o seguinte comando:

`git push -u origin master`

Algumas vezes aqui será solicitado que você adicione seu nome de usuário e senha do GitHub, o que deve ser feito se solicitado.

Feche essa janela e a próxima. Go to your project on GitHub, refresh, and check that the `README` file is still there in all its newly edited glory. You should see the commit message you made next to the file too.

  


**ETAPA OPCIONAL AVANÇADA/ESPETACULAR**

Alright, so you just pushed some content to your first repo, awesome! Now let's put it into practice for a real project. Like, the one you are participating in right now. Let's try this out:

1. Go to the repository for this project on [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Fork the repository to your own GitHub account. The URL for this should be: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Head into RStudio, go to **File > New Project**, choose *Version Control*, select *Git*, and then paste the forked repository URL found in your copy of the repository. You now have your own versioned copy of this whole module. Neat. Save this somewhere on your local machine.

4. Now, you need to tell Git that a different version of this project exists. Open up the *Shell*, and enter the command: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. What you just did was name the original branch here `upstream`, just to keep things simple for now. Now, create a new **branch** to document your changes to this independent of the main branch. Enter the command: `git checkout -b proposed-changes master`

6. You just created a new branch called `proposed-changes` where you can now edit all of the content and files to your heart's delight. Hopefully, the structure of this project is simple enough for you to navigate around. All of the raw files for the MOOC can be found in the `content_development` folder, and this is `Task_3.md`.

7. If you scroll to the bottom of `Task_3.md`, you should see a place where you can edit in your name and affiliation. Add these in, and then go through the commit procedure detailed above. If you see anything else that needs editing too, feel free to add them in too!

8. Now, you want to push the changes back to the original branch. Use the following command in your *Shell*: `git push origin proposed-changes`

9. Go back to GitHub and find your fork here. Click the little green button, and create a pull request. This is essentially a review to integrate the changes made into the original branch for this MOOC project.

10.     The owners in charge of the MOOC project will now get a notification of this, review it, and confirm it if everything went to plan! We will review it, and if it all went okay, your name will now appear for all eternity as someone who completed this advanced task.
      

11.     Have a cup of tea, coffee, or wine to celebrate!
      

**PARABÉNS!**

You just integrated Git with R Studio, and made your first change to a version controlled project. Your life will now never be the same, and your research workflow will probably be more rapid, agile, and collaborative than ever. Good luck going back to Word.

The great thing is that this doesn't have to just be used for code. You can use it for plain text, markdown, html, and, well, R code. The possibilities are limitless - what you have just learned is a new form of openly collaborative project management that works for an enormous range of tasks.

From now on, it is all up to you! Some advice is to:

* Make frequent commits. Treat Git like your puppy, in that it requires constant and special attention. Just a pat on the head every now and then is enough to keep it satisfied, but it'll be happiest with sustained servicing.

* The best way to do this is to make a commit each time you work on a specific problem. For example, writing a paragraph, running an analysis, or fixing a bug.

* Push often. Don't let those commits build up, otherwise you run more risk of getting into merge conflicts. Seeing as these can be the stuff of nightmares, just make sure to push often.

* Pull often. If others are working remotely on the same project, you will want to stay up to date with their changes. Make sure to frequently pull in their changes from GitHub to make sure you are all in sync.

* Experiment and explore! This task really only scratches the surface, and there are many different functions, tools, and ways this can be used. Really, it is up to you to find out how to use this information to improve your research workflow, and ultimately collaborate on better, more open and reliable research!

* To learn more about issues, branches, merge conflicts, pull requests, and other advanced aspects of using Git and RStudio, check out this [awesome guide](http://r-pkgs.had.co.nz/git.html) by Hadley Wickham.

  


**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

## Lista de participantes que completaram a versão AVANÇADA desta tarefa

* Brendan Palmer, CRF-C, Universidade College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, Universidade de Leicester 
* Eric D. Wilkey, Western University, Canadá
* José-Raúl Canay-Pazos, Universidade de Santiago de Compostela, Espanha
* Encarnación Martínez Álvarez, Espanha
* Alberto Albz Marocchino, Itália
* Iratxe Rubio, Centro Basco para Mudança Climática BC3
* Gabriele Orlandi, Escola de Estudos Avançados em Ciências Sociais de Paris (EHESS), França
* Hande Sodacı, Turquia
* Luke W. Johnston, Universidade de Aarhus, Dinamarca
* Philippe Joly, WZB e HU-Berlim
* Paul Griffiths, NCAS e U. Cambridge
* Harin Lee, Goldsmiths, Universidade de Londres
* Luis Camacho, Universidade Católica, Perú
* Tom Cridford, Academia Imperial Londres
* Nithiya Streethran, Universidade de Stavanger 

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)