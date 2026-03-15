<details>
<summary><strong>1. Što je algoritam? Primjer.</strong></summary>

**Alogoritam** je i dio posla u procesu koji od uočenog problema dovodi do rezultata (najčešće pomoću računalnog programa).
- Primjer algoritma računanja dva broja:

1. Učitaj prvi broj A.

2. Učitaj drugi broj B.

3. Izračunaj S = A + B.

4. Ispiši rezultat S.

5. Kraj algoritma.

</details>

---
<br>
<br>

<details>
<summary><strong>2. Koja je razlika između algoritma i programa?</strong></summary>
  
**Algoritam** je točno definiran niz koraka za rješavanje nekog problema i može biti zapisan riječima.
**Program** je implementacija algoritma u nekom programskom jeziku koju računalo može izvršiti i mora imati točnu sintaksu.


</details>

---
<br>
<br>

<details>
<summary><strong>3. Znakovni tip podataka. Kako se prikazuje u memoriji, a kako na ekranu?</strong></summary>

Znakovni tip podataka char predstavlja slovo, broj, simbol ili kontrolni znak.
U memoriji se znak ne sprema kao znak, nego kao numerički kod prema nekom standardu npr ASCII, a na ekranu se prevede pomoću tablice kodiranja te se prikaže odgovarajući znak.

</details>

---
<br>
<br>

<details>
<summary><strong>4. Cjelobrojni tip podataka. Vrste i raspon vrijednosti.</strong></summary>

Vrste cjelobrojnih tipova su char, short, int, long, signed i unsigned.

| Tip | Veličina | Raspon vrijednosti |
|---|---|---|
| `char` | 1 bajt (8 bitova) | −128 do 127 |
| `short` | 2 bajta (16 bitova) | −32 768 do 32 767 |
| `int` | 4 bajta (32 bita) | −2 147 483 648 do 2 147 483 647 |
| `long` | 4 ili 8 bajtova (64 bita) | -9223372036854775808 do 9223372036854775807 |


</details>

---
<br>
<br>

<details>
<summary><strong>5. Cjelobrojni tip podataka. Kako se prikazuje u memoriji?</strong></summary>

Cjelobrojni tip podataka u memoriji se prikazuje kao **binarni zapis** 0 i 1.

</details>

---
<br>
<br>

<details>
<summary><strong>6. Opisati dvostruki (binarni) komplement.</strong></summary>

Obavlja se u dva koraka: 
1. Unarno kompementirati broj (0 -> 1 i 1 -> 0), tj. invertirati
2. Aritmetički dodati 1

</details>

---
<br>
<br>

<details>
<summary><strong>7. Realni tip podataka. Kako se prikazuje u memoriji?</strong></summary>

Realni tip podataka koristi se za brojeve s decimalnim dijelom, u memoriji se prikazuju prema standardu **IEEE 754**, u obliku predznaka, eksponenta i mantise.

</details>

---
<br>
<br>

<details>
<summary><strong>8. Realni tip podataka. Greške pomičnog zareza, zbog čega? Primjer.</strong></summary>

Kod 32-bitnih brojeva s pomičnim zarezom će raditi samo do određene vrijednosti. Ako je razlika brojeva dovoljno velika, zbrajanje će uvijek dati rezultat jednak većem broju, zbog zaokruživanja.
Nastaju zbog načina na koji računala pohranjuju decimalne brojeve u binarnom obliku.

</details>

---
<br>
<br>

<details>
<summary><strong>9. Nizovi (jednodimenzionalna polja) kao struktura podataka. Svojstva?</strong></summary>

**Niz** je skup elemenata istog tipa podataka pohranjenih u kontinuiranom dijelu memorije.

  
**Svojstva:**

- ima konačan broj elemenata N
- svi elementi istog tipa
- elementi slijede jedan iza drugog
- direktan pristup svakom elementu O (1)

</details>

---
<br>
<br>

<details>
<summary><strong>10. Algoritam SEKVENCIJALNO PRETRAŽIVANJE niza. Složenost?</strong></summary>

