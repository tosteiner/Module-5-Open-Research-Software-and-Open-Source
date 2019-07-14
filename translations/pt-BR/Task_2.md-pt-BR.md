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

> **Dica profissional**: Copie a URL do DOI para o arquivo README do seu repositório GitHub a fim de tornar ainda mais fácil a interconexão, assim como você deve exibir em destaque um emblema DOI para que os usuários possam ver e usar o seu DOI. You only need to do this once with your first release DOI as it acts as a 'concept DOI' and is linked to all subsequent release DOIs.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437   .)

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

### Recursos adicionais<a name="Resources"></a>

[Tornando seu código citável](https://guides.github.com/activities/citable-code/) - Guias do GitHub.

**Sabe como esse conteúdo pode ser melhorado?**

Está na hora de fazer um teste com as suas novas habilidades no GitHub! Todo o desenvolvimento de conteúdo acontece principalmente [aqui](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Se você tiver uma sugestão de melhoria do conteúdo, layout, ou qualquer outra coisa, você pode fazer isso, e, então se tornará automaticamente parte do conteúdo do curso após a verificação de um moderador!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)