# Opis projektu

# Technologia

 - Java 8
 - Spring Framework (v5.0.x)
 - Spring Boot (2.0.x)

# Architektura logiczna

diagram komponentów

## Opis komponentów architektury

# Struktura projektu

- https://terasolunaorg.github.io/guideline/5.0.x/en/ImplementationAtEachLayer/CreateWebApplicationProject.html#x-xx-fw-9999-format-message-id

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

# Strategia zarządzania repozytorium GIT

![alt text](https://cdn-images-1.medium.com/max/1600/1*CChjPbEmKDWIpPG-OVXfFg.png "Logo Title Text 1")

![alt text](https://cdn-images-1.medium.com/max/1600/1*ddK2ImDbJmkBAH8MGKkT2Q.png "Logo Title Text 1")

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

### Format numeru wersji
```
nazwa-vX.Y.Z
```

## Develop

### Opis
opis

### Gałąź bazowa
master

### Gałąź decelowa
master, release

### Konwencja nazewnicza
develop

### Format numeru wersji
```
nazwa-YYYYMMDD-HHMMSS.COMMMIT_ID-SNAPSHOT
```

## Release

## Feature (gałęzie tematyczne)

## Hot-fix

# Strategia wersjonowania

link do wiki

# Proces ciągłej integracji

link do wiki

# Testy

## Testy jednostkowe

Każda warstwa testowana oddzielnie z zaślepionymi wywołaniami metod z interfejsów z innych warstw.

## Testy integracyjne

Wszystkie warstwy testowane są razem (testy komunikacji i zgodności wewnętrznego API) z zaślepionymi odwołaniami do usług udostępnianch przez systemy zewnętrzne (np.: bazy danych, usługi sieciowe).

### Mockowanie bazy danych

Wykorzystanie wewnętrznej bazy danych H2 (skrypty SQL kreujące schemat bazy danych oraz dane testowe)

### Mockowanie usług sieciowych typu RESTful

Wykorzystanie narzędzia WireMock do symulowania odpowiedzi z usług typu RESTful udostępnianych przez zewnętrzne systemy.
- https://dzone.com/articles/using-wiremock-to-mock-underlying-services-during
- http://cloud.spring.io/spring-cloud-static/spring-cloud-contract/1.1.2.RELEASE/#_spring_cloud_contract_wiremock

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
