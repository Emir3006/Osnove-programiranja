#include <stdio.h>

// Unijeti datum. Korisniku ispisati koliko je dana proslo od 1. januara
// tekuce godine.

int main() {
  printf("Unesite datum");
  int d, m, g;
  scanf("%d %d %d", &d, &m, &g);

  int prestupna = (g % 4 == 0 && g % 100 != 0) || (g % 400 == 0);
  printf("Prestupna: %d", prestupna);

  long count = 0;

  switch (m) {
    case 12:
      count += 30;
    case 11:
      count += 31;
    case 10:
      count += 30;
    case 9:
      count += 31;
    case 8:
      count += 31;
    case 7:
      count += 30;
    case 6:
      count += 31;
    case 5:
      count += 30;
    case 4:
      count += 31;
    case 3:
      count += 28 + prestupna;
    case 2:
      count += 31;
    case 1:
      count += 0;
  }
  count += d;

  printf("Trenutno je %ld. dan u godini\n", count);
}
