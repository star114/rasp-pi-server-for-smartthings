# Smartthings - Raspberry PI - Docker settings

my raspberry pi server

## [Download Raspbian](https://www.raspberrypi.org/downloads/)

- To install Raspbian to micro SD, use Raspberry Pi Imager
- Use minimal version

## Initial Setup

### `$ sudo raspi-config`

- passward change
- locale (network, time)
- ssh server enable
- network name change

## Docker

```
curl -fsSL https://get.docker.com -o get-docker.sh
chmod u+x get-docker.sh
sudo ./get-docker.sh
sudo usermod -aG docker pi && logout
```

## Docker compose

`sudo apt-get -y install docker-compose`

### Image pull

```
# Download the latest image:
docker-compose pull containername
```

### Start

```
# If a newer version of the image was downloaded, upgrade the container using the new image by running the up command again:
docker-compose up -d
```

### Stop

```
docker-compose down
```

### Restart

`docker-compose restart container`

### Logs

`docker-compose logs -f`

### Shell

`docker-compose exec container sh`

## Docker images

## [AirConnect](https://github.com/philippe44/AirConnect)

Make your google home/galaxy home devices use apple's airplay

## [GH-Connector](https://github.com/fison67/GH-Connector)

Google Connector to Smartthings

* [Installation](https://cafe.naver.com/stsmarthome/4326)

## [docker-homebridge](https://github.com/oznu/docker-homebridge)

Homebridge docker - Smartthings to Apple Homekit

## [Mi Connector](https://github.com/fison67/mi_connector)

Xiaomi Connector to Smartthings

## [harmony-api](https://github.com/maddox/harmony-api)

Logitech Harmony for Smartthings

* Use [turlvo's prebuilt image for raspberry pi](https://github.com/turlvo/KuKuHarmony)