```
Za svaki i=1 do N činiti 
  |  Ako je Vi =x onda 
  |      |  Ispiši “DA, na “,i,”. mjestu” 
  |      |  Završi algoritam 
Ispiši “NE”
```

Vremenska složenost algoritma: O(N) - “linearna složenost”

</details>

---
<br>
<br>

<details>
<summary><strong>11. Algoritam BINARNO PRETRAŽIVANJE niza. Složenost?</strong></summary>

```
Postaviti dg=1, gg=N 
Ponavljati  
  |  Postaviti s=[(dg+gg)/2] 
  |  Ako je Vs = x onda 
  |  |  Ispiši “DA, na”,s,”. mjestu” 
  |  |  Završi algoritam  
  |  Ako je x>Vs onda dg=s+1  
  |  Ako je x<Vs onda gg=s-1 
  |  Ako je dg>gg onda 
  |  |  Ispiši “NE” 
  |  | Završi algoritam
```

Vremenska složenost algoritma: O(log N)  “logaritamska složenost”

</details>

---
<br>
<br>

<details>
<summary><strong>12. Usporedba algoritama sekvencijalnog i binarnog pretraživanja niza.</strong></summary>

| Značajka          | Sekvencijalno                   | Binarno                            |
| ----------------- | ------------------------------- | ---------------------------------- |
| **Uvjet**         | Niz može biti nesortiran        | Niz mora biti sortiran             |
| **Brzina**        | O(n) – sporije za velike nizove | O(log n) – brzo i za velike nizove |
| **Jednostavnost** | Jednostavno za implementaciju   | Složenije                          |
| **Primjena**      | Male ili nesortirane nizove     | Velike, sortiran nizove            |


</details>

---
<br>
<br>

<details>
<summary><strong>13. Algoritam SELEKT-SORT. Složenost?</strong></summary>

- Prolazi se kroz polje i pronalazi najmanji element u njemu. Kad se pronađe, zamijeni se s početnim elementom. U sljedećem koraku prvi se element zanemari te se traži najmanji od preostalih elemenata, koji se premjesti na drugo mjesto.

- Vremenska složenost O(N 2) - “kvadratna složenost”

```
Za i=1 do n-1 činiti
|  mjesto_min=i;     
|  za j=i+1 do n činiti
|  |  ako je a[j]<a[mjesto_min] onda 
|  |  |  mjesto_min=j     
|  zamijeni(a[i],a[mjesto_min])
```

</details>

---
<br>
<br>

<details>
<summary><strong>14. Matrice (dvodimenzionalna polja) kao struktura podataka. Svojstva?</strong></summary>

Pravokutna shema podataka 
**Svojstva:**
- podaci su raspoređeni u M redaka i N stupaca
- svi elementi istog tipa
- direktan pristup svakom elementu
- Matricu A označavamo preciznije AˇMxN

</details>

---
<br>
<br>

<details>
<summary><strong>15. Primjer algoritma s matricom. Složenost?</strong></summary>

Množenje matrica:
```
Za svaki i = 1 do m 
|  Za svaki j = 1 do k 
|  |  Ci,j = 0 
|  |  |  Za svaki p = 1 do n 
|  |  |  |  Ci,j = Ci,j + Ai,p • B
```

</details>

---
<br>
<br>

<details>
<summary><strong>16. Algoritam MNOŽENJE KVADRATNIH MATRICA. Složenost?</strong></summary>

```
Za i = 1 do n:
|  Za j = 1 do n:
|  |  C[i,j] = 0
|  |  Za k = 1 do n:
|  |  |  C[i,j] = C[i,j] + A[i,k] * B[k,j]
```

</details>

---
<br>
<br>

<details>
<summary><strong>17. Statičko i dinamičko alociranje memorije. Objasniti na primjeru niza.</strong></summary>

**Statičko:**

- Veličina niza mora biti poznata unaprijed.
- Alocirana memorija se automatski oslobodi kada niz izađe iz opsega.

