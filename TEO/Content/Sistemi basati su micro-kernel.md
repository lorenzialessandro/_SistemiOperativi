Sistemi basati su micro-kernel
- mettere nel **kernel solo ciò che è strettamente necessario**
	- IPC, gestore memoria, scheduling pcu
	- resto gira in mod utente
- vantaggio
	- meno codice
	- sistema piu stabile
	- facile da mantenere
	- modulare
	- sicurezza
	- porting facile
- svantaggio
	- performance
		- che sono la cosa più importante