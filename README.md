# Opis projektu

# Technologia

 - Java 8
 - Spring Framework (v5.0.x)
 - Spring Boot (2.0.x)

# Architektura logiczna

diagram komponentów

## Opis komponentów architektury

# Struktura projektu

## Opis modułów

| Nazwa modułu | Opis |
|---|---|
| a | b |

# Budowa Projektu

# Uruchomienie aplikacji

## standalone

## kontener serwletow

## docker

# Narzędzia i biblioteki

| Nazwa modułu | Wersja | Opis |
|---|---|---|
| Lombok | v | Użycie: https://projectlombok.org/features/all |
| Logback | v | Użycie: |
| Maven Wrapper | v | |
| Feign | v | Klient usług sieciowych typu RESTful |

# Strategia zarządzaniem repozytorium GIT

link do wiki

# Proces ciągłej integracji

link do wiki

# Testy

## Testy jednostkowe

## Testy integracyjne

# Weryfikacja pokrycia kodu testami 

jacoco
https://stackoverflow.com/questions/13031219/how-to-configure-multi-module-maven-sonar-jacoco-to-give-merged-coverage-rep


# Weryfikacja jakości kodu źródłowego

Jakość kodu źródłowego weryfikowana jest za pomocą narzędzia SonarQube dostepnego w lokalizacji: 

Lista reguł według których weryfikowany jest kod źródłowy znajduje się:
- dla kodu Java: 
- dla kodu XML:

Weryfikacja kodu uruchamiana jest za każdym razem kiedy kod źródłowy zostanie wypchnięty do zdalnego repozytorium dla brancha master oraz develop.

Aby lokalnie zweryfikować jakość kodu należy uruchomić polecenie:

```
mvn clean install
mvn sonar:sonar
```
