# Comandos para configurar DNS

cd ~/

sudo apt update

sudo apt upgrade -y

sudo apt install -y bind9 bind9-utils ipcalc

curl -o dns_script1.txt "https://raw.githubusercontent.com/sstiago1243/VM_dns/main/1.txt"

curl -o dns_script2.txt "https://raw.githubusercontent.com/sstiago1243/VM_dns/main/2.txt"

sudo su

chmod +x dns_script1.txt

chmod +x dns_script2.txt

./dns_script1.txt


# Despues de que reinicie el sistema ejecute los siguientes comandos

cd ~/

sudo su

./dns_script2.txt
