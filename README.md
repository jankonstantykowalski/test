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

Gałąź bazowa to gałąź na podstawie której tworzona jest inna gałąź.
Gałąź docelowa to gałąź z którą integrowane są zmiany z bieżącej gałęzi.
Konwencja nazewnicza to konwencja wg której nadawane są nazwy poszczególnym gałęziom.

## Master

### Opis
opis

### Gałąź bazowa
n/d

### Gałąź decelowa
n/d

### Konwencja nazewnicza
master

## Develop

### Opis
opis

### Gałąź bazowa
master

### Gałąź decelowa
master, release

### Konwencja nazewnicza
develop

## Release

## Feature (gałęzie tematyczne)

## Hot-fix

# Strategia wersjonowania

link do wiki

# Proces ciągłej integracji

link do wiki

# Testy

## Testy jednostkowe

## Testy integracyjne

## Weryfikacja pokrycia kodu testami 

### Konfiguracja sonar + jacoco
- sonar jacoco maven multi module
- https://stackoverflow.com/questions/13031219/how-to-configure-multi-module-maven-sonar-jacoco-to-give-merged-coverage-rep
- https://github.com/acntech/jacoco-multimodule-maven
- https://github.com/johan974/maven-multi-module-unittest-integrationtest-jacoco

## Weryfikacja jakości kodu źródłowego

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
