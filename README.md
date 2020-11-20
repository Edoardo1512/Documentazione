# Documentazione
Breve documentazione sui comandi per creare un web server sulla macchina  virtuale

Passaggi eseguiti:

- aggiornare i pacchetti:
  - apt update
  - apt upgrade
  
- installare il server ssh
  - #apt install openssh-server
  
- modificare il file della configurazione di rete in questo modo:

      network:
  
        version: 2
    
        renderer: networkd
    
        ethernets:
    
          enp0s3:
      
            addresses: [172.16.29.112/16]
        
        
        
    
