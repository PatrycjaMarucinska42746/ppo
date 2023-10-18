## Klasy abstrakcyjne

### Agenda
Przewidywany plan zajęć kształtuje się następująco:
* przedstawienie idei klasy abstracyjnej
* analiza zadania przykładowego,
* indywidualna praca nad listą zadań.

### Klasa abstrakcyjna
Klasa abstrakcyjna, reprezentuje koncepcję obiektu, który nie ma pełnej formy. 
Nie można utworzyć jej instancji, co oznacza, że nie możemy tworzyć obiektów bezpośrednio z klasy abstrakcyjnej. Zamiast tego klasa abstrakcyjna służy jako bazowa klasa dla innych klas.

Klasa abstrakcyjna jest jak wzór lub szablon, którego nie można użyć w takiej formie, w jakiej jest. Zamiast tego inne klasy korzystają z tego wzoru jako punktu wyjścia, aby stworzyć konkretne "wersje" tego wzoru.

`Przykład:` Pomyśl o klasie abstrakcyjnej jako o kategorii "pojazd". Wiesz, co to jest pojazd, ale "pojazd" sam w sobie jest zbyt ogólny, aby dało się go zdefiniować jako konkretny obiekt. Niemniej jednak "samochód", "motocykl" czy "rower" są konkretnymi manifestacjami pojęcia "pojazd".

### Dlaczego warto korzystać z klas abstrakcyjnych

#### 1. Abstrakcja: 

Klasy abstrakcyjne umożliwiają modelowanie na wyższym poziomie abstrakcji. W rzeczywistości każdy obiekt w świecie rzeczywistym posiada wiele szczegółów. Dzięki klasom abstrakcyjnym możemy skupić się tylko na tych cechach obiektu, które są dla nas ważne, pomijając nieistotne detale.
Klasy abstrakcyjne umożliwiają przedstawienie ogólnego pomysłu bez potrzeby określania wszystkich drobnych szczegółów.

`Przykład:` Kategoria "pojazd" pozwala myśleć o różnych środkach transportu bez konieczności zastanawiania się, czy mają one dwa czy cztery koła, czy są napędzane paliwem czy elektrycznością.

#### 2. Wymuszanie kontraktu: 

Metody abstrakcyjne w klasie abstrakcyjnej nie mają ciała. Klasy dziedziczące są zobowiązane do dostarczenia implementacji dla tych metod, co gwarantuje, że każda klasa pochodna będzie miała te metody.
Klasy abstrakcyjne mogą wymagać, aby klasy dziedziczące zdefiniowały określone metody.

`Przykład:` Możemy wymagać, aby każdy "pojazd" miał metodę "przyspiesz" i "zatrzymaj", ale to, jak dokładnie te metody działają, będzie zależało od konkretnego pojazdu (samochód przyspiesza inaczej niż rower).

#### 3. Udostępnianie wspólnego kodu: 
Klasy abstrakcyjne nie tylko definiują metody abstrakcyjne, ale mogą również zawierać normalne metody z pełną implementacją. To oznacza, że klasy dziedziczące mogą korzystać z tej gotowej implementacji, nie pisząc jej od nowa.
Klasy abstrakcyjne mogą zawierać metody, które mają sens dla wszystkich klas dziedziczących.

`Przykład:` Każdy "pojazd" mógłby mieć metodę "zatankuj", ale tylko niektóre pojazdy (na przykład elektryczne) mogą mieć dodatkową metodę "naładuj".

### Metody abstrakcyjne 

Metody abstrakcyjne stanowią jedną z kluczowych cech klas abstrakcyjnych. To metody, które są deklarowane w klasie abstrakcyjnej, ale nie mają konkretnego ciała lub implementacji.

Metody abstrakcyjne w klasie abstrakcyjnej działają jak lista obowiązków, które klasy dziedziczące muszą "wypełnić".

`Przykład:` Jeśli klasa abstrakcyjna "pojazd" ma metodę abstrakcyjną "przyspiesz", to klasa "samochód" może zdefiniować tę metodę jako "wciskanie pedału gazu", podczas gdy klasa "rower" zdefiniuje ją jako "pedałowanie szybciej".
Cechy charakterystyczne metod abstrakcyjnych:

* Brak ciała: Główna cecha metody abstrakcyjnej to brak ciała. Oznacza to, że nie wykonuje ona żadnej konkretnej operacji.
* Wymaganie implementacji w klasie dziedziczącej: Jeśli klasa dziedziczy po klasie abstrakcyjnej i nie dostarczy implementacji dla metod abstrakcyjnych, stanie się ona również klasą abstrakcyjną.
* Widoczność: Tak samo jak normalne metody, metody abstrakcyjne mogą mieć modyfikatory dostępu, takie jak prywatne, chronione czy publiczne, w zależności od języka programowania.

Używając metod abstrakcyjnych, programista może określić, które metody klasy dziedziczącej muszą zostać zaimplementowane, zapewniając jednocześnie swobodę w zakresie konkretnego sposobu ich implementacji.