# TUTORIAT SISTEME DE OPERARE #2

**Topics:**
* Environmentul

## Environmentul

Environmentul reprezinta totalitatea variabilelor de mediu ce descriu un proces.
Aceste variabile sunt intotdeauna de forma “NAME=VALUE” si au diferinte functionalitati.
Una dintre aceste variabile este `PATH` – daca avem un program executabil in unul din path-urile din aceasta variabila, executabilul respective poate fi executat de oriunde.

## Afisarea environmentului

* Prin al treilea parametru al functiei main – `char** envp`

> !!! Acest parametru ne ajuta sa vizualizam environmentul procesului la inceputul acestuia.
> Daca vrem sa modificam variabilele de mediu, trebuie folosit `environ`.!!!

```c
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

int main(int argc, char** argv, char** envp)
{
    for(int i=0; envp[i]!=NULL; i++)
        printf("%s\n", envp[i]);

    return 0;
}
```
* Prin utilizarea variabilei externe (vizibila pentru toate procesele din calculator) – `extern char** environ`

```c
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>

extern char** environ;

int main(int argc, char** argv, char** envp)
{
    char** env=environ;
    while(*env!=NULL)
    {
      printf("%s\n",*env);
      env++;
    }

    return 0;
}
```
