Go to live! kata
==================================

# Ansible Wordpress + Apache + PHP + MySQL

In questo progetto ho utlizzato le componenti wordpress (versione 4.9.6), apache, php e mysql vengono deployate automaticamente su 2 macchine virtuali (vm), che vengono instanziate da vagrant. Come specificato nel file 'host', in una vm (AppServer) viene deployato MySQL server mentre nella vm WebServer vengono caricate le componenti Wordpress, Apache e PHP.
Gli indirizzi IP e le porte delle due VM sono specificati nel Vagrantfile.

Allo scopo di rendere più ordinato il codice, ho utilizzato _ansible-galaxy_.

L'accesso a Wordpress si effettua immettendo l'url l'indirizzo relativo della VM WebServer, il quale effettuerà una connessione al db mysql(con nome utente e password) 

## Requisiti
* Ansible (versione >= 2.5.3)
* Vagrant (versione >= 2.1.1)
* OpenSSL
* Virtualbox

## Istruzioni
1. Scaricare l'immagine ubuntu 14.04 x64.
2. Settare l'IP delle vm nel file _Vagrantfile_, oppure lasciare quelle preimpostate.
3. Eseguire 'vagrant up'.
4. Terminato la creazione dell'infrastruttura e il deploy delle app, immettere nel url del browser l'IP della vm dove si trova Wordpress.
5. Creare il proprio sito.
