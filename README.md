Linii:
->voi verifica prima data fiecare linie in parte prin evidenta primei cifre
->cifra pe care o verific o transform in echivalentul sau in litera 1-A, 2-B, 3-C, 4-D
->in timp ce verific cifra pe linia curenta raman in aceeasi stare si merg mai departe pana ce dau
de aceeasi cifra ceea ce inseamna ca masina nu accepta inputul, sau pana ce dau de * ce marcheaza sfarsitul liniei
->cand am ajuns la sfarsit merg in starea reset inapoi pana ce dau de prima litera pentru a putea apoi
sa trec in starea start si sa am un nou start ce verifica urmatoarea cifra daca se repeta in sirul ramas sau nu
->cand termin linia curenta primul caracter diferit de litera este *, trec apoi la start pentru ce se afla 
in dreapta lui *
->verific astfel toate liniile pana ajung la blank din start ceea ce indica faptul ca inputul este acceptat pt linii
->astfel trec in starea de verificare coloane

Coloane:
->verific fiecare element in ordinea in care se afla pe linie si descopar pe ce coloana se afla
in functie de cate elemente dupa prima * de dupa blank are in fata
->astfel startul este reprezentat de col1,col2,col3,col4 care reprezinta si ce element verific
->elementul acum verificat se suprascrie cu cifra sa corespunzatoare
->in functie de coloana pe care ma aflu vad al catelea element de pe linia urmatoare trebuie
sa verific daca este sau nu egal cu el
->am mereu o stare de check pt fiecare coloana si pentru coloanele pare inca una auxiliara
care sare inca un element
->dupa ce am ajuns la utlima linie (care este de fapt prima intrucat se porneste de la dreapta la stanga),
aici se reseteaza urmatorul element si se merge pana in capatul de inceput unde se va incepe
parcurgerea pe linii a coloanelor
->noul element va fi primul diferit de o litera, parcurg in coloane pana se intampla asta 

Regiuni:
->verific fiecare element din prima jumatate a regiunii, adica voi verifica pentru fiecare regiune
doar de 2 ori, verific cu celelalte 2 elemente ale portiunii
->a doua jumatate de regiune in care trebuie sa verific elementul pentru care fac agloritmul in acel
moment se afla dupa terminarea parcurgerii liniei curente si pana in ":" in cazul in care se incepe cu *
->daca regiunea are prima jumatate imediat dupa ":" atunci a doua jumatate in care verific se afla imediat 
dupa urmatorul ":"
->dupa ce hotarasc ce start am, cum incepe prima jumatate a regiunii de verificat retin prima cifra,
o sterg, ajung in a doua jumatate si atunci cand ajung prima data transform cifrele in litere 
in cazul in care nu gasesc un duplicat
->transformarea  din cifre litere pt a doua jumatate se face pt ca atunci cand ajung la ea, sa nu fie
confundata cu prima jumatate dintr-o portiune, atunci cand se ajunge la ea, se sterge ca restul inputului
de pana atunci
->la finalul portiunii resetez startul si sterg mereu ce urmeaza pana ce pe banda voi ajunge din blank in blank 