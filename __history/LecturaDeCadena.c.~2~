#include <18F4620.h>
#include <stdlib.h>
#fuses HS, NOFCMEN, NOIESO, PUT, NOBROWNOUT, NOWDT
#fuses NOPBADEN, NOMCLR, STVREN, NOLVP, NODEBUG
#use delay(clock=16000000)
#define __DEBUG_SERIAL__ //Si comentas esta linea se deshabilita el debug por serial y el PIN_C6 puede ser usado en forma digital I/O

#ifdef __DEBUG_SERIAL__
   #define TX_232        PIN_C6
   #define RX_232        PIN_C7
   #use RS232(BAUD=9600, XMIT=TX_232, BITS=8,PARITY=N, STOP=1,UART1,RCV=RX_232)
   #use fast_io(c)
#endif 

char buffer[9]={""};
char cadena;

#int_timer0
void timer_0()
{
    output_toggle(pin_e0);
    set_timer0(5);
}
#INT_RDA
void isrRDA (void)
{

}

void main (void){
    setup_timer_0(RTCC_INTERNAL | RTCC_DIV_128);
    set_timer0(5);
    enable_interrupts(int_timer0);
    enable_interrupts(GLOBAL);
    enable_interrupts(INT_RDA);
    enable_interrupts(GLOBAL);
    printf("\nIngresa una cadena y un numero: \n"); 
while(TRUE){
     enable_interrupts(INT_RDA);
     enable_interrupts(GLOBAL);
    }
}
