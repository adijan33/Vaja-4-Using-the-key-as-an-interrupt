# Vaja-4-Using-the-key-as-an-interrupt
b) V Pinout Configuraton pogledu glede na vašo razvojno ploščico ugotovite, ali lahko uporabite modro tipko 
za digitalni vhod kot interrupt (GPIO_EXT…). Če da, kateri pin je to? 

Pin PA1

c) Zapišite naslov izhodnih pinov za zeleno in modro LED: 

Modra- PC8
Zelena- PC9

3.c)Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a). 
HAL_GPIO_TogglePin(GPIOC,GPIO_PIN_9);


d)Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala:
for(uint32_t i=0; i<10000; i++);

0,3125ms

e) V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a):
 HAL_GPIO_TogglePin(GPIOC, GPIO_PIN_8);
 
f)V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a):
HAL_Delay(500);

<img width="685" height="535" alt="image" src="https://github.com/user-attachments/assets/98344416-4534-4d50-90eb-7c02bbe749e9" />
