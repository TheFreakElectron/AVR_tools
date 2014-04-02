#include<avr/io.h>
#define FOSC 16000000 // Clock Speed
#define BAUD 31250 // baud rate
#define MYUBRR FOSC/16/BAUD-1
void USART_Init(unsigned int ubrr);

int main( void )
{
  USART_Init(MYUBRR);
  /*YOUR CODE GOES HERE*/
}

void USART_Init(unsigned int ubrr)
{
  /* Set baud rate */
  UBRR0H = (unsigned char)(ubrr>>8);
  UBRR0L = (unsigned char)ubrr;
  /* Enable receiver and transmitter */
  UCSR0B = (1<<RXEN0)|(1<<TXEN0);
  /* Set frame format: 8data, 2stop bit */
  UCSR0C = (1<<USBS0)|(3<<UCSZ00);
}

/*

To compile in GCC:
avr-gcc -mmcu=atmega328p -Wall -Os -o uart_basic_template.elf UART_BASIC_TEMPLATE.C

To create .hex in GCC:
avr-objcopy -j .text -j .data -O ihex uart_basic_template.elf uart_basic_template.hex

To upload in AVRdude:
sudo avrdude -p m328p -c usbtiny -e -U flash:w:uart_basic_template.hex

*/
