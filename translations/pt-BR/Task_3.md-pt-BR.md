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

OK, mantenha sua respiração, vamos fazer uma pausa aqui apenas para aprender alguns comandos básicos do Git. Alguns dos principais comandos dos quais você se beneficiaria em aprender são:

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

Feche essa janela e a próxima. Vá para o seu projeto no GitHub, atualize e verifique se o arquivo `README` ainda está lá em toda a sua glória recém editada. Você deve visualizar a mensagem de submissão (commit) que criou ao lado do arquivo também.

  


**ETAPA OPCIONAL AVANÇADA/ESPETACULAR**

Muito bem, então você acabou de transferir alguns conteúdos para o seu primeiro repositório, fantástico! Agora vamos colocá-lo em prática para um projeto real. Como o que está participando agora. Vamos tentar o seguinte:

1. Vá para o repositório deste projeto no [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Bifurque o repositório utilizando o comando 'Fork 'em sua própria conta do GitHub. A URL para isso deve ser: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Dirija-se ao RStudio, vá para File (Arquivo) **> New Project (Novo Projeto)**, escolha *Version Control (Controle de Versão)*, selecione *Git* e cole o URL do repositório bifurcado localizado na sua cópia do repositório. Agora você tem sua própria cópia de uma versão deste módulo inteiro. Tudo pronto. Salve isso em algum lugar na sua máquina local.

4. Agora, você precisa dizer ao Git que existe uma versão diferente deste projeto. Abra o *Shell* e insira o comando: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. O que você acabou de fazer foi nomear o branch original aqui em `upstream`, apenas para manter as coisas simples por enquanto. Agora, crie um novo **branch** para documentar suas alterações para este independente do branch principal (main branch). Digite o comando: `git checkout -b proposed-changes master`

6. Você acabou de criar uma nova ramificação chamada `proposed-changes` onde agora é possível editar todo o conteúdo e arquivos para o deleite do seu coração. Espero que a estrutura deste projeto seja simples o suficiente para você navegar. Todos os arquivos brutos para este curso podem ser encontrados na pasta `content_development` , e esta é `Task_3.md`.

7. Se você rolar para a parte inferior do `Task_3.md`, você verá um lugar onde você pode editar em seu nome e afiliação. Adicione-os e, em seguida, passe pelo procedimento de confirmação (commit) detalhado acima. Se você notar algo mais que precise ser editado, sinta-se à vontade para adicioná-lo também!

8. Agora, você quer fazer com que as mudanças voltem para o brach original. Use o seguinte comando em seu *Shell*: `git push origin proposed-changes`

9. Volte para o GitHub e encontre seu fork aqui. Clique no botão verde e crie um pull request. Esta é essencialmente uma revisão para integrar as alterações feitas no branch original para este projeto do curso.

10.     Os proprietários encarregados do projeto do curso agora receberão uma notificação, revisarão e confirmarão se tudo saiu conforme o planejado! Vamos revisá-lo e, se tudo correr bem, seu nome aparecerá por toda a eternidade como alguém que completou essa tarefa avançada.
      

11.     Tome uma xícara de chá, café ou vinho para comemorar!
      

**PARABÉNS!**

Você acabou de integrar o Git com o R Studio e fez sua primeira alteração em um projeto de versão controlada. Sua vida nunca mais será a mesma e seu fluxo de trabalho de pesquisa provavelmente será mais rápido, ágil e mais colaborativo do que nunca. Boa sorte voltando ao Word.

O melhor é que isso não precisa ser usado apenas para código. Você pode usá-lo para texto simples, markdown, html e, bem, código R. As possibilidades são ilimitadas - o que você acabou de aprender é uma nova forma de gerenciamento de projeto abertamente colaborativo que funciona para uma enorme variedade de tarefas.

De agora em diante, tudo depende de você! Alguns conselhos são para:

* Faça commits frequentes. Trate o Git como seu filhote, pois requer atenção constante e especial. Apenas um tapinha na cabeça de vez em quando é suficiente para mantê-lo satisfeito, mas será mais feliz com manutenção sustentada.

* A melhor maneira de fazer isso é fazer um commit toda vez que você trabalha em um problema específico. Por exemplo, escrevendo um parágrafo, executando uma análise ou corrigindo um erro.

* Execute o comando 'Push' frequentemente Não deixe que os commits se acumulem, caso contrário, você corre mais risco de entrar em conflitos de mesclagem. Visto que estes podem representar o material dos pesadelos, não se esqueça de executar o comando 'Push' com frequência.

* Execute o comando 'Pull' frequentemente Se os outros estiverem trabalhando remotamente no mesmo projeto, você deverá manter-se atualizado com as alterações. Certifique-se de efetuar as alterações frequentemente no GitHub para ter certeza de que estão todos em sincronia.

* Experimente e explore! Esta tarefa realmente só racha a superfície, existem muitas funções, ferramentas e maneiras diferentes de usá-la. Realmente, cabe a você descobrir como usar essas informações para melhorar o seu fluxo de trabalho de pesquisa e, finalmente, colaborar em uma pesquisa melhor, mais aberta e confiável!

* Para saber mais sobre issues (questões e problemas), branches (ramificações), merge conflicts (conflitos de mesclagem), pull requests (solicitações de extração) e outros aspectos avançados do uso do Git e do RStudio, confira este [incrível guia](http://r-pkgs.had.co.nz/git.html) de Hadley Wickham.

  


**Sabe como esse conteúdo pode ser melhorado?**

Está na hora de fazer um teste com as suas novas habilidades no GitHub! Todo o desenvolvimento de conteúdo acontece principalmente [aqui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Se você tiver uma sugestão de melhoria do conteúdo, layout, ou qualquer outra coisa, você pode fazer isso, e, então se tornará automaticamente parte do conteúdo do curso após a verificação de um moderador!

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