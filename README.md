# PROJEKT-ZALICZENIOWY
*Ten projekt został stworzony w ramach nauki programowania w C# i tworzenia aplikacji konsolowych.* 

# PadelShopManager

Kompleksowy system zarządzania magazynem dla sklepów ze sprzętem do padla, napisany w C#.

## Spis treści
- [Wprowadzenie](#wprowadzenie)
- [Technologie](#technologie)
- [Funkcjonalności](#funkcjonalności)
- [Instalacja](#instalacja)
- [Instrukcja użytkowania](#instrukcja-użytkowania)
- [Struktura projektu](#struktura-projektu)
- [Przechowywanie danych](#przechowywanie-danych)
- [Zrzuty ekranu](#zrzuty-ekranu)
- [Status projektu](#status-projektu)
- [Autor](#autor)

## Wprowadzenie

PadelShopManager to aplikacja konsolowa zaprojektowana, aby pomóc właścicielom sklepów ze sprzętem do padla w efektywnym zarządzaniu magazynem. System zapewnia interfejs do zarządzania trzema głównymi kategoriami produktów: rakiety, piłki i ubrania.

Aplikacja posiada polskojęzyczny interfejs użytkownika przy zachowaniu czystej struktury kodu w języku angielskim, co czyni ją dostępną dla polskich użytkowników, jednocześnie zachowując czytelność kodu na arenie międzynarodowej.

## Technologie

- **Język**: C# (.NET)
- **Platforma**: Aplikacja konsolowa
- **Przechowywanie danych**: Pliki CSV (tekst)
- **Architektura**: Programowanie proceduralne ze strukturami
- **Operacje plikowe**: FileStream, StreamReader, StreamWriter

## Funkcjonalności

### Kategorie produktów
- **Rakiety** (`Rakiety`)
  - Zarządzanie marką, modelem i ceną
  - Trwałość danych w pliku `rackets.txt`

- **Piłki** (`Pilki`) 
  - Zarządzanie nazwą i ceną
  - Trwałość danych w pliku `balls.txt`

- **Ubrania** (`Ubrania`)
  - **Koszulki** (`Koszulki`): Nazwa, Rozmiar, Cena
  - **Spodenki** (`Spodenki`): Nazwa, Rozmiar, Cena  
  - **Buty** (`Buty`): Nazwa, Rozmiar, Cena
  - Trwałość danych w plikach `shirts.txt`, `shorts.txt`, `shoes.txt`

### Podstawowe funkcjonalności
- **Dodawanie nowych elementów** do każdej kategorii
- **Wyświetlanie wszystkich elementów** w uporządkowanych listach
- **Usuwanie elementów** z potwierdzeniem
- **Automatyczne generowanie ID** dla wszystkich produktów
- **Walidacja danych wejściowych** dla wszystkich pól
- **Trwałość danych** między sesjami aplikacji
- **Polskojęzyczny interfejs** dla lepszej obsługi użytkownika

### Funkcje techniczne
- **Parsowanie oparte na Convert** zamiast TryParse
- **Strukturalne typy danych** używające struktur C#
- **Przechowywanie w plikach** w formacie CSV
- **System nawigacji menu** 
- **Obsługa błędów** dla nieprawidłowych danych

## Instalacja

1. **Wymagania wstępne**
   - Zainstalowany .NET SDK w systemie
   - Dowolne IDE obsługujące C# (Visual Studio, VS Code, Rider)

2. **Sklonuj repozytorium**
   ```bash
   git clone https://github.com/twojanazwa/PadelShopManager.git
   cd PadelShopManager
   ```

3. **Zbuduj projekt**
   ```bash
   dotnet build
   ```

4. **Uruchom aplikację**
   ```bash
   dotnet run
   ```

## Instrukcja użytkowania

### Nawigacja w menu głównym
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

1. **Dodawanie elementów**: Wybierz kategorię i opcję "Dodaj"
2. **Przeglądanie elementów**: Wybierz "Wyświetl wszystkie", aby zobaczyć wszystkie elementy w kategorii
3. **Usuwanie elementów**: Wybierz "Usuń" i podaj ID elementu do usunięcia

### Przykłady wprowadzania danych

**Dodawanie rakiety:**
- Marka: "Babolat"
- Model: "Drive Max 110" 
- Cena: "299.99"

**Dodawanie ubrań:**
- Nazwa: "Profesjonalna koszulka polo"
- Rozmiar: "L"
- Cena: "79.99"

## Struktura projektu

```
PadelShopManager/
├── Program.cs              # Główny plik aplikacji
├── README.md              # Dokumentacja projektu (angielska)
├── README_PL.md           # Dokumentacja projektu (polska)
├── rackets.txt            # Przechowywanie danych rakiet
├── balls.txt              # Przechowywanie danych piłek
├── shirts.txt             # Przechowywanie danych koszulek
├── shorts.txt             # Przechowywanie danych spodenków
└── shoes.txt              # Przechowywanie danych butów
```

### Architektura kodu

- **Struktury**: `Racket`, `Ball`, `Shirt`, `Shorts`, `Shoes`
- **Tablice danych**: Statyczne tablice z pojemnością 100 elementów na kategorię
- **Operacje plikowe**: Metody Load/Save dla każdego typu produktu
- **Metody UI**: Systemy menu i operacje CRUD

## Przechowywanie danych

Aplikacja używa prostego formatu CSV do trwałości danych:

**Format rakiet:** `id,marka,model,cena`
```
1,Babolat,Drive Max 110,299.99
2,Wilson,Pro Staff,449.00
```

**Format ubrań:** `id,nazwa,rozmiar,cena`
```
1,Profesjonalna koszulka polo,L,79.99
2,Spodenki kortowe,M,59.99
```

**Format piłek:** `id,nazwa,cena`
```
1,Zestaw piłek turniejowych,25.99
2,Piłki treningowe,18.50
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

## Status projektu

**Aktywny rozwój**

**Ukończone funkcjonalności:**
- Pełne operacje CRUD dla wszystkich kategorii produktów
- Trwałość danych w plikach CSV
- Polskie UI z angielskim kodem
- Walidacja danych wejściowych i obsługa błędów

**Potencjalne przyszłe ulepszenia:**
- Integracja z bazą danych (SQLite/SQL Server)
- Wyszukiwanie i filtrowanie produktów
- Funkcje raportowania sprzedaży
- Obsługa wielu języków
- Wersja GUI (WPF/WinForms)

## Cele edukacyjne

Ten projekt demonstruje:
- **Operacje wejścia/wyjścia plików** w C#
- **Modelowanie danych opartych na strukturach**
- **Tworzenie aplikacji konsolowych**
- **Walidację danych** i obsługę wprowadzania użytkownika
- **Architekturę aplikacji opartą na menu**
- **Obsługę formatu danych CSV**

## Autor

**Michalina Głodek  Dominik Błażejczyk**
- GitHub: MichalinaG1  DominikB2005
- Email: m.glodek.961@studms.ug.edu.pl  d.blazejczyk.982@studms.ug.edu.pl

