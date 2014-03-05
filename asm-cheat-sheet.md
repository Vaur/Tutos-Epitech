# ASM Cheat sheet

## Registre pour les paramètres

```asm
rdi ; premier paramètre
rsi ; second paramètre
rdx ; troisième paramètre
```

## prologue et epilogue

```asm
function:
	push	rbp
	mov	rbp,	rsp

function_end:
	mov	rsp,	rbp
	pop	rbp
	ret
```