---
output:
  html_document: padrão
  pdf_document: padrão
---

# Tarefa 2: Como tornar seu código passível de ser citado usando o GitHub e o Zenodo

Esta tarefa é projetada para estudantes e pesquisadores que desejam criar e reutilizar projetos / repositórios baseados no GitHub na literatura acadêmica.

Não se esqueça de que você pode participar das discussões no nosso fórum aberto no [** canal do Slack **](https://osmooc.herokuapp.com/). Por favor, apresente-se no #módulo5opensource e conte-nos um pouco sobre quem você é, qual a sua formação e como chegou aqui!

Tempo estimado para conclusão: 45 a 60 minutos.

## Sumário

- [Prefácio](#Prefácio)
- [Configurar um repositório do GitHub](#Configuração)
- [Escolha o seu repositório GitHub](#Escolher)
- [Login para Zenodo](#Login)
- [Autorize o GitHub a se conectar com o Zenodo](#Autorizar)
- [Selecione o repositório para arquivamento](#Arquivamento)
- [Verificação das configurações do repositório](#Verificação)
- [Crie uma nova versão](#Lançamento)
- [Obtendo um DOI](#DOI)
- [Lista de verificação para citar seu projeto](#Checklist)
- [Recursos adicionais](#Recursos)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Fluxo de trabalho da tarefa 2" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>O fluxo de trabalho da Tarefa 2. Mantenha isso acessível e ao seu alcance enquanto executa a tarefa!</i></p>

  


## Prefácio<a name="Foreword"></a>

Embora a integração do GitHub e Zenodo torne realmente mais fácil trabalhar com estas ferramentas atualmente (Janeiro de 2019), é importante salientar que existem alternativas para o GitHub (Gitlab, Bitbucket,...) e alternativas para o Zenodo (Outros repositórios podem ser mais adequados à sua comunidade, você pode perguntar aos seus colegas). Por exemplo, pode-se trabalhar com o Gitlab e carregar manualmente cada nova versão para o repositório da sua universidade, obtendo um DOI. Os princípios (trabalhando com um sistema de controle de versão online e arquivando as versões principais em um repositório que fornece um identificador único persistente) podem ser aplicados em diferentes fluxo de trabalho.

## Configurar um repositório GitHub <a name="Setup"></a>

> **Dica**: Certifique-se de incluir um arquivo LICENSE e README no seu repositório. Isso indicará às pessoas o objetivo do projeto e como elas podem se envolver com ele no futuro.

Descubra como configurar um repositório do GitHub neste outro guia [Tarefa 1: Construindo um repositório do GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) que também faz parte do 'Módulo 5: Software de Pesquisa Aberta e Open Source'.

## Escolha o seu repositório GitHub <a name="Choose"></a>

Uma vez que estiver na sua página de listagem de projetos do [github.com](https://github.com) acesse a aba 'Repositories' no topo da página do github. Selecione qual repositório você gostaria de arquivar e abra-o.

  


## Login para Zenodo <a name="Login"></a>

Agora acesse o [zenodo.org](https://zenodo.org). Zenodo é uma plataforma onde você pode arquivar permanentemente seu código e outros elementos do projeto. Zenodo faz isso através da atribuição de um **Digital Object Identifier** (DOI) para um projeto, o qual também auxilia na facilidade de citar um trabalho. Isso é diferente do GitHub, o qual atua como um local onde o trabalho real em um projeto acontece, em vez de arquivá-lo a longo prazo. No GitHub, o conteúdo pode ser modificado, apagado, reescrito e irreversivelmente alterado, o que o torna um pouco relativo a ser usado para fins de referência mais duradouros. Zenodo oferece mais segurança e permanência para os resultados da pesquisa.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Inscreva-se no Zenodo</i></p>

  


Se você já tem uma conta Zenodo, isso é fácil. Se não, siga os passos para criar um - você pode até mesmo fazer o login usando sua conta do GitHub ou o perfil ORCID para simplificar as coisas, já que o Zenodo construiu uma integração para isso. Isso pode ser mais fácil do que criar outra conta e perfil de pesquisa.

  


## Autorize o GitHub a se conectar com o Zenodo <a name="Authorise"></a>

No site Zenodo, autorize-o a se conectar à sua conta do GitHub na seção '[Using GitHub](https://zenodo.org/account/settings/github/)'. Aqui, o Zenodo irá redirecioná-lo para o GitHub para solicitar permissões para usar '[webhooks](https://developer.github.com/webhooks/)' nos seus repositórios. Você pode autorizar o Zenodo aqui com as permissões necessárias para formar esses links.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autorizando o Zenodo a se conectar com o GitHub</i></p>

  


Se você estiver tentando dar acesso ao Zenodo a um repositório organizacional, você (ou administrador) precisará ter certeza de que o Zenodo tem permissão de acesso a terceiros. O GitHub enviará um email de autorização que precisa ser confirmado. Neste ponto, de volta às configurações do seu repositório no GitHub, você também precisa ter certeza de que o repositório está configurado para 'público', não privado.

  


## Selecione o repositório para arquivar <a name="Archive"></a>

Se você chegou até aqui, isso significa que o Zenodo está agora autorizado a configurar os webhooks de repositórios necessários para arquivamento do repositório e emissão de um DOI. Para fazer isso, no site Zenodo, navegue até a página de listagem do repositório [GitHub](https://zenodo.org/account/settings/github/) e simplesmente clique no botão 'on' próximo ao seu repositório.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Habilitar repositórios individuais do GitHub para serem preservados no Zenodo</i></p>

  


## Verificação das configurações do repositório <a name="Check"></a>

Agora você configurou um novo webhook entre o Zenodo e seu repositório. No GitHub, clique nas configurações do seu repositório e na aba Webhooks no menu do lado esquerdo. Isso deve exibir o novo webhook Zenodo configurado para o Zenodo. Observe, pode demorar um pouco para a listagem do webhook aparecer.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Verifique se os webhooks estão habilitados para o seu repositório GitHub. Exemplo aqui usando a Open Scholarship Strategy</i></p>

  


## Crie uma nova versão <a name="Release"></a>

A primeira vez que você arquiva um repositório é conhecido como a 'primeira versão'. Cada vez que você criar uma nova versão desse repositório e arquivá-lo, você cria uma nova versão. Isso pode ser rastreado na guia 'releases' do seu repositório no GitHub (centro superior).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Verifique se a primeira liberação do repositório foi bem-sucedida. Exemplo aqui usando a Open Scholarship Strategy</i></p>

  


Para a primeira versão arquivada do seu repositório, clique em "Create a new release" (Criar uma nova versão) no Zenodo. Preencha o formulário e dê alguns detalhes sobre o que a versão implica. Para a primeira versão, certifique-se de chamá-la v1.0.0, como é prática padrão.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Criar uma nova versão. Exemplo aqui usando a Open Scholarship Strategy, para a qual já existe uma primeira versão</i></p>

  


Finalmente, clique em 'publish release' (publicar lançamento), e seu arquivo será publicado e versionado no GitHub.

Para ver sua versão no Zenodo, você precisa visitar a guia [Upload (Enviar)](https://zenodo.org/deposit) . Para concluir o arquivamento, mais alguns detalhes são necessários no Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Verifique se a nova versão foi carregada. Exemplo aqui mostrado usando a Open Scholarship Strategy</i></p>

  


## Obtendo um DOI <a name="DOI"></a>

Isto às vezes é chamado de atribuição de um DOI, inclusive requer alguns bits extras de informações sobre o repositório no Zenodo. No Zenodo, clique na guia [Upload](https://zenodo.org/deposit) no menu principal e seu novo repositório carregado deve estar lá. Role a página para baixo e preencha as informações extras conforme necessário, e, os campos obrigatórios são marcados com um asterisco vermelho, em seguida, clique em 'Publicar'.

**Nota**: Somente depois que esta informação extra for adicionada, seu DOI se tornará ativo. Também pode demorar um pouco para que o DOI se torne ativo. Exemplo DOI mostrado abaixo (para a Open Scholarship Strategy).

> **Dica profissional**: Copie a URL do DOI para o arquivo README do seu repositório GitHub a fim de tornar ainda mais fácil a interconexão, assim como você deve exibir em destaque um emblema DOI para que os usuários possam ver e usar o seu DOI. Você só precisa fazer isso uma vez com a sua primeira publicação de um DOI, pois, trata-se de uma espécie de "conceito" e está vinculado a todos os DOIs posteriores ao lançamento.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg )](https://doi.org/10.5281/zenodo.1323437   .)

A integração do GitHub / Zenodo irá agora atribuir um DOI a cada versão / release de um repositório de projetos. Isto permite aos usuários referenciarem e citarem versões específicas de projetos. Além disso, a lista de autores para a citação é automaticamente determinada pelos nomes da conta de usuário do GitHub usados pelo repositório - isso significa que ninguém fica de fora. Detalhes sobre o autor podem ser editados posteriormente no Zenodo. Os DOIs usados no Zenodo são registrados através do serviço [DataCite](https://www.datacite.org/).

> **Dica**: Crie uma versão 'legível para humanos' desta citação no arquivo README do seu projeto. Isso será útil para investigadores que talvez não estejam familiarizados com a utilização de DOIs para criar referências e facilitar a outros citar o seu software e reconhecer o seu trabalho. Um exemplo disso poderia ser: Jon Tennant. (2018, 30 de julho). Foundations for Open Scholarship Strategy Development: First formal release (Version 1.2). Zenodo. [ http://doi.org/10.5281/zenodo.1323437 ](http://doi.org/10.5281/zenodo.1323437)

**PARABÉNS!!!**

Seu repositório GitHub agora está arquivado no Zenodo, e com um DOI que pode ser versionado para refletir as atualizações para a versão do repositório ao longo do tempo. Você deve poder ver os detalhes disso na página do Zenodo do GitHub para o seu repositório. Isso também significa que seus projetos arquivados podem ser recuperados por outros serviços de indexação e motores de busca que também usam DOIs.

Fornecer um arquivo de longo prazo e um DOI para o seu trabalho é necessário para que outros possam citá-lo corretamente, pois isso fornece metadados básicos de citação. Para a Ciência Aberta é importante poder citar o software que você usa em sua pesquisa, detalhar inclusive o fluxo de trabalho integrado permite que isso aconteça em conformidade com as melhores práticas para a citação de pesquisa. Além disso, essa prática é importante para elevar o padrão de software (e projetos relacionados) ao padrão de outros resultados de pesquisa.

> **Dica**: A sua pesquisa é financiada por um subsídio da União Europeia ou alguma outra agência de financiamento? Agora você pode conectar diretamente o seu projeto arquivado ao seu financiamento, atualizando a seção de concessão de verbas nos metadados contidos no registro do projeto no Zenodo. Isso ajuda imensamente a aumentar sua capacidade de descoberta!

  


## Lista de verificação para citar seu projeto <a name="Checklist"></a>

Então, agora você tem um repositório do GitHub arquivado de forma sustentável no Zenodo e que está pronto para ser reutilizado e citado! Antes de continuar, certifique-se de que:

- [ ] Vinculou seu projeto do GitHub ao Zenodo. Se você visualizar uma cópia completa do seu repositório GitHub no Zenodo, então as coisas estão funcionando.
- [ ] A configuração integrada do Zenodo e do GitHub está funcionando bem. Por exemplo, tem todos os nomes dos autores e o título correto do projeto aparece no Zenodo. Caso contrário, ou se os autores tiverem apenas apelidos, você poderá editar esses detalhes no Zenodo.
- [ ] O projeto tem uma primeira versão, com um DOI. Você deve ter um DOI exibido em sua página Zenodo de projetos. This first DOI is called the 'concept DOI' and is the master DOI linking to all subsequent release DOIs. Copy this DOI link and embed it in your GitHub projects README page. You're done!

### Recursos adicionais<a name="Resources"></a>

[Tornando seu código citável](https://guides.github.com/activities/citable-code/) - Guias do GitHub.

**Sabe como esse conteúdo pode ser melhorado?**

Está na hora de fazer um teste com as suas novas habilidades no GitHub! Todo o desenvolvimento de conteúdo acontece principalmente [aqui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Se você tiver uma sugestão de melhoria do conteúdo, layout, ou qualquer outra coisa, você pode fazer isso, e, então se tornará automaticamente parte do conteúdo do curso após a verificação de um moderador!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)