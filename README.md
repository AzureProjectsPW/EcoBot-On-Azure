# Ekologiczny Bot
Projekt realizowany w ramach przedmiotu *Wprowadzenie do aplikacji i rozwiązań opartych o Sztuczną Inteligencję i Microsoft Azure* prowadzonym na Politechnice Warszawskiej. 

## Opis i cel projektu
Z danych Głównego Urzędu Statystycznego wynika, że w 2020 roku zostało zebranych 13.1 mln ton odpadów komunalnych. Porównując z danymi z 2019 roku nastąpił wzrost o 2.9%. Na jednego mieszkańca przypada średnio 342 kg odpadów komunalnych. 59% odpadów została skierowana do procesu odzysku. Celem naszego projektu było stworzenie bota i wdrożenie go jako aplikacji webowej. Chcieliśmy w ramach projektu zwiększyć świadomość użytkowników na temat ekologii i recyklingu, aby w kolejnych latach ilość odpadów spadała, a procent odpadów wykorzystywanych do odzysku wzrastał. Stworzony bot podaje przydatne informacje związane z segregacją śmieci, ale również na temat zagrożonych gatunków. Bot działa na zasadzie pytań i odpowiedzi. Użytkownik zadaje pytanie, a bot odpowiada.

<a href="https://www.teraz-srodowisko.pl/aktualnosci/gus-ochrona-srodowiska-w-2020-odpady-komunalne-10550.html" target="_blank">Link do danych GUSu</a>

## Skład zespołu
* Kinga Kocoł - <a href="https://github.com/kingakocol" target="_blank">Link do konta</a>
* Aleksander Wodnicki - <a href="https://github.com/AleksanderWodnicki" target="_blank">Link do konta</a>

## Opis funkcjonalności

*Ekologiczny Bot* posiada rozbudowaną bazę wiedzy, która umożliwia użytkownikowi interakcję poprzez zadawanie różnorodnych pytań z kilku kategorii powiązanych z ekologią.

Poniżej przedstawione są funkcjonalności *Ekologicznego Bota*:
- wyświetlanie pomocy związanej z przykładowymi pytaniami po otrzymaniu pytania o nie od użytkownika
- przekazywanie informacji ogólnych dotyczących segregacji odpadów oraz definicji związanych z segregacją
- możliwość identyfikacji konkretnych rodzajów odpadów przez bota i przekazanie informacji użytkownikowi, do jakich odpadów się one zaliczają
- wyświetlanie informacji związanych z zagrożonymi gatunkami ssaków, gadów, ryb, owadów, ptaków oraz roślin i grzybów
- przekazanie informacji o autorach projektu oraz opisu działalności po zadaniu odpowiednich pytań opisanych w sekcji *Opis działania rozwiązania*
- oprócz odpowiedzi w formie tekstowej, bot przesyła również odpowiedzi zawierające zdjęcia oraz odnośniki do zewnętrznych stron (np. Google Maps)
- obsługa *follow-up prompts* po części odpowiedzi udzielonych przez bota, aby zasugerować użytkownikowi pytanie, które nawiązuje bezpośrednio do udzielonej odpowiedzi.

## Architektura
<p align="center">
  <img src="https://user-images.githubusercontent.com/64069048/142772811-39a68217-45ee-49aa-9e1c-488613ab60a5.png"/>
</p>

## Wybrany stos technologiczny

- Azure:
  - Active Directory – utworzenie bota w organizacji Politechniki Warszawskiej było niemożliwe, przez co zdecydowaliśmy się na utworzenie nowej organizacji `EcoBotOnAzure`. Możliwość pracy w tej organizacji pozwoliła nam na bezproblemowe skorzystanie ze wszystkich niezbędnych przedstawionych serwisów.
  - App Service – wykorzystywany jest przez nas w przypadku *Bota Aplikacji Internetowej* oraz *QnA Maker* – między innymi mogliśmy edytować kod źródłowy bota dzięki App Service'om tworzonym przy okazji tworzenia zasobu *Bota Aplikacji Internetowej*
  - App Service Editor – posłużył on do edycji plików `QnAMakerBaseDialog.cs` oraz  `QnABot.cs`, w których zawarte są odpowiednio domyślna odpowiedź w przypadku nieznalezienia żadnej w przygotowanym *Knowledge Base* oraz wiadomość powitalna, którą bot wysyła do użytkownika od razu po uruchomieniu.
  - Bot Service – dzięki tej usłudze powstał *Bot Aplikacji Internetowej* `EcoBotOnAzure-Bot`.
  - Cognitive Service – dzięki tej usłudze, konkretnie QnA Maker, byliśmy w stanie utworzyć *Knowledge Base*, z której korzysta utworzony przez nas bot.
