# Ekologiczny bot
Projekt realizowany w ramach przedmiotu "Wprowadzenie do aplikacji i rozwiązań opartych o Sztuczną Inteligencję i Microsoft Azure" prowadzonym na Politechnice Warszawskiej. 

## Opis projektu
Z danych Głównego Urzędu Statystycznego wynika, że w 2020 roku zostało zebranych 13.1 mln ton odpadów komunalnych. Porównując z danymi z 2019 roku nastąpił wzrost o 2.9%. Na jednego mieszkańca przypada średnio 342 kg odpadów komunalnych. 59% odpadów została skierowana do procesu odzysku. Celem naszego projektu było stworzenie bota i wdrożenie go jako aplikacji webowej. Chcieliśmy w ramach projektu zwiększyć świadomość użytkowników na temat ekologii i recyklingu, aby w kolejnych latach ilość odpadów spadała, a procent odpadów wykorzystywanych do odzysku wzrastał. Stworzony bot podaje przydatne informacje związane z segregacją śmieci, ale również na temat zagrożonych gatunków. Bot działa na zasadzie pytań i odpowiedzi. Użytkownik zadaje pytanie, a bot odpowiada.

<a href="https://www.teraz-srodowisko.pl/aktualnosci/gus-ochrona-srodowiska-w-2020-odpady-komunalne-10550.html" target="_blank">Link do danych GUSu</a>

## Skład zespołu
* Kinga Kocoł
* Aleksander Wodnicki

<a href="https://github.com/AzureProjectsPW/EcoBot-On-Azure" target="_blank">Link do repozytorium</a>

## Opis funkcjonalności

## Architektura
<p align="center">
  <img src="https://user-images.githubusercontent.com/64069048/142736761-f7c0b9d4-f569-477f-881b-b2f69ee4eb51.png"/>
</p>

## Wybrany stos technologiczny

## Opis działania rozwiązania
W celu uruchomienia bota należy przejść na adres <a href="https://webchat.botframework.com/embed/EcoBotOnAzure-Bot/gemini?b=EcoBotOnAzure-Bot&s=htOptp1LqEI.6I42djWzWvpFh7hcKjDJbm_sOUSgh7IdOZClvYwiPt4&username=You" target="_blank">link do Ekologicznego bota</a>. Następnie zostaniemy przekierowani do Web Chatu.

![bot_1](https://user-images.githubusercontent.com/64069048/142758636-5b2a6114-ab02-433e-ada8-8f97d78c5e49.png)

Od tego momentu możemy się komunikować z botem. Poniżej znajduje się przykładowa lista pytań, które można zadać:
- przywitanie 
  - Cześć!
- pytania odnośnie bota 
  - Kim jesteś?
  - Do czego służysz?
  - Kto Cię stworzył?
  - O co mogę Cię zapytać?
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

W przypadku niektórych odpowiedzi otrzymujemy link do strony. Przykładem jest pytanie o najbliższy PSZOK, klikając w link zostaniem przekierowani do Google Maps, gdzie wyświetla się lista najbliższych punktów.

![bot_2](https://user-images.githubusercontent.com/64069048/142759122-30b641bc-d54b-417b-976f-4cdb323bb582.png)

![bot_3](https://user-images.githubusercontent.com/64069048/142759167-c0f976d9-a1fc-4486-b180-5192944e1852.png)


## Demo
