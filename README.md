# Portfolio: Testy API dla GoREST (Postman)

Cześć!

Nazywam się Kamil Szyszkowski. Jako student informatyki rozwijam swoje kompetencje w obszarze testowania oprogramowania, skupiając się na umiejętnościach technicznych.

W tym repozytorium prezentuję moje projekty z zakresu testowania API z wykorzystaniem narzędzia Postman, zrealizowane podczas kursów i samodzielnej nauki.

📫 **Kontakt:** kamilszyszkowskii@op.pl  
🔗 [Zobacz mój profil na LinkedIn](https://www.linkedin.com/in/kamil-szyszkowski-a55a00270)


### 📝 Opis projektu

Ten projekt zawiera kolekcję testów w Postmanie dla publicznego API **GoREST**. Testy weryfikują podstawowe operacje CRUD (Create, Read, Update, Delete) na zasobie `/users`. Kolekcja obejmuje zarówno scenariusze pozytywne, jak i negatywne, demonstrując kompleksowe podejście do zapewnienia jakości API.

### 🛠️ Użyte narzędzia

* **Postman** - do tworzenia i wykonywania zapytań oraz testów API.
* **JavaScript** (Chai.js Assertion Library) - do pisania skryptów testowych.
* **GoREST API** - jako testowane środowisko (SUT - System Under Test).

### ✨ Główne funkcje i zaimplementowane testy

#### Scenariusze Pozytywne
* **Pobieranie listy użytkowników (`GET`):** Test sprawdzający status `200 OK` oraz poprawność struktury odpowiedzi.
* **Tworzenie nowego użytkownika (`POST`):** Test weryfikujący status `201 Created` i zapisujący ID nowego użytkownika do zmiennych środowiskowych.
* **Usuwanie użytkownika (`DELETE`):** Test sprawdzający status `204 No Content` po usunięciu zasobu.

#### Scenariusze Negatywne
* **Próba stworzenia użytkownika z zajętym adresem e-mail:** Test sprawdza, czy API poprawnie zwraca błąd `422 Unprocessable Entity`.
* **Próba pobrania nieistniejącego zasobu:** Test weryfikuje, czy serwer odpowiada statusem `404 Not Found`.
* **Próba stworzenia zasobu bez autoryzacji:** Test bezpieczeństwa sprawdzający, czy API jest chronione przed nieautoryzowanym dostępem i zwraca błąd `401 Unauthorized`.

### 🚀 Jak uruchomić ten projekt?

1.  Pobierz plik kolekcji `Portfolio - GoREST API Tests.postman_collection.json` z tego repozytorium.
2.  Otwórz aplikację Postman i kliknij przycisk **Import**.
3.  Wybierz pobrany plik `.json`, aby zaimportować kolekcję.
4.  Aby uruchomić testy, należy skonfigurować środowisko (Environment) w Postmanie, dodając zmienną `accessToken` z własnym tokenem ze strony `gorest.co.in`.
