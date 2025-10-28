# 1-second-delay-using-Timer-1-in-Mode-1-and-toggle-all-bits-of-Port-1-continuously.
## AIM
To Write an assembly language program in 8051 to generate a 1 second delay using Timer 1 in Mode 1 and toggle all bits of Port 1 continuously.

## APPARATUS REQUIRED
Personal computer with Keil software

## PROGRAM
```
ORG 0000H

MAIN:
    MOV TMOD, #10H       
    MOV TH1, #00H        
    MOV TL1, #00H        
    SETB TR1             
HERE:
    MOV R7, #15          
DELAY_LOOP:
    JNB TF1, $            
    CLR TF1               
    DJNZ R7, DELAY_LOOP   
	
    XRL P1, #0FFH         
    SJMP HERE             

END
```

## OUTPUT

![WhatsApp Image 2025-10-28 at 13 09 32_6752222f](https://github.com/user-attachments/assets/ed245dfe-16cb-415d-80e8-0755bc88329f)

## RESULT
Thus, an assembly language program in 8051 to generate a 1 second delay using Timer 1 in Mode 1 and toggle all bits of Port 1 continuously is executed successfully using 8051 Keil.
