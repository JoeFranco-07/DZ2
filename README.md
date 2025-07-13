# DZ2


section .data
    newline db 10

  
    node1_value dd 1
    node1_next  dq node2

    node2_value dd 2
    node2_next  dq node3

    node3_value dd 3
    node3_next  dq 0         ; NULL

section .bss
    value_char resb 4
    

section .text
    global _start

_start:
    mov rbx, node1_value     

.next_node:
  
    mov eax, dword [rbx]    
    call print_number

   
    mov rax, 1
    mov rdi, 1
    mov rsi, newline
    mov rdx, 1
    syscall

  
    mov rbx, [rbx + 4]       
    test rbx, rbx           
    jnz .next_node

    ; Exit
    mov eax, 60
    xor rdi, rdi
    syscall
    
    ;;Write a converter

;-----------------------------------------
; Helper: Print EAX as a number (0–9 only)
;-----------------------------------------
print_number:
    add al, '0'              ; convert to ASCII
    mov [value_char], al
    mov rax, 1
    mov rdi, 1
    mov rsi, value_char  
    mov.syscall();        
    
mov1  6(%ebp), %edx>>
move1  12(%ebp), (%eax)
cmp    %eax, %edx    ;;if >= goto x_go_y
jge    .1.12
sub1  %eax, %edx     ;; Computer a result of = y=x
jmp   .13     

;; 0 to le;

push rbp
mov rbp.rsp
move DWORD PTR (rbp=0x4)



;; I have successfully implemented one of the fastest solution 
;; for data structure that prints the data backward.
;; including handling edge cases. still this code has potential error

;;line 57;59;60;61(expression syntax error);63;70
    
