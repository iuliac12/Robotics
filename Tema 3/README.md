# Tema 3: Quick Time
Proiectul constă în crearea unui joc de reflexe destinat a doi jucători, în care fiecare jucător trebuie să apese rapid butonul asociat culorii afișate pe LED-ul RGB al echipei sale. Jocul include mai multe runde, iar punctajele sunt afișate pe un ecran LCD. La sfârșitul jocului, este declarat câștigător jucătorul cu cel mai mare punctaj.

<details>
  <summary><b>Descriere</b></summary>

  ## 1. Hardware:

Două plăci Arduino Uno: Una este configurată ca master și cealaltă ca slave, comunicând prin protocol SPI.

LED-uri și Butoane:
    - Fiecare jucător dispune de 3 LED-uri colorate (roșu, verde, albastru) și 3 butoane asociate.
    - Un LED RGB indică culoarea activă pentru runda curentă.

Ecran LCD:
    - Afișează punctajele jucătorilor în timp real.
    - Mesaje personalizate, precum starea jocului și rezultatele finale.

Servomotor:
    - Indică progresul jocului, rotindu-se pentru a semnala sfârșitul timpului alocat.

Buzzer (opțional):
    - Sunete pentru răspunsuri corecte/greșite, începutul și finalul jocului.

  ## 2. Flow:
 
 Jocul începe cu afișarea unui mesaj de bun venit pe ecranul LCD, iar jucătorii pot iniția partida apăsând un buton. La fiecare rundă, LED-ul RGB al jucătorului activ indică o culoare aleatorie, iar acesta trebuie să apese rapid butonul asociat culorii respective pentru a acumula puncte, afișate în timp real pe LCD. 
 
 Un răspuns corect crește scorul în funcție de viteza reacției, iar unul greșit nu modifică punctajul. Rândurile jucătorilor alternează până la finalizarea jocului, marcată de o rotație completă a servomotorului. 
 
 Jocul se încheie prin afișarea scorurilor finale și a câștigătorului pe LCD, după care revine la starea inițială.

  ## 3. Detalii tehnice:

Arduino Master
    - Controlează LCD-ul, servomotorul și logica jocului.
    - Menține punctajul și decide LED-ul RGB care trebuie aprins.

Arduino Slave
    - Controlează butoanele și LED-urile.
    - Comunică prin SPI cu master-ul pentru a primi culoarea activă și a raporta apăsările butoanelor.

 Elemente Opționale
    - Personalizare: introducerea numelui jucătorilor prin USART sau joystick-uri.
    - Animații și Sunete: animații pe LCD sau LED-uri pentru începutul jocului / buzzer pentru feedback auditiv.
    - Dificultate: posibilitatea de a ajusta durata rundelor sau viteza de apariție a culorilor.   

</details>


<details>
  <summary> <b> Componente </b> </summary>

 ## Componente:
  - Arduino UNO (ATmega328P microcontroller)
  - 1x LED RGB (pentru a semnaliza dacă cuvântul corect e scris greșit sau nu)
  - 2x Butoane (pentru start/stop rundă și pentru selectarea dificultății)
  - 5x Rezistoare (3x 220/330 ohm, 2x 1000 ohm)
  - Breadbord
  - Fire de legătură
  
</details>


<details>
  <summary> <b> Schema electrica </b> </summary>

  ## Schema electrica a circuitului in TinkerCAD 
  
</details>


<details>
  <summary> <b> Setup </b> </summary>


</details>


<details>
  <summary> <b> Video </b> </summary>
  
  ## Link:

</details>