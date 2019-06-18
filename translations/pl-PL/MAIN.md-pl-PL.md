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
- [Społeczność Open Source, zarządzanie i wkład](#OS_Community)
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

Niektórzy uważają ruch OSS za przeciwny ruch neoliberalizmu i prywatyzacji, sprzeciwiając się przepisom i normom w zakresie konstruowania i ponownego wykorzystywania informacji oraz potencjalnej transformacji współczesnego kapitalizmu poprzez udostępnianie oprogramowania w obfitości przy minimalnym wysiłku. Zobacz [Ruch oprogramowania wolnego / otwartego: Opór czy zmiana?](http://www.redalyc.org/html/742/74212712006/) autorstwa Panayioty Georgopoulou, aby uzyskać więcej informacji na ten temat.

  


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

W społeczności wolnego oprogramowania istnieją dwa główne obozy: ruch **wolnego oprogramowania**i ruch **OSS**. Oba mają odmienne ideologie oparte na swobodzie użytkownika i praktycznym zastosowaniu oprogramowania. Często termin „FLOSS” jest używany do pogodzenia tych dwóch obozów politycznych i oznacza „Wolne / Libre i oprogramowanie Open Source”; Libre to francuski i hiszpański za „wolny” w kontekście wolności.

Podstawową zasadą ponownego wykorzystania jest to, co odróżnia OSS od „wolnego oprogramowania”. Bezpłatne i otwarte oprogramowanie (FOSS) to termin obejmujący oprogramowanie, które można zaklasyfikować jako bezpłatne i otwarte. Dobrym przykładem FOSS jest system operacyjny [Ubuntu Linux](https://www.ubuntu.com/).

Duża różnica między wolnym oprogramowaniem a OSS polega na tym, że te pierwsze muszą rozpowszechniać zaktualizowane wersje na tej samej licencji co oryginał, podczas gdy nowsze wersje OSS mogą być dystrybuowane na różnych licencjach. FOSS łączy to, co najlepsze w obu światach.

Definicje te zostały obecnie szeroko przyjęte, zarówno przez rządy międzynarodowe, jak i niektóre duże organizacje, takie jak [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) i [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home). Do głównych organizacji w przestrzeni FLOSS należą brytyjski [Software Sustainability Institute](https://www.software.ac.uk/), który produkuje cenne zasoby, takie jak najnowszy [poradnik dotyczący oprogramowania dla naukowców](https://softwaresaved.github.io/software-deposit-guidance/).

### Dla indywidualnych projektów

Typowy projekt open source ma następujące typy ról formalnych:

- **Autor**: To osoba, która stworzyła projekt
- **Właściciel**: osoba / osoby, które posiadają własność administracyjną nad organizacją lub repozytorium 
- **Opiekunowie**: Współtwórcy odpowiedzialni za kierowanie wizją i zarządzanie organizacyjnymi aspektami projektu. (Mogą być również autorami lub właścicielami projektu).
- **Współtwórcy**: Użytkownik, który już przyczynił się do projektu.
- **Członkowie społeczności**: Ludzie, którzy korzystają z projektu. Mogą być aktywni w rozmowach, tworzyć nowe problemy lub wyrażać swoją opinię na temat przyszłych ulepszeń projektu.

Zazwyczaj role są upubliczniane poprzez plik `README` plik współtwórców lub oddzielną stronę zespołu dla projektu.

  


## Istniejące platformy i narzędzia do oprogramowania Open Source <a name="Platforms"></a>

Środowiska wirtualne i maszyny stają się coraz bardziej popularne jako elementy wspomagające przepływ pracy badawczej o dużej mocy, a wiele z nich opiera się na OSS (np. Systemach operacyjnych, językach programowania i strukturach przetwarzania danych). Popularne usługi obejmują [Google Cloud](https://cloud.google.com/compute/) i [Amazon Web Services](https://aws.amazon.com/), które również pomagają w przechowywaniu baz danych i dostarczaniu treści, a także mocy obliczeniowej. [InsideDNA](https://insidedna.me/) to platforma obliczeniowa do powtarzalnych badań w dziedzinie bioinformatyki, genomiki i nauk przyrodniczych.

Jak wspomniano [powyżej](#What_OSS), LibreOffice zapewnia Open Source alternatywę dla Microsoft Office. Oba są prawie całkowicie kompatybilne, tylko z różnymi domyślnymi formatami plików. Dla menedżerów cytowań, [Zotero](https://www.zotero.org/) jest najpopularniejszą alternatywą Open Source dla zastrzeżonych platform, takich jak Mendeley lub EndNote.

[Zotero](https://www.zotero.org/) używa formatu BibTeX (wymawiane „bib-tech”) opartego na LaTeX (wymawiane „lay-tech”) i ma wtyczki do przeglądarek, które ułatwiają zarządzanie cytatami. Integrując to z innym oprogramowaniem, takim jak LibreOffice, w wielu przypadkach możliwe jest teraz posiadanie w pełni otwartego przepływu pracy badawczej.

### GitHub <a name="GitHub"></a>

> Czy wiesz, że ten cały projekt został zbudowany jako otwarty i oparty na współpracy wysiłek społeczności w [GitHub](https://github.com/OpenScienceMOOC/)?

[GitHub](https://github.com/) jest popularnym serwisem hostingowym zarówno dla zawartości oprogramowania, jak i oprogramowania (często nazywanego „notebookami”), z dodatkowymi możliwościami kontroli wersji, zarządzania projektami i śledzenia oraz usługami przechowywania. GitHub jest zbudowany w oparciu o OSS [Git](https://git-scm.com/), który umożliwia użytkownikom zdalną pracę w celu utrzymania, udostępniania i współpracy w zakresie oprogramowania badawczego i innych projektów niezwiązanych z oprogramowaniem.

Kontrola wersji to zasadniczo proces, który wykonuje migawki plików w repozytorium i śledzi ich modyfikacje. Rejestruje, kiedy dokonano zmian, czym były i kto je wykonał. Jeśli kilka osób pracuje nad jednym plikiem naraz, wszelkie nakładające się zmiany są wykrywane i muszą zostać rozwiązane przed kontynuowaniem. Zapewnia to znacznie bardziej uproszczony i zautomatyzowany proces niż ręczne zapisywanie i rejestrowanie zmian w miarę rozwoju projektów. Unika również nieuniknionych list mylących nazwanych wersji plików ...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub pomaga nam uniknąć, poniżej, optymalnych konwencji nazewnictwa plików (źródło: XKCD)</i></p>

  


Jednym z bardziej popularnych i przydatnych funkcji GitHub jest [tracker Wydanie](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), który jest używany do organizowania rozwoju OSS. Powyższy link prowadzi do śledzenia problemów w celu opracowania tego modułu! Jeśli uważasz, że jest coś, co może się poprawić lub chcesz komentować, każdy może dodać lub przyczynić się do powstania problemu!

Inne podobne usługi hostingowe obejmują [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/)i [Launchpad](https://launchpad.net/). Jeśli niedawne przejęcie GitHub przez Microsoft jest dla ciebie trochę zniechęcające, to są świetne alternatywy.

Wiemy jednak również, że GitHub może mieć dość wysoką krzywą uczenia się. Dlatego pierwsze praktyczne zadanie tego MOOC nauczy Cię, jak skonfigurować swoje pierwsze repozytorium projektów GitHub!

**[PRZEJDŹ DO ZADANIA 1: Budowanie pierwszego repozytorium GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## Oprogramowanie Open Source wykorzystywane w badaniach <a name="Research"></a>

Zwłaszcza w badaniach naukowych korzystanie z oprogramowania Open Source i jego rozwój stały się praktycznie normą. Jest wiele powodów tego, oprócz tych, które dotyczą ogólnej akceptacji OSS przez, na przykład, konsumentów, przemysł lub rząd. Wśród tych powodów są:

- Coraz częściej algorytmy implementowane w oprogramowaniu analitycznym stanowią integralną część metod opisanych w publikacjach naukowych. W związku z tym jest całkowicie sprzeczny z rygorystyczną recenzją, jeśli implementacje algorytmów są zamknięte dla osób z zewnątrz.

- Współpraca naukowa często obejmuje wiele instytucji i rozproszonych sieci badawczych, w których tajemnica i hierarchia poleceń nie są utrzymywane w sposób „niezbędny” do rozwoju zamkniętego źródła.

- Wiele analiz obliczeniowych jest uruchamianych w środowiskach zwirtualizowanych (takich jak instytucjonalna, krajowa lub międzynarodowa infrastruktura „chmury”) i hostowanych na serwerach wielu użytkowników. Zamknięte oprogramowanie komercyjne często nie pozwala na takie wykorzystanie.

- Rozwój OSS często opiera się na ochotnikach. W czasach ograniczeń budżetowych dla badań naukowych jest to wyraźna zaleta.

Z tych i innych powodów narzędzia Open Source są bardzo często wykorzystywane w badaniach naukowych. Obejmuje to wykorzystanie w dziedzinach, w których wielu badaczy to sami programiści-amatorzy i polegają na narzędziach takich jak [R](https://www.r-project.org/) do analizy statystycznej i skryptów, które w ostatniej dekadzie prawie całkowicie zastąpiły komercyjne oprogramowanie do analizy statystycznej, takie jak SPSS lub JMP w dużo pól. W dziedzinach takich jak bioinformatyka, które wymagają dużej obsługi plików na wyjściach platform do sekwencjonowania DNA, języki skryptowe ogólnego przeznaczenia, takie jak [Python](https://www.python.org/) i powszechnie używane biblioteki zbudowane na nim (takie jak [biopython](http://biopython.org)) stały się istotnymi część zestawu narzędzi wielu badaczy.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Pyton</i></p>

  


Narzędzia takie jak R i Python są zasadniczo oprogramowaniem do pisania oprogramowania. Mimo że programowanie jest coraz bardziej powszechne wśród badaczy aktywność, oczywiście nie *każdy* naukowiec robi. Jednym krokiem od programowania jest łączenie wejść i wyjść różnych narzędzi analitycznych w dłuższe przepływy pracy. Jako przykład z genomiki, bardzo powszechny jest przepływ pracy z odczytami o wysokiej przepustowości, a następnie i) przeprowadzanie podstawowych kontroli jakości; ii) odwzorować odczyty na genomie odniesienia; iii) zidentyfikować punkty, w których nowe dane są sprzeczne z odniesieniem. Kroki te są rutynowo wykonywane jako przepływ pracy, w którym inny plik wykonywalny Open Source jest uruchamiany w środowisku wiersza polecenia systemu Linux dla każdego z trzech kroków. Chociaż prawdopodobnie nie jest to całkiem otwarte oprogramowanie, wymaga użycia i produkcji artefaktów typu open source (takich jak skrypty powłoki Linuksa), do których mają zastosowanie zasady omawiane w tym module.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Wreszcie OSS jest również wykorzystywany w badaniach naukowych z powodów, które bardziej odzwierciedlają te, które napędzają przyjęcie OSS w szerszym społeczeństwie, a mianowicie, że jest on tani. Na przykład osoby lub organizacje mogą zdecydować się na przejście z pakietu Microsoft Office na LibreOffice w celu napisania manuskryptu lub przetwarzania arkusza kalkulacyjnego, ponieważ ten drugi jest bezpłatny (zarówno w wersji [**„darmowe piwo”**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) i „darmowa mowa”). Podobnie wybór przełączenia z ArcGIS na [QGIS](https://www.qgis.org/en/site/) celu analizy informacji geograficznych może być spowodowany względami kosztowymi.   


## Pierwsze kroki z OSS - FAQ <a name="FAQ"></a>

**Używam X [np. Matlab, STATA, Excel] i chcę przejść do czegoś bardziej otwartego. Jakie są kolejne kroki?**

Nawet jeśli używasz zastrzeżonego oprogramowania, zazwyczaj możesz nadal udostępniać swój kod źródłowy / dokumenty itp. *Najlepszym pierwszym krokiem jest dzielenie się wszystkim, co możesz*.

**Świetny! Mogę je umieścić w moim nowym repozytorium github.**

Jeśli to ci teraz wystarcza, świetnie! Jeśli nie dla większości programów zastrzeżonych, istnieją odpowiedniki Open Source. Idź z jednym i zobacz, co myślisz.

| Zamknięte                                                                                                     | otwarty                                                                                                                                                         |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Matlab                                                                                                        | Python, Julia                                                                                                                                                   |
| STATA / SPSS                                                                                                  | R                                                                                                                                                               |
| pakiet biurowy Microsoft Office                                                                               | LibreOffice                                                                                                                                                     |
| Matematyka                                                                                                    | JupyterLab                                                                                                                                                      |
| Sprawdź swoje nowe [Pull Request-PR-](https://help.github.com/articles/about-pull-requests/) Umiejętności ... | ... dodając własny przykład [tutaj](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Fajne! Ale jeśli dokonam przełączenia, to utknę: biorąc wieki, aby nauczyć się nowego narzędzia / bez wsparcia / z błędnym oprogramowaniem.**

Dobre pytanie! Odpowiedź brzmi: zależy. Najlepiej jest znaleźć kogoś, kto wcześniej dokonał zmiany i wyciągnąć wnioski z ich doświadczeń. Lub po prostu wyszukaj w Google! Niektóre OSS są znacznie lepsze niż ich zamknięte odpowiedniki, niektóre nie, więc warto wybrać ostrożnie.

## Tworzenie dobrego oprogramowania do ponownego wykorzystania <a name="Reuse"></a>

Najbardziej prawdopodobną osobą, która może chcieć ponownie wykorzystać oprogramowanie w przyszłości, jest ... ty! Tak więc dzielenie się jest zawsze lepsze niż nie dzielenie się, możesz sprawić, że twoje życie i życie innych osób będzie znacznie łatwiejsze dzięki odpowiedniej dokumentacji. Dokumentacja może zawierać kilka rzeczy, takich jak pomocne komentarze i adnotacje w kodzie, które pomagają wyjaśnić, dlaczego dana czynność została wykonana, a nie to, co ma osiągnąć.

Jednym z najbardziej krytycznych aspektów tego jest informacyjny plik `README` , który towarzyszy niemal każdemu projektowi OSS, a czasem nawet więcej niż jeden. Dobrą praktyką może być dołączenie jednego takiego pliku do każdego katalogu, który zawiera listę plików, spis treści i jaki jest cel katalogu. Plik `README` jest zwykle zwykłym tekstem lub przeceną (ponownie, tak jak wszystkie te dla MOOC!) I może zawierać krytyczne informacje o tym, jak zainstalować i uruchomić oprogramowanie, poprzednie zależności i wymagania, a także samouczki lub przykłady.

> **Czy wiesz, że ...** Termin `README` jest czasem żartobliwie przypisywany słynnej scenie w Przygodach Alicji Lewisa Carrolla w Krainie Czarów, w której Alice konfrontuje się z magicznymi munchies oznaczonymi „Eat Me” i „Drink Me”. Silny.

Celem jest, aby zapewnić wystarczającą ilość informacji, aby zmaksymalizować ponowne wykorzystanie i powtarzalność środowiska obliczeniowego tak, że ktoś bez doświadczenia z projektem mogą łatwo uzyskać dostęp i ponowne korzystanie z oprogramowania ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). Obniżając bariery wejścia, zwiększasz szanse innych osób na ponowne wykorzystanie Twojej pracy, co jest jednym z ostatecznych celów OSS ([Ince i in., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

Rozszerzeniem tego, co może jeszcze bardziej ułatwić przyszłe ponowne wykorzystanie, jest technologia „kontenerowa”. Kontenery są jak ekosystem zamrożony w czasie, gdzie kod, dane, wszelkie inne zależności są doskonale zachowane, zapakowane i zapisane w obecnych funkcjonujących wersjach. Oznacza to, że każdy w przyszłości może wejść i ponownie przeprowadzić analizy. Jako takie, są one generalnie dobre do ponownego wykorzystania, ale może to nastąpić w wyniku poświęcenia modyfikacji lub zrozumienia przez innych, ponieważ często wiele szczegółów może być ukrytych w kodzie źródłowym i jego zależnościach. Typowe przykłady implementacji kontenerów w badaniach obejmują [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (kontener Docker dla języka R), [Binder](https://mybinder.readthedocs.io/en/latest/)i [Code Ocean](https://codeocean.com/).

**Zrównoważone oprogramowanie to dobre oprogramowanie.**

  


## 10 prostych reguł dla powtarzalnych badań obliczeniowych

10 prostych zasad uczynienia badań obliczeniowych bardziej powtarzalnymi w oparciu o [Sandve i in., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), to:

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

<p align="center"><i>Infografika zaadaptowana z Sandve i in., (2013). Ściągnij to i wydrukuj, aby móc się przydać podczas swoich badań!</i></p>

  


Jeśli wykonasz te kroki wraz z procesami w [**Zadanie 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) i [**Zadanie 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), powinieneś mieć się dobrze!

  


## Licencja Open Source <a name="Licensing"></a>

Licencja Open Source jest rodzajem licencji zaprojektowanej specjalnie dla oprogramowania i kodu, która wyraźnie określa, jakie są prawne warunki udostępniania i ponownego wykorzystania. Jak wspomniano [powyżej](#What_OSS), dodanie odpowiedniej licencji jest co odróżnia publicznie udostępniane oprogramowanie z OSS. Na przykład szeroko stosowany program [MATLAB](https://www.mathworks.com/products/matlab.html) jest oprogramowaniem zastrzeżonym, a [Octave](https://www.gnu.org/software/octave/) jest otwartym, licencjonowanym alternatywnym językiem programowania.

Obecnie istnieje ponad 1400 unikalnych licencji Open Source, złożoność wynikająca z trudności w zrozumieniu różnic między implikacjami prawnymi różnych licencji.

Niektóre z bardziej popularnych licencji to:

- [Berkeley Software Distribution („BSD”)](https://en.wikipedia.org/wiki/BSD_licenses),
- [Apache](https://www.apache.org/licenses/LICENSE-2.0),
- [stylu MIT (Massachusetts Institute of Technology)](https://opensource.org/licenses/MIT)lub
- [Licencja GNU General Public License („GPL”)](https://www.gnu.org/licenses/gpl-3.0.en.html).

Nie musisz znać całego legalnego problemu, ale dobrze jest przynajmniej wiedzieć, jakie opcje są dla ciebie dostępne.

Istnieją dwa sposoby uzyskania licencji na projekt:

1. *Wyraźnie*, przy czym indywidualny wkład ma wyraźnie wskazaną licencję niezależną od głównego projektu; lub
2. *Bezwarunkowo*, przy czym wkład podlega pierwotnemu kodowi licencyjnemu głównego projektu.

Na szczęście proces wyboru licencji Open Source jest stosunkowo trywialny dzięki przyjaznym dla użytkownika narzędziom, takim jak [Wybierz licencję](https://choosealicense.com/). Każda z tych licencji pozwala innym użytkownikom na używanie, kopiowanie, rozpowszechnianie i rozbudowę Twojej pracy, często zapewniając jednocześnie, że twórcy są odpowiednio rozpoznawani za swoją pracę. W tym przypadku kluczem jest wybór odpowiedniej licencji dla swojej pracy, w zależności od tego, co chcesz lub nie chcesz, aby inni z nią zrobili.

  


## Cytowanie oprogramowania <a name="Citation"></a>

Cytaty stanowią jedną z najważniejszych interakcji w badaniach naukowych, stanowiąc podstawę naszych systemów odniesienia i metryk. Zazwyczaj jest to wykonywane dzięki pomocy stałego unikalnego identyfikatora, takiego jak [cyfrowych identyfikatorów obiektów](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). DOI to trwały identyfikator, zaimplementowany w systemie [Handle System](https://en.wikipedia.org/wiki/Handle_System), który spełnia wspólny standard, w zależności od celu, na przykład w celu identyfikacji informacji akademickich. Taka identyfikacja ma kluczowe znaczenie dla śledzenia genealogii i pochodzenia badań, dla ich powtarzalności, a także dla przyznania odpowiedniego kredytu tym, którzy stworzyli oprogramowanie. Co ważne, oprogramowanie należy uznać za uzasadniony wynik badań naukowych, a cytowanie staje się coraz bardziej powszechnym sposobem na to.

W 2016, [Smith i in., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) napisali artykuł badawczy na temat zasad cytowania oprogramowania w ramach Grupy Roboczej ds. Cytowań Oprogramowania FORCE11. W taki sam sposób, w jaki chciałbyś cytować oprogramowanie, którego używałeś w ramach dobrych praktyk badawczych, ważne jest, aby twoje badania były łatwe do cytowania. Powołując się na dowolne oprogramowanie używane do własnych badań, powinieneś podać co najmniej:

- Imię i nazwisko autora,
- Tytuł oprogramowania,
- Numer wersji i
- Unikalny identyfikator / lokalizator (DOI lub URL).

Sześć zasad cytowania oprogramowania przez [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) jest podanych tutaj:

- **Znaczenie**: Oprogramowanie powinno być uważane za legalny i cytowalny produkt badań. Cytowania oprogramowania powinny mieć takie samo znaczenie w dokumentacji naukowej, jak cytaty z innych produktów badawczych, takich jak publikacje i dane; powinny być uwzględnione w metadanych pracy cytującej, na przykład na liście referencyjnej artykułu w czasopiśmie, i nie powinny być pomijane ani rozdzielane. Oprogramowanie powinno być cytowane na tej samej podstawie, co każdy inny produkt badawczy, taki jak papier lub książka, to znaczy autorzy powinni cytować odpowiedni zestaw oprogramowania, tak jak cytują odpowiedni zestaw dokumentów.

- **Kredyt i przypisanie**: Cytaty dotyczące oprogramowania powinny ułatwiać udzielanie kredytów naukowych i normatywnych, prawnych przypisań wszystkim współpracownikom oprogramowania, uznając, że pojedynczy styl lub mechanizm przypisania może nie mieć zastosowania do całego oprogramowania.

- **Wyjątkowa identyfikacja**: Cytat z oprogramowania powinien zawierać metodę identyfikacji, która jest możliwa do działania maszynowo, unikatowa w skali globalnej, interoperacyjna i rozpoznawana przez przynajmniej społeczność odpowiednich ekspertów domeny, a najlepiej przez badaczy publicznych.

- **Wytrwałość**: Unikalne identyfikatory i metadane opisujące oprogramowanie i jego rozmieszczenie powinny się utrzymywać - nawet poza okresem życia opisywanego oprogramowania.

- **Dostępność**: Cytaty dotyczące oprogramowania powinny ułatwiać dostęp do samego oprogramowania i związanych z nim metadanych, dokumentacji, danych i innych materiałów niezbędnych ludziom i maszynom do świadomego korzystania z odnośnego oprogramowania.

- **Specyfika**: Cytowania oprogramowania powinny ułatwiać identyfikację i dostęp do konkretnej wersji oprogramowania, które było używane. Identyfikacja oprogramowania powinna być tak szczegółowa, jak to konieczne, na przykład przy użyciu numerów wersji, numerów wersji lub wariantów takich jak platformy.

Uwaga: Aby uzyskać instrukcje „jak zrobić swoje oprogramowanie cytatem”, zobacz sekcję [**Korzystanie z GitHub i Zenodo**](#GitHub_Zenodo) poniżej i [**Zadanie 2: Łączenie GitHub i Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## Korzystanie z GitHub i Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) to popularne narzędzie do zarządzania projektami, przechowywania treści i kontroli wersji. Zauważ, że sam GitHub nie jest OSS. Jednak Git, narzędzie, na którym się opiera, jest. Git został zaprojektowany, aby pomagać w zarządzaniu plikami kodu źródłowego i aktualizacjami do nich w związku z projektem związanym z oprogramowaniem. Można go jednak rozszerzyć także na inne projekty niezwiązane z oprogramowaniem; na przykład [MOOC](https://github.com/OpenScienceMOOC/)!

Jednak wprowadzenie badań na GitHub to tylko pierwszy krok. Równie ważne jest, aby był on trwały i można go było ponownie wykorzystać, dlatego przydatny może być skojarzony z nim cyfrowy identyfikator obiektu (DOI). Najprostszym sposobem na to jest skorzystanie z usługi o nazwie [Zenodo](https://zenodo.org/), która jest darmowym i wielodyscyplinarnym repozytorium utworzonym przez OpenAIRE i CERN i może być użyta do przypisania DOI do poszczególnych repozytoriów GitHub. Istnieje przewodnik [GitHub](https://guides.github.com/activities/citable-code/) który wyjaśnia szczegóły, które wiążą repozytoria GitHub bezpośrednio z Zenodo, dzięki czemu, gdy programiści tworzą formalne wersje oprogramowania, Zenodo tworzy i archiwizuje tę wersję oprogramowania.

Nie ma nic specjalnego w używaniu Zenodo do tworzenia DOI, innych niż **za darmo**; można również użyć innych repozytoriów ogólnych, takich jak [DataCite DOI Fabrica](https://doi.datacite.org/)lub własne repozytoria instytucjonalne, takie jak [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

Wielu naukowców zazwyczaj obawia się udostępniania kodu, który jest niekompletny, wadliwy lub niedoskonały. Jednak w społeczności OSS taka praktyka udostępniania „surowego” kodu jest dość powszechna. Dzielenie się kodem otwarcie umożliwia innym ponowne wykorzystanie i udoskonalenie go, a także głębsze zaangażowanie w badania związane z nim. Jest to jeden z podstawowych aspektów współpracy partnerskiej, najlepiej na przykładzie tradycyjnego procesu recenzowania rękopisów.

Zadanie 2 poprowadzi Cię przez proces łączenia repozytorium GitHub z Zenodo w celu archiwizacji.

> **Czy wiesz, że ...** Cała zawartość stworzona dla tego MOOC jest dostępna jako część społeczności w [Zenodo](https://zenodo.org/communities/open-science-mooc/)?

**[PRZEJDŹ DO ZADANIA 2: Łączenie GitHub i Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## Współpraca i współtworzenie poprzez Open Source <a name="Collaborating"></a>

Często OSS jest rozwijany w sposób publiczny, zdecentralizowany i oparty na współpracy między wieloma współpracownikami. Celem tego jest zwiększenie różnorodności i zakresu projektu i jego projektu, aby stać się bardziej korzystnym i zrównoważonym. Takie podejście słynęło z modelu „bazaru” autorstwa Erica Raymonda, wczesnego zwolennika OSS. Jedną z głównych zasad przewodnią jest to, że od **równorzędnego produkcji**, która polega na samoorganizujących się społeczności regulować rozwój treści, koordynowane w kierunku wspólnego celu lub rezultatu.

Projekty OSS polegają w dużej mierze na współpracy wolontariuszy, co często pociąga za sobą ciągły przepływ nowych osób, aby stały się produktywne i zrównoważone ([Steinmacher i in., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Stworzenie odpowiedniej atmosfery społecznej dla projektu i przyjazne środowisko zaangażowania często mają kluczowe znaczenie dla udanej współpracy w OSS.

  


## Gdzie iść stąd <a name="Future_OSS"></a>

Mam nadzieję, że teraz dostrzegłeś znaczenie oprogramowania jako fundamentu nowoczesnej nauki i znaczenie, jakie odgrywa w tym OSS.

**efektów uczenia się** z tego powinno być:

1. Będziesz teraz w stanie zdefiniować cechy OSS i niektóre argumenty dotyczące etycznego, prawnego, ekonomicznego i badawczego wpływu na i przeciw.

2. Opierając się na standardach społeczności, będziesz mógł opisać wymagania jakościowe dotyczące udostępniania i ponownego używania otwartego kodu.

3. Teraz będziesz mógł korzystać z szeregu narzędzi badawczych wykorzystujących OSS.

4. Teraz będziesz mógł przekształcić kod przeznaczony do ich osobistego użytku w kod, który jest dostępny i może być ponownie używany przez innych.

5. Deweloperzy oprogramowania będą mogli tworzyć swoje oprogramowanie, a użytkownicy oprogramowania będą wiedzieć, jak cytować oprogramowanie, którego używają.

  


**ZADANIE BONUS**

Jeśli ukończyłeś [Zadanie 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) i [Zadanie 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), mamy również **ZADANIE BONUSU** , jeśli chcesz posunąć swoje umiejętności o krok dalej. [Zadanie 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) przybliży Cię do integracji Git z typowym przepływem pracy badawczej, pokazując, jak zintegrować go z R Studio. Zaleca się wykonanie pierwszych 2 zadań przed kontynuowaniem tego zadania.

Jednak podróż Open Source nie kończy się tutaj! To był dopiero początek, a jeśli chcesz zrobić lub dowiedzieć się więcej, możesz skorzystać z niesamowitych zasobów:

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

*Te odniesienia są tylko początkiem. Obejmują one niektóre z najbardziej przydatnych ogólnych przeglądów krajobrazu Open Source w badaniach. Jeśli jednak chcesz znaleźć coś bardziej specyficznego dla swojej dziedziny badań, ta ścieżka jest do odkrycia!*

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

**Wiesz, w jaki sposób można poprawić tę zawartość?**

Czas wziąć swoje nowe umiejętności GitHub na próbę! Cały rozwój treści odbywa się przede wszystkim [tutaj](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). Jeśli masz sugerowane ulepszenie treści, układu lub czegokolwiek innego, możesz to zrobić, a następnie automatycznie stanie się częścią treści MOOC po weryfikacji od moderatora!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)