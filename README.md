# Practica Cloud Java 2022-2023

Aitor Iturrioz & Pablo Rubio

Este repositorio es el código inicial del ejercicio principal del Curso Cloud de Tknika.


**Instrucciones de comandos de  instalación en Ubuntu**

Eliminar versiones previas:

```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

Configura el repositorio de apt:

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

```bash
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Actualiza los repositorios apt:

```bash
sudo apt update
```

Instala Docker y sus plugins:

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Añade el usuario del sistema al grupo Docker, para no tener que usar sudo:

```bash
sudo usermod -aG docker $USER
```

Aplica los cambios (espero que sin tener que reiniciar)

```bash
newgrp docker
```