- Język:
  - C# – używany był przy edycji plików wspomnianych przy okazji *Azure App Service Editor*.

## Opis działania rozwiązania
W celu uruchomienia bota należy zaznaczyć ten <a href="https://webchat.botframework.com/embed/EcoBotOnAzure-Bot/gemini?b=EcoBotOnAzure-Bot&s=htOptp1LqEI.6I42djWzWvpFh7hcKjDJbm_sOUSgh7IdOZClvYwiPt4&username=You" target="_blank">link do *Ekologicznego bota*</a>. Następnie zostaniemy przekierowani do Web Chatu.

![bot_1](https://user-images.githubusercontent.com/64069048/142758636-5b2a6114-ab02-433e-ada8-8f97d78c5e49.png)

Od tego momentu możemy się komunikować z botem. Poniżej znajduje się przykładowa lista pytań, które można zadać:
- przywitanie 
  - Cześć!
- pytania odnośnie bota 
  - Kim jesteś?
  - Do czego służysz?
  - Kto Cię stworzył?
- pytania związane z segregacją śmieci 
  - Czym jest segregacja smieci?
  - Gdzie mam wyrzucic baterie?
  - Gdzie mam wyrzucić chwasty?
  - Po co opróżniać opakowania?
  - Dlaczego nie trzeba myć opakowań przed wyrzuceniem?
  - Czym są elektrośmieci?
  - Co mogę wrzucić do pojemnika na papier?
  - Gdzie jest PSZOK?
- pytania związane z ekologią
  - Czy zużycie papieru niszczy las?
  - Jak ograniczyć marnowanie żywności?
- pytania o zagrożone gatunki
  - Czym jest czerwona księga gatunków zagrożonych?
  - Czy mogę się dowiedzieć czegoś o zagrożonych gatunkach zwierząt?
  - Powiesz mi coś o zagrożonych gatunkach roślin?
  - Powiesz mi coś o zagrożonych gatunkach grzybów?

Bot odpowiada również na pytanie o co można go zapytać. Pojawia się wówczas lista przykładowych pytań i możemyw wybrać jedno z nich.

![bot_7](https://user-images.githubusercontent.com/64069048/142759429-218efee4-5821-4950-a05b-6ae32e773d5f.png)

W przypadku niektórych odpowiedzi otrzymujemy link do strony. Przykładem jest pytanie o najbliższy PSZOK, klikając w link zostaniemy przekierowani do Google Maps, gdzie wyświetli się lista najbliższych punktów.

![bot_2](https://user-images.githubusercontent.com/64069048/142759122-30b641bc-d54b-417b-976f-4cdb323bb582.png)

![bot_3](https://user-images.githubusercontent.com/64069048/142759167-c0f976d9-a1fc-4486-b180-5192944e1852.png)

Możemy również w przypadku, niektórych pytań prowadzić dłuższą konwersację z botem. Przykładem jest pytanie o zagrożone gatunki zwierząt.

![bot_4](https://user-images.githubusercontent.com/64069048/142759261-bb531cbe-550d-4c80-87e9-7beeb0dd9b4b.png)

![bot_5](https://user-images.githubusercontent.com/64069048/142759265-a1e2cd0f-4af0-4ff2-a065-5692474d8472.png)

W przypadku pytań, na które bot nie zna odpowiedzi zostanie wyświetlona odpowiedź domyślna.

![bot_6](https://user-images.githubusercontent.com/64069048/142772953-4afd3c09-3f5c-4c6f-bfdc-698de452db72.png)

Aby obejrzeć demo opisanego wyżej projektu, należy skorzystać z obrazka załączonego poniżej:

[![Demo Projektu #1](https://user-images.githubusercontent.com/92271405/142781864-273507cc-5041-4fce-a88e-0c791f35d036.png)](https://www.youtube.com/watch?v=okmf708xc0g)
