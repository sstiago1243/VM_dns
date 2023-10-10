# Comandos para configurar DNS

cd ~/

sudo apt update

sudo apt upgrade -y

sudo apt install -y bind9 bind9-utils ipcalc

curl -L -o dns_script1.txt "https://drive.google.com/file/d/1AaffYidkcOl37L_6IFllgE4cqgR9Jc5R/view?usp=drive_link"

curl -L -o dns_script2.txt "https://drive.google.com/file/d/19VCyDj3vVkSf7Y8-6-C5c8HrvTeH5YEE/view?usp=drive_link"

sudo su

chmod +x dns_script1.txt

chmod +x dns_script2.txt

./dns_script1.txt


# Despues de que reinicie el sistema ejecute los siguientes comandos

cd ~/

sudo su

./dns_script2.txt
