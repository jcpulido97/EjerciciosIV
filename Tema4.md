# Virtualización ligera usando contenedores

## 1 

```bash
$ sudo apt-get install lxc lxc-templates -y
```

Y si todo está correcto con el siguiente comando obtendríamos

```bash
$ lxc-checkconfig 
Kernel configuration not found at /proc/config.gz; searching...
Kernel configuration found at /boot/config-4.2.0-27-generic
--- Namespaces ---
Namespaces: enabled
Utsname namespace: enabled
Ipc namespace: enabled
Pid namespace: enabled
User namespace: enabled
Network namespace: enabled
Multiple /dev/pts instances: enabled

--- Control groups ---
Cgroup: enabled
Cgroup clone_children flag: enabled
Cgroup device: enabled
Cgroup sched: enabled
Cgroup cpu account: enabled
Cgroup memory controller: enabled
Cgroup cpuset: enabled

--- Misc ---
Veth pair device: enabled
Macvlan: enabled
Vlan: enabled
Bridges: enabled
Advanced netfilter: enabled
CONFIG_NF_NAT_IPV4: enabled
CONFIG_NF_NAT_IPV6: enabled
CONFIG_IP_NF_TARGET_MASQUERADE: enabled
CONFIG_IP6_NF_TARGET_MASQUERADE: enabled
CONFIG_NETFILTER_XT_TARGET_CHECKSUM: enabled
FUSE (for use with lxcfs): enabled

--- Checkpoint/Restore ---
checkpoint restore: enabled
CONFIG_FHANDLE: enabled
CONFIG_EVENTFD: enabled
CONFIG_EPOLL: enabled
CONFIG_UNIX_DIAG: enabled
CONFIG_INET_DIAG: enabled
CONFIG_PACKET_DIAG: enabled
CONFIG_NETLINK_DIAG: enabled
File capabilities: enabled

Note : Before booting a new kernel, you can check its configuration
usage : CONFIG=/path/to/config /usr/bin/lxc-
```



## 2 Crear y ejecutar un contenedor basado en tu distribución y otro basado en otra distribución, tal como Fedora



## 3 Instalar docker

Primero hemos de instalar las siguientes dependencias

```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Añadir las claves públicas del repo de Docker

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Añadir el repo oficial de docker

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```

Ahora debemos de actualizar el sistema para que este instale las nuevas dependencias añadidas

```
sudo apt update
```

Ahora instalamos la versión docker-ce oficial del repo añadido.

```
sudo apt install docker-ce
```



## 4 Instalar a partir de docker una imagen alternativa de Ubuntu y alguna adicional, por ejemplo de CentOS. Buscar e instalar una imagen que incluya MongoDB.

El siguiente comando descargará la última imagen que haya disponible de CentOS

```
docker pull centos:latest
```

Para descargar la imagen de MongoDB la podremos buscar en [dockerhub](https://hub.docker.com/) 

```
docker pull bitnami/mongodb:latest
```



## 7  Crear un Dockerfile para el servicio web que se ha venido desarrollando en el proyecto de la asignatura.

Para mi servicio web he creado el siguiente [Dockerfile](https://github.com/jcpulido97/ProyectoIV/blob/master/Dockerfile)



## 8 Desplegar un contenedor en alguno de estos servicios, de prueba gratuita o gratuitos.

[Aquí](https://github.com/jcpulido97/ProyectoIV/blob/master/doc/docker.md) explico como hago el despliegue de mi docker en Heroku.