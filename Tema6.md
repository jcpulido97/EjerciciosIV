# Gestión de infraestructuras virtuales

## 1 Desplegar la aplicación de DAI con todos los módulos necesarios usando un *playbook* de Ansible.

Se explica [aquí](https://github.com/jcpulido97/ProyectoIV/blob/master/doc/Ansible.md) el despliegue que hago con Ansible



## 2 Instalar una máquina virtual Debian usando Vagrant y conectar con ella. 

Para crear una máquina virtual con vagrant es fácil. 

Primero debemos inicializar la vm y crear el Vagrantfile automáticamente.

```vagr
vagrant init ubuntu/trusty64
```

Después debemos de iniciarla

```
vagrant up
```

Esto realizará todas las configuraciones necesarias para iniciar nuestra máquina además de dar acceso a la máquina mediante ssh.

```
vagrant ssh
```

Nos creará una sesión ssh dentro de nuestra recién creada máquina virtual.

