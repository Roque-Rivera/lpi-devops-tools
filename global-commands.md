# LPI DevOps Tools Engineer Certification
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
```

## Packer

Necesita un package.json con las variables, builders, provisioners, post-processors
```
# Valida la sintaxis
packer validate
# Contruye la imagen
packer build -var 'variable'


