# ASM Cheat sheet

Note: beaucoup d'anglicismes sont utilisé ici, pour deux bonnes raisons: la première c'est que je ne connais pas forcément la traduction correcte en anglais, la seconde est que tout le monde saura de quoi je parle.

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
	rte
```

Explication: le prologue de la fonction push l'ancien base pointer sur la stack pour pouvoir le restaurer.
