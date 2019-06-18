---
output:
  html_document: domyślna
  pdf_document: domyślna
---

# Zadanie 1: Jak skonfigurować repozytorium na GitHub

To zadanie jest przeznaczone dla studentów i naukowców, którzy chcą stworzyć swój pierwszy projekt Open Source (oprogramowanie lub oprogramowanie) na GitHub. GitHub to miejsce, w którym możesz przyjść, zagrać i eksperymentować z nowymi przepływami pracy badawczej, i to naprawdę tylko początek, który pomoże przygotować grunt pod twoje własne ścieżki i pomysły.

Nie zapomnij, że możesz dołączyć do dyskusji na naszym otwartym [**Slack channel**](https://osmooc.herokuapp.com/). Przedstaw się w # module5opensource i powiedz nam trochę o tym, kim jesteś, swoim tłem i tym, jak się tu znalazłeś!

**UWAGA** że nagrywanie ekranu dla tego zadania jest również dostępne za pośrednictwem [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&).

Szacowany czas wykonania: 30-45 minut.

Oszacuj oszczędność czasu po zakończeniu: niewyobrażalne ..

## Spis treści

* [Rozpoczęcie](#Getting_started) 
  * [Konfigurowanie profilu GitHub](#Profile)
  * [Język GitHub](#Language)
  * [Tworzenie nowego repozytorium](#Create_new)
* [Podstawowe kroki](#Foundation) 
  * [Wybór licencji](#License)
  * [Tworzenie pliku README](#Readme)
  * [Tworzenie wytycznych pomocniczych](#Contributing)
  * [Tworzenie kodeksu postępowania](#Conduct)
  * [Dokonywanie cytowania kodu](#Citation)
* [Uaktualnianie Twoich problemów](#Issues)
* [Lista kontrolna do uruchomienia projektu](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="Przepływ zadań 1" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Przepływ pracy dla zadania 1. Trzymaj to pod ręką, gdy wykonujesz zadanie!</i></p>

  


## Rozpoczęcie <a name="Getting_started"></a>

„Repozytorium” to naprawdę tylko wymyślna nazwa projektu w GitHub. GitHub to miejsce online, w którym możesz zarządzać projektami, przechowywać pliki i otwarcie współpracować z innymi. Wszystko to osiąga się, wykorzystując kontrolę wersji do śledzenia projektów w miarę ich postępu. W związku z tym GitHub jest potężnym narzędziem zarówno dla projektów oprogramowania, jak i innych.

Jedną z najważniejszych rzeczy do rozważenia na tym wczesnym etapie jest zastanowienie się, w jaki sposób chcesz, aby szersza społeczność wchodziła w interakcję z Twoim projektem. Gdy pracujesz na otwartej przestrzeni, chcesz mieć pewność, że inni czują się swobodnie w dostępie, przeglądaniu i angażowaniu się w pracę. Utworzenie repozytorium w sposób obniżający bariery wejścia i obawa przed byciem „outsiderem” to pierwszy krok w kierunku udanego projektu.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat, mała maskotka GitHuba</i></p>

  


### Konfigurowanie profilu GitHub <a name="Profile"></a>

Aby skonfigurować profil GitHub, wystarczy przejść do strony głównej i kliknąć [Zarejestruj się w GitHub](https://github.com/join). Tutaj możesz utworzyć swoje konto osobiste, z nazwą użytkownika, adresem e-mail i hasłem w standardzie.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>Zarejestruj się w GitHub</i></p>

  


Następnym krokiem jest stworzenie osobistego planu. Na razie po prostu wybierz plan „Nieograniczone publiczne repozytoria za darmo”, chyba że obawiasz się prywatności, w którym to przypadku wybierz prywatny plan. Jeśli zamierzasz skonfigurować projekt dla organizacji, możesz również wybrać tę opcję.

  


### Język GitHub <a name="Language"></a>

Jest to prawdopodobnie najbardziej mylący i odpychający aspekt GitHuba. Oto niektóre z najczęściej używanych terminów i ich definicje:

* **Initialise**: Utwórz puste repozytorium.
* **Checkout**: Utwórz roboczą kopię lokalnego repozytorium.
* **Klon**: Skopiuj repozytorium do lokalnego katalogu na komputerze.
* **Widelec**: Stwórz osobną pochodną repozytorium, aby równolegle pracować nad nim.
* **Oddział**: Niezależna i równoległa wersja repozytorium. Zmiany nie wpływają na gałąź główną.
* **Master**: Główna i domyślna gałąź repozytorium.
* **Wyczyść**: Brak zatwierdzeń w oddziale.
* **Etap**: Dodaj aktualizacje gotowe do zatwierdzenia w oddziale.
* **Zatwierdzenie**: wersja repozytorium, podobnie jak funkcja „zapisz” w wersji.
* **Komunikat zatwierdzenia**: opis zmian towarzyszących zatwierdzeniu.
* **Sprawdź**: Sprawdzenie stanu.
* **Fetch**: Nic wspólnego z psami. Dotyczy pobierania najnowszych zmian z repozytorium online bez ich scalania.
* **Indeks**: „Drzewo”, które działa jako obszar przejściowy.
* **Katalog roboczy**: „Drzewo”, w którym przechowywane są pliki.
* **Głowa**: „Drzewo”, które wskazuje ostatnie dokonane zatwierdzenia.
* **Push**: Dodaj zatwierdzone zmiany do głowy zdalnego repozytorium.
* **Merge**: Łączenie zmian dokonanych w jednym oddziale z oddziałem głównym po zakończeniu.
* **Ciąg**: Zaktualizuj repozytorium, pobierając i scalając najnowsze zatwierdzenia.
* **Żądanie ściągnięcia**: Żądanie scalenia zaktualizowanej gałęzi z gałęzią główną.
* **Problem**: Sugerowane ulepszenia, zadania lub pytania związane z repozytorium.

Whew! Na razie nie martw się zapamiętywaniem *wszystkich* z nich. Jak każda nowa umiejętność, znajomość pochodzi z doświadczenia.

Prawdopodobnie możesz zobaczyć, jak niektóre z nich są dość podobne do takich rzeczy jak zapisywanie, kopiowanie, wklejanie - standardowe operacje przepływu pracy, ale dostosowane do procesu zarządzania oprogramowaniem. Jest jeszcze [kilka więcej](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) , ale powinno to zrobić, aby zacząć.

Jeśli jesteś zainteresowany, większość tych warunków pochodzi z podstawowego systemu [Git](https://git-scm.com). Git został zbudowany, aby umożliwić programistom zarządzanie różnymi wersjami kodu źródłowego w sposób rozproszony, co jest świetne. Posiada wiele funkcji i możliwość zrobić wiele rzeczy złożonej, napisany przez [bardzo mądry facet](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/). Jednak interfejs użytkownika [nie został zaprojektowany z myślą o nowych użytkownikach](https://xkcd.com/1597/), więc może być trudny do nauczenia.

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>Bezkonkurencyjny przewodnik po korzystaniu z Gita. (Źródło: XKCD)</i></p>

  


### Tworzenie nowego repozytorium <a name="Create_new"></a>

W swoim profilu GitHub kliknij „Utwórz nowe repozytorium”. Pierwszym krokiem jest stworzenie nazwy jako marki dla swojego projektu. Najlepiej byłoby, gdyby był pamiętny i dał pewne wskazówki na temat tego, co robi projekt.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>Utwórz nowe repozytorium</i></p>

  


Upewnij się, że nie powielasz nazw, nie naruszasz innych znaków towarowych, ani nie nazywaj niczego, co mogłoby zostać uznane za obraźliwe.

  


## Podstawowe kroki <a name="Foundation"></a>

Każde repozytorium GitHub wymaga 4 kluczowych elementów, aby rozpocząć i rozpocząć tworzenie przyjaznej społeczności:

1. Licencja Open Source;
2. Plik `README`;
3. Przyczyniające się wytyczne; i
4. Kodeks postępowania.

Są to krytyczne aspekty i najlepsze praktyki każdego projektu, aby użytkownicy mogli zrozumieć swoje prawa, oczekiwania, cel projektu i poprawić ogólne wrażenia użytkownika.

Wszystkie cztery pliki powinny być przechowywane w katalogu głównym repozytorium projektu. Konwencja polega na stosowaniu formatów plików znaczników (`.md`) dla większości tych plików (chociaż plik licencji jest najczęściej zwykłym tekstem (`.txt`)), a wszystkie nazwy plików są pisane wielką literą. Zamiast spacji w nazwach plików, używaj podkreśleń `_`.

Więc powinieneś skończyć z podstawowym wyborem plików takim jak ten:

1. `LICENSE.md`
2. `README.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>Podstawowa struktura repozytorium</i></p>

  


### Wybór licencji <a name="License"></a>

Wybór odpowiedniej licencji odróżni Twoje repozytorium Open Source od publicznie dostępnego oprogramowania. Chociaż nie jesteś zobowiązany do wyboru licencji, to gwarantuje to, że inni będą mogli modyfikować, udostępniać, ponownie wykorzystywać i rozwijać swój projekt w ramach prawnych.

Na początek chcesz sprawdzić [Wybierz licencję](https://choosealicense.com/) aby znaleźć licencję najlepiej pasującą do Twoich zamiarów dotyczących repozytorium.

Trzy podstawowe do wyboru to:

* **Licencja MIT**: Licencja zezwalająca, która pozwala ludziom robić to, co chcą, za pomocą kodu, pod warunkiem, że dostarczają Ci odpowiedniego przypisania i nie ponoszą odpowiedzialności.
* **Licencja Apache 2.0**: Podobne uprawnienia do licencji MIT, ale zapewnia również wyraźne przyznanie praw patentowych od współpracowników użytkownikom.
* **Licencja GNU General Public License (GPL) v3**: Licencja [copyleft](https://en.wikipedia.org/wiki/Copyleft) która wymaga, aby każdy, kto redystrybuuje Twój kod lub pracę pochodną, udostępnił źródło na tych samych warunkach, co oryginalna licencja; zapewnia również wyraźne przyznanie praw patentowych od uczestników do użytkowników.

Na szczęście po uruchomieniu nowego repozytorium w GitHub masz możliwość wybrania istniejącej licencji z menu rozwijanego. Powinieneś zawsze (z nielicznymi wyjątkami) korzystać z istniejącej licencji, ponieważ to właśnie zobaczą potencjalni użytkownicy i współpracownicy, zanim zdecydują się skorzystać z twojego oprogramowania.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>Wybór przykładowej licencji</i></p>

  


Jeśli nie masz takiego, możesz go dodać ręcznie. Aby to zrobić, po prostu kliknij „Utwórz nowy plik” w repozytorium, a następnie skopiuj i wklej istniejący tekst licencji. Nazwij plik w stylu `LICENSE.txt` lub `LICENSE.md` aby go wyjaśnić, i zachowaj go w głównym folderze repozytorium (np. Root). Pamiętaj, aby dodać czysty komunikat zatwierdzenia i gotowe!

> **Pomocna dłoń**: Ten MOOC wykorzystuje inną kombinację licencji na zawartość kodu i treść niekodującą. Tutaj znajdziesz przykład licencji [MIT](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) , którą stosujemy dla całego kodu i oprogramowania generowanego w ramach produkcji MOOC.

  


### Tworzenie pliku README <a name="Readme"></a>

Po zainicjowaniu nowego repozytorium powinna istnieć możliwość zrobienia tego za pomocą pliku `README`. Podobnie jak Alicja w Krainie Czarów, robią dokładnie to, co mówią - dostarczają kluczowych informacji o projekcie. Zazwyczaj są to pierwsze rzeczy, które spoza autorów zobaczą, gdy wejdą do twojego repozytorium, więc kluczowe znaczenie ma ich informowanie i powitanie.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>Część pliku README dla tego modułu</i></p>

  


Plik będzie oryginalnie w formacie przeceny (`.md`). Jest to lekki język znaczników w formacie zwykłego tekstu. Aby nauczyć się podstawowych przecen, zobacz [tego arkusza kalkulacyjnego](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Ale na razie możemy po prostu użyć zwykłego tekstu.

Jest kilka rzeczy, które chcesz dołączyć do swojego pliku `README`:

* O czym jest ten projekt i co robi.
* Dlaczego ludzie powinni się troszczyć i dlaczego jest to przydatne.
* Jak ktoś może zacząć przyczyniać się do projektu.
* Z kim można się skontaktować, jeśli ktoś potrzebuje pomocy.
* Łącze do licencji, wytycznych i kodeksu postępowania.
* Opis struktury projektu.
* Kto jest zaangażowany i jakie są ich role.
* Aktualny stan projektu.

> **Pro-tip**: Później, w miarę rozwoju projektu, możesz dodać FAQ na podstawie opinii społeczności lub samouczka, aby pomóc użytkownikom zrozumieć, jak działa Twój projekt.

Pamiętaj, że nie wszyscy przychodzący do twojego projektu będą ekspertami lub zrozumieją, co robisz i dlaczego. Posiadanie dobrze udokumentowanego pliku `README` poprawi wrażenia użytkownika dla osób o szerokim zakresie wiedzy.

Gdy plik `README` znajduje się w katalogu głównym, GitHub automatycznie wyświetli to na stronie głównej repozytorium. Oznacza to, że jest to pierwsza rzecz, którą ludzie często widzą, więc zrób to!

> **Pomocna dłoń**: Tutaj znajdziesz plik `README` użyty dla tego [modułu MOOC](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md). Obejmuje to informacje na temat statusu, uzasadnienia, efektów uczenia się, zespołu programistów, kluczowych dokumentów i licencji na pomoc. W razie potrzeby możesz kopiować i dostosowywać tę strukturę do własnych projektów.

  


### Tworzenie wytycznych pomocniczych <a name="Contributing"></a>

Wytyczne wspierające mają na celu przekazanie potencjalnym autorom krótkiego przewodnika na temat zaangażowania w projekt i społeczność. Chcesz mieć pewność, że będziesz mile widziany i wskażesz, że chętnie angażujesz się w projekt. Za każdym razem, gdy uczestnik otworzy nowe żądanie ściągnięcia lub utworzy nowy numer, zobaczy link do twojego pliku składkowego.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>Część wytycznych `CONTRIBUTING` dla tego modułu</i></p>

  


Trzymając się wszystkich nazw plików czapek, następnym krokiem jest utworzenie pliku `CONTRIBUTING`. Kliknij „Utwórz nowy plik” i upewnij się, że został zapisany w formacie przeceny jak poprzednio. Ten plik powie innym użytkownikom, jak mogą się angażować i uczestniczyć w projekcie. Jest to pierwszy krok w kierunku stworzenia społeczności wokół twojego projektu, więc spraw, by był wciągający, zwięzły i informacyjny.

Plik `CONTRIBUTING` powinien zawierać informacje na temat:

* Jakiego rodzaju wkładów szukasz?
* Jak sugerować aktualizacje lub nowe funkcje.
* Jak współdziałać z projektem za pomocą funkcji GitHub (np. Protokół żądania ściągnięcia).
* Jak złożyć raport o błędzie lub utworzyć problem.
* Ostateczny cel, wizja lub plan działania dla projektu.
* Jak skontaktować się z osobami odpowiedzialnymi za projekt.
* Linki do dowolnej zewnętrznej dokumentacji lub stron internetowych.

> **Pro-tip**: Rozważ rozpoczęcie od krótkiej notki z podziękowaniami dla ludzi, którzy poświęcają czas na rozważenie wniesienia wkładu - kliknęli na plik, aby dowiedzieć się więcej! Jeśli masz na myśli inne metody rozpoznawania, pamiętaj o ich uwzględnieniu tutaj.

Tutaj zasadniczo starasz się zachęcić ludzi do poświęcenia swojego czasu na rozwój twojego projektu. Upewnij się, że jesteś przyjazny i przyjazny, i bądź precyzyjny, jak ludzie mogą się angażować. Pisząc to, pomyśl o tym z perspektywy użytkownika - jak możesz ułatwić sobie życie, składając wnioski o ściągnięcie i otwierając, aby cały projekt przebiegał sprawniej.

> **Pomocna dłoń**: [wytyczne dotyczące](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) tego modułu MOOC obejmują kilka bardzo konkretnych rzeczy: wprowadzenie do używania Git i GitHub, wskazówki dotyczące rozpoczynania pracy, informacje kontaktowe, jak zmienić treść i problemy z reporterami, link do `Plik README` oraz informacje o preferowanej zawartości i stylach kodu. Nie krępuj się kopiować i dostosowywać do własnego projektu według potrzeb.

  


### Tworzenie kodeksu postępowania <a name="Conduct"></a>

Kodeks postępowania jest ważny dla ustalenia podstawowych zasad dla oczekiwanego zachowania i udziału uczestników projektu, a także jest dokumentem, do którego można się odwołać, aby pokazać, że zespół projektowy poważnie traktuje konstruktywne dialogi. Dlatego jest to kluczowy element tworzenia i utrzymywania zdrowej społeczności, która angażuje się w konstruktywny i produktywny sposób w pozytywnej atmosferze społecznej.

Kodeks postępowania nie tylko zapewnia oczekiwania dotyczące zachowania, ale także opisuje, do kogo mają zastosowanie te oczekiwania, kiedy mają zastosowanie, co należy zrobić, jeśli dojdzie do naruszenia kodu, i jakie będą działania w tym zakresie. Jako takie, punkty kontaktowe muszą być jasno określone w kodeksie postępowania. Zazwyczaj powinno to odbywać się w sposób prywatny, taki jak adres e-mail.

> **Pro-tip**: W przypadku, gdy należy zgłosić naruszenie dotyczące osoby, która otrzymuje te raporty, upewnij się, że zawiera opcję skontaktowania się z drugą stroną.

Aby dodać kodeks postępowania, możesz utworzyć własny kod od podstaw, dodając nowy plik przeceny lub użyć istniejących szablonów, takich jak [Współtwórca kontraktu](https://contributor-covenant.org/). Nazwij swój plik `CODE_OF_CONDUCT.md`i upewnij się, że jest widoczny w pliku `README`.

> **Pomocna dłoń**: Ten MOOC posiada również [Kodeks Postępowania](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md) oparty na Porozumieniu Współtwórcy. Jak widać, zawiera on informacje na temat oczekiwanych standardów zachowania, obowiązków osób w społeczności oraz egzekwowania Kodeksu postępowania, w tym danych kontaktowych. Ponownie skorzystaj ponownie i dostosuj to do swojego projektu, jak uznasz za stosowne.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>Część pliku CODE OF CONDUCT dla tego modułu na podstawie Przymierza Współtwórcy</i></p>

  


Konieczność egzekwowania kodeksu postępowania jest ważna, ponieważ pokazuje, że nie tylko cenisz kod, ale szanujesz jego wpływ na społeczność. Ważne jest, aby traktować każdego członka społeczności z szacunkiem, uprzejmością i znaczeniem, na które zasługują. Jeśli dojdzie do naruszenia lub powtarzający się sprawca naruszy zasady, najlepiej jest odwołać się do [przewodnika Open Source](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) aby zobaczyć, jak egzekwować kodeks postępowania.

  


### Dokonywanie cytowania kodu <a name="Citation"></a>

Jeśli chcesz, aby kod od początku był cytowalny, powinieneś przechowywać metadane potrzebne do cytowania od początku, tworząc plik `[codemeta.json](https://codemeta.github.io)` lub `[CITATION.cff](https: //citation-file-format.github.io)` plik. Oba narzędzia umożliwiają obecnie tworzenie narzędzi do automatycznego tworzenia informacji o cytatach, a nie proszenia o wpisanie ich później w formularzu.

Jeśli jesteś zainteresowany, [cite.research-software.org](https://cite.research-software.org) zawiera dodatkowe informacje na temat cytowania oprogramowania w środowisku akademickim.

  


## Uaktualnianie Twoich problemów <a name="Issues"></a>

Kwestie niekoniecznie dotyczą problemów z projektem, ale także sugestie dotyczące ulepszeń, rzeczy, które należy opracować w przyszłości, a także komentarze i opinie na temat projektu, nad którym należy pracować. W razie potrzeby można je otwarcie udostępniać i omawiać z autorami, w rodzaju forum.

Jeśli jesteś kierownikiem projektu, ważne jest, aby zachować listę zagadnień, które wyjaśniają uczestnikom, jakie aspekty projektu wymagają uwagi. Ważne jest również, aby angażować się w jak najwięcej problemów od innych w pozytywny sposób, aby pokazać, że traktujesz ich wkład poważnie.

Kluczowe elementy zagadnień obejmują:

* Informacyjny tytuł i opis;
* Etykiety / znaczniki kodowane kolorem, które ułatwiają klasyfikowanie i filtrowanie;
* Kamienie milowe związane z powiązaniem problemów z konkretnymi funkcjami lub fazami projektu;
* Cesjonariusze wskazują, kto jest odpowiedzialny za pracę nad danym zagadnieniem;
* Komentarze do przekazywania opinii.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>Tracker problemów dla projektu Otwartej Strategii Stypendialnej</i></p>

  


W ramach zagadnień można użyć wzmianek @, aby powiadomić innych kontrargumentów o problemie i skutecznie zaangażować odpowiednie osoby. GitHub ma wewnętrzny system powiadomień, podobnie jak Facebook lub Twitter, a także może wysyłać wiadomości e-mail do osób wymienionych w module śledzenia problemów. Wszystko to można dostosować dla osób w ustawieniach użytkownika.

  


## Lista kontrolna do uruchomienia projektu <a name="Checklist"></a>

Teraz jesteś gotowy, aby uruchomić swój projekt, zacząć go reklamować i otrzymywać składki! Zanim przejdziesz dalej, upewnij się, że masz:

* [] Projekt ma pamiętną i pouczającą nazwę
* [] Projekt ma `LICENCJI` plik, który jest dokładną kopią licencji Open Source
* [] Pełna dokumentacja zawierająca pliki `README`, `CONTRIBUTING`i `CODE_OF_CONDUCT`
* [] Projekt ma co najmniej jeden wyraźnie oznaczony problem
* [] Każdy kod zawarty na tym etapie jest jasno skonstruowany i opatrzony komentarzami

**GRATULACJE!**

Uruchomiłeś projekt badawczy Open Source! Mam nadzieję, że od tej pory twoja praca będzie działać na korzyść szerszej społeczności, tworzyć nową współpracę i tworzyć nowe, fantastyczne możliwości dla wszystkich. Spróbuj i zastanów się, w jaki sposób te umiejętności mogą być zastosowane w przyszłych projektach i jak mogły one pomóc w przeszłości.

Od teraz wszystko zależy od Ciebie! Porady to:

* Napisz czysty kod;
* Miej dobrze zorganizowany projekt;
* Rób częste zobowiązania dzięki czystym wiadomościom;
* Utrzymuj dobrze udokumentowane projekty;
* Mieć jasne wytyczne;
* Skorzystaj z opisu i funkcji znaczników;
* Nie rozwidlaj cudzego repozytorium, chyba że zamierzasz nad nimi pracować;
* Upewnij się, że również przyczynisz się do projektów innych ludzi.

**Wiesz, w jaki sposób można poprawić tę zawartość?**

Czas wziąć swoje nowe umiejętności GitHub na próbę! Cały rozwój treści odbywa się przede wszystkim [tutaj](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md). Jeśli masz sugerowane ulepszenie treści, układu lub czegokolwiek innego, możesz to zrobić, a następnie automatycznie stanie się częścią treści MOOC po weryfikacji od moderatora!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)