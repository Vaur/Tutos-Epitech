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
	push	rbp				;; prologue
	mov		rbp,	rsp

function_end:
	mov		rsp,	rbp		;; epilogue
	pop		rbp
	ret
```