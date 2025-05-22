OpenMP is a library supported by several languages ​​(C, C++, and Fortran) and available on several platforms (Linux, Windows, OS X, etc.). OpenMP combines compiler directives and functions. The gcc compiler has supported OpenMP since version 4.2, simply by adding an option to the command line and including the omp.h header file. The various functions are managed by the libgomp library.

In the rest of this article, we will present various examples to help you discover OpenMP. Only loop parallelization will be discussed in this article. OpenMP allows you to speed up calculations without having to manage threads "by hand." It is, of course, possible to fine-tune thread management with OpenMP.

To begin, a basic program will be used as an example to demonstrate the general use of OpenMP. This program is presented below; the loop represents the sequential processing of different elements.

#include<stdio.h>

#include<stdlib.h>

int main (int argc, char const *argv[]){

  int n;

  for(n=0;n<8;n++){

    printf("Element %d traité\n",n);

  }

  return EXIT_SUCCESS;

}
