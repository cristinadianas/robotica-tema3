# Robotica - Tema 3: Quick Time Game

## Descriere
Fiecare jucător va avea butoane și LED-uri proprii, iar jocul se va desfășura în mai multe runde. Sistemul include două plăci Arduino care comunică prin SPI: una este master și coordonează jocul (LCD-ul, timerul cu servomotor și starea jocului), iar cealaltă este slave și gestionează inputurile (butoane) și LED-urile.

Scopul fiecărui jucător este să apese cât mai rapid butonul care corespunde culorii afișate pe LED-ul RGB al echipei sale. Placa master trimite culoarea pentru fiecare tură, iar slave aprinde LED-ul corespunzător și așteaptă input. Scorul depinde de timpul de reacție: sub 0,3s, sub 0,6s sau sub 1s. Greșelile sau întârzierea peste 1s duc la 0 puncte, iar un buzzer semnalează erorile. La final, master calculează scorurile, anunță câștigătorul și revine la meniul principal pentru un nou joc.

## Componente
* 6x LED-uri (2 grupuri de câte 3 leduri: albastru, verde si rosu)
* 2x LED RGB (1 pentru fiecare jucător)
* 12x Rezistențe 330 ohm
* 7x Butoane (3 pentru fiecare jucător + 1 pentru pornirea jocului)
* 1x LCD
* 1x Potențiometru
* 1x Servomotor
* 2x Breadboard
* Fire de legătură
* 2x Arduino Uno

## Flow
### Inițializare
Jocul pornește cu afișarea unui mesaj de bun venit pe LCD. Un al 7-lea buton dedicat porneste jocul.

### Desfășurarea Rundelor
Fiecare jucător are trei butoane, fiecare asociat unui LED de o culoare diferită și un al 4-lea LED RGB.
La fiecare rundă, fiecare jucător este cel activ.
LED-ul RGB al jucătorului activ se aprinde într-o culoare corespunzătoare unuia dintre butoanele sale. Jucătorul trebuie să apese cât mai rapid butonul care corespunde culorii LED-ului RGB, pentru a obține puncte. Cu cât reacționează mai repede, cu atât primește mai multe puncte.
La finalul unei runde LCD-ul afișează punctajul actualizat al ambilor jucători.
Pe tot parcursul jocului display-ul LCD va arata punctajul fiecarui jucator.

### Timpul și Finalizarea Jocului
Servomotorul se rotește pe parcursul jocului, indicând progresul. O rotație completă a servomotorului marchează sfârșitul jocului.
Buzzerul indica un raspuns corect sau gresit. Un sunet mai scurt corespunde unui raspuns corect, iar un sunet mai lung corespunde unui raspuns gresit.
La final, LCD-ul afișează numele câștigătorului și scorul final pentru câteva secunde, apoi revine la ecranul de start cu mesajul de bun venit.

## Poze ale Setup-ului Fizic
![WhatsApp Image 2024-11-19 at 8 24 50 PM](https://github.com/user-attachments/assets/777c472e-7e0c-4267-a151-a3edfb000604)
![WhatsApp Image 2024-11-19 at 8 25 47 PM](https://github.com/user-attachments/assets/beac6c5e-cc81-44ae-b61e-9f6582a540ca)
![WhatsApp Image 2024-11-19 at 8 26 22 PM](https://github.com/user-attachments/assets/fb492e5e-eaae-4c6a-8189-b85b8ae99ca3)

## Video cu Funcționalitatea Montajului
https://github.com/user-attachments/assets/718e43c8-c444-4bec-8dbf-1157481cb6ff

## Schema Electrică
![WhatsApp Image 2024-11-18 at 6 26 58 PM](https://github.com/user-attachments/assets/6be75af4-7395-41cc-96a4-96f9bcd5c313)
<img width="867" alt="Screenshot 2024-11-19 at 8 34 32 PM" src="https://github.com/user-attachments/assets/72aea055-93ee-4455-9605-726f9204caea">
![WhatsApp Image 2024-11-20 at 1 05 31 PM](https://github.com/user-attachments/assets/b6a0bfa5-8c9a-4e34-bb4b-e614dd925a88)













