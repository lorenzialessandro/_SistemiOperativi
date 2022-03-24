Creazione processo in UNIX
- system call `fork`
	- trasforma un singolo processo in due processi identici, riconoscibili come processo padre e processo figlio
	- crea figlio come **clone** del padre
	- c'è condivisone
	- crea due processi clone
- system call `exec`
	- cambiare natura del figlio
	- cambiare la copia esatta del figlio fatta con fork
	- cambio programma caricato rispetto a quello del padre
- system call `wait`
	- determinare se esecuzione è sincrona tra padre e figlio o no
- codice slide 23
	- fork ritorna
		- -1 errore (ex non c'è abbastanza mem)
		- 0 al figlio (non è il suo pid)
			- figlio non può arrivare al padre con pid (0 non è il pid del padre)
			- usa system call get..()
		- pid del figlio assegnato al padre
			- padre arriva al figlio col pid tornato
		- wait decide se asincrona o sincrona
			- con NULL aspetta figlio finisca
- il codice non viene duplicato al figlio
	- quindi meno memoria occupata
	- se padre occupa n spazio di mem, figlio non è tutto n