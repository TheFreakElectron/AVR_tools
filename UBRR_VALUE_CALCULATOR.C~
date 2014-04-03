#include<stdio.h>

int main()
{
  float target_baud_rate;
  int clock_freq;
  int UBRR;
  float error;
  int mode;
  float baud_rate;
  mode = 16;

  printf("select mode\n1. Asynchronous Normal Mode\n2. Asynchronous Double speed\n3. Synchronous Master Mode: ");
  scanf("%d", &mode);
  if(mode == 1)mode = 16;
  if(mode == 2)mode = 8;
  if(mode == 3)mode = 2;
  printf("target baud rate: ");
  scanf("%f", &target_baud_rate);
  printf("clock frequency (Hertz): ");
  scanf("%d", &clock_freq);
  UBRR = mode*target_baud_rate;
  UBRR = clock_freq / UBRR -1;
  printf("UBRR = %d\n",UBRR);
  baud_rate = UBRR + 1;
  baud_rate = mode*baud_rate;
  baud_rate = clock_freq/baud_rate;
  printf("baud rate = %f\n",baud_rate);
  error = baud_rate / target_baud_rate -1;
  error = error*100;
  printf("error = %f%%\n",error);

return 0;
}

/*

To compile with GCC: 
gcc UBRR_VALUE_CALCULATOR.C -o ubrr_value_calculator

To run:
./ubrr_value_calculator

*/

