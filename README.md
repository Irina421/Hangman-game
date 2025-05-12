# Hangman-game
Acesta este un joc simplu de spânzurătoarea implementat în C++. Scopul jocului este ca jucătorul să ghicească un cuvânt generat aleatoriu. Jucătorul are un număr limitat de încercări (6 erori) pentru a realiza acest lucru, altfel jocul este pierdut.

Funcționalități

- Generare aleatorie a unui cuvânt dintr-o listă prestabilită;

- Inregistrarea literelor introduse de jucator si verificarea corectitudinii acestora;

- Afisarea stării curente a cuvântului (cu linii de subliniere pentru literele necunoscute);

- Desenarea omului pe măsură ce jucătorul face greșeli, până când ajunge la 6 erori;

- Afișarea unui mesaj de câștig sau pierdere în funcție de rezultat.


Descrierea codului

1. Clasa Cuvant

Aceasta este clasa care se ocupă cu gestionarea cuvântului secret. Ea are:

- Un constructor care primește un cuvânt și îl separă în litere;

- Metode pentru:

  - Actualizarea cuvântului (înlocuirea liniilor cu litere ghicite);

  - A verifica dacă litera introdusă este corectă;

  - A verifica dacă jocul a fost câștigat (cuvântul este complet ghicit);

  - Afișarea stării curente a cuvântului.

2. Clasa Om

Această clasă gestionează starea omului din joc:

- Desenează omulețul care se formează pe măsură ce jucătorul greșește;

- Are un contor pentru numărul de erori făcute;

 - Metode pentru actualizarea erorilor și afisarea desenului corespunzător numărului de erori.

3. Funcții de Utilitate
   
- genereaza_nr_aleatoriu(int min, int max): Generează un număr aleatoriu între un interval specificat;

- genereaza_cuvant_aleatoriu(): Alege un cuvânt aleatoriu dintr-o listă prestabilită.

4. Clasa Joc

Este clasa principală care:

- Inițializează jocul, afisează starea inițială a cuvântului și desenul omului;

- Permite utilizatorului să joace, ghicind litere;

- Verifică dacă jocul s-a încheiat cu o victorie sau o pierdere și afișează rezultatul.
  

Fluxul jocului:

- Jocul începe prin generarea unui cuvânt aleatoriu;

- Jucătorul este rugat să ghicească litere;

- Dacă litera este corectă, aceasta este adăugată la cuvântul parțial, altfel se actualizează desenul omului;

- Jocul se încheie dacă jucătorul ghicește întregul cuvânt sau dacă omului este complet desenat (6 erori);

- La sfârșit, jocul afișează un mesaj corespunzător (câștig sau pierdere).

