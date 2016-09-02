# Instalando Jekyll

Instalar Jekyll en Linux.

"Caminante, no hay camino,
se hace camino al andar
al andar se hace camino..."


----
## Instalar Docker

```bash
sudo apt-get install docker.io
```

![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/VM_Docker.png)

_
====
### Docker version

```bash
docker --version
Docker version 1.11.2, build b9f10c9
```

Añada su usuario en /etc/group linea docker:
```bash
docker:x:117:miusuario
```

_
====
### Testing docker

```bash
docker run -i -t ubuntu /bin/bash
```

_
====
### Testing docker

```bash
docker run -d -p 80:80 oems/wikkawiki
```

```bash
run --rm  -p 1234:80 -e ALLOW_ARBITRARY=1 nazarpc/phpmyadmin
```
https://hub.docker.com/r/oems/wikkawiki/

----
## Instalar Git

```bash
sudo apt-get install git
```

_
====
## Clonar Jekyll Pages

```bash
git clone git clone https://github.com/poole/poole.git
```

_
====
## Running Jekyll

```bash
docker run -p 4000:4000 --rm -it -v $PWD:/srv/jekyll jekyll/jekyll:pages sh -c 'bundle exec jekyll serve'
```