```C
#include <stdio.h>
int main() {
    int niz[5];
    for(int i = 0; i < 5; i++) {
        niz[i] = i + 1;
    }
    for(int i = 0; i < 5; i++) {
        printf("%d ", niz[i]);
    }
    return 0;
}
```
**Dinamičko:**

- Memorija se dodjeljuje za vrijeme izvođenja programa (runtime).
- Veličina niza može biti određena u toku izvođenja programa.
- Potrebno je ručno osloboditi memoriju kada više nije potrebna.

```C
#include <stdio.h>
#include <stdlib.h> 

int main() {
    int n;
    printf("Velicina niza: ");
    scanf("%d", &n);
    int *niz = (int*) malloc(n * sizeof(int));
    if(niz == NULL) {
        printf("Greska pri alociranju memorije");
        return 1;
    }
    for(int i = 0; i < n; i++) {
        niz[i] = i + 1;
    }
    for(int i = 0; i < n; i++) {
        printf("%d ", niz[i]);
    }
    free(niz);
    return 0;
}
```
</details>

---
<br>
<br>

<details>
<summary><strong>18. Memorijska adresa kao tip podataka.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>19. Povezani popis kao struktura podataka.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>20. Algoritam KREIRANJE POVEZANOG POPISA.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>21. Algoritam OBILAZAK POVEZANOG POPISA.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>22. Usporedba niza i povezanog popisa. Prednosti i mane.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>23. Algoritam INSERT SORT. Složenost?</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>24. Stog. Definicija, princip rada.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>25. Stog. Pomoću kojih struktura ga ostvarujemo?</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>26. Stog. Izvedba push i pop procedura kada je stog ostvaren pomoću niza.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>27. Stog. Izvedba push i pop procedura kada je stog ostvaren pomoću povezanog popisa.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>28. Stog. Primjer algoritma.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>29. Red. Definicija, princip rada.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>30. Red. Pomoću kojih ga struktura možemo ostvariti?</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>31. Red. Izvedba push i pop procedura.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>32. Red. Primjer algoritma.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>33. Rekurzivne funkcije. Definicije.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>34. Primjer jednostavne rekurzivne funkcije.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>35. Veza između rekurzivnih funkcija i stoga.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>36. Algoritam POVRH koristeći rekurziju.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>37. Algoritam QUICK SORT.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>38. Algoritam MERGE SORT.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>39. Stablo kao struktura podataka. Definicija.</strong></summary>



</details>

---

<br>
<br>

<details>
<summary><strong>40. Binarno stablo kao struktura podataka. Definicija.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>41. Binarno stablo. Prikaz u računalu.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>42. Binarno stablo. Algoritmi obilaska. Primjer jednog od njih.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>43. Poredano binarno stablo, definicija.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>44. Poredano binarno stablo, algoritam DODAJ P.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>45. Poredano binarno stablo, algoritam NADJI P.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>46. Poredano binarno stablo, algoritmi i njihova složenost.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>47. Prošireno binarno stablo, definicija i primjer.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>48. Prošireno binarno stablo, težinski put.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>49. Huffmanovo stablo i algoritam generiranja takvog stabla.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>50. Huffmanovo kodiranje.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>51. Potpuno binarno stablo, definicija i primjer.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>52. Potpuno binarno stablo, efikasni prikaz u računalu.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>53. Hrpa. Definicija, primjer.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>54. Hrpa. Algoritam NAPRAVI HRPU. Složenost.</strong></summary>



</details>

---
<br>
<br>

<details>
<summary><strong>55. Algoritam HEAP SORT. Složenost.</strong></summary>



</details>

---

<br>
<br>

<details>
<summary><strong>56. Hrpa. Dodavanje čvorova u hrpu.</strong></summary>



</details>

---

<br>
<br>

<details>
<summary><strong>57. Hrpa. Brisanje čvorova iz hrpe.</strong></summary>



</details>

---

<br>
<br>

