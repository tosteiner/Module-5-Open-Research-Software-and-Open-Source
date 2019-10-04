---
output:
  html_document: domyślna
  pdf_document: domyślna
---

# Moduł 5: Otwarte oprogramowanie badawcze i otwarte oprogramowanie

## Spis treści

- [Wprowadzenie](#Introduction)
- [Czym jest oprogramowanie Open Source](#What_OSS)
- [Zasady oprogramowania Open Source](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [Istniejące platformy i narzędzia do oprogramowania Open Source](#Platforms)
- [Oprogramowanie Open Source wykorzystywane w badaniach](#Research)
- [Pierwsze kroki z OSS - FAQ](#FAQ)
- [Tworzenie dobrego oprogramowania do ponownego wykorzystania](#Reuse)
- [Licencja Open Source](#Licensing)
- [Cytowanie oprogramowania](#Citation)
- [Korzystanie z GitHub i Zenodo](#GitHub_Zenodo)
- [Współpraca za pośrednictwem Open Source](#Collaborating)
- [Gdzie iść stąd](#Future_OSS)

**UWAGA** że wersja audio tego jest dostępna do pobrania za pośrednictwem [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) i [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM).

## Wprowadzenie <a name="Introduction"></a>

Witamy w **Module 5** otwartej nauki MOOC: **Open Research Software i Open Source**.

Moduł ten został opracowany [w otwartej przestrzeni](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) dzięki współpracy międzynarodowego zespołu [afficianados Open Source](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-). Wszystko, co widzisz tutaj, zostało opracowane w sposób otwarty dzięki interaktywnej informacji zwrotnej i współpracy ze strony szerszej społeczności. Składa się z serii filmów, infografiki, czytania opartego na tekście i praktycznych zadań, w które zatopisz zęby.

Nie zapomnij, że możesz dołączyć do dyskusji na naszym otwartym [**Slack channel**](https://osmooc.herokuapp.com/). Przedstaw się w # module5opensource i powiedz nam trochę o tym, kim jesteś, swoim tłem i tym, jak się tu znalazłeś!

### Dla kogo jest ten moduł?

Moduł ten jest przeznaczony przede wszystkim dla badaczy obliczeniowych na poziomie magisterskim i licencjackim, a także początkujących naukowców zajmujących się danymi i każdego innego badacza, który używa kodu analitycznego lub oprogramowania. W dzisiejszym środowisku badawczym obejmuje to prawie każdego, kto korzysta z komputera do pracy.

> „Artykuł o wyniku obliczeniowym to reklama, a nie stypendium. Rzeczywiste stypendium to pełne środowisko oprogramowania, kod i dane, które dały wynik. ”- J. Buckheit i DL Donoho, 1995.

Oprogramowanie i technologia stanowią podstawę wielu współczesnych badań, które są teraz w nieunikniony sposób obliczeniowe w taki czy inny sposób - wyszukiwarki, platformy społecznościowe, oprogramowanie analityczne i publikacje cyfrowe. Dzięki temu istnieje coraz większe zapotrzebowanie na bardziej zaawansowane oprogramowanie Open Source, któremu towarzyszy rosnąca skłonność naukowców do otwartej współpracy nad nowymi narzędziami.

Moc Open Source polega na tym, że obniża bariery dla współpracy i adopcji, umożliwiając tym samym szybsze rozprzestrzenianie się pomysłów i technologii. Moduł ten wprowadzi niezbędne narzędzia niezbędne do przekształcenia oprogramowania w coś, co może być otwarte i ponownie wykorzystywane przez innych.

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>Zdjęcie: Patrick Hochstenbach (CC0 1.0 Universal)</i></p>

  


### **Szczegółowe cele nauczania dla tego modułu**:

1. Poznaj cechy otwartego oprogramowania; zrozumieć **argumentów etycznych, prawnych, ekonomicznych i badawczych dotyczących i przeciw oprogramowaniu Open Source**i lepiej zrozumieć wymagania jakościowe otwartego kodu.

2. Być w stanie przekształcić kod stworzony do użytku osobistego w otwarty kod, który jest dostępny dla innych.

3. Korzystaj z oprogramowania (narzędzi), które wykorzystuje otwartą treść i zachęca do szerszej współpracy.

  


## Czym jest oprogramowanie Open Source <a name="What_OSS"></a>

Praktycznie wszystkie nowoczesne przepływy pracy naukowo-badawczej opierają się na szeregu narzędzi programowych, zarówno działających na różnych zestawach danych, o różnych parametrach, jak i stosowanych iteracyjnie na różne sposoby (nauka o danych) lub działających na różnych wejściach i wykorzystujących modele i metody do przewidywania stanu wyjściowego ( nauka obliczeniowa). Oprogramowanie Open Source (OSS) to oprogramowanie komputerowe, w którym pełny kod źródłowy jest dostępny w ramach określonej licencji, która umożliwia innym użytkownikom dostęp, przeglądanie, modyfikowanie i redystrybucję tego kodu w dowolnym celu. Ponieważ OSS wymaga takiej licencji, zazwyczaj domyślnie pozostaje bezpłatnie. To jawne licencjonowanie odróżnia OSS od wolnego oprogramowania. Ponowne wykorzystanie OSS do analizy, symulacji i wizualizacji do badań jest również zazwyczaj łatwiejsze i bardziej elastyczne w porównaniu z oprogramowaniem zastrzeżonym. Często, niezależnie od tego, czy wiemy o tym, czy nie, korzystamy już z OSS w ramach własnych procesów badawczych.

OSS wpisuje się w szerszy schemat Otwartej Nauki, ponieważ pomaga w pełni udostępnić i ponownie wykorzystać pełne środowisko badawcze, w tym oprogramowanie wytwarzające wyniki badań. Jako taki stanowi niezbędny komponent najlepszych praktyk ([Jiménez et al., 2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)) oraz powtarzalność i powtarzalność badań (zarówno osobiście, jak i przez innych), wraz z innymi komponentami, takimi jak udostępnianie danych ([Stodden, 2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)).

W niektórych przypadkach udostępnianie kodu źródłowego może być nawet uzależnione od akceptacji powiązanych manuskryptów badawczych ([Shamir i in., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)). Ogólnie uważa się, że zwiększa to wpływ badań ([Vandwalle, 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)).

Niektóre z typowych zalet dla programistów to:

- Zwiększona lojalność i upodmiotowienie programistów;

- Niższe koszty usług i marketingu;

- Zwiększona marka usług i produktów;

- Produkcja wysokiej jakości oprogramowania przy niższych kosztach;

- Elastyczność i szybka innowacja;

- Dostosowywanie i integracja modułowa;

- Zwiększona niezawodność i niezależność; i

- Na podstawie otwartych standardów dostępnych dla wszystkich.

W związku z tym główne zalety dla naukowców (użytkowników) obejmują **niższych kosztów**, **zwiększoną przejrzystość**, **zwiększone bezpieczeństwo i stabilność**, **brak dostawcy „zablokowanie” ze zwiększoną kontrolą użytkownika**i **ogólnie wyższą jakość**. Co więcej, współdzielenie OSS umożliwia naukowcom uzyskanie uznania za ich wysiłki, na przykład poprzez bezpośrednie cytowanie oprogramowania [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

Powszechnie używane OSS to przeglądarka internetowa [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) i pełny pakiet biurowy [LibreOffice](https://www.libreoffice.org/). LibreOffice jest podobny do popularnego pakietu Microsoft Office, w tym edytor tekstu, menedżer arkuszy kalkulacyjnych i oprogramowanie do prezentacji slajdów, ale jest całkowicie darmowy i otwarty.

Niektórzy uważają ruch OSS za przeciwny ruch neoliberalizmu i prywatyzacji, sprzeciwiając się przepisom i normom w zakresie konstruowania i ponownego wykorzystywania informacji oraz potencjalnej transformacji współczesnego kapitalizmu poprzez udostępnianie oprogramowania w obfitości przy minimalnym wysiłku. See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## Zasady oprogramowania Open Source <a name="Principles"></a>

[Open Source Initiative](https://opensource.org/), jeden z pionierów OSS, oferuje następujące [definicji](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition):

*Nie martw się, nie musisz zapamiętywać tego wszystkiego, ale dobrze jest znać zasady, z których pochodzi OSS.*

- **Bezpłatna redystrybucja**: Licencja nie ogranicza żadnej ze stron do sprzedaży lub rozdawania oprogramowania jako komponentu zbiorczej dystrybucji oprogramowania zawierającego programy z kilku różnych źródeł. Licencja nie wymaga opłaty licencyjnej ani innej opłaty za taką sprzedaż.
    
    - **Kod źródłowy**: Program musi zawierać kod źródłowy i musi umożliwiać dystrybucję w kodzie źródłowym oraz w postaci skompilowanej. W przypadku, gdy jakaś forma produktu nie jest dystrybuowana z kodem źródłowym, musi istnieć dobrze nagłośniony sposób uzyskania kodu źródłowego za nie więcej niż rozsądny koszt reprodukcji, najlepiej, pobieranie za pośrednictwem Internetu bez opłat. Kod źródłowy musi być preferowaną formą, w której programista zmodyfikuje program. Celowo zaciemniony kod źródłowy jest niedozwolony. Formularze pośrednie, takie jak dane wyjściowe preprocesora lub tłumacza, nie są dozwolone.
    
    - **Prace pochodne**: Licencja musi zezwalać na modyfikacje i prace pochodne oraz musi umożliwiać ich rozpowszechnianie na takich samych warunkach, jak licencja oryginalnego oprogramowania.
    
    - **Integralność kodu źródłowego autora**: Licencja może ograniczać rozpowszechnianie kodu źródłowego w zmodyfikowanej formie tylko wtedy, gdy licencja zezwala na dystrybucję „plików łat” z kodem źródłowym w celu modyfikacji programu w czasie kompilacji. Licencja musi wyraźnie zezwalać na dystrybucję oprogramowania zbudowanego ze zmodyfikowanego kodu źródłowego. Licencja może wymagać, aby prace pochodne miały inną nazwę lub numer wersji niż oryginalne oprogramowanie.
    
    - **Brak dyskryminacji wobec osób lub grup**: Licencja nie może dyskryminować żadnej osoby lub grupy osób.
    
    - **Brak dyskryminacji wobec obszarów wymagających starań**: Licencja nie może ograniczać nikomu możliwości korzystania z programu w określonej dziedzinie. Na przykład nie może ograniczać używania programu w biznesie ani wykorzystywania go do badań genetycznych.
    
    - **Dystrybucja licencji**: Prawa związane z programem muszą dotyczyć wszystkich, którym program jest rozpowszechniany bez konieczności wykonywania dodatkowej licencji przez te strony.
    
    - **Licencja nie może być specyficzna dla produktu**: Prawa związane z programem nie mogą zależeć od tego, czy program jest częścią konkretnej dystrybucji oprogramowania. Jeśli program jest wyodrębniony z tej dystrybucji i używany lub rozpowszechniany zgodnie z warunkami licencji programu, wszystkie strony, którym program jest rozpowszechniany, powinny mieć te same prawa, które są przyznawane w związku z oryginalną dystrybucją oprogramowania.
    
    - **Licencja nie może ograniczać innego oprogramowania**: Licencja nie może nakładać ograniczeń na inne oprogramowanie dystrybuowane wraz z licencjonowanym oprogramowaniem. Na przykład licencja nie może wymagać, aby wszystkie inne programy dystrybuowane na tym samym nośniku były oprogramowaniem open-source.
    
    - **Licencja musi być neutralna technologicznie**: Żadne postanowienie licencji nie może być uzależnione od żadnej indywidualnej technologii lub stylu interfejsu.

To wszystko może być trochę skomplikowane do zapamiętania. Można go jednak podsumować jako *aby oprogramowanie było możliwe do ponownego wykorzystania w przyszłych pracach, a jednocześnie jest dostępne*.

  


## Lista kontrolna Open Source

Istnieje wiele istniejących platform i narzędzi, które obsługują OSS i współpracę. Podręcznik szkoleniowy [Open Science](https://open-science-training-handbook.gitbook.io/book/) zawiera listę kontrolną do wykorzystania przy ocenie „otwartości” istniejącego oprogramowania badawczego w oparciu o definicję Open Source powyżej:

- [] Czy oprogramowanie jest dostępne do pobrania i zainstalowania?

- [] Czy oprogramowanie można łatwo zainstalować na różnych platformach?

- [] Czy oprogramowanie ma warunki użytkowania?

- [] Czy kod źródłowy jest dostępny do kontroli?

- [] Czy pełna historia kodu źródłowego jest dostępna do wglądu w publicznie dostępnej historii wersji?

- [] Czy zależności oprogramowania (sprzętu i oprogramowania) są prawidłowo opisane? Czy te zależności wymagają jedynie minimalnej ilości wysiłku, aby je zdobyć i wykorzystać?

Sprawdź, sprawdź, sprawdź, gotowe! Simples.

  


## Społeczność Open Source i jej zarządzanie <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). Oba mają odmienne ideologie oparte na swobodzie użytkownika i praktycznym zastosowaniu oprogramowania. The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### Dla indywidualnych projektów

A typical open source project has the following types of formal roles:

- **Autor**: To osoba, która stworzyła projekt
- **Właściciel**: osoba / osoby, które posiadają własność administracyjną nad organizacją lub repozytorium 
- **Opiekunowie**: Współtwórcy odpowiedzialni za kierowanie wizją i zarządzanie organizacyjnymi aspektami projektu. (Mogą być również autorami lub właścicielami projektu).
- **Współtwórcy**: Użytkownik, który już przyczynił się do projektu.
- **Członkowie społeczności**: Ludzie, którzy korzystają z projektu. Mogą być aktywni w rozmowach, tworzyć nowe problemy lub wyrażać swoją opinię na temat przyszłych ulepszeń projektu.

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## Istniejące platformy i narzędzia do oprogramowania Open Source <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub <a name="GitHub"></a>

> Czy wiesz, że ten cały projekt został zbudowany jako otwarty i oparty na współpracy wysiłek społeczności w [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Oprogramowanie Open Source wykorzystywane w badaniach <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- Coraz częściej algorytmy implementowane w oprogramowaniu analitycznym stanowią integralną część metod opisanych w publikacjach naukowych. W związku z tym jest całkowicie sprzeczny z rygorystyczną recenzją, jeśli implementacje algorytmów są zamknięte dla osób z zewnątrz.

- Współpraca naukowa często obejmuje wiele instytucji i rozproszonych sieci badawczych, w których tajemnica i hierarchia poleceń nie są utrzymywane w sposób „niezbędny” do rozwoju zamkniętego źródła.

- Wiele analiz obliczeniowych jest uruchamianych w środowiskach zwirtualizowanych (takich jak instytucjonalna, krajowa lub międzynarodowa infrastruktura „chmury”) i hostowanych na serwerach wielu użytkowników. Zamknięte oprogramowanie komercyjne często nie pozwala na takie wykorzystanie.

- Rozwój OSS często opiera się na ochotnikach. W czasach ograniczeń budżetowych dla badań naukowych jest to wyraźna zaleta.

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## Pierwsze kroki z OSS - FAQ <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| Zamknięte                                                                                               | otwarty                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                  | Python, Julia                                                                                                                                                     |
| STATA / SPSS                                                                                            | R                                                                                                                                                                 |
| pakiet biurowy Microsoft Office                                                                         | LibreOffice                                                                                                                                                       |
| Matematyka                                                                                              | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## Tworzenie dobrego oprogramowania do ponownego wykorzystania <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **Czy wiesz, że ...** Termin `README` jest czasem żartobliwie przypisywany słynnej scenie w Przygodach Alicji Lewisa Carrolla w Krainie Czarów, w której Alice konfrontuje się z magicznymi munchies oznaczonymi „Eat Me” i „Drink Me”. Silny.

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 10 prostych reguł dla powtarzalnych badań obliczeniowych

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. Dla każdego wyniku śledzić, jak został wyprodukowany.
2. Unikaj kroków ręcznej manipulacji danymi.
3. Archiwizuj dokładne wersje wszystkich używanych programów zewnętrznych.
4. Wersja kontroluje wszystkie niestandardowe skrypty.
5. Nagraj wszystkie wyniki pośrednie, w miarę możliwości w standardowych formatach.
6. W przypadku analiz, które obejmują przypadkowość, zanotuj przypadkowe nasiona losowe.
7. Zawsze przechowuj surowe dane za działkami.
8. Generuj wyniki analizy hierarchicznej, pozwalając na kontrolowanie warstw o rosnącej szczegółowości.
9. Połącz oświadczenia tekstowe z podstawowymi wynikami.
10. Zapewnij publiczny dostęp do skryptów, przebiegów i wyników.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## Licencja Open Source <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution („BSD”)](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [stylu MIT (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT)lub
- [Licencja GNU General Public License („GPL”)](https://www.gnu.org/licenses/gpl-3.0.en.html).

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *Wyraźnie*, przy czym indywidualny wkład ma wyraźnie wskazaną licencję niezależną od głównego projektu; lub
2. *Bezwarunkowo*, przy czym wkład podlega pierwotnemu kodowi licencyjnemu głównego projektu.

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## Cytowanie oprogramowania <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- Imię i nazwisko autora,
- Tytuł oprogramowania,
- Numer wersji i
- Unikalny identyfikator / lokalizator (DOI lub URL).

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **Znaczenie**: Oprogramowanie powinno być uważane za legalny i cytowalny produkt badań. Cytowania oprogramowania powinny mieć takie samo znaczenie w dokumentacji naukowej, jak cytaty z innych produktów badawczych, takich jak publikacje i dane; powinny być uwzględnione w metadanych pracy cytującej, na przykład na liście referencyjnej artykułu w czasopiśmie, i nie powinny być pomijane ani rozdzielane. Oprogramowanie powinno być cytowane na tej samej podstawie, co każdy inny produkt badawczy, taki jak papier lub książka, to znaczy autorzy powinni cytować odpowiedni zestaw oprogramowania, tak jak cytują odpowiedni zestaw dokumentów.

- **Kredyt i przypisanie**: Cytaty dotyczące oprogramowania powinny ułatwiać udzielanie kredytów naukowych i normatywnych, prawnych przypisań wszystkim współpracownikom oprogramowania, uznając, że pojedynczy styl lub mechanizm przypisania może nie mieć zastosowania do całego oprogramowania.

- **Wyjątkowa identyfikacja**: Cytat z oprogramowania powinien zawierać metodę identyfikacji, która jest możliwa do działania maszynowo, unikatowa w skali globalnej, interoperacyjna i rozpoznawana przez przynajmniej społeczność odpowiednich ekspertów domeny, a najlepiej przez badaczy publicznych.

- **Wytrwałość**: Unikalne identyfikatory i metadane opisujące oprogramowanie i jego rozmieszczenie powinny się utrzymywać - nawet poza okresem życia opisywanego oprogramowania.

- **Dostępność**: Cytaty dotyczące oprogramowania powinny ułatwiać dostęp do samego oprogramowania i związanych z nim metadanych, dokumentacji, danych i innych materiałów niezbędnych ludziom i maszynom do świadomego korzystania z odnośnego oprogramowania.

- **Specyfika**: Cytowania oprogramowania powinny ułatwiać identyfikację i dostęp do konkretnej wersji oprogramowania, które było używane. Identyfikacja oprogramowania powinna być tak szczegółowa, jak to konieczne, na przykład przy użyciu numerów wersji, numerów wersji lub wariantów takich jak platformy.

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Korzystanie z GitHub i Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **Czy wiesz, że ...** Cała zawartość stworzona dla tego MOOC jest dostępna jako część społeczności w [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Współpraca i współtworzenie poprzez Open Source <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## Gdzie iść stąd <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. Będziesz teraz w stanie zdefiniować cechy OSS i niektóre argumenty dotyczące etycznego, prawnego, ekonomicznego i badawczego wpływu na i przeciw.

2. Opierając się na standardach społeczności, będziesz mógł opisać wymagania jakościowe dotyczące udostępniania i ponownego używania otwartego kodu.

3. Teraz będziesz mógł korzystać z szeregu narzędzi badawczych wykorzystujących OSS.

4. Teraz będziesz mógł przekształcić kod przeznaczony do ich osobistego użytku w kod, który jest dostępny i może być ponownie używany przez innych.

5. Deweloperzy oprogramowania będą mogli tworzyć swoje oprogramowanie, a użytkownicy oprogramowania będą wiedzieć, jak cytować oprogramowanie, którego używają.

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- Jeśli czujesz się szczególnie zainspirowany tym, możesz poprzeć Manifest [Science Code](http://sciencecodemanifesto.org/), który opiera się na pięciu zasadach kodu, prawach autorskich, cytatach, kredytach i kuratorstwie.

- Aby uruchomić i opracować własny projekt, program [Przewodników Open Source](https://opensource.guide/) oferuje szereg praktycznych przewodników i umiejętności, które pomogą uruchomić i rozwinąć projekty OSS.

- Dla szczegółowego spojrzenia na OSS opartych workflow badawczych do potrzeb, [Otwarta Nauka, Open Data, Open Source](https://pfern.github.io/OSODOS/gitbook/) ręcznie przypomnienie Pedro L. Fernandesa i Rutger A. Vos jest jednym z najlepszych źródeł w Internecie.

- Istnieją również bardziej sformalizowane obiekty czasopism dotyczące artykułów opartych na oprogramowaniu, w tym [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) i [The Journal of Open Source Software](https://joss.theoj.org/). Wykaz takich lokali jest także [dostępny](https://www.software.ac.uk/which-journals-should-i-publish-my-software).

- Zestaw [PLOS Open Source Toolkit](https://channels.plos.org/open-source-toolkit) stanowi globalne forum dla badań i aplikacji sprzętu i oprogramowania Open Source.

- [NumFOCUS](http://www.numfocus.org) to organizacja non-profit, która wspiera i promuje światowej klasy, innowacyjne, otwarte oprogramowanie naukowe. Niektóre z projektów, które sponsorują, obejmują:
    
    - [Inicjatywy IPython](http://ipython.org) i [Jupyter Notebook](https://jupyter.org).
    
    - [rOpenSci](http://ropensci.org), który promuje środowisko statystyczne R open source dla przejrzystych i powtarzalnych badań.
    
    - Aby zdobyć więcej doświadczenia w pracy z OSS, społeczność [Software Carpentry](https://software-carpentry.org/) organizuje regularne warsztaty w celu poprawy umiejętności obliczeniowych w laboratorium ([Wilson i in., 2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)).

  


### Dalsza lektura <a name="Reading"></a>

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

- Przyszłość badań nad rozwojem wolnego / otwartego oprogramowania [(Scacchi, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf).

- Metoda naukowa w praktyce: powtarzalność w naukach obliczeniowych [(Stodden, 2010)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf).

- Przypadek otwartych programów komputerowych [(Ince i in., 2012)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf).

- Aktualne problemy i trendy badawcze w społecznościach oprogramowania typu open source [(Martinez-Torres i Diaz-Fernandez, 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf).

- Dziesięć prostych reguł dla powtarzalnych badań obliczeniowych [(Sandve i in., 2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF).

- Systematyczny przegląd literatury na temat barier napotykanych przez nowoprzybyłych w projektach oprogramowania open source [(Steinmacher i in., 2014)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf).

- Wymiana wiedzy w społecznościach oprogramowania open source: motywacje i zarządzanie [(Iskoujina i Roberts, 2015)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf).

- Zasady cytowania oprogramowania [(Smith et al., 2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf).

- Wprowadzenie do Rocker: Docker dla R [(Boettiger i Eddelbuettel, 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf).

- Dobre praktyki w informatyce [(Wilson i in., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf).

- Cztery proste zalecenia zachęcające do stosowania najlepszych praktyk w oprogramowaniu badawczym [(Jiménez et al., 2017)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf).

  


### Zespół ds. Rozwoju <a name="Development_team"></a>

- [Alex Morley](https://twitter.com/alex__morley), Open Sourceror, University of Oxford, Wielka Brytania.
- [Kevin Moerman](https://twitter.com/KMMoerman), Open Sourceror, MIT, USA.
- [Tania Allard](https://twitter.com/ixek), Open Sourceress, Data Enchantress, University of Leeds, Wielka Brytania.
- [Simon Worthington](https://twitter.com/mrchristian99), Book Liberationist, TIB, Niemcy.
- [Paola Masuzzo](https://twitter.com/pcmasuzzo), Open Source Batman, Włochy.
- [Ivo Grigorov](https://twitter.com/OAforClimate), Open Source Robin, Dania.
- [Rutger Vos](https://twitter.com/rvosa), Open Sourceror, Naturalis Biodiversity Center, Holandia.
- [Julien Colomb](https://twitter.com/j_colomb), Open Ninja, Berlin.
- [Jon Tennant](https://twitter.com/protohedgehog), Zaklinacz dinozaurów.

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)