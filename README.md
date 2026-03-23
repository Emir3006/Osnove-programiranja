#include <stdio.h>

int main() {
  char karakter;

  // karakter = getchar();
  scanf("%c", &karakter);

  printf("Uneseni karakter je |%c|\n", karakter);

  switch (karakter) {
    case 'A':
    case 'E':
    case 'I':
    case 'O':
    case 'U':
    case 'a':
    case 'e':
    case 'i':
    case 'o':
    case 'u':
      puts("samoglasnik");
      break;
    default:
      puts("Suglasnik");
  }
  // Pitanje: da li default moze doci prvi (prije case-a)?
}
