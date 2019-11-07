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

Para alguns, o Movimento Open Source Software (OSS) representa um contra-movimento ao neoliberalismo e à privatização, desafiando os regulamentos e normas na construção e reutilização da informação, além de uma potencial transformação do capitalismo moderno através da disponibilização abundante de software com o mínimo esforço. Ver também [Movimento do software livre / de código aberto: Resistência ou mudança?](https://doi.org/10.15448/1984-7289.2009.1.5569) de Panayiota Georgopoulou para saber mais sobre este assunto.

  


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

  


## Um checklist do código-fonte aberto

Há várias plataformas e ferramentas existentes que apoiam o programa de código-fonte aberto e a colaboração. O [Manual de Treinamento em Ciência Aberta](https://open-science-training-handbook.gitbook.io/book/) fornece uma checklist para avaliar a "abertura" do software de pesquisa existente, com base na Definição de Código Aberto acima:

- [] O software está disponível para download e instalação?

- [] O software pode ser facilmente instalado em diferentes plataformas?

- [] O software impõe condições de uso?

- [] O código-fonte está disponível para inspeção?

- [] O histórico completo do código-fonte está disponível para verificação por meio de um histórico de versões disponível publicamente?

- Há descrição adequada das dependências do programa (hardware e software)? Essas dependências exigem um esforço mínimo razoável para a sua obtenção e uso?

Verifique, confira, confirme, e está feito! Simples assim.

  


## A comunidade de código-fonte aberto e sua governança <a name="OS_Community"></a>

Existem dois campos principais dentro da comunidade de software livre: o **movimento do software livre** e o **movimento do programa de código-fonte aberto**). Ambos têm diferentes ideologias baseadas nas liberdades dos usuários e nas aplicações práticas do software. O termo 'FLOSS' é usado como um termo excessivamente neutro para se referir a ambos; sendo livre em francês e 'gratuito' em espanhol no contexto da liberdade.

Da mesma forma que as pessoas ativas no movimento da ciência aberta são heterogêneas em suas suposições e objetivos, também existem opiniões diferentes na comunidade do FLOSS. Recordando o módulo 1, duas das escolas de pensamento em ciência aberta eram a escola *pragmática* e a escola *democrática*. Enquanto o primeiro é impulsionado pelo pressuposto de que a pesquisa poderia ser mais eficiente se os cientistas trabalhassem juntos, o segundo quer corrigir uma distribuição desigual de conhecimento. Provavelmente, ambos acabam compartilhando suas pesquisas, mas, cada um com intenções diferentes.

Isso é aproximadamente comparável ao OSS e ao movimento do software livre: o último evoluiu por volta de 1983 para proteger o que eles chamam de quatro liberdades essenciais do usuário de um programa. Isso inclui a liberdade de executar, copiar, distribuir, estudar, alterar e melhorar um programa. O software que respeita essas liberdades com uma licença apropriada é considerado 'livre'. As quatro liberdades são vistas como vitais para uma sociedade como um todo, no sentido de que apenas permitem o compartilhamento, a cooperação e, finalmente, a liberdade em geral. Nesse sentido, o movimento do software livre é um movimento social que cria um imperativo ético.

O movimento do software de código aberto, que se fragmentou em 1998, concentra-se nas vantagens práticas e não faz campanha por princípios. Está preocupado com o desenvolvimento de software de alta qualidade, para o qual a capacidade de todos para obter, modificar e contribuir com o código-fonte é considerada altamente benéfica.

Entre várias conclusões que chegam, o acesso ao código-fonte de um programa é compartilhado. Assim, o software pode ser considerado *livre*, *código aberto*ou ambos, de acordo com as definições acordadas pela Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) e pela Open Source Initiative ([OSI](https://opensource.org/osd)). A FSF argumenta que o software livre é um subconjunto de OSS, com apenas um [fração](https://www.gnu.org/philosophy/free-open-overlap.html) sendo de código aberto, mas não livre.

Portanto, destacar um status de licença específico do software em uso - de código aberto ou gratuito - é principalmente sobre diferentes filosofias, não sobre o software não ter o outro status também. Cada movimento tem sua parcela de problemas para explicar seu termo: *livre* significa mais do que ser gratuito e *código aberto* significa mais do que ter acesso ao código-fonte. O FSF [](https://www.gnu.org/philosophy/open-source-misses-the-point.html) e a contrapartida europeia [FSFE](https://fsfe.org/documents/whyfs.html) fornecem mais informações sobre este tópico.

### Para projetos individuais

Um projeto típico de código aberto tem os seguintes tipos de papéis formais:

- **Autor**: É a pessoa que criou o projeto
- **Proprietário**: A/s pessoa/s que possui propriedade administrativa sobre a organização ou o repositório 
- **Mantenedores**: Colaboradores responsáveis por conduzir a visão e gerenciar os aspectos organizacionais do projeto. (Eles também podem ser autores ou proprietários do projeto.)
- **Colaboradores**: O usuário que já contribuiu para o projeto.
- **Membros da Comunidade**: Pessoas que trabalham no projeto. Eles podem ser ativos em conversas, criar novas questões para discussão ou expressar sua opinião sobre as futuras melhorias do projeto.

Normalmente, as funções são divulgadas publicamente em um arquivo `README` , um arquivo de colaboradores ou uma página separada com informações sobre a equipe do projeto.

  


## Plataformas e ferramentas de software com código-fonte aberto existentes <a name="Platforms"></a>

Ambientes e máquinas virtuais estão se tornando cada vez mais populares como facilitadores do fluxo de trabalho de pesquisas de alta capacidade, e muitos deles são construídos sobre Softwares de Código-fonte Aberto (OSS) (por exemplo, sistemas operacionais, linguagens de programação e estruturas de processamento de dados). Os serviços populares incluem [Google Cloud](https://cloud.google.com/compute/) e [Amazon Web Services](https://aws.amazon.com/), os quais também auxiliam no armazenamento de bases de dados e na entrega de conteúdos, bem como no poder computacional. [InsideDNA](https://insidedna.me/) é uma plataforma computacional para a reprodutibilidade da pesquisa em bioinformática, genômica e ciências da vida.

Como mencionado [acima](#What_OSS), o LibreOffice é uma alternativa de código aberto ao Microsoft Office. Os dois são quase completamente compatíveis, apenas com diferentes formatos de arquivo padrão. Para os gerenciadores de referência, [Zotero](https://www.zotero.org/) é a alternativa mais popular de código aberto para plataformas proprietárias como Mendeley ou EndNote.

[Zotero](https://www.zotero.org/) usa o formato BibTeX (pronuncia-se 'bib-tech'), baseado em LaTeX (pronuncia-se 'lay-tech'), e possui plugins de navegador para fazer o gerenciamento de referências e construir citações de forma simples. Ao integrar isso a outros softwares, como o LibreOffice, agora é possível ter um fluxo de trabalho de pesquisa totalmente em código-fonte aberto em muitos casos.

### GitHub<a name="GitHub"></a>

> Você sabia que este projeto inteiro foi construído como um esforço comunitário aberto e colaborativo no [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) é um site de hospedagem popular para conteúdo de software e não software (geralmente chamado de 'notebooks'), com recursos adicionais para controle de versão, gerenciamento e rastreamento de projetos e serviços de armazenamento. O GitHub é construído com base em programa de código-fonte aberto / Open Source Software (OSS) [Git](https://git-scm.com/), que permite aos usuários trabalhar remotamente para manter, compartilhar e colaborar em softwares de pesquisa e outros projetos não baseados em software.

O controle de versão é essencialmente um processo que captura imagens instantâneas dos arquivos em um repositório e rastreia modificações neles. Ele registra quando as mudanças foram feitas, grava o estado em que estavam e quem as fez. Se várias pessoas estiverem trabalhando em um arquivo de uma vez, todas as alterações sobrepostas serão detectadas e deverão ser resolvidas antes de continuar. Isso proporciona um processo muito mais simplificado e automatizado do que salvar e registrar mudanças manualmente à medida em que os projetos se desenvolvem. Também evita as inevitáveis listas de versões de arquivos com nomes confusos...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>O GitHub nos ajuda a evitar, por exemplo, convenções de nomenclatura de arquivos abaixo do padrão ideal (fonte: XKCD)</i></p>

  


Uma das funções mais populares e úteis do GitHub é o [issue tracker (rastreador de problemas) ](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), que é usado para organizar o desenvolvimento do programa de código-fonte aberto / Open Source Software (OSS). O link acima direciona para o rastreador de problemas referente ao desenvolvimento deste módulo! Se você acha que há algo aqui que pode ser melhorado, ou se você quiser fazer comentários, qualquer um pode adicionar ou contribuir com uma questão lá!

Outros serviços similares de hospedagem de projetos incluem o [BitBucket](https://bitbucket.org/), o [ GitLab](https://about.gitlab.com/) e o [Launchpad](https://launchpad.net/). Se a recente aquisição do GitHub pela Microsoft é um pouco desagradável para você, estas são ótimas alternativas.

No entanto, também sabemos que o GitHub pode ter uma curva de aprendizagem bastante elevada. É por isso que a primeira tarefa prática deste curso online irá te ensinar a configurar o seu primeiro repositório de projetos no GitHub!

**[IR PARA TAREFA 1: Criando seu primeiro repositório do GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Software de código aberto usado em pesquisa <a name="Research"></a>

Especialmente em pesquisa científica, o uso e desenvolvimento de Software de Código Aberto tornou-se praticamente uma norma. Há várias razões para isso além daquelas que se aplicam à aceitação geral do programa de código-fonte aberto/Open Source Software (OSS), por exemplo, consumidores, indústria ou governo. Entre essas razões estão:

- Cada vez mais, os algoritmos implementados no software de análise são parte integrante dos métodos descritos nas publicações acadêmicas. Como tal, está completamente em conflito com a rigorosa revisão por pares se estas implementações de algoritmos forem restritas a pessoas de fora.

- A colaboração científica abrange muitas vezes múltiplas instituições e redes de pesquisa distribuídas em que o sigilo e a hierarquia de comando não são mantidos de uma forma que seja "necessária" para o desenvolvimento de fontes fechadas.

- Muitas análises computacionais são executadas em ambientes virtualizados (como infraestruturas institucionais, nacionais ou internacionais na 'nuvem') e hospedadas em servidores multiusuários. Softwares comerciais de código fechado, muitas vezes, não permitem esse uso.

- O desenvolvimento de programas de código-fonte aberto/Open Source Software (OSS) geralmente dependem de voluntários. Em um tempo de restrições orçamentárias para a pesquisa científica, essa é uma clara vantagem.

Por essas e outras razões, as ferramentas de código aberto são muito usadas em pesquisas científicas. Isso inclui o uso em campos em que muitos pesquisadores são desenvolvedores amadores e dependem de ferramentas como o [R](https://www.r-project.org/) para análise e scripts estatísticos, que, na última década, substituíram quase completamente o software comercial para análises estatísticas como o SPSS ou JMP em um muitos campos. Em áreas como a bioinformática, que envolve muita manipulação de arquivos dos resultados das plataformas de sequenciamento de DNA, linguagens de scripts com propósitos gerais como [Python](https://www.python.org/) e bibliotecas comumente usadas construídas com base nela (como [biopython](http://biopython.org)) se tornaram uma parte vital do conjunto de ferramentas de muitos pesquisadores.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Ferramentas como R e Python são essencialmente programas para escrever softwares. Embora a programação seja uma atividade cada vez mais comum entre os pesquisadores, obviamente *nem todos* os cientistas fazem isso. Um passo para além da programação é o encadeamento das entradas e saídas de várias ferramentas de análise em fluxos de trabalho mais longos. Como exemplo da área genômica, um fluxo de trabalho muito comum é começar com leituras de alto desempenho e depois i) fazer verificações básicas de controle de qualidade; ii) mapear as leituras comparando com um genoma de referência; iii) identificar os pontos onde os novos dados estão em desacordo com a referência. Estes passos são executados rotineiramente como um fluxo de trabalho onde um código aberto executável diferente é executado em um ambiente de linha de comando Linux para cada um dos três passos. Embora isto não seja um desenvolvimento de software de código aberto, ele envolve o uso e produção de artefatos de código aberto (como scripts de shell do Linux) para os quais os princípios que discutimos neste módulo são aplicáveis.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Por fim, o programa de código-fonte aberto/Open Source Software (OSS) também é usado em pesquisas científicas por razões que mais se aproximam daquelas que impulsionam a adoção do programa de código aberto na sociedade em geral, ou seja, porque é barato. Por exemplo, indivíduos ou organizações podem decidir mudar do Microsoft Office para o LibreOffice a fim de escrever manuscritos ou processar planilhas porque este último é gratuito (tanto em [**'cerveja grátis'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) quanto em 'liberdade de expressão'). Da mesma forma, a opção de mudar do ArcGIS para [QGIS](https://www.qgis.org/en/site/) a fim de analisar informações geográficas pode ser solicitada simplesmente por considerações de custo.   


## Primeiros passos com o Programa de Código Aberto - FAQ <a name="FAQ"></a>

**Estou usando o X [por exemplo, Matlab, STATA, Excel] e quero fazer a transição para um software mais aberto. Quais são os próximos passos?**

Mesmo que você esteja usando um software proprietário, você pode continuar compartilhando seu código-fonte/documentos etc. *O melhor primeiro passo é compartilhar tudo o que você puder*.

**Ótimo! Eu posso colocá-los no meu novo repositório do github.**

Se isso é o suficiente para você, por enquanto, ótimo! Caso contrário, para a maioria dos softwares proprietários, existem equivalentes de código aberto. Dê uma olhada e veja o que você acha.

| Fechado                                                                                                 | Aberto                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                          |
| STATA / SPSS                                                                                            | R                                                                                                                                                                      |
| MS Office                                                                                               | LibreOffice                                                                                                                                                            |
| Mathematica                                                                                             | JupyterLab                                                                                                                                                             |
| Max/MSP                                                                                                 | PureData                                                                                                                                                               |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... adicionando seu próprio exemplo [aqui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Legal! Mas se eu fizer a troca ficarei estagnado: levando muito tempo para aprender uma nova ferramenta / sem suporte / com erros no software.**

Boa pergunta! A resposta é que isso depende. A melhor coisa a se fazer é encontrar alguém que tenha optado pela troca antes e aprender com sua experiência. Ou apenas faça uma pesquisa no Google! Alguns programas de código-fonte aberto são muito melhores do que os seus equivalentes fechados, outros não, por isso, vale a pena escolher cuidadosamente.

## Fazendo um bom software para reutilização <a name="Reuse"></a>

Provavelmente, a pessoa que poderá querer reutilizar o seu software no futuro é...você! Assim, enquanto compartilhar é sempre melhor do que não compartilhar, você pode tornar sua própria vida, e a dos outros, muito mais fácil através de documentação apropriada. A documentação pode incluir várias coisas, como a inclusão de comentários úteis e anotações no código que ajudam a explicar por que razão foi realizada uma determinada ação, ao invés do que se pretende alcançar.

Um dos aspectos mais críticos disso é incluir um arquivo `README` informativo, que acompanha quase todos os projetos de software de código aberto, e algumas vezes até mais de um. Pode ser uma boa prática incluir um arquivo deste tipo em cada diretório, incluindo ainda uma lista de arquivos, um índice e qual é a finalidade do diretório. O arquivo `README` é normalmente apenas texto simples ou markdown (novamente, como todos os arquivos deste curso), e pode incluir informações críticas sobre como instalar e executar software, informar previamente quais são as dependências e requisitos, bem como tutoriais ou exemplos.

> **Você sabia ...** O termo `README` é algumas vezes atribuído à famosa cena de Alice no País das Maravilhas, de Lewis Carroll, em que Alice enfrenta petiscos mágicos rotulados com a mensagem "Coma-me" e "Beba-me". Potente.

O objetivo aqui é fornecer informações suficientes para maximizar a reutilização e reprodutibilidade do ambiente computacional, de modo que alguém sem experiência com o projeto possa facilmente acessar e reutilizar o software. ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). Ao reduzir as barreiras de entrada, você aumenta as chances de outros serem capazes de reutilizar seu trabalho, que é um dos objetivos finais do programa de código-fonte aberto. ([Shamir et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

Uma extensão que pode ajudar a facilitar ainda mais a reutilização futura é a tecnologia dos "contêineres". Os contêineres são como um ecossistema congelado no tempo, onde o código, os dados, quaisquer outras dependências, são perfeitamente preservados, empacotados e salvos nas versões atuais de funcionamento. Isso significa que qualquer pessoa no futuro poderá entrar e executar as análises novamente. Como tal, eles geralmente são bons para reutilização, mas isso pode resultar no sacrifício da modificação ou do entendimento de outras pessoas, pois muitas vezes muitos detalhes podem ser ocultados no código-fonte e em suas dependências. Exemplos comuns de implementação de contêiner em pesquisa incluem [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (um contêiner Docker para a linguagem R), [Binder](https://mybinder.readthedocs.io/en/latest/)e [Code Ocean](https://codeocean.com/).

**Software sustentável é um bom software.**

  


## 10 regras simples para pesquisa computacional reprodutível

As 10 regras simples para tornar a pesquisa computacional mais reprodutível, baseadas em [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), são:

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

<p align="center"><i>Infográfico adaptado de Sandve et al., (2013). Sinta-se livre para fazer o download e imprimir isto a fim de se manter atualizado durante sua pesquisa!</i></p>

  


Se você seguir estas etapas ao longo dos processos na [**Tarefa 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [**Tarefa 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), você vai se sair bem!

  


## Licenças de código aberto <a name="Licensing"></a>

Uma licença Open Source é um tipo de licença projetada especificamente para software e código que tornam explícito quais são as condições legais para compartilhamento e reutilização. Como mencionado [acima](#What_OSS), a adição de uma licença adequada é o que diferencia software compartilhado publicamente de um programa de código-fonte aberto. Por exemplo, o amplamente utilizado [MATLAB](https://www.mathworks.com/products/matlab.html) é um software proprietário, e [Octave](https://www.gnu.org/software/octave/) é uma linguagem de programação alternativa licenciada abertamente.

Existem atualmente mais de 1.400 licenças exclusivas de código aberto, uma complexidade resultante da dificuldade em entender as diferenças entre as implicações legais através de uma licença diferente.

Algumas das licenças mais comuns incluem:

- [Berkeley Software Distribution ("BSD")](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [MIT-style (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT), ou
- [Licença Pública Geral GNU ("GPL")](https://www.gnu.org/licenses/gpl-3.0.en.html).

Você não precisa conhecer todos os detalhes legais por trás de tudo isso, mas é bom pelo menos saber quais opções estão disponíveis para você.

Existem duas maneiras pelas quais as contribuições para um projeto se tornam licenciadas:

1. *Explicitamente*, em que a contribuição individual tem uma licença claramente indicada, independente do projeto principal; ou
2. *Implicitamente*, em que a contribuição se enquadra no código de licenciamento original do projeto principal.

Felizmente, o processo de seleção de uma licença de código aberto é relativamente trivial, graças a ferramentas fáceis de usar, como [Escolha uma licença](https://choosealicense.com/) ou [Seletor de licença público](https://ufal.github.io/public-license-selector/). Cada uma dessas licenças permite que outros usuários usem, copiem, distribuam e desenvolvam seu trabalho, geralmente garantindo que os criadores sejam devidamente reconhecidos por seu trabalho. Aqui, a chave é selecionar uma licença apropriada para o seu trabalho, dependendo do que você quer, ou não quer, que outros façam com isso.

  


## Citação de software <a name="Citation"></a>

As citações fornecem uma das interações mais importantes na pesquisa acadêmica, formando a base de nossos sistemas de referência e métricas. Normalmente, isto é realizado graças à assistência de um identificador único permanente, como um [Identificador de Objetos Digital](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). Um DOI é um identificador persistente, implementado no [Handle System](https://en.wikipedia.org/wiki/Handle_System), que atende a um padrão comum, dependendo do propósito, como para identificar informações acadêmicas. Essa identificação é fundamental para rastrear a genealogia e a proveniência da pesquisa, para a reprodutibilidade, bem como para dar crédito apropriado àqueles que criaram o software. É importante ressaltar que o software deve ser considerado um produto legítimo da pesquisa acadêmica, e a citação está se tornando uma forma cada vez mais comum de indicar isso.

Em 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) escreveram um trabalho de pesquisa sobre os princípios da citação de software como parte do FORCE11 Software Citation Working Group. Da mesma forma que você gostaria de citar um software que você usou como parte de boas práticas de pesquisa, é importante tornar sua pesquisa facilmente citável também. Ao citar qualquer software usado para sua própria pesquisa, você deve incluir no mínimo:

- O(s) nome do(s) autor(es),
- Título do software,
- Número da versão
- O identificador/localizador único (DOI ou URL).

Os seis princípios de citação de software por [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) são fornecidos aqui:

- **Importância**: O software deve ser considerado um produto legítimo e citável da pesquisa. As citações de software devem ter a mesma importância no registro acadêmico que as citações de outros produtos de pesquisa, como publicações e dados; eles devem ser incluídos nos metadados do trabalho de citação, por exemplo, na lista de referência de um artigo de periódico, e não devem ser omitidos ou separados. O software deve ser citado da mesma forma que qualquer outro produto de pesquisa, como um artigo ou um livro, ou seja, os autores devem citar o conjunto apropriado de produtos de software, da mesma forma que citam o conjunto de documentos apropriado.

- **Crédito e atribuição**: As citações de software devem facilitar a concessão de crédito acadêmico e a atribuição normativa e legal a todos os colaboradores do software, reconhecendo que um estilo único ou mecanismo de atribuição pode não ser aplicável a todos os softwares.

- **Identificação única**: Uma citação de software deve incluir um método de identificação que seja acionável por máquina, globalmente exclusivo, interoperável e reconhecido por pelo menos uma comunidade dos especialistas de domínio correspondentes e, de preferência, por pesquisadores públicos em geral.

- **Persistência**: Identificadores únicos e metadados que descrevem o software e sua disposição devem persistir - mesmo para além da duração do software que descrevem.

- **Acessibilidade**: Citações de software devem facilitar o acesso ao próprio software e aos seus metadados, documentação, dados e outros materiais associados necessários para que humanos e máquinas façam uso informado do software referenciado.

- **Especificidade**: As citações de software devem facilitar a identificação e o acesso à versão específica do software que foi usada. A identificação do software deve ser tão específica quanto necessária, como o uso de números de versão, números de revisão ou variantes, como plataformas.

Nota: Para obter instruções sobre 'como tornar seu software passível de ser </strong>citado', consulte a seção [**Usando o GitHub e o Zenodo **](#GitHub_Zenodo) abaixo e [**Tarefa 2: Vinculando o GitHub e o Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Usando o GitHub e o Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) é uma ferramenta popular para gerenciamento de projetos, armazenamento de conteúdo e controle de versão. Note que o próprio GitHub não é um programa de código-fonte aberto/Open Souce Software (OSS). No entanto, o Git, a ferramenta na qual ele se baseia, é. O Git foi projetado para ajudar a gerenciar os arquivos de código-fonte e as atualizações para um projeto relacionado ao software. No entanto, ele também pode ser estendido a outros projetos que não sejam de software; por exemplo, esse [curso](https://github.com/OpenScienceMOOC/)!

No entanto, ter pesquisa no GitHub é apenas o primeiro passo. É igualmente importante torná-lo persistente e reutilizável, e é por isso que ter um Identificador de Objeto Digital (DOI) associado a ele pode ser útil. A maneira mais simples de fazer isso é através de um serviço chamado [Zenodo](https://zenodo.org/), que é um repositório multidisciplinar de código aberto e gratuito criado pelo OpenAIRE e CERN, e pode ser usado para atribuir um DOI a repositórios individuais do GitHub. Existe um [ Guia GitHub ](https://guides.github.com/activities/citable-code/) que explica os detalhes envolvidos na ligação dos repositórios do GitHub diretamente ao Zenodo, de modo que quando os desenvolvedores criam versões formais para o seu software, o Zenodo cria e arquiva uma versão do software.

Não há nada de especial sobre o uso do Zenodo para criar DOIs, além de sua **gratuidade**; outros repositórios gerais também podem ser usados, como o [DataCite DOI Fabrica](https://doi.datacite.org/), ou seus próprios repositórios institucionais, como o [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

Muitos pesquisadores podem ter medo de compartilhar códigos incompletos, com erros ou imperfeitos. No entanto, na comunidade de software de código-fonte aberto /Open Source Software (OSS), essa prática de compartilhamento de código "bruto" é bastante comum. O compartilhamento aberto de código permite que outras pessoas o reutilizem e aprimorem, bem como se envolvam de maneira mais profunda com qualquer pesquisa associada a ele. Esse é um dos aspectos fundamentais da colaboração entre pares, talvez melhor exemplificado pelo processo tradicional de revisão por pares de manuscritos de pesquisa.

A tarefa 2 irá guiá-lo através do processo de vinculação de um repositório do GitHub ao Zenodo para arquivamento.

> **Você sabia ...** Todo o conteúdo produzido para este curso está disponível como parte de uma comunidade no [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[IR PARA A TAREFA 2: Vinculando GitHub e Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Colaborando e contribuindo através da Código Aberto <a name="Collaborating"></a>

Muitas vezes, o Software de Código Aberto é desenvolvido de forma pública, descentralizada e colaborativa entre múltiplos colaboradores. O objetivo é aumentar a diversidade e o escopo de um projeto e seu design, a fim de se tornar mais benéfico e sustentável. Tal abordagem foi comparada a um modelo de "bazar" por Eric Raymond, um dos primeiros defensores do programa de código-fonte aberto (OSS). Um dos mais importantes princípios orientadores disto é o da **produção entre os pares**, que depende de comunidades auto-organizadas para regular o desenvolvimento de conteúdo, coordenado para um objetivo ou resultado compartilhado.

Os projetos de software de código aberto dependem fortemente da colaboração voluntária, o que muitas vezes implica em um fluxo constante de novos participantes para se tornarem produtivos e sustentáveis. ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Criar a atmosfera social certa para um projeto e um ambiente de engajamento acolhedor são muitas vezes cruciais para colaborações bem sucedidas em programas de código-fonte aberto.

  


## Onde ir a partir daqui <a name="Future_OSS"></a>

Esperamos que agora você tenha percebido a importância do software como uma pedra angular da ciência moderna, assim como a relevância que o programa de código-fonte aberto desempenha neste contexto.

Os **resultados da aprendizagem** a partir disso devem ser:

1. Você agora será capaz de definir as características do software de código aberto, além de alguns dos argumentos éticos, legais, econômicos e de impacto na pesquisa a favor e contra ele.

2. Com base nos padrões da comunidade, você poderá descrever os requisitos de qualidade de compartilhamento e reutilização de código aberto.

3. Agora, você poderá usar uma série de ferramentas de pesquisa que utilizam o programa de código-fonte aberto.

4. Agora você será capaz de transformar o código desenvolvido para seu uso pessoal em código acessível e reutilizável para outros usuários.

5. Os desenvolvedores de software serão capazes de tornar seu software passível de ser citado, assim como os usuários saberão como citar o programa que utilizaram.

  


**TAREFA BÔNUS**

Se você completou [ as tarefas 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) e [ 2 ](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)</strong>, nós também temos uma ** Tarefa BÔNUS** para você, caso queira aperfeiçoar suas habilidades ainda mais. [a Tarefa 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) irá levá-lo a um passo adiante na integração do Git em um fluxo de trabalho de pesquisa comum, mostrando-lhe como integrá-lo com o R Studio. É recomendável que você tenha concluído as duas primeiras tarefas antes de prosseguir com esta.

No entanto, sua jornada de código aberto não para por aqui! Este foi apenas o começo, há alguns recursos incríveis se você quiser fazer ou aprender mais:

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

*Estas referências são apenas o início. Incluem algumas das visões gerais mais úteis do panorama do código aberto na pesquisa. Contudo, se você quiser encontrar algo mais específico para o seu próprio campo de pesquisa, esse caminho está aí para você explorar!*

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