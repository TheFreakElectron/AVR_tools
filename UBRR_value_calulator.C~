#include<stdio.h>

int main()
{
  float baud_rate;
  int clock_freq;
  int UBRR;
  float error;

  printf("baud rate: ");
  scanf("%f", &baud_rate);
  printf("clock frequency (Hertz): ");
  scanf("%d", &clock_freq);
  baud_rate = 16*baud_rate;
  baud_rate = clock_freq / baud_rate -1;
  UBRR = baud_rate;
  printf("UBRR = %d\n",UBRR);
  error = UBRR - baud_rate;
  error = error/baud_rate*100;
  printf("error = %f%%\n",error);

return 0;
}

/*

To compile: 
gcc UBRR.C -o ubrr

To run:
./ubrr

*/

