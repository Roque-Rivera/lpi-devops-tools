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


