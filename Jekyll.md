<section data-background="https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/jekyllback.png" data-markdown>
# Laboratorio Docker y Jekyll

Instalar Jekyll en Linux.

"Caminante, no hay camino,
se hace camino al andar..."


----
## Instalar Docker on ubuntu


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

Anada su usuario en /etc/group linea docker:
```bash
docker:x:117:miusuario
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/docker.png)

_
====
### Testing docker

```bash
docker run -i -t ubuntu /bin/bash
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/ubuntu.jpg)

```bash
docker run -i -t fedora /bin/bash
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/fedora.png)

_
====
### phpmyadmin instance

```bash
docker run --rm  -p 8080:80 -e ALLOW_ARBITRARY=1 nazarpc/phpmyadmin
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/phpmyadmin.png)

_
====
### wordpress instance


```bash
docker run -d -p 8081:80 tutum/wordpress
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/wordpress.png)

_
====
### LAMP example:

```bash
docker run -d -p 8082:80 oems/wikkawiki
```
https://hub.docker.com/r/oems/wikkawiki/

![alt tag](https://github.com/oemunoz/wikkawiki/raw/master/images/wikka_logo.jpg)

----
## Instalar Git

```bash
sudo apt-get install git
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/GitAll.png)

_
====
## Clonar Jekyll Pages

```bash
git clone git clone https://github.com/poole/poole.git
```

```bash
cd poole
wget https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/Gemfile .
```

_
====
## Running Jekyll

```bash
docker run -p 4000:4000 --rm -it -v $PWD:/srv/jekyll jekyll/jekyll:pages sh -c 'bundle exec jekyll serve'
```
![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/jekyll.png)

_
====
## Using it

[oemunoz](https://oemunoz.github.io/)

![alt tag](https://raw.githubusercontent.com/oemunoz/IntegracionRedes/master/images/MatrixAir.jpg)

_
====
### Useful links
[WordPress vs. Jekyll](https://www.sitepoint.com/wordpress-vs-jekyll-might-want-make-switch/)
