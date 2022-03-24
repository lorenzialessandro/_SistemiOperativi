Principi di progettazione
- principio della **separazione tra policy e meccanismi**
	- policy : cosa deve essere fatto
		- non cambiano molto
	- meccanismi : come deve essere fatto
		- implementazione
		- cambia spesso (modifica, aggiunta, ...)
- principio di **KISS**: Keep it small and simple
	- per programmi di sistema dove performace è molto importante
	- partire da efficienza e aggiungere funzionalità solo se necessario
- principio **POLA**: Principle of the Least Privileges
	- ogni componente deve avere solo privilegi necessari per la funzione che deve fare, niente di più
	- se quel modulo si guasta o è compromesso, il danno che fa è il minimo
	- affidabilità e sicurezza del so
	- difficile da mettere in pratica
	- di fatto non è implementato da nessun so