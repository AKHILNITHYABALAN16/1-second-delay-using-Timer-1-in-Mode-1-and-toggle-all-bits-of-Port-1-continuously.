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
<img width="1455" height="730" alt="Screenshot 2025-10-25 084225" src="https://github.com/user-attachments/assets/8cae6ccb-b5c5-4b5a-8a9e-0ea1610a684f" />

## RESULT
Thus, an assembly language program in 8051 to generate a 1 second delay using Timer 1 in Mode 1 and toggle all bits of Port 1 continuously is executed successfully using 8051 Keil.
