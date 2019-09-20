# WarframeInventoryHelper

Webowa apka, która będzie pilnowała za Ciebie podczas otwierania reliktów

## English support

I am not a native English speaker so I won't bother translating this yet. See **Planowane funkcjonalności**

## Czym ma być ta apka

Pierwszą i główną funkcjonalnością ma być możliwość wyświetlenia 4 wybranych reliktów na raz z informacjami, które z części możliwych do wylosowania użytkownik już posiada. W zależności co odpisze DE, planuję albo sczytywanie ekwipunku w czasie rzeczywistym albo raz na jakiś czas poprzez wymuszoną przez użytkownika synchronizację a w najgorszym wypadku ekwipunek zdefiniowany w stu procentach przez stronę.

## Wykorzystane narzędzia

Na chwile obecną jest za wcześnie aby się ograniczać do konkretnych narzędzi dlatego staram się dopasować to co znam do moich potrzeb cały czas szukając czy nie ma innych, lepiej dopasowanych do moich potrzeb. 

### Amazon Web Services

+ **Cloud9** - Środowisko programistyczne, które zawsze jest ze mną, niezależnie od tego czy akurat jestem w domu, u rodziny czy mam chwilę wolnego w pracy/na uczelni. 
+ **Cognito** - Zostanie dodane w momencie gdy będę potrzebował zarządzać użytkownikami. Wydaje się zdecydowanie prostsze w obsłudze oraz bezpieczniejsze niż trzymanie wszystkiego na własnym serwerze w dowolnej postaci.
+ **DynamoDB** - Zaciekawiła mnie idea baz noSQL dlatego stwierdziłem, że spróbuję ją zastosować w moim projekcie. Według zapewnień Amazona jest skalowalna, szybka a przede wszystkim dobrze zintegrowana z innymi usługami.
+ **EC2** - Niestety najdroższa część całego projektu (mimo tego, że nie są to jakieś duże kwoty). Mały serwerek, na którym będzie stała apka. Jest to usługa, z której korzystałem najwięcej dlatego też od niej zaczęła się cała rozbudowa pomysłu. Zastanawiam się jeszcze nad alternatywą w postaci **Fargate** ale na dzień dzisiejszy **EC2** jest oficjalnym wyborem.
+ **Lambda** - Myślę, że nada się idealnie do prostych i cyklicznych zadań w stylu aktualizacja bazy lub scrapowanie wiki. 
+ **S3** - Obecnie służy mi jako podstawa pod moją statyczną stronę ale na pewno wykorzystam jedno *wiaderko* jako magazyn do apki.

### Flask

Znam co nieco Pythona i nie chcąc się uczyć nowego języka od podstaw wpisując w Google *dynamic website python* albo *python web app* wyskakują głównie dwa narzędzia: Flask i Django. Słysząc od znajomego jakiś czas temu, że Django jest dość toporne i słuchając opowieści o jego problemach wybrałem Flaska. Zobaczę czy spełni moje oczekiwania i nie zamykam się na inne narzędzia.

## Planowane funkcjonalności

+ **English support** - This app will be in English, relax ;-)
+ Synchronizacja ekwipunku
+ Rozbudowa do *completionist checklist*
+ Profile użytkowników
+ Automatyczne update'y bazy
