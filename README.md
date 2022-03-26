![skar_github](https://user-images.githubusercontent.com/22836301/160253554-8089d851-0535-4bcf-9334-e2be1fbe22e7.png)


# Jak używać gita Skaru ?

## Po co i kiedy ?

Wraz z coraz większą organizacją SKARu warto zacząć lepiej dokumentować pracę którą wykonujemy.
W organizacji SKAR na Githubie powinno znajdować się jak najwięcej projektów w celu łatwiejszej współpracy jak i poprawy ogólnej organizacji pracy.

Warto również wspomnieć że dzielenie się swoim kodem i pokazywanie z czego składa się dany projekt, umożliwia mniej doświadczonym osobom zobaczenie jak wygląda dana praca zza kulisów. Dodatkowo warto dodać że trzymanie projektu na gicie potencjalnie **wydłuża życie projektu** oraz zwiększa szansę na jego kontynuację.

Jeżeli robisz jakiś projekt i wykorzystujesz w nim jakikolwiek **język programowania** to warto wykorzystać rozwiązanie jakim jest git. 
Git umożliwia kontrolę wersji twojego kodu, a wraz z GitHubem znacznie ułatwia kolaborację z innymi osobami nad tworzonym kodem.
Warto również dodać że do projektu/repozytorium na GitHubie można dodać inne pliki takie jak **szkice**, **modele 3D** itp.

Na koniec wspomnę również że github umożliwia dokumentację projektów za pomocą Markdowna (również w formie Wiki), a także posiada wiele funkcjonalności ułatwiających pracę zespołową.

## Jak radzić sobie z gitem i Githubem ?

Najlepiej poczytać na ten temat w internecie. Jest mnóstwo dobrych materiałów na ten temat, osobiście polecam film od [fireship.io](https://www.youtube.com/watch?v=HkdAHXoRtos) oraz [dokumentację Githuba](https://docs.github.com/en/github/getting-started-with-github).

Inny potencjalnie przydatny [film](https://www.youtube.com/watch?v=PWqS4NBhEY8) bardziej pod Windowsa.

## Organizacja projektów na Githubie

Wszyscy członkowie Skaru powinni być dodani do organizacji, z możliwością tworzenia repozytoriów i zarządzania stworzonymi przez siebie repozytoriami. 
Warto jednak dodać że każdy może zrobić pull request do dowolnego repozytorium (o ile jest publiczne), a ten będzie mógł być zaakceptowany przez administratora danego repozytorium. W przypadku repozytoriów prywatnych, istnieje też możliwość dodania do nich osób spoza organizacji SKARPG.

Dodam też że nie zalecane jest pushowanie bezpośrednio na gałąź `main/master` (szczególnie w przypadku pracy w grupie) tylko używanie oddzielnej gałęzi np. `devel` lub zrobienie forka repozytorium na swoim prywatnym koncie Github i robienie pull requestów (nawet jak mają być od razu zatwierdzone), lub robić obie rzeczy na raz :) .

### Schemat folderów na repozytoriach

Zalecane jest trzymanie się następującego schematu plików i folderów repozytoriach:
- plik README.md - Do opisu na czym polega projekt
- plik .gitignore - Zawiera pliki (ścieżki do nich) które nie powinny znajdować się w repozytorium, np. przekompilowany kod źródłowy
- folder sw/ - Folder zawierający software do projektu. Może zawierać podfoldery dotyczące poszczególnych elementów projektu.
- folder hw/ - Folder zawierający hardware do projektu. Może zawierać podfoldery dotyczące poszczególnych elementów projektu.

W ten sposób repozytoria wyglądają bardziej czytelnie oraz schludnie. Dodatkowo napomnieć warto, że każdy folder może posiadać swoje własne README.md opisujące co się w nim znajduje.

### Schemat pracy z gitem

Ogólne zasady/tipy:
- Unikamy argumentu `--force`.
- Gdy siadamy do pracy nad repozytorium, wykonujemy najpierw `git pull`

Każdy projekt na gitcie posiada główną gałąź, zwykle nazwaną `main`. Warto jednak podkreślić, że pracowanie tylko na jednej gałęzi **nie** jest zalecane w przypadku projektów grupowych.
W przypadku takich projektów najlepiej jest wykorzystać jedną z dwóch metod:
a) Dla kaźdej nowej funkcjonalności tworzyć nową gałąź, a w momencie gdy jest ona gotowa zrobić Pull Request do głównej gałęźi.
b) Każdy członek zespołu może zrobić fork projektu, a następnie gdy wykona jakąś zmianę, zrobić Pull Request spowrotem na główną gałąź. Jest to o tyle mniej wygone, że utrudnia to wspólną pracę nad tą samą funkcjonalnością.

