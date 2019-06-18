---
output:
  html_document: domyślna
  pdf_document: domyślna
---

# Zadanie 2: Jak sprawić, by kod był cytowalny przy użyciu GitHub i Zenodo

To zadanie jest przeznaczone dla studentów i naukowców, którzy chcą tworzyć i ponownie wykorzystywać projekty / repozytoria oparte na GitHub w literaturze akademickiej.

Nie zapomnij, że możesz dołączyć do dyskusji na naszym otwartym [**Slack channel**](https://osmooc.herokuapp.com/). Przedstaw się w # module5opensource i powiedz nam trochę o tym, kim jesteś, swoim tłem i tym, jak się tu znalazłeś!

Szacowany czas na ukończenie: 45-60 minut.

## Spis treści

- [Przedmowa](#Foreword)
- [Skonfiguruj repozytorium GitHub](#Setup)
- [Wybierz swoje repozytorium GitHub](#Choose)
- [Zaloguj się do Zenodo](#Login)
- [Autoryzuj GitHub, aby połączyć się z Zenodo](#Authorise)
- [Wybierz repozytorium do archiwizacji](#Archive)
- [Sprawdź ustawienia repozytorium](#Check)
- [Utwórz nowe wydanie](#Release)
- [Uzyskiwanie DOI](#DOI)
- [Lista kontrolna do cytowania twojego projektu](#Checklist)
- [Dodatkowe zasoby](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="Przepływ zadań 2" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>Przepływ pracy dla zadania 2. Trzymaj to pod ręką, gdy wykonujesz zadanie!</i></p>

  


## Przedmowa <a name="Foreword"></a>

Chociaż integracja GitHub i Zenodo sprawia, że obecnie łatwiej jest pracować z tymi narzędziami (styczeń 2019), należy podkreślić, że istnieją alternatywy dla GitHub (Gitlab, Bitbucket, ...) i alternatywy dla Zenodo (inne repozytoria mogą być bardziej odpowiednim dla twojej społeczności, możesz zapytać swoich kolegów). Na przykład można pracować z Gitlab i ręcznie przesyłać każdą nową wersję do repozytorium uniwersyteckiego, uzyskując DOI. Zasady (praca z systemem kontroli wersji online i archiwizacja głównych wersji w repozytorium, które zapewnia trwały unikalny identyfikator) mogą być stosowane w różnych przepływach pracy.

## Skonfiguruj repozytorium GitHub <a name="Setup"></a>

> **Pro-tip**: Upewnij się, że w repozytorium znajduje się plik LICENSE i README. To wskaże ludziom cel projektu i sposób, w jaki mogą się nim zająć w przyszłości.

Dowiedzieć się, jak skonfigurować repozytorium GitHub w tej drugiej przewodnik [Zadanie 1: Budowa repozytorium GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) , która jest również częścią „Moduł 5: Badania Open Software i Open Source”.

## Wybierz swoje repozytorium GitHub <a name="Choose"></a>

Po przejściu na stronę z listą projektów GitHub pod adresem [github.com](https://github.com) przejdź do karty „Repozytoria”. Wybierz repozytorium, które chcesz zarchiwizować, i otwórz je.

  


## Zaloguj się do Zenodo <a name="Login"></a>

Teraz przejdź do [zenodo.org](https://zenodo.org). Zenodo to platforma, na której możesz na stałe zarchiwizować swój kod i inne elementy projektu. Zenodo robi to, przypisując projektowi **Digital Object Identifier** (DOI), co również pomaga uczynić pracę bardziej cytowalną. Inaczej niż w GitHub, który działa jako miejsce, w którym odbywa się rzeczywista praca nad projektem, a nie długoterminowa archiwizacja. W GitHub treść może być modyfikowana, usuwana, przepisywana i nieodwracalnie zmieniana, co sprawia, że jest trochę niepokojąca, aby można ją było używać do długotrwałych celów odniesienia. Zenodo oferuje większe bezpieczeństwo i trwałość wyników badań.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>Zarejestruj się w Zenodo</i></p>

  


Jeśli masz już konto Zenodo, jest to łatwe. Jeśli nie, postępuj zgodnie z instrukcjami, aby go utworzyć - możesz nawet zalogować się za pomocą konta GitHub lub profilu ORCID, aby ułatwić sobie sprawę, ponieważ Zenodo ma wbudowaną integrację. Może to być łatwiejsze niż utworzenie kolejnego konta badawczego i profilu.

  


## Autoryzuj GitHub, aby połączyć się z Zenodo <a name="Authorise"></a>

Na stronie Zenodo upoważnij go do połączenia się z Twoim kontem GitHub w sekcji „[Korzystanie z GitHub](https://zenodo.org/account/settings/github/)”. Tutaj Zenodo przekieruje Cię do GitHub, aby poprosić o uprawnienia do używania „[webhooks](https://developer.github.com/webhooks/)” w twoich repozytoriach. Chcesz autoryzować Zenodo tutaj z uprawnieniami, których potrzebuje, aby utworzyć te linki.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>Autoryzuj Zenodo do łączenia się z GitHub</i></p>

  


Jeśli próbujesz udostępnić Zenodo dostęp do repozytorium organizacyjnego, Ty (lub administrator) będziesz musiał upewnić się, że Zenodo ma uprawnienia dostępu stron trzecich. GitHub wyśle e-mail autoryzacyjny, który wymaga potwierdzenia. W tym momencie, w ustawieniach repozytorium w GitHub, musisz również upewnić się, że repozytorium jest ustawione na „publiczne”, a nie prywatne.

  


## Wybierz repozytorium do archiwizacji <a name="Archive"></a>

Jeśli dotarłeś tak daleko, oznacza to, że Zenodo jest teraz upoważniony do konfigurowania webhooków repozytorium potrzebnych do archiwizacji repozytorium i wydania go DOI. Aby to zrobić, na stronie internetowej Zenodo przejdź do [GitHub repozytorium aukcji stronie](https://zenodo.org/account/settings/github/) i kliknij przycisk „on” obok repozytorium.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>Włącz przechowywanie poszczególnych repozytoriów GitHub w Zenodo</i></p>

  


## Sprawdź ustawienia repozytorium <a name="Check"></a>

Teraz utworzyłeś nowy webhook między Zenodo a twoim repozytorium. W GitHub kliknij ustawienia swojego repozytorium i zakładkę Webhooks w menu po lewej stronie. To powinno wyświetlić nowy webhook Zenodo skonfigurowany dla Zenodo. Uwaga: wyświetlenie listy webhooków może zająć trochę czasu.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>Sprawdź, czy webhooks są włączone dla twojego repozytorium GitHub. Przykład tutaj przy użyciu otwartej strategii stypendialnej</i></p>

  


## Utwórz nowe wydanie <a name="Release"></a>

Pierwsze archiwizowanie repozytorium jest znane jako „pierwsze wydanie”. Za każdym razem, gdy tworzysz nową wersję tego repozytorium i archiwizujesz je, tworzysz nową wersję. Można to śledzić w zakładce „releases” dla twojego repozytorium na GitHub (top center).

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>Sprawdź, czy pierwsze wydanie repozytorium powiodło się. Przykład tutaj przy użyciu otwartej strategii stypendialnej</i></p>

  


W przypadku pierwszej zarchiwizowanej wersji repozytorium kliknij „Utwórz nową wersję” w Zenodo. Wypełnij formularz i podaj szczegóły dotyczące tego, co pociąga za sobą wydanie. W pierwszym wydaniu upewnij się, że nazywasz go v1.0.0, co jest standardową praktyką.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>Utwórz nowe wydanie. Przykład tutaj przy użyciu otwartej strategii stypendialnej, dla której pierwsze wydanie już istnieje</i></p>

  


Na koniec kliknij „release release”, a twoje archiwum zostanie opublikowane i wersjonowane na GitHub.

Aby wyświetlić swoje wydanie na Zenodo, musisz odwiedzić zakładkę [Prześlij](https://zenodo.org/deposit). Aby zakończyć archiwizację, potrzebne są dodatkowe informacje na temat Zenodo.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>Sprawdź, czy nowe wydanie zostało przesłane. Przykład tutaj pokazany przy użyciu otwartej strategii stypendialnej</i></p>

  


## Uzyskiwanie DOI <a name="DOI"></a>

Jest to czasami określane jako „bicie” DOI i wymaga kilku dodatkowych informacji o repozytorium na Zenodo. Na Zenodo kliknij zakładkę [Prześlij](https://zenodo.org/deposit) w menu głównym, a nowo przesłane repozytorium powinno tam być. Przewiń stronę w dół i uzupełnij dodatkowe informacje w razie potrzeby, wymagane pola są oznaczone czerwoną gwiazdką, a następnie kliknij przycisk „Publikuj”.

**Uwaga**: Dopiero po dodaniu tych dodatkowych informacji twój DOI stanie się aktywny. Może upłynąć trochę czasu, zanim DOI stanie się aktywne. Przykład DOI pokazany poniżej (dla Otwartej Strategii Stypendialnej).

> **Pro-tip**: Skopiuj adres URL DOI do pliku README, aby repozytorium GitHub było jeszcze łatwiejsze, a także przedstaw wyraźną podświetloną odznakę DOI, aby użytkownicy mogli zobaczyć i korzystać z DOI. Wystarczy to zrobić raz przy pierwszym wydaniu DOI, ponieważ działa ono jako „koncepcja DOI” i jest powiązane ze wszystkimi kolejnymi wydaniami DOI.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

Integracja GitHub / Zenodo przypisze teraz DOI do każdej wersji / wydania repozytorium projektu. Umożliwia to użytkownikom odwoływanie się do konkretnych wersji projektów i cytowanie ich. Lista autorów cytatów jest automatycznie określana przez nazwy kont użytkowników GitHub używane przez repozytorium - oznacza to, że nikt nie zostaje pominięty. Szczegóły autora można później edytować na Zenodo. DOI używane w Zenodo są rejestrowane za pośrednictwem usługi [DataCite](https://www.datacite.org/).

> **Pro-tip**: Utwórz „czytelną dla człowieka” wersję tego cytatu w pliku README projektu. Będzie to pomocne dla naukowców, którzy mogą nie być zaznajomieni z używaniem DOI do tworzenia cytatów i ułatwienia innym cytowania oprogramowania i potwierdzania pracy. Przykładem może być: Jon Tennant. (2018, 30 lipca). Podstawy rozwoju strategii otwartego stypendium: Pierwsze oficjalne wydanie (wersja 1.2). Zenodo. <http://doi.org/10.5281/zenodo.1323437>

**GRATULACJE!!**

Twoje repozytorium GitHub jest teraz archiwizowane w Zenodo oraz z DOI, które może być wersjonowane, aby odzwierciedlać aktualizacje wersji repozytorium w czasie. Powinieneś być w stanie zobaczyć szczegóły tego na stronie GitHub Zenodo twojego repozytorium. Oznacza to również, że Twoje zarchiwizowane projekty mogą zostać odebrane przez inne usługi indeksowania i wyszukiwarki korzystające z DOI.

Zapewnienie długoterminowego archiwum i DOI dla twojej pracy jest wymagane, aby inni mogli ją prawidłowo cytować, ponieważ zapewnia to podstawowe metadane cytatów. Dla Open Science ważne jest, aby móc cytować oprogramowanie, którego używasz w swoich badaniach, a ten zintegrowany przepływ pracy umożliwia to, zgodnie z najlepszymi praktykami cytowania badań. Ponadto praktyka ta jest ważna dla podniesienia standardu oprogramowania (i powiązanych projektów) do standardu innych wyników badań.

> **Pro-tip**: Czy twoje badania są finansowane z dotacji UE? Teraz możesz bezpośrednio połączyć zarchiwizowany projekt z dotacją, aktualizując sekcję dotacji metadanych w rekordzie Zenodo projektu. To ogromnie pomaga zwiększyć jego wykrywalność!

  


## Lista kontrolna do cytowania twojego projektu <a name="Checklist"></a>

Teraz masz zarchiwizowane archiwum GitHub w Zenodo, które jest gotowe do ponownego użycia i cytowania! Zanim przejdziesz dalej, upewnij się, że masz:

- [] Połączył Twój projekt GitHub z Zenodo. Jeśli zobaczysz pełną kopię swojego repozytorium GitHub w Zenodo, wtedy wszystko działa.
- [] Zintegrowana instalacja Zenodo i GitHub działa dobrze. Na przykład, wszystkie nazwy autorów i poprawny tytuł projektu trafiają do Zenodo. Jeśli nie, lub jeśli autorzy mają tylko pseudonimy, możesz edytować te szczegóły w Zenodo.
- [] Projekt ma pierwsze wydanie, z DOI. Powinieneś mieć DOI wyświetlane na swoich stronach Zenodo. Ten pierwszy DOI nazywany jest „pojęciem DOI” i jest głównym DOI łączącym się ze wszystkimi kolejnymi wydaniami DOI. Skopiuj ten link DOI i umieść go na stronie README projektów GitHub. Jesteś skończony!

### Dodatkowe zasoby <a name="Resources"></a>

[Tworzenie własnego kodu](https://guides.github.com/activities/citable-code/) - GitHub Guides.

**Wiesz, w jaki sposób można poprawić tę zawartość?**

Czas wziąć swoje nowe umiejętności GitHub na próbę! Cały rozwój treści odbywa się przede wszystkim [tutaj](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md). Jeśli masz sugerowane ulepszenie treści, układu lub czegokolwiek innego, możesz to zrobić, a następnie automatycznie stanie się częścią treści MOOC po weryfikacji od moderatora!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)