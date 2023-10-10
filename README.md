# Configuración de netplan en el servidor FTP

    network:
        
      version: 2
          
      ethernets:
          
        ens33:
            
          dhcp4: true
              
          dhcp4-overrides:
              
            use-dns: no
                
          nameservers:
              
            addresses: [???.???.???.???]

IMPORTANTE: reemplazar ???.???.???.??? por la dirección IP del servidor DNS y no borres los corchetes.

# Configuración previa del servidor DNS

sudo apt update

sudo apt upgrade -y

sudo apt install -y bind9 bind9-utils ipcalc dos2unix

cd ~/

sudo su

IMPORTANTE: La maquina virtual debe ser nueva y debe hacer ping con el servidor FTP.

# Copia y Pega los siguentes comandos en el servidor DNS

curl -o dns_script1.txt "https://raw.githubusercontent.com/sstiago1243/VM_dns/main/1.txt"

curl -o dns_script2.txt "https://raw.githubusercontent.com/sstiago1243/VM_dns/main/2.txt"

chmod +x dns_script1.txt && dos2unix dns_script1.txt

chmod +x dns_script2.txt && dos2unix dns_script2.txt

./dns_script1.txt


# Después de que reinicie el sistema ejecute los siguientes comandos

cd ~/

sudo su

./dns_script2.txt ???.???.???.???

IMPORTANTE: reemplaza ???.???.???.??? con una dirección IP.
