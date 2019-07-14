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

- [Prefácio](#Foreword)
- [Configurar um repositório do GitHub](#Setup)
- [Escolha o seu repositório GitHub](#Choose)
- [Login para Zenodo](#Login)
- [Autorize o GitHub a se conectar com o Zenodo](#Authorise)
- [Selecione o repositório para arquivamento](#Archive)
- [Verificação das configurações do repositório](#Check)
- [Crie uma nova versão](#Release)
- [Obtendo um DOI](#DOI)
- [Lista de verificação para citar seu projeto](#Checklist)
- [Recursos adicionais](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Task 2 workflow" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
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

  


## Check repository settings <a name="Check"></a>

Now you have set up a new webhook between Zenodo and your repository. In GitHub, click on the settings for your repository, and the Webhooks tab on the left hand side menu. This should display the new Zenodo webhook configured to Zenodo. Note, it may take a little time for the webhook listing to show up.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Check that webhooks are enabled for your GitHub repository. Example here using the Open Scholarship Strategy</i></p>

  


## Create a new release <a name="Release"></a>

The first time you archive a repository is known as the 'first release'. Each time you create a new version of that repository and archive it, you create a new release. This can be tracked in the 'releases' tab for your repository on GitHub (top center).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Check that the repository first release was successful. Example here using the Open Scholarship Strategy</i></p>

  


For the first archived version of your repository, click 'Create a new release' back in Zenodo. Fill in the form and give some details as to what the release entails. For the first release, make sure to call it v1.0.0, as is standard practice.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Create a new release. Example here using the Open Scholarship Strategy, for which a first release already exists</i></p>

  


Finally, click 'publish release', and your archive will be published and versioned on GitHub.

To view your release on Zenodo you need to visit the [Upload](https://zenodo.org/deposit) tab. To finish the archiving a few more details are needed on Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Check the new release has been uploaded. Example here shown using the Open Scholarship Strategy</i></p>

  


## Getting a DOI <a name="DOI"></a>

This is sometimes referred to as DOI 'minting', and requires a couple of extra bits of information about the repository on Zenodo. On Zenodo click the [Upload](https://zenodo.org/deposit) tab in the main menu, and your newly uploaded repository should be there. Scroll down the page and fill in the extra information as needed, required fields are marked with a red asterisk, and then click 'Publish'.

**Note**: Only after this extra information has been added will your DOI become live. It may also take a short time for the DOI to become active. Example DOI shown below (for the Open Scholarship Strategy again).

> **Pro-tip**: Copy the URL for the DOI into the README file for your GitHub repo to make cross-linking even easier, as well as present a clear highlighted DOI badge for users to see and make use of your DOI. You only need to do this once with your first release DOI as it acts as a 'concept DOI' and is linked to all subsequent release DOIs.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

The GitHub/Zenodo integration will now assign a DOI to each version/release of a project repository. This enables users to refer to and cite specific versions of projects. Also, the list of authors for the citation is automatically determined by the GitHub user account names used by the repository - this means no-one gets left out. Author details can be edited later on Zenodo. DOIs used in Zenodo are registered through the [DataCite](https://www.datacite.org/) service.

> **Pro-tip**: Create a 'human-readable' version of this citation in your project's README file. This will be helpful to researchers who might not be familiar with using DOIs to create citations, and make it easier for others to cite your software and acknowledge your work. An example of this could be: Jon Tennant. (2018, July 30). Foundations for Open Scholarship Strategy Development: First formal release (Version 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**CONGRATULATIONS!!**

Your GitHub repository is now archived in Zenodo, and with a DOI that can be versioned to reflect updates to the repository version through time. You should be able to see details of this on the GitHub Zenodo page for your repository. This also means that your archived projects can get picked up by other indexing services and search engines that use DOIs too.

Providing a long-term archive and a DOI for your work is required for others to be able to properly cite it, as this provides basic citation metadata. For Open Science, it is important to be able to cite the software that you use in your research, and this integrated workflow enables that to happen, in line with best practices for research citation. Furthermore, this practice is important in elevating the standard of software (and related projects) to that of the standard of other research outputs.

> **Pro-tip**: Is your research funded by an EU grant? Now you can directly connect your archived project to your grant by updating the grant section of the metadata on the project's Zenodo record. This massively helps to increase its discoverability!

  


## Checklist for citing your project <a name="Checklist"></a>

So now you have a sustainably archived GitHub repository in Zenodo that is ready to be re-used and cited! Before continuing, make sure that you have:

- [ ] Linked your GitHub project to Zenodo. If you see a complete copy of your GitHub repository in Zenodo then things are working.
- [ ] Zenodo and GitHub integrated setup works nicely. For example have all the author names, and correct project title come across to Zenodo. If not, or if authors just have nicknames you can edit these details in Zenodo.
- [ ] Project has a first release, with a DOI. You should have a DOI displayed on your projects Zenodo page. This first DOI is called the 'concept DOI' and is the master DOI linking to all subsequent release DOIs. Copy this DOI link and embed it in your GitHub projects README page. You're done!

### Additional resources <a name="Resources"></a>

[Making your code citable](https://guides.github.com/activities/citable-code/) - GitHub Guides.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)