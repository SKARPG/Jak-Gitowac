# Jak używać gita Skaru ?

## Po co i kiedy ?

Wraz z coraz większą organizacją SKARu warto zacząć lepiej dokumentować pracę którą wykonujemy.
W organizacji SKAR na Githubie powinno znajdować się jak najwięcej projektów w celu łatwiejszej współpracy jak i poprawy ogólnej organizacji pracy.

Warto również wspomnieć że dzielenie się swoim kodem i pokazywanie z czego składa się dany projekt, umożliwia mniej doświadczonym osobom zobaczenie jak wygląda dana praca zza kulisów.

Jeżeli robisz jakiś projekt i wykorzystujesz w nim jakikolwiek **język programowania** to warto wykorzystać rozwiązanie jakim jest git. 
Git umożliwia kontrolę wersji twojego kodu, a wraz z GitHubem znacznie ułatwia kolaborację z innymi osobami nad tworzonym kodem.
Warto również dodać że do projektu/repozytorium na GitHubie można dodać inne pliki takie jak **szkice**, **modele 3D** itp.

Na koniec wspomnę również że github umożliwia dokumentację projektów za pomocą Markdowna (również w formie Wiki), a także posiada wiele funkcjonalności ułatwiających pracę zespołową.

## Krótko o organizacji

Wszyscy członkowie Skaru zostaną dołączeni do organizacji, z możliwością tworzenia repozytoriów i zarządzania stworzonymi przez siebie repozytoriami. 
Warto jednak dodać że każdy może zrobić pull request do dowolnego repozytorium (o ile jest publiczne), a ten będzie mógł być zaakceptowany przez administratora danego repozytorium.

Repozytoria z zasady nie muszą kierować się z góry ustaloną strukturą, jednak miło by było jak by posiadały plik README.md aby wiadomo było o co chodzi.

Dodam też że nie zalecane jest pushowanie bezpośrednio na gałąź `main/master` tylko używanie oddzielnej gałęzi np. `devel` lub zrobienie forka repozytorium na swoim prywatnym koncie Github i robienie pull requestów (nawet jak mają być od razu zatwierdzone), lub robić obie rzeczy na raz :) .


## Jak radzić sobie z gitem i Githubem ?

Najlepiej poczytać na ten temat w internecie. Jest mnóstwo dobrych materiałów na ten temat, osobiście polecam film od [fireship.io](https://www.youtube.com/watch?v=HkdAHXoRtos) oraz [dokumentację Githuba](https://docs.github.com/en/github/getting-started-with-github).

Inny potencjalnie przydatny [film](https://www.youtube.com/watch?v=PWqS4NBhEY8) bardziej pod Windowsa.

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

Jeżeli chcesz udoskonalić ten dokument, możesz to zrobić tworząc pull requesta, na pewno z przyjemnością go przyjmę. Poprawki błędów ortograficznych jak i merytorycznych są mile widziane.

W razie pytań do gita na ten moment można napisać do:

- [Mateusza Mazura](https://www.github.com/Mazurel)


