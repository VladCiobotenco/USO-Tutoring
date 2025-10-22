# TUTORIAT SISTEME DE OPERARE #1

## Topics:

### Instalarea WSL (pentru cei care nu au masina virtuala sau dual boot cu linux) 

1.  Pentru a instala **WSL (Windows Subsystem for Linux)** trebuie sa va descarcati pentru inceput **Ubuntu** din Microsoft Store.
2.  [cite_start]Dupa aceea, deschideti terminalul **Windows PowerShell** si rulati comanda `wsl.exe –install`[cite: 5].
3.  [cite_start]Dupa finalizarea descarcarii, va trebui sa dati restart la laptop/pc[cite: 6]. [cite_start]Cand se deschide sistemul, intrati pe **Ubuntu**[cite: 6].
4.  [cite_start]Se vor instala mai multe lucruri si vi se va cere sa introduceti un **username** si o **parola**[cite: 7]. [cite_start]**NU UITATI PAROLA!!!**[cite: 8].
5.  [cite_start]Odata ce se finalizeaza instalarea, va trebui sa instalati un compilator pentru C[cite: 8]. [cite_start]Cel mai uzual este **gcc**[cite: 8].
6.  [cite_start]Pentru a-l instala trebuie sa rulati comanda `sudo apt install gcc`[cite: 9]. [cite_start]Sistemul va cere parola pe care ati setat-o mai devreme deoarece orice comanda care este precedata de argumentul `sudo` este o comanda data cu drepturi de administrator[cite: 9].
7.  [cite_start]Vor aparea niste erori, asa ca va trebui sa rulati comanda `sudo apt-get update`[cite: 10].
8.  [cite_start]La final reincercati comanda pentru instalarea gcc-ului[cite: 11].

---

## [cite_start]Comenzi uzuale [cite: 12]

[cite_start]Exista un set de comenzi uzuale pe care le veti folosi[cite: 13]:

* [cite_start]`cd [director/path_catre_un_director]` – mergem in directorul ales [cite: 14]
* [cite_start]`cd ..` – merge in directorul parinte (practic facem un pas inapoi) [cite: 15]
* [cite_start]`ls` – afiseaza continutul directorului curent [cite: 16]
* [cite_start]`mkdir [nume_director]` – cream un director cu numele specificat [cite: 17]
* [cite_start]`rmdir [nume_director]` – stergem directorul cu numele specificat (pentru directoare goale) [cite: 18]
* [cite_start]`rm -r [nume_director]` – stergem un director care contine lucruri[cite: 19]. `-r` specifica ca va avea loc o stergere recursiva, in care toate elementele incluse in directorul specificat vor fi eliminate[cite: 19].
* [cite_start]`rm [nume_fisier]` – stergem fisierul ales [cite: 20]
* [cite_start]**!!!nano este un editor de texte; putem utiliza `nano [nume_fisier]` pentru a deschide un fisier existent sau pentru a crea si deschide un fisier nou!!!** [cite: 21]

---

## [cite_start]Cum lucrez? [cite: 22]

1.  [cite_start]In primul rand trebuie creat un fisier cu codul sursa[cite: 23].
2.  [cite_start]Vom utiliza comanda `nano [nume_fisier].c` pentru a face un fisier nou (nu uitati ca trebuie sa aiba terminatia `.c`)[cite: 24].
3.  [cite_start]In el vom scrie codul, iar pentru salvare folosim **ctrl x -> y -> enter**[cite: 25].
4.  [cite_start]Odata ce avem un fisier cu cod, il vom compila cu `gcc -Wall -o [nume_executabil] [nume_fisier].c` si vom rula executabilul cu `./[nume_executabil]`[cite: 26].
5.  [cite_start]Puteti stabili orice nume pentru executabil, nu trebuie sa aiba legatura cu numele fisierului care contine codul sursa[cite: 27].

---

## [cite_start]Notiuni elementare in limbajul de programare C [cite: 28]

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    FILE* f=fopen("fisier.txt", "r");

    if(f==NULL)
    {
        printf("Eroare la deschiderea fisierului de intrare!");
        return 1;
    }

    int n,x,i,s=0;
    fscanf(f,"%d",&n);

    for(i=1;i<=n;i++)
    {
        fscanf(f, "%d", &x);
        s=s+x;
    }
    fclose(f);

    FILE* g=fopen("fisier.out", "w");
    if(g==NULL)
    {
        printf("Eroare la deschiderea fisierului de intrare!");
        return 2;
    }
    fprintf(g, "Suma este %d\n", s);
    fclose(g);

    return 0;
}```
