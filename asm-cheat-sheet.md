# ASM Cheat sheet

## Registre pour les paramètres

```asm
rdi ;; premier parametre
rsi ;; second parametre
rdx ;; troisieme parametre
```

## prologue et epilogue

```asm
function:
	;; prologue
	push	rbp				
	mov		rbp,	rsp

function_end:
	;; epilogue
	mov		rsp,	rbp
	pop		rbp
	ret
```