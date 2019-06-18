---
output:
  html_document: domyślna
  pdf_document: domyślna
---

# Zadanie 3: Jak zintegrować Git z R Studio

To zadanie jest przeznaczone dla studentów i naukowców, którzy chcą wdrożyć system kontroli wersji w ramach standardowego przepływu pracy opartego na R. Można to zastosować do szeregu prac programistycznych, analizy danych i zarządzania projektami. Twoje przyszłe samodzielne badania będą wdzięczne za wygodę.

Nie zapomnij, że możesz dołączyć do dyskusji na naszym otwartym [**Slack channel**](https://osmooc.herokuapp.com/). Przedstaw się w # module5opensource i powiedz nam trochę o tym, kim jesteś, swoim tłem i tym, jak się tu znalazłeś!

Szacowany czas realizacji: 30 minut

Oszczędność czasu po zakończeniu: praktycznie nieskończona

**UWAGA** Wersja przewodnika wideo tego zadania jest teraz dostępna w [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA).

## Spis treści

* [Rozpoczęcie](#Getting_started) 
  * [Git](#Git)
  * [R Studio](#Rstudio)
* [Krok pierwszy: Pobierz wszystkie rzeczy](#one)
* [Krok drugi: Skonfiguruj Git wewnątrz RStudio](#two)
* [Krok trzeci: Dlaczego to zrobiłem?](#three)
* [Krok czwarty: idealne małżeństwo między Git i R](#four)
* [Krok piąty: pobieranie treści z treścią](#five)
* [Krok szósty: Odważne zaangażowanie](#six)
* [Krok siódmy: PUSH!](#seven)

## Rozpoczęcie <a name="Getting_started"></a>

Gratulacje, że udało nam się dotrzeć tak daleko! Jeśli to czytasz, przetrwałeś żądania ściągania, haki sieciowe i prawdopodobnie możesz nawet powiedzieć nam, co oznacza skrót F w FOSS (*nie* Frustracja ...) Mam nadzieję, że pokonałeś sceptycyzm lub niechęć w kierunku korzyści płynących z GitHub i oprogramowania Open Source i jesteśmy gotowi do podjęcia kolejnego kroku.

Przed rozpoczęciem tego zadania upewnij się, że ukończyłeś już [Zadanie 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) i [Zadanie 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), dzięki czemu będziesz lepiej zaznajomiony z GitHub i niektórymi standardowymi praktykami Open Source.

To zadanie nauczy Cię, jak zintegrować oprogramowanie do kontroli wersji, Git, z popularnym środowiskiem kodowania, RStudio. I tak, to Git jak w gif lub Bóg, nie Jit jak w złym sposobie wymawiania rzeczy.

Jeśli jesteś jednym z tych naukowców, którzy uważają, że mając kod rozproszony na wielu dyskach twardych, które czekają na złamanie, Dropbox, Dysk Google lub inne nie wyspecjalizowane oprogramowanie, zadanie to jest właśnie dla Ciebie. Jeśli kiedykolwiek doświadczyłeś paraliżującego umysłu procesu posiadania wielu „ostatecznych” wersji papieru odbijających się od różnych współautorów, jest to również dla ciebie.

Wszyscy jesteśmy winni tego rodzaju rzeczy raz na jakiś czas, ale są sposoby, aby to zrobić lepiej dla ciebie, dla ciebie i dla tych, którzy mogą skorzystać z twojej pracy.

  


### Pierwsze Git <a name="Git"></a>

Czym jest Git i czym różni się od GitHub? Git to system kontroli wersji, który umożliwia zapisywanie i śledzenie stemplowanych czasowo kopii swojej pracy w całym procesie tworzenia. Działa również z elementami nie kodowanymi, takimi jak MOOC, z których większość została napisana markdown w RStudio i zintegrowana z przepływem pracy Git / GitHub.

Jest to ważne, ponieważ wszystkie badania przechodzą zmiany i czasami chcemy wiedzieć, co to było. Czy usunąłeś jakiś tekst, który teraz uważasz za ważny? Kontrola wersji pozwoli Ci to zaoszczędzić. Czy twój kod działał doskonale w przeszłości, ale teraz jest niewiarygodny? Kontrola wersji. To świetny sposób na uniknięcie tego chaotycznego stanu, w którym masz wiele kopii tego samego pliku, ale bez głupiej i irytującej konwencji nazewnictwa plików. `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` będzie przeszłością.

GitHub to platforma, która pozwala na bezproblemowe współdzielenie kodu z obszaru roboczego (np. Laptopa) do hostingu w przestrzeni online. Tak jakby przypominał publiczny interfejs do GitHuba. Zalety Git / GitHub to:

1. Możesz zachować kopie całej swojej pracy w czasie;
2. Możesz porównać pracę przez różne kopie w czasie, co pomaga wykryć błędy lub błędy;
3. Inni ludzie mogą współpracować otwarcie z twoją pracą;
4. Masz zarówno lokalną, jak i online kopię swojej pracy, która pozostaje zsynchronizowana;
5. Jest całkowicie przejrzyste, kto wniósł swój wkład, dlaczego to zrobił i kiedy; i
6. Możesz mieć jednocześnie wiele osób pracujących nad tym samym projektem jednocześnie.

Chociaż był on zaprojektowany przede wszystkim dla kodu źródłowego, powinien być natychmiast oczywisty, jak to stanie się potężnym narzędziem dla praktycznie wszystkich procesów badawczych.

  


### RStudio <a name="Rstudio"></a>

RStudio jest popularnym środowiskiem kodowania dla naukowców, którzy używają języka programowania statystycznego, R. Jest dostarczany z edytorem tekstu, więc nie musisz instalować innego i przełączać się między nimi. Zawiera również graficzny interfejs użytkownika (GUI) do Git i GitHub, z którego będziemy korzystać tutaj.

Czy to nie miłe, gdy genialne narzędzia Open Source bezproblemowo się integrują. To powinno znacznie ułatwić codzienne korzystanie z Git.

Jeśli w dowolnym momencie musisz zainstalować nowe pakiety dla R, użyj następującego polecenia:

`install.packages („PACKAGE NAME”, zależności = TRUE)`

Zastępując `PACKAGE NAME` nazwą, er, package. Niektóre przykłady, które mogą się przydać, mogą zawierać `knitr`, `devtools` lub `ggplot2`.

  


## Krok pierwszy: Pobierz wszystkie rzeczy <a name="one"></a>

1. Powinieneś mieć już konto GitHub, jeśli wykonałeś poprzednie zadania. Jeśli nie, [zarejestruj się tutaj](https://github.com/). Bezpłatne nieograniczone repozytoria dla wszystkich!
2. Pobierz i zainstaluj najnowszą wersję [R](https://www.r-project.org/). Dostępne również dla [Mac](https://cloud.r-project.org/) i [Linux](https://cloud.r-project.org/bin/linux/).
3. Pobierz i zainstaluj najnowszą wersję [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop). Oh, hej, wygląda na Open Source! Śmigać.
4. Pobierz i zainstaluj najnowszą wersję [Git](https://gitforwindows.org/). **Pamiętaj, aby podczas instalacji wybrać „Użyj Git z wiersza polecenia systemu Windows”.**

> **Pro-tip**: Aby zaktualizować wszystkie pakiety R w jednym, po prostu wykonaj następujący kod `update.packages (ask = FALSE, checkBuilt = TRUE)`

Na razie wybierz wszystkie standardowe opcje dla każdej instalacji. W zależności od systemu operacyjnego (np. Mac, Windows, Linux) może to być inne dla każdego z was. Na razie, i do końca tego zadania, będziemy trzymać się rzeczy łatwych w użyciu systemu Windows (ale także podać instrukcje dotyczące używania wiersza poleceń).

Dla użytkowników Linuksa lub Debiana, użyj następującego polecenia, aby zainstalować Git:

`sudo apt-get install git-core`

Dla użytkowników komputerów Mac, [to łącze](http://git-scm.com/download/mac)lub zakup nowego laptopa z innym systemem operacyjnym.

Jeśli chcesz, możesz także pobrać lokalną wersję [GitHub](https://desktop.github.com/) i użyć jej w prostym GUI. Jest dostępny w systemach Windows i Mac oraz Linux i może nieco ułatwić Ci życie, zwłaszcza jeśli chcesz użyć innej platformy niż RStudio.

> **Pro-tip:** Widzisz, gdy instalujesz Git, mówi: „Używaj Git Bash jako powłoki dla projektów Git? To jest miejsce, w którym możesz użyć wiersza poleceń, aby uzyskać dostęp do Git spoza RStudio. To potężna bestia. Wypróbuj następujące dwa polecenia, aby rozpocząć:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


## Krok drugi: Skonfiguruj Git wewnątrz RStudio <a name="two"></a>

Racja, to proste zadanie. Następnie przejdź do RStudio i na zakładkach u góry przejdź do Idź do **Narzędzia> Opcje globalne> Git / SVN**. SVN to kolejny system kontroli wersji, taki jak Git, i nie musimy się o to martwić.

W miejscu gdzie jest napisane *Git wykonywalny*, należy dodać ścieżkę do pliku tutaj git.exe że po prostu pobranego w poprzednim kroku. Upewnij się, że pole, które mówi **Włącz interfejs kontroli wersji dla projektów RStudio** jest zaznaczone. Teraz powiązano kontrolę wersji z przyszłymi projektami w RStudio, aby zapewnić naprawdę potężny dodatkowy wymiar pracy zespołowej lub solowej.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>Okno Opcje globalne w RStudio</i></p>

  


Następnie naciśnij przycisk w tym oknie, który mówi: *Utwórz klucz RSA*, Jest to klucz prywatny, który jest używany do uwierzytelniania między różnymi systemami i oszczędza ci konieczności wielokrotnego wpisywania hasła. Tutaj pojawi się nowe okno z kluczem publicznym, który chcesz skopiować do schowka.

Udaj się do GitHub, przejdź do ustawień swojego profilu oraz na kartę *kluczy SSH i GPG*. Kliknij *Nowy klucz SSH*. Tutaj wklej klucz z RStudio i nazwij go czymś wyobraźni, takim jak „RStudio”.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>Wewnątrz GitHub, gdzie będziesz chciał wprowadzić klucz, który właśnie wygenerowałeś w RStudio</i></p>

  


OK, teraz trzymaj się tyłek, wchodzimy do linii poleceń. Nie martw się, jeśli nigdy wcześniej nie korzystałeś z powłoki, ponieważ jest ona bardzo podobna do używania R lub innego systemu kodowania. Główną różnicą jest jednak to, że zamiast wywoływać funkcje takie jak w R, wywołujesz polecenia.

Wracając do RStudio, przejdź do **Narzędzia> Powłoka**, a otworzy się okno wiersza polecenia. Jeśli grałeś już z Git Bash powyżej, powinieneś już wykonać ten krok. Wprowadź następujące dwa polecenia:

`git config --global user.name 'YOUR USERNAME'`   
`git config --global user.email 'YOUR EMAIL'`   


Mam nadzieję, że nie trzeba tutaj mówić o zastępowaniu własnej nazwy użytkownika i adresu e-mail GitHub. Możesz uzyskać do niego dostęp w dowolnym momencie, tylko poprzez znalezienie „powłoki” w systemie Windows. Lub, jeśli klikniesz prawym przyciskiem myszy na dowolnym folderze na pulpicie, który jest powiązany z repozytorium GitHub, możesz natychmiast otworzyć Shell i Bash away.

Tym etapem jest konfiguracja Git, czyli oprogramowania działającego na twoim pulpicie, na GitHub, który jest witryną repozytorium.

Uruchom ponownie R Studio. Uff, to było trudne. Kolejny.

  


## Krok trzeci: Dlaczego to zrobiłem? <a name="three"></a>

OK, wstrzymaj oddech, zatrzymamy się tutaj, aby nauczyć się podstawowych poleceń Gita. Niektóre z kluczowych elementów, które możesz zrobić podczas nauki to:

* **Dodaj**: Tutaj przesyłasz pliki do obszaru przemieszczania przed zatwierdzeniem.

* **Zatwierdź** To jest jak „zapisywanie” swojej pracy, tworząc nową wersję lub kopię.

* **Push**: W ten sposób wysyłasz pliki z lokalnego projektu do repozytorium online.

* **Ciąg**: W ten sposób można uzyskać pliki z repozytorium online do lokalnego projektu.

Powrót w RStudio wpisz następujące do *Terminalu*, lub poprzez otwarcie nowego Shell:

`git dodaj.`

Na razie nie zrobi niczego, ale w przyszłości doda wszystkie pliki w bieżącym katalogu roboczym (tak robi `` ) do gotowości do zatwierdzenia.

  


## Krok czwarty: idealne małżeństwo między Git i R <a name="four"></a>

Teraz w Zadaniu 1 powinieneś dowiedzieć się, jak zbudować swoje pierwsze repozytorium GitHub. Jeśli tego nie zrobiłeś, możemy poczekać tutaj, kiedy idziesz i to zrobić. Jeśli już masz lub masz już repozytorium GitHub, możemy przejść dalej.

Więc powinieneś mieć repozytorium w GitHub, wraz z plikiem `README` plikiem `LICENSE` i kilkoma innymi bitami i bobami.

Teraz zamierzamy zintegrować to repozytorium z Git. Spokojnie teraz.

1. Najpierw przejdź do **Projekt> Utwórz projekt> Kontrola wersji> Git**.
2. Po powrocie do GitHub powinieneś zobaczyć trochę adresu URL https: //. To jest link do twojego repozytorium i daje ci możliwość klonowania go na pulpicie. Na razie po prostu skopiuj ten link, przełącz się z powrotem na RStudio i wklej go w „URL repozytorium”, jak wskazano.
3. Nadaj projektowi nazwę katalogu, na przykład test, Jim lub cokolwiek innego.
4. Następnie przejdź do miejsca na pulpicie, w którym chcesz uruchomić ten projekt, jego podkatalogu.
5. Kliknij „Utwórz projekt” i pozwól magii się skończyć!

Właśnie powiedziałeś RStudio, aby skojarzył nowy projekt w R z konkretnym repozytorium w GitHub.

## **Krok czwarty: alternatywa**

Jeśli nadal nie zbudowałeś swojego pierwszego repozytorium na GitHub, możemy zrobić coś nieco innego tutaj. W RStudio kliknij *Nowy projekt* a następnie *Nowy katalog*. Nazwij to, co chcesz i zmień katalog w razie potrzeby, upewnij się, że zaznaczysz *Utwórz repozytorium git*, a następnie kliknij *Utwórz projekt*. Tworzy to plik `.Rproj` , który można zarządzać w zwykły sposób za pomocą RStudio, w tym dodając `pliki README.md`i `LICENSE.md` jako omówienie w zadaniu 1.

## Krok piąty: pobieranie treści z treścią <a name="five"></a>

Pamiętasz ten plik `README` , który stworzyliśmy jakiś czas temu? Czas to napisać. Wracając do zadania 1, były pewne konkretne rzeczy, które, jak powiedzieliśmy, tworzą dobry plik `README`. Pamiętasz co z nich było? Aby odświeżyć pamięć, były to:

* O czym jest ten projekt i co robi.
* Dlaczego ludzie powinni się troszczyć i dlaczego jest to przydatne.
* Jak ktoś może zacząć przyczyniać się do projektu.
* Z kim można się skontaktować, jeśli ktoś potrzebuje pomocy.
* Łącze do licencji, wytycznych i kodeksu postępowania.
* Opis struktury projektu.
* Kto jest zaangażowany i jakie są ich role.
* Aktualny stan projektu.

W RStudio otwórz ten plik i spróbuj dodać trochę informacji o tym dla swojego projektu. Jeśli robisz to dla rzeczywistego projektu, spróbuj go uczynić użytecznym. Jeśli na razie majsterkowujesz, możesz dodać to, co chcesz.

Pamiętaj, że Twój plik `README` jest w formacie przeceny (.md). Dla przypomnienia niektórych prostych sposobów użycia składni, sprawdź ten [przydatny arkusz](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>Zrzut ekranu na temat tego, co ten moduł wygląda na przecenie, podczas tworzenia. Meta.</i></p>

  


## Krok szósty: Odważne zaangażowanie <a name="six"></a>

OK, więc powinieneś mieć ładnie edytowany plik `README`. Teraz zamierzamy „przypisać” to do projektu za pomocą Git. Jest to w zasadzie odpowiednik zapisania tej wersji projektu, wraz z zapisem zmian. Kolejne zobowiązania tworzą historię, którą można zbadać w późniejszym czasie, pozwalając ci pracować z ufnością.

Jest na to kilka sposobów.

1. Przejdź do **Narzędzia> Kontrola wersji> Zatwierdź**
2. W panelu środowiska w RStudio powinna znajdować się nowa karta „Git”. Poręczny.
3. W twoim panelu konsoli powinien być teraz nowy „Terminal”, przez który możesz uruchamiać linie poleceń Gita.

Trzymajmy się na razie drugiej opcji. To okienko Git pokazuje, które pliki zostały zmienione i zawiera przyciski najważniejszych poleceń Gita, które widzieliśmy wcześniej.

Wybierz plik `README` w oknie Git, który powinien pojawić się automatycznie, jeśli dokonałeś w nim jakichkolwiek zmian. Powoduje to dodanie tego pliku do obszaru „przemieszczania”, który przypomina coś, co pozwala zaoszczędzić miejsce na pracę. Kliknij „Zatwierdź” i pojawi się nowe okno.

Tutaj masz szansę przejrzeć zmiany i napisać miłą wiadomość zatwierdzenia. Wpisz coś krótkiego, ale informuj o zmianach wprowadzonych w tej wersji lub migawce swojej pracy. Chcesz, aby informacje były wystarczające, abyś ty lub ktoś inny spojrzał na to z powrotem, wiesz, dlaczego dokonałeś tego zatwierdzenia i zmian z nim związanych. Są to siatki bezpieczeństwa dla twojego projektu na wypadek, gdybyś musiał z jakiegoś powodu wycofać się.

> **Pro-tip**: Tutaj zobaczysz listę wszystkich zmian dokonanych od ostatniego zatwierdzenia. Starsze usunięte linie są czerwone, a nowo dodane linie są zielone. Sprawdź je dwukrotnie, aby upewnić się, że zmiany, które wprowadziłeś, są tymi, które zamierzasz wprowadzić. Jest to bardzo pomocne w wykrywaniu literówek, bezpańskich edycji i innych drobnych błędów, które przypadkowo wprowadziłeś. Bezpieczeństwo przede wszystkim.

**Uwaga** Jeśli jesteś w ciemno i nie widzisz, które linie zostały dodane lub usunięte, możesz użyć numerów linii w dwóch kolumnach po lewej stronie okna jako przewodnika. Tutaj liczba w pierwszej kolumnie identyfikuje starszą wersję, a liczba w drugiej kolumnie określa nową wersję.

Teraz, gdy klikniesz „Zatwierdź”, pojawi się kolejne okno z informacją, ile plików zmieniłeś i ile linii w tym pliku zmieniłeś. Zamknij to małe okno.

  


## Krok siódmy: PUSH! <a name="seven"></a>

Kliknij przycisk *Push* w prawym górnym rogu nowego okna. Pojawi się teraz nowe okno. To, co to robi, to synchronizacja plików zmienionych w lokalnym repozytorium z plikiem `README` do wersji online projektu na GitHub.

Aby to zrobić z powłoki, użyj następującego polecenia:

`git push -u origin master`

Czasami zostaniesz poproszony o dodanie nazwy użytkownika i hasła z GitHub, co powinieneś zrobić, jeśli zostaniesz o to poproszony.

Zamknij to okno i następne. Przejdź do swojego projektu na GitHub, odśwież i sprawdź, czy plik `README` jest nadal obecny w całej nowo edytowanej chwale. Powinieneś zobaczyć także komunikat zatwierdzenia, który zrobiłeś obok pliku.

  


**OPCJONALNIE ZAAWANSOWANY / NIESAMOWITY KROK**

W porządku, więc po prostu wrzuciłeś trochę treści do swojego pierwszego repo, niesamowite! Teraz zastosujmy to do prawdziwego projektu. Na przykład ten, w którym teraz uczestniczysz. Wypróbujmy to:

1. Przejdź do repozytorium dla tego projektu na [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)

2. Rozwiń repozytorium na własne konto GitHub. Adres URL dla tego powinien być: `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. Wejdź do RStudio, przejdź do **Plik> Nowy projekt**, wybierz *Kontrola wersji*, wybierz *Git*, a następnie wklej widelecowy adres URL repozytorium znaleziony w twojej kopii repozytorium. Masz teraz własną wersjonowaną kopię tego całego modułu. Schludny. Zapisz to gdzieś na lokalnym komputerze.

4. Teraz musisz powiedzieć Gitowi, że istnieje inna wersja tego projektu. Otwórz *Shell*i wprowadź polecenie: `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. To, co właśnie zrobiłeś, to nazwa oryginalnej gałęzi tutaj `górę`, tylko po to, by na razie zachować prostotę. Teraz utwórz nową **oddział** do dokumentowania zmian w tym niezależny od głównego oddziału. Wpisz komendę: `git checkout -b proponowane-zmiany wzorzec`

6. Właśnie utworzyłeś nowy oddział o nazwie `proponowanych zmian` którym możesz teraz edytować wszystkie treści i pliki z zachwytem. Mam nadzieję, że struktura tego projektu jest na tyle prosta, że można go poruszać. Wszystkie pliki raw dla MOOC można znaleźć w folderze `content_development` , a to jest `Task_3.md`.

7. Jeśli przewiniesz do dołu `Task_3.md`, powinieneś zobaczyć miejsce, w którym możesz edytować swoje imię i przynależność. Dodaj je, a następnie wykonaj procedurę zatwierdzania opisaną powyżej. Jeśli zobaczysz coś jeszcze, co wymaga również edycji, możesz je również dodać!

8. Teraz chcesz przenieść zmiany z powrotem do oryginalnej gałęzi. Użyj następującej komendy w swojej *Powłoce*: `git push pochodzenie proponowane zmiany`

9. Wróć do GitHub i znajdź tutaj swój widelec. Kliknij mały zielony przycisk i utwórz żądanie ściągnięcia. Jest to zasadniczo przegląd integracji zmian wprowadzonych w pierwotnym oddziale tego projektu MOOC.

10.     Właściciele odpowiedzialni za projekt MOOC otrzymają teraz powiadomienie o tym, przejrzą go i potwierdzą, jeśli wszystko pójdzie zgodnie z planem! Przejrzymy go i jeśli wszystko pójdzie dobrze, twoje imię pojawi się teraz na całą wieczność jako ktoś, kto ukończył to zaawansowane zadanie.
      

11.     Zjedz filiżankę herbaty, kawy lub wina, aby świętować!
      

**GRATULACJE**

Właśnie zintegrowałeś Git z R Studio i dokonałeś pierwszej zmiany w projekcie kontrolowanym przez wersję. Twoje życie nigdy nie będzie takie samo, a twój przepływ pracy badawczej będzie prawdopodobnie szybszy, sprawniejszy i bardziej kolaboracyjny niż kiedykolwiek. Powodzenia w powrocie do Worda.

Wspaniałą rzeczą jest to, że nie musi to być tylko kod. Możesz go używać do zwykłego tekstu, znaczników, html i, cóż, kodu R. Możliwości są nieograniczone - to, czego się właśnie nauczyłeś, to nowa forma otwartego, opartego na współpracy zarządzania projektami, która działa w ogromnym zakresie zadań.

Od teraz wszystko zależy od Ciebie! Porady to:

* Rób częste zobowiązania. Traktuj Gita jak swojego szczeniaka, ponieważ wymaga stałej i szczególnej uwagi. Wystarczy poklepać po głowie co jakiś czas, aby utrzymać go w pełni, ale będzie to najszczęśliwsze dzięki długotrwałej obsłudze.

* Najlepszym sposobem na to jest zatwierdzenie za każdym razem, gdy pracujesz nad konkretnym problemem. Na przykład pisanie akapitu, przeprowadzanie analizy lub naprawianie błędu.

* Pchaj często. Nie dopuść do tego, aby te zobowiązania się zwiększyły, w przeciwnym razie ryzykujesz konfliktami. Widząc, że mogą to być koszmary, po prostu pchaj się często.

* Ciągnij często. Jeśli inni pracują zdalnie w tym samym projekcie, będziesz chciał być na bieżąco ze zmianami. Pamiętaj, aby często wprowadzać zmiany z GitHub, aby upewnić się, że wszyscy jesteście zsynchronizowani.

* Eksperymentuj i eksploruj! To zadanie naprawdę tylko zarysowuje powierzchnię i istnieje wiele różnych funkcji, narzędzi i sposobów, w jakie można to wykorzystać. Naprawdę to od Ciebie zależy, jak wykorzystać te informacje do usprawnienia pracy badawczej, a ostatecznie do współpracy w zakresie lepszych, bardziej otwartych i wiarygodnych badań!

* Aby dowiedzieć się więcej na temat problemów, gałęzi, konfliktów łączenia, żądań ściągania i innych zaawansowanych aspektów korzystania z Git i RStudio, sprawdź ten [niesamowity przewodnik](http://r-pkgs.had.co.nz/git.html) autorstwa Hadley Wickham.

  


**Wiesz, w jaki sposób można poprawić tę zawartość?**

Czas wziąć swoje nowe umiejętności GitHub na próbę! Cały rozwój treści odbywa się przede wszystkim [tutaj](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md). Jeśli masz sugerowane ulepszenie treści, układu lub czegokolwiek innego, możesz to zrobić, a następnie automatycznie stanie się częścią treści MOOC po weryfikacji od moderatora!

## Lista uczestników, którzy ukończyli ADVANCED wersję tego zadania

* Brendan Palmer, CRF-C, University College Cork
* Lisa Matthias, Freie Universität Berlin
* Hollie Marshall, University of Leicester 
* Eric D. Wilkey, Western University, Kanada
* José-Raúl Canay-Pazos, Universidade de Santiago de Compostela, Hiszpania
* Encarnación Martínez Álvarez, Hiszpania
* Alberto Albz Marocchino, Włochy
* Iratxe Rubio, Baskijskie Centrum Zmian Klimatu BC3
* Gabriele Orlandi, Paris School of Advanced Studies in Social Sciences (EHESS), Francja
* Hande Sodacı, Turcja
* Luke W. Johnston, Aarhus University, Dania
* Philippe Joly, WZB i HU-Berlin
* Paul Griffiths, NCAS i U. Cambridge
* Harin Lee, Goldsmiths, University of London
* Luis Camacho, Uniwersytet Katolicki, Perú
* Tom Cridford, Imperial College London
* Nithiya Streethran, Uniwersytet w Stavanger 

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)