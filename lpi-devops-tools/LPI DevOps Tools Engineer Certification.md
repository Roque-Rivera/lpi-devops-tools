# LPI DevOps Tools Engineer Certification
## Instalacion máquina playground
```
# retrieve and check CENTOS_MAIN_VERSION (6 or 7):
CENTOS_MAIN_VERSION=$(cat /etc/centos-release | awk -F 'release[ ]*' '{print $2}' | awk -F '.' '{print $1}')
echo $CENTOS_MAIN_VERSION
# output should be "6" or "7"

# Install IUS Repo and Epel-Release:
yum install -y https://repo.ius.io/ius-release-el${CENTOS_MAIN_VERSION}.rpm
yum install -y epel-release 

# re-install git:
yum erase -y git*
yum install -y git-core

#Install homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
#Install github cli
brew install gh

# Install terraform
wget https://releases.hashicorp.com/terraform/0.13.5/terraform_0.13.5_linux_amd64.zip
unzip terraform_0.13.5_linux_amd64.zip
mv terraform /usr/local/bin/
rm -f terraform_0.13.5_linux_amd64.zip

# Install vagrant
sudo yum install -y https://releases.hashicorp.com/vagrant/2.2.10/vagrant_2.2.10_x86_64.rpm

# Install packer
wget https://releases.hashicorp.com/packer/1.6.5/packer_1.6.5_linux_amd64.zip
unzip packer_1.6.5_linux_amd64.zip
mv packer /usr/local/bin/
rm -f packer_1.6.5_linux_amd64.zip


```





## Vagrant

```
# Iniciar entorno (crea vagrantfile)
vagrant init
# Levanta entorno
vagrant up
# Destruye entorno
vagrant destroy
# Valida sintaxis
vagrant validate
# Ejecuta provisionadores
vagrant provision
# Reinicia el entorno (para y vuelve a arrancar)
vagrant reload
# Muestra es estado de las instancias
vagrant status
# Accede a la shell de una instancia
vagrant ssh