### Issue

Github oferuje dość wygodną funkcjonalność jaką są Issue. Issue umożliwiają opisywanie zadań, błędów, etc, a następnie przydzielanie do nich odpowiednich osób. Warto jest rozważyć skorzystanie z nich przy większym projekcie.

## Dodawanie istniejącego projektu

### Czy powinienem dodawać swój projekt ?

Moim zdaniem tak. Używając gita uczysz się nowej technologi (która prawie na pewno ci się przyda w przyszłości) jednocześnie pokazując pracę Skaru.

### Czego potrzebujesz

Potrzebne minimum to [git](https://git-scm.com/). 
Osobiście dla użytkowników Windowsa polecam też zainstalować zestaw z bashem (z tego co pamiętam przy instalacji gita jest taka opcja).
W [tym filmie](https://www.youtube.com/watch?v=PWqS4NBhEY8) możesz dowiedzieć się jak z niego korzystać.

Warto też skorzystać z vs code, na ten temat więcej dowiesz się w [tym filmie](https://www.youtube.com/watch?v=HkdAHXoRtos).

### Jak to zrobić

> Poniższe kroki są dość poglądowe, w razie czego polecam podane linki i stack overflow ;)

Dodanie projektu do organizacji SKAR na Githubie jest dość proste:

- Jeżeli używasz Githuba do swojego projektu, w ustawieniach repozytorium masz możliwość przetransferowania repozytorium do organizacji SKAR. Więcej na ten temat można przeczytać w [dokumentacji Githuba](https://docs.github.com/en/github/administering-a-repository/transferring-a-repository).
- Jeżeli używasz innej strony wraz z gitem, musisz wykonać następujące czynności:
    1. Stwórz nowe repozytorium w organizacji
    2. Zapisz adres repozytorium
    3. Wejdź do folderu z twoim obecnym projektem i otwórz konsolę (zakładam że posiadasz gita)
    4. Zmień repozytorium `origin` używając komendy `git remote set-url origin <Tu wklej adres>`
    5. Wykonaj pulla: `git pull`
    6. Wykonaj pusha: `git push`
    7. Jeżeli napotkałeś się na problem warto poczytać na temat [zmian adresów](https://docs.github.com/en/github/getting-started-with-github/managing-remote-repositories#changing-a-remote-repositorys-url).
- Jeżeli masz jakiś projekt i chcesz zacząć używać gita, możesz poczytać o tym w [tym artykule](https://towardsdatascience.com/start-using-git-in-your-existing-data-science-project-27118c92f86e), co znosi się do następujących kroków:
    1. Stwórz nowe repozytorium w organizacji
    2. Zapisz adres repozytorium
    3. Wejdź do folderu z twoim obecnym projektem i otwórz konsolę (zakładam że posiadasz gita)
    4. Stwórz repozytorium git za pomocą: `git init`
    5. Dodaj wszystkie pliki `git add .` 
    6. Stwórz pierwszy commit `git commit -m "Init"`
    7. Dodaj repozytorium `origin`: `git remote add origin <Tu wklej adres>`
    8. (Opcjonalne) Sprawdź powyższe ustawienie: `git remote -v`
    9. Wykonaj pusha `git push -u origin main`
 
## Inne informacje

Jeżeli chcesz udoskonalić ten dokument, możesz to zrobić tworząc pull requesta, na pewno z przyjemnością go przyjmę. Poprawki błędów ortograficznych jak i merytorycznych są mile widziane. Dodatkowo, dodawać też można Issue, gdy jakiś temat powinien zostać poruszony.

W razie pytań do gita i Githuba na ten moment można napisać do:

- [Mateusza Mazura](https://www.github.com/Mazurel)


