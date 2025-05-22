OpenMP est une bibliothèque supportée par plusieurs langages (C,C++ et Fortran) disponible sur plusieurs plate-formes (Linux, Windows, OS X, ...). OpenMP regroupe des directives de compilation et des fonctions. Le compilateur gcc supporte OpenMP depuis la version 4.2, en ajoutant simplement une option sur la ligne de commande et en incluant le fichier d'en-têtes omp.h. La gestion des différentes fonctions est assurée par la libraire libgomp.

Dans la suite de cet article, nous présenterons différents exemples pour découvrir OpenMP. Seule la parallélisation des boucles sera abordée dans cet article. OpenMP permet d'accélérer les calculs sans devoir gérer les threads « à la main ». Il est bien sûr possible de gérer finement les threads avec OpenMP.



Pour commencer, un programme élémentaire va être pris comme exemple pour montrer l'utilisation générale d'OpenMP. Ce programme est présenté ci-dessous, la boucle représente le traitement de différents éléments de manière séquentielle.

#include<stdio.h>

#include<stdlib.h>

int main (int argc, char const *argv[]){

  int n;

  for(n=0;n<8;n++){

    printf("Element %d traité\n",n);

  }

  return EXIT_SUCCESS;

}
