---
output:
  html_document: padrão
  pdf_document: padrão
---

# Módulo 5: Software de Pesquisa e Código-fonte aberto

## Sumário

- [Introdução](#Introduction)
- [O que é um Software de código-fonte aberto](#What_OSS)
- [Princípios do Software de Código-fonte aberto](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Plataformas e ferramentas de software com código-fonte aberto existentes](#Platforms)
- [Software de código aberto usado em pesquisa](#Research)
- [Começando com OSS - FAQ](#FAQ)
- [Fazendo um bom software para reutilização](#Reuse)
- [Licenças de código aberto](#Licensing)
- [Citação de software](#Citation)
- [Usando o GitHub e o Zenodo](#GitHub_Zenodo)
- [Colaborando através do código aberto](#Collaborating)
- [Onde ir a partir daqui](#Future_OSS)

**OBSERVAÇÃO** Há uma versão em áudio disponível no [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) e uma no [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## Introdução<a name="Introduction"></a>

Bem-vindo ao **Módulo 5** do curso Ciência Aberta: ** Software de Pesquisa e código-fonte aberto **.

Este módulo tem sido desenvolvido [ em aberta ](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) colaboração por uma equipe internacional de [ aficionados em código aberto](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Todos os conteúdos aqui apresentados foram desenvolvidos de forma aberta, por meio de feedback interativo e colaboração da comunidade em geral. Compreende uma série de vídeos, infográficos, leituras baseadas em texto e tarefas práticas para que você se envolva profundamente com o tema.

Não se esqueça de que você pode participar das discussões no nosso fórum aberto no [** canal do Slack **](https://osmooc.herokuapp.com/). Por favor, apresente-se no #module5opensource e conte-nos um pouco sobre quem você é, qual a sua formação e como chegou aqui!

### Para quem é este módulo?

Este módulo é projetado principalmente para pesquisadores computacionais no nível de graduação e pós-graduação, bem como cientistas de dados iniciantes e qualquer outro pesquisador que use código analítico ou software. Em um ambiente de pesquisa moderno, isso abrange praticamente qualquer pessoa que usa um computador para o trabalho.

> "Um artigo sobre resultados computacionais é publicidade, não educacional. O conhecimento real é o ambiente de software completo, códigos e dados, que produziu o resultado." - J. Buckheit e DL Donoho, 1995.

O software e a tecnologia sustentam grande parte da pesquisa moderna, que agora é quase inevitavelmente computacional de uma forma ou de outra - mecanismos de pesquisa, plataformas de redes sociais, software analítico e publicação digital. Com isso, há uma demanda cada vez maior por softwares de código aberto mais sofisticados, combinados com uma crescente disposição dos pesquisadores em colaborar abertamente em novas ferramentas.

O poder do Código Aberto está em reduzir as barreiras à colaboração e adoção, permitindo assim que as ideias e a tecnologia se espalhem mais rapidamente. Este módulo apresentará as ferramentas necessárias para transformar o software em algo que possa ser acessado abertamente e reutilizado por outros.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Imagem de Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Objetivos específicos de aprendizagem para este Módulo**:

1. Aprender as características do software aberto; compreender os **argumentos éticos, legais, econômicos e de impacto na pesquisa, a favor e contra o Software de Código Aberto**, e compreender melhor os requisitos de qualidade do código aberto.

2. Ser capaz de transformar código feito para uso pessoal em código aberto acessível para todos.

3. Usar software (ferramentas) que utiliza conteúdo aberto e incentiva uma colaboração mais ampla.

  


## O que é um Software de código-fonte aberto <a name="What_OSS"></a>

Praticamente todos os fluxos de trabalho de pesquisa científica moderna dependem de uma série de ferramentas de software, seja operando em diferentes conjuntos de dados, com diferentes parâmetros, e aplicados iterativamente de várias maneiras (Ciência dos Dados) ou operando em diferentes entradas e usando modelos e métodos para prever algum estado de saída (Ciência Computacional). Open Source Software (OSS) / Programa de Código Aberto é um software de computador no qual o código fonte está completamente disponível sob uma licença específica que permite a outros usuários acessar, visualizar, modificar e redistribuir esse código para qualquer finalidade. Uma vez que o OSS requer tal licença, geralmente esta é gratuita por padrão. Este licenciamento explícito é também o que distingue o OSS do software livre. A reutilização de OSS para análise, simulação e visualização para investigação é normalmente mais fácil e flexível do que os programas informáticos proprietários. Muitas vezes, quer saibamos quer não, já estamos utilizando o OSS como parte de nossos próprios fluxos de trabalho na pesquisa.

O OSS enquadra-se no esquema mais amplo da Ciência Aberta, uma vez que ajuda a transformar todo o ambiente de pesquisa, incluindo o software que produziu os resultados das investigações, plenamente acessível e reutilizável. Como tal, forma um componente necessário para as melhores práticas ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) e replicabilidade e reprodutibilidade da pesquisa (tanto pessoalmente como por terceiros), assim como outros componentes, como o compartilhamento de dados ([Stodden, 2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)).

Em alguns casos, o compartilhamento de código fonte pode até mesmo ser uma condição para a aceitação de manuscritos de pesquisa associados. ([Shamir et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). É também geralmente reconhecido como um fator de maior impacto na pesquisa. ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Algumas das principais vantagens para os desenvolvedores incluem:

- Aumento da confiança e empoderamento dos desenvolvedores;

- Redução dos custos dos serviços e marketing;

- Crescimento da imagem de marca dos serviços e produtos;

- Produção de software de alta qualidade com menor custo;

- Flexibilidade e inovação rápida;

- Customização e integração modular;

- Maior confiabilidade e independência; e

- Baseado em padrões abertos disponíveis para todos.

Neste sentido, as principais vantagens para os pesquisadores (usuários) incluem **custos menores**, **maior transparência**, **mais segurança e estabilidade**, **sem bloqueio do fornecedor e com maior controle do usuário** e **maior qualidade em geral**. Além disso, o compartilhamento do OSS permite aos pesquisadores receber o crédito por seus esforços, por exemplo, por meio da citação direta de um software. [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Os OSS mais usados incluem o navegador </a> de internet [ Mozilla Firefox ](https://www.mozilla.org/en-US/firefox/) e e o pacote completo [ do LibreOffice](https://www.libreoffice.org/). O LibreOffice é semelhante ao popular Microsoft Office, incluindo um processador de texto, um gerenciador de planilhas e um software de apresentação de slides, porém é completamente gratuito e de código-fonte aberto.

Para alguns, o Movimento Open Source Software (OSS) representa um contra-movimento ao neoliberalismo e à privatização, desafiando os regulamentos e normas na construção e reutilização da informação, além de uma potencial transformação do capitalismo moderno através da disponibilização abundante de software com o mínimo esforço. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Princípios do Software de Código-fonte aberto <a name="Principles"></a>

A [iniciativa de Código-fonte aberto](https://opensource.org/) é um dos pioneiros do OSS e oferece a seguinte [definição](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Não se preocupe, você não precisa memorizar tudo isso, no entanto, é bom saber de onde vem o Open Source Software (OSS) / Software de código-fonte aberto.*

- **Redistribuição gratuita**: A licença não deve restringir qualquer parte da venda ou cessão do software como componente de uma distribuição agregada que contenha programas de várias fontes diferentes. A licença não deve exigir royalties ou outras taxas pela venda.
    
    - **Código Fonte**: O programa deve incluir código-fonte, bem como permitir a sua distribuição na forma compilada. Quando um produto não é distribuído com código fonte, deve haver um processo de obtenção do mesmo por um custo de reprodução não superior a um valor razoável, preferencialmente através da Internet, sem encargos. O código fonte deve ser a forma principal pela qual um programador pode modificar o software. Código-fonte ocultado deliberadamente não é permitido. Formas intermediárias como a saída de um pré-processador ou tradutor não são permitidas.
    
    - **Obras Derivadas**: A licença deve permitir modificações e a criação de obras derivadas, assim como deve permitir a sua distribuição nos mesmos termos que a licença do software original.
    
    - **Integridade do Código Fonte do Autor**: A licença pode restringir que o código fonte seja distribuído na forma modificada somente se a licença permitir a distribuição de "arquivos patch", ou seja, "arquivos de correção", contendo o código fonte para fins de modificação do programa no momento da compilação. A licença deve permitir explicitamente a distribuição de software construído a partir do código-fonte modificado. A licença pode exigir que as obras derivadas tenham um nome ou número de versão diferente do software original.
    
    - **Sem discriminação contra pessoas ou grupos**: A licença não deve discriminar nenhuma pessoa ou grupo de pessoas.
    
    - **Sem discriminação contra as áreas de atuação**: A licença não deve restringir ninguém de fazer uso do programa em um campo específico de atuação. Por exemplo, não pode restringir o programa de ser usado em qualquer tipo de negócio, ou de ser usado para alguma pesquisa genética.
    
    - **Distribuição da Licença**: Os direitos associados ao programa devem se aplicar a todos àqueles para quem o programa é redistribuído sem a necessidade de execução de uma licença adicional por essas partes.
    
    - **A Licença não deve ser específica para um produto**: Os direitos associados ao programa não devem depender do fato de o programa ser parte de uma distribuição de software específica. Se o programa for extraído dessa distribuição e usado ou distribuído dentro dos termos da licença do programa, todas as partes a quem o programa é redistribuído devem ter os mesmos direitos que aqueles que são garantidos em conjunto com a distribuição de software original.
    
    - **A Licença não deve restringir outro software**: A licença não deve impor restrições a outro software que seja distribuído juntamente com o software licenciado. Por exemplo, a licença não deve exigir que todos os outros programas distribuídos pelo mesmo meio sejam programas de código aberto.
    
    - **A Licença deve ser neutra em termos de tecnologia**: Nenhuma disposição da licença pode ser baseada em qualquer tecnologia individual ou estilo de interface.

Tudo isto pode ser um pouco complexo para memorizar. No entanto, pode ser resumido como *uma forma de tornar o software tão reutilizável quanto possível para trabalhos futuros, estando também disponível gratuitamente. *.

  


## Uma checklist do código-fonte aberto

Há várias plataformas e ferramentas existentes que apoiam o programa de código-fonte aberto e a colaboração. O [Manual de Treinamento em Ciência Aberta](https://open-science-training-handbook.gitbook.io/book/) fornece uma checklist para avaliar a "abertura" do software de pesquisa existente, com base na Definição de Código Aberto acima:

- [] O software está disponível para download e instalação?

- [] O software pode ser facilmente instalado em diferentes plataformas?

- [] O software impõe condições de uso?

- [] O código-fonte está disponível para inspeção?

- [] O histórico completo do código-fonte está disponível para verificação por meio de um histórico de versões disponível publicamente?

- Há descrição adequada das dependências do programa (hardware e software)? Essas dependências exigem um esforço mínimo razoável para a sua obtenção e uso?

Verifique, confira, confirme, e está feito! Simples assim.

  


## A comunidade de código-fonte aberto e sua governança <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Ambos têm diferentes ideologias baseadas nas liberdades dos usuários e nas aplicações práticas do software. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Para projetos individuais

A typical open source project has the following types of formal roles:

- **Autor**: É a pessoa que criou o projeto
- **Proprietário**: A/s pessoa/s que possui propriedade administrativa sobre a organização ou o repositório 
- **Mantenedores**: Colaboradores responsáveis por conduzir a visão e gerenciar os aspectos organizacionais do projeto. (Eles também podem ser autores ou proprietários do projeto.)
- **Colaboradores**: O usuário que já contribuiu para o projeto.
- **Membros da Comunidade**: Pessoas que trabalham no projeto. Eles podem ser ativos em conversas, criar novas questões para discussão ou expressar sua opinião sobre as futuras melhorias do projeto.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Plataformas e ferramentas de software com código-fonte aberto existentes <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub<a name="GitHub"></a>

> Você sabia que este projeto inteiro foi construído como um esforço comunitário aberto e colaborativo no [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software de código aberto usado em pesquisa <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Cada vez mais, os algoritmos implementados no software de análise são parte integrante dos métodos descritos nas publicações acadêmicas. Como tal, está completamente em conflito com a rigorosa revisão por pares se estas implementações de algoritmos forem restritas a pessoas de fora.

- A colaboração científica abrange muitas vezes múltiplas instituições e redes de pesquisa distribuídas em que o sigilo e a hierarquia de comando não são mantidos de uma forma que seja "necessária" para o desenvolvimento de fontes fechadas.

- Muitas análises computacionais são executadas em ambientes virtualizados (como infraestruturas institucionais, nacionais ou internacionais na 'nuvem') e hospedadas em servidores multiusuários. Softwares comerciais de código fechado, muitas vezes, não permitem esse uso.

- O desenvolvimento de programas de código-fonte aberto/Open Source Software (OSS) geralmente dependem de voluntários. Em um tempo de restrições orçamentárias para a pesquisa científica, essa é uma clara vantagem.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Começando com OSS - FAQ <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Fechado                                                                                                 | Aberto                                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                     |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| MS Office                                                                                               | LibreOffice                                                                                                                                                       |
| Mathematica                                                                                             | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Fazendo um bom software para reutilização <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Você sabia ...** O termo `README` é algumas vezes atribuído à famosa cena de Alice no País das Maravilhas, de Lewis Carroll, em que Alice enfrenta petiscos mágicos rotulados com a mensagem "Coma-me" e "Beba-me". Potente.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 regras simples para pesquisa computacional reprodutível

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Para cada resultado, acompanhe como foi produzido.
2. Evite etapas manuais de manipulação de dados.
3. Arquive as versões exatas de todos os programas externos usados.
4. Controle as versões de todos os scripts personalizados.
5. Registre todos os resultados intermediários, quando possível, em formatos padronizados.
6. Para análises que incluem aleatoriedade, anote as características aleatórias de cada uma das seeds.
7. Sempre armazene os dados brutos por trás dos gráficos.
8. Gerar saída de análise hierárquica, permitindo que camadas mais detalhadas sejam inspecionadas.
9. Conecte declarações textuais aos respectivos resultados.
10. Forneça acesso público a scripts, execuções e resultados.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Licenças de código aberto <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), ou
- [Licença Pública Geral GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Explicitamente*, em que a contribuição individual tem uma licença claramente indicada, independente do projeto principal; ou
2. *Implicitamente*, em que a contribuição se enquadra no código de licenciamento original do projeto principal.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Citação de software <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- O(s) nome do(s) autor(es),
- Título do software,
- Número da versão
- O identificador/localizador único (DOI ou URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Importância**: O software deve ser considerado um produto legítimo e citável da pesquisa. As citações de software devem ter a mesma importância no registro acadêmico que as citações de outros produtos de pesquisa, como publicações e dados; eles devem ser incluídos nos metadados do trabalho de citação, por exemplo, na lista de referência de um artigo de periódico, e não devem ser omitidos ou separados. O software deve ser citado da mesma forma que qualquer outro produto de pesquisa, como um artigo ou um livro, ou seja, os autores devem citar o conjunto apropriado de produtos de software, da mesma forma que citam o conjunto de documentos apropriado.

- **Crédito e atribuição**: As citações de software devem facilitar a concessão de crédito acadêmico e a atribuição normativa e legal a todos os colaboradores do software, reconhecendo que um estilo único ou mecanismo de atribuição pode não ser aplicável a todos os softwares.

- **Identificação única**: Uma citação de software deve incluir um método de identificação que seja acionável por máquina, globalmente exclusivo, interoperável e reconhecido por pelo menos uma comunidade dos especialistas de domínio correspondentes e, de preferência, por pesquisadores públicos em geral.

- **Persistência**: Identificadores únicos e metadados que descrevem o software e sua disposição devem persistir - mesmo para além da duração do software que descrevem.

- **Acessibilidade**: Citações de software devem facilitar o acesso ao próprio software e aos seus metadados, documentação, dados e outros materiais associados necessários para que humanos e máquinas façam uso informado do software referenciado.

- **Especificidade**: As citações de software devem facilitar a identificação e o acesso à versão específica do software que foi usada. A identificação do software deve ser tão específica quanto necessária, como o uso de números de versão, números de revisão ou variantes, como plataformas.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Usando o GitHub e o Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **Você sabia ...** Todo o conteúdo produzido para este curso está disponível como parte de uma comunidade no [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Colaborando e contribuindo através da Código Aberto <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Onde ir a partir daqui <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Você agora será capaz de definir as características do software de código aberto, além de alguns dos argumentos éticos, legais, econômicos e de impacto na pesquisa a favor e contra ele.

2. Com base nos padrões da comunidade, você poderá descrever os requisitos de qualidade de compartilhamento e reutilização de código aberto.

3. Agora, você poderá usar uma série de ferramentas de pesquisa que utilizam o programa de código-fonte aberto.

4. Agora você será capaz de transformar o código desenvolvido para seu uso pessoal em código acessível e reutilizável para outros usuários.

5. Os desenvolvedores de software serão capazes de tornar seu software passível de ser citado, assim como os usuários saberão como citar o programa que utilizaram.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Se você se sentir particularmente inspirado por isso, poderá endossar o [Manifesto do Código Científico](http://sciencecodemanifesto.org/), que se baseia nos cinco princípios de código, direitos autorais, citação, crédito e curadoria.

- Para lançar e desenvolver o seu próprio projeto, o programa [Open Source Guides](https://opensource.guide/) oferece uma série de guias práticos e habilidades para ajudar a lançar e avançar em seus projetos de código aberto.

- Para uma análise detalhada dos fluxos de trabalho de pesquisa baseados em código aberto, o manual de [Ciência Aberta, Dados Abertos, Código Aberto](https://pfern.github.io/OSODOS/gitbook/) de Pedro L. Fernandes e Rutger A. Vos é um dos principais recursos online.

- As revistas mais formais funcionam também para artigos baseados em software, incluindo o [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) e o [The Journal of Open Source Software](https://joss.theoj.org/). Uma lista de tais locais também está [disponível](https://www.software.ac.uk/which-journals-should-i-publish-my-software).

- O [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) fornece um fórum global para a pesquisa e aplicações de hardware e software de código aberto.

- O [NumFOCUS](http://www.numfocus.org) é uma organização sem fins lucrativos que apoia e promove programas científicos inovadores, de código aberto e de primeira classe. Alguns dos projetos patrocinados incluem:
    
    - Iniciativas [IPython](http://ipython.org) e [Jupyter Notebook](https://jupyter.org).
    
    - [rOpenSci](http://ropensci.org), que promove o ambiente estatístico R de fonte aberta para pesquisa transparente e reprodutível.
    
    - Para ganhar mais experiência prática com programas de código aberto, a comunidade [Software Carpentry](https://software-carpentry.org/) realiza workshops regulares para melhorar as habilidades de computação baseadas em laboratório ([Wilson et al., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).

  


### Leitura adicional <a name="Reading"></a>

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

- The Future of Research in Free/Open Source Software Development [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).

- The Scientific Method in Practice: Reproducibility in the Computational Sciences [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).

- The case for open computer programs [(Ince et al., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).

- Current issues and research trends on open-source software communities [(Martinez-Torres and Diaz-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).

- Ten simple rules for reproducible computational research [(Sandve et al., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).

- A systematic literature review on the barriers faced by newcomers to open source software projects [(Steinmacher et al., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).

- Knowledge sharing in open source software communities: motivations and management [(Iskoujina and Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).

- Software citation principles [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

- An introduction to Rocker: Docker containers for R [(Boettiger and Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).

- Good enough practices in scientific computing [(Wilson et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).

- Four simple recommendations to encourage best practices in research software [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).

  


### Equipe de desenvolvimento <a name="Development_team"></a>

- [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, Universidade de Oxford, Reino Unido.
- [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, EUA.
- [Tania Allard](https://twitter.com/ixek), Open Sourceress, Data Enchantress, Universidade de Leeds, Reino Unido.
- [Simon Worthington](https://twitter.com/mrchristian99), Book Liberationist, TIB, Alemanha.
- [Paola Masuzzo](https://twitter.com/pcmasuzzo), Open Source Batman, Itália.
- [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Dinamarca.
- [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Centro de Biodiversidade Naturalis, Holanda.
- [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlim.
- [Jon Tennant](https://twitter.com/protohedgehog), O Encantador de Dinossauros.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)