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

![alt tag](https://github.com/oemunoz/secretarytool/raw/master/images/db_1.png)

_
====
### Docker version

```bash
docker --version
Docker version 1.11.2, build b9f10c9
```
_
====
### Devices status
- arch
- uname -m
- uname -r
- dmidecode -q
- ls -all

![alt tag](https://github.com/oemunoz/IntegracionRedes/raw/master/images/firstCommands.png)

_
====

cat /proc/cpuinfo
cat /proc/interrupts
cat /proc/meminfo

----
## Instalar Git

```bash
sudo apt-get install git
```

----
## Clonar Jekyll Pages

```bash
git clone git clone https://github.com/poole/poole.git
```

```bash
docker run -p 4000:4000 --rm -it -v $PWD:/srv/jekyll jekyll/jekyll:pages sh -c 'bundle exec jekyll serve'
```
