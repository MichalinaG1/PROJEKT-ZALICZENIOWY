# PROJEKT-ZALICZENIOWY
Oto dokładne tłumaczenie Twojego pliku `README.md` na język **polski**, bez zmieniania formy ani struktury – gotowe do wklejenia na GitHub jako dokumentacja projektu:

````markdown
# PadelShopManager

Kompleksowy konsolowy system zarządzania inwentarzem dla sklepów ze sprzętem do padla, zbudowany w języku C#.

## Spis Treści
- [Wprowadzenie](#wprowadzenie)
- [Technologie](#technologie)
- [Funkcje](#funkcje)
- [Instalacja](#instalacja)
- [Użytkowanie](#użytkowanie)
- [Struktura Projektu](#struktura-projektu)
- [Przechowywanie Danych](#przechowywanie-danych)
- [Zrzuty ekranu](#zrzuty-ekranu)
- [Status Projektu](#status-projektu)
- [Autor](#autor)

## Wprowadzenie

PadelShopManager to aplikacja konsolowa zaprojektowana w celu pomocy właścicielom sklepów ze sprzętem do padla w efektywnym zarządzaniu stanem magazynowym. System zapewnia kompletny interfejs CRUD (Tworzenie, Odczyt, Aktualizacja, Usuwanie) do zarządzania trzema głównymi kategoriami produktów: rakietami, piłkami i odzieżą.

Aplikacja posiada polski interfejs użytkownika przy jednoczesnym zachowaniu przejrzystej, anglojęzycznej struktury kodu, co czyni ją dostępną dla polskich użytkowników przy zachowaniu międzynarodowej czytelności kodu.

## Technologie

- **Język**: C# (.NET)
- **Platforma**: Aplikacja konsolowa
- **Przechowywanie danych**: Pliki CSV (zwykły tekst)
- **Architektura**: Programowanie proceduralne z użyciem struktur
- **Operacje na plikach**: FileStream, StreamReader, StreamWriter

## Funkcje

### Kategorie produktów
- **Rakiety** (`Rakiety`)
  - Zarządzanie marką, modelem, ceną
  - Trwałość danych w `rackets.txt`

- **Piłki** (`Pilki`) 
  - Zarządzanie nazwą, ceną
  - Trwałość danych w `balls.txt`

- **Odzież** (`Ubrania`)
  - **Koszulki** (`Koszulki`): nazwa, rozmiar, cena
  - **Spodenki** (`Spodenki`): nazwa, rozmiar, cena  
  - **Buty** (`Buty`): nazwa, rozmiar, cena
  - Trwałość danych w `shirts.txt`, `shorts.txt`, `shoes.txt`

### Podstawowa funkcjonalność
- ✓ **Dodawanie nowych przedmiotów** do dowolnej kategorii
- ✓ **Wyświetlanie wszystkich przedmiotów** w uporządkowanych listach
- ✓ **Usuwanie przedmiotów** z potwierdzeniem
- ✓ **Automatycznie generowane ID** dla wszystkich produktów
- ✓ **Walidacja danych wejściowych** dla wszystkich pól
- ✓ **Trwałość danych** między sesjami aplikacji
- ✓ **Polski interfejs użytkownika** dla lepszych doświadczeń

### Funkcje techniczne
- Parsowanie oparte na Convert zamiast TryParse
- Ustrukturyzowane typy danych z użyciem struktur C#
- Przechowywanie danych w plikach w formacie CSV
- Nawigacja oparta na menu
- Obsługa błędów dla nieprawidłowych danych

## Instalacja

1. **Wymagania wstępne**
   - Zainstalowany .NET SDK
   - Dowolne IDE obsługujące C# (Visual Studio, VS Code, Rider)

2. **Sklonuj repozytorium**
   ```bash
   git clone https://github.com/yourusername/PadelShopManager.git
   cd PadelShopManager
````

3. **Zbuduj projekt**

   ```bash
   dotnet build
   ```

4. **Uruchom aplikację**

   ```bash
   dotnet run
   ```

## Użytkowanie

### Nawigacja po menu głównym

Po uruchomieniu aplikacji zobaczysz menu główne:

```
=== PADEL SHOP MANAGER ===

1. Rakiety
2. Pilki  
3. Ubrania
4. Wyjście

Wybierz opcję (1-4):
```

### Zarządzanie produktami

1. **Dodawanie przedmiotów**: wybierz kategorię i opcję „Dodaj”
2. **Wyświetlanie przedmiotów**: wybierz „Wyświetl wszystkie”, aby zobaczyć wszystkie przedmioty w kategorii
3. **Usuwanie przedmiotów**: wybierz „Usuń” i wprowadź ID przedmiotu do usunięcia

### Przykłady wprowadzania danych

**Dodawanie rakiety:**

* Marka: "Babolat"
* Model: "Drive Max 110"
* Cena: "299.99"

**Dodawanie odzieży:**

* Nazwa: "Professional Polo Shirt"
* Rozmiar: "L"
* Cena: "79.99"

## Struktura Projektu

```
PadelShopManager/
├── Program.cs              # Główny plik aplikacji
├── README.md               # Dokumentacja projektu
├── rackets.txt             # Przechowywanie danych o rakietach
├── balls.txt               # Przechowywanie danych o piłkach
├── shirts.txt              # Przechowywanie danych o koszulkach
├── shorts.txt              # Przechowywanie danych o spodenkach
└── shoes.txt               # Przechowywanie danych o butach
```

### Architektura kodu

* **Struktury**: `Racket`, `Ball`, `Shirt`, `Shorts`, `Shoes`
* **Tablice danych**: Statyczne tablice z limitem 100 elementów na kategorię
* **Operacje na plikach**: Metody wczytujące/zapisujące dla każdego typu produktu
* **Metody UI**: System menu i operacje CRUD

## Przechowywanie danych

Aplikacja wykorzystuje prosty format CSV do zachowania danych:

**Format rakiet:** `id,marka,model,cena`

```
1,Babolat,Drive Max 110,299.99
2,Wilson,Pro Staff,449.00
```

**Format odzieży:** `id,nazwa,rozmiar,cena`

```
1,Professional Polo,L,79.99
2,Court Shorts,M,59.99
```

**Format piłek:** `id,nazwa,cena`

```
1,Tournament Ball Set,25.99
2,Training Balls,18.50
```

## Zrzuty ekranu

*Przykład interfejsu konsolowego:*

```
=== ZARZĄDZANIE RAKIETAMI ===

1. Wyświetl wszystkie
2. Dodaj
3. Usuń
4. Cofnij

Wybierz opcję (1-4):
```

## Status Projektu

**Aktywny rozwój**

**Zrealizowane funkcje:**

*  Pełna obsługa CRUD dla wszystkich kategorii produktów
*  Trwałość danych przy użyciu plików CSV
*  Polski interfejs użytkownika i anglojęzyczna baza kodu
*  Walidacja danych i obsługa błędów

**Potencjalne przyszłe usprawnienia:**

* Integracja z bazą danych (SQLite/SQL Server)
* Wyszukiwanie i filtrowanie produktów
* Funkcje raportowania sprzedaży
* Obsługa wielu języków
* Wersja z graficznym interfejsem (WPF/WinForms)

## Cele edukacyjne

Projekt demonstruje:

* Operacje wejścia/wyjścia na plikach w C#
* Modelowanie danych przy użyciu struktur
* Tworzenie aplikacji konsolowych
* Walidację danych i obsługę danych wejściowych
* Architekturę aplikacji opartą na menu
* Obsługę formatu danych CSV

## Autor

**Your Name**

* GitHub: [@yourusername](https://github.com/yourusername)
* Email: [your.email@example.com](mailto:your.email@example.com)

*Projekt został stworzony w ramach nauki programowania w C# i tworzenia aplikacji konsolowych.*


