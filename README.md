# Documentazione
Breve documentazione sui comandi per creare un web server sulla macchina  virtuale

Passaggi eseguiti:

- aggiornare i pacchetti:
  - apt update
  - apt upgrade
  
- installare il server ssh
  - #apt install openssh-server
  
- accedere al file della configurazione di rete con i seguenti comandi:
  - cd /etc/netplan/
  - sudo nano 00-installer-config.yaml
  
- modificare il file della configurazione di rete in questo modo:

      network:
  
        version: 2
    
        renderer: networkd
    
        ethernets:
    
          enp0s3:
      
            addresses: [172.16.29.112/16]
            
            gateway4: 172.16.1.7
            
            nameservers:
            
              addresses: [172.16.1.10, 172.16.1.18]

-  salvare il file e successivamente applicare le modifiche con il comando:
   - netplan try

- installare apache2
  - apt install apache2
        
        
        
    
