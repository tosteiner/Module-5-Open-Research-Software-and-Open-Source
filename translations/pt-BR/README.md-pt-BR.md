# Desenvolvimento de conteúdo do módulo 5

Estes são os principais arquivos de desenvolvimento de conteúdo para este módulo MOOC.

** STATUS ** : ** AO VIVO! Este módulo está online e pronto para ser lançado através de [ Eliademy ](https://eliademy.com/catalog/oer/module-5-open-research-software-and-open-source.html) . **

A terceira versão deste módulo agora também está pronta e foi publicada no Zenodo:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1434288.svg)](https://doi.org/10.5281/zenodo.1434288) e um vídeo introdutório também foi publicado [ ](https://www.youtube.com/watch?v=1fwGliIyAZs) .

Para citar este trabalho, por favor, use a seguinte referência:

Jon Tennant; Simon Worthington; Tania Allard; Philipp Zumstein; Daniel S. Katz; Alexander Morley; Stephan Druskat; Julien Colomb; Arfon Smith; Ina Smith; Tobias Steiner; Rutger Vos; Konrad Förstner; Heidi Seibold; Alessandro Sarretta; Abigail Cabunoc Mayes. (2018, 4 de dezembro). OpenScienceMOOC / Module-5-Open-Research-Software-e-Open-Source: Terceira versão (Versão 3.0.0). Zenodo. [ http://doi.org/10.5281/zenodo.1937708 ](http://doi.org/10.5281/zenodo.1937708) .

Por favor, consulte as [Contribuindo diretrizes](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) antes de fazer alterações aqui.

Qualquer um pode se juntar ao nosso [canal aberto no Slack](https://osmooc.herokuapp.com/) e [a equipe no GitHub](https://open-science-mooc-invite.herokuapp.com/) para todo o projeto MOOC.

## Conteúdo principal

Estes são os arquivos do conteúdo do rascunho. O conteúdo é totalmente acessível e pode ser usado para fins de aprendizado, individualmente ou em grupo, e pode ser compartilhado e reutilizado como você desejar. No entanto, eles ainda não foram integrados em uma plataforma formal do MOOC. No momento, eles estão sendo escritos no formato markdown e depois são convertidos usando a ferramenta [notedown](https://github.com/aaren/notedown) para transformá-los no formato iPython notebook. Versões PDF e HTML são criadas usando [pandoc](https://pandoc.org/demos.html) e o [markdown para o pacote PDF](https://atom.io/packages/markdown-pdf) para [Atom](https://atom.io/).

Para o notedown:

1. Certifique-se de que você está trabalhando no Linux ou no Debian
2. Altere o diretório de trabalho: por exemplo, ` cd / mnt / c / users / pc / desktop / `
3. Instale o notedown: `pip install notedown`
4. Converta os arquivos: ` remarkown input.md > output.ipynb `

**IMPORTANTE** Por favor, edite os arquivos **markdown** e não os arquivos iPython/HTML. Esses serão periodicamente convertidos e sincronizados conforme necessário.

### No formato markdown

- [**CONTENTE**](MAIN.md) - O conteúdo principal deste Módulo. ([Vídeo do YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM))
- [**TASK 1**](Task_1.md) - Como configurar seu primeiro repositório no GitHub. ([Vídeo do YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&t=4s))
- [** TAREFA 2 **](Task_2.md) - Como tornar seu código passível de citação usando o GitHub e o Zenodo. ([Vídeo do YouTube](https://www.youtube.com/watch?v=pjsbBQYOOaE&t=4s))
- [** TAREFA 3 **](Task_3.md) - Como integrar o Git com o RStudio. ([Vídeo do YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA))

### No formato do iPython notebook

Nota: Estes são melhor visualizados no Juypter para funcionalidade completa, ao contrário do visualizador do GitHub.

- [** CONTEÚDO PRINCIPAL **](MAIN.ipynb) (clique [ aqui ](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.ipynb) ver)
- [** TAREFA 1 **](Task_1.ipynb) (clique [ aqui ](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.ipynb) ver)
- [** TAREFA 2 **](Task_2.ipynb) (clique [ aqui ](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.ipynb) ver)
- [** TAREFA 3 **](Task_3.ipynb) (clique [ aqui ](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.ipynb) ver)

## Em formato PDF

- [**CONTEÚDO PRINCIPAL**](MAIN.pdf)
- [**TAREFA 1**](Task_1.pdf)
- [**TAREFA 2**](Task_2.pdf)
- [**TAREFA 3**](Task_3.pdf)

## Formato HTML

- [**CONTEÚDO PRINCIPAL**](MAIN.html)
- [**TAREFA 1**](Task_1.html)
- [**TAREFA 2**](Task_2.html)
- [**TAREFA 3**](Task_3.html)

## Arquivos de produção

1. [Plano](01-plan.md) 
2. [Design](02-design.md)
3. [Gravação e edição](03-recording.md)
4. [Revisão interna](04-quizzes.md)

## Principais recursos do kit de ferramentas de produção [ ](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/tree/master/production_toolkit)

- [Protocolo de design do módulo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/MODULE_DESIGN_PROTOCOL.md)
- [Modelo de planejamento de MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/MOOC_planning_template.md)
- [Modelo de script](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Script_template.md)
- [Protocolo de gerenciamento de vídeo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Video_management_protocol.md)
- [Escrevendo um script](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Writing_a_script.md)