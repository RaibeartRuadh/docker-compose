# Решения для docker-compose на разные жизненные случаи
Поставить себе docker CE stable в одну строку (UBUNTU 16-18-20).  Рекомендуется выполнять через оболочку bash
```
    $ sudo apt install snapd curl && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(. /etc/os-release; echo "$UBUNTU_CODENAME") stable" && sudo apt update && sudo apt install docker-ce -y && sudo usermod -aG docker $USER && sudo docker --version
```
Поставить себе docker-compose 1.29.1 в одну строку (UBUNTU 16-18-20). Рекомендуется выполнять через оболочку bash

```
$ sudo curl -L https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose && docker-compose --version
```

1. docker-compose_ethereum_go.yml - развертывание локальной клиентской ноды сети Ethereum с примерами для основной сети, тестовых сетей Ropsten n Rinkeby
2. docker-compose_rabbitMQ.yml - пример развертывания брокера сообщений RabbitMQ с загрузкой модуля отложенных сообщений.
3. docker-compose_postgresql.yml - пример развертывания на хосте postgresql 13.2
4. docker-compose_wordpress.yml - пример развертывания системы wordpress включающей mysql:5.7 и сам wordpress
5. docker-compose_aerospike.yml - пример развертывания системы aerospike
6. docker-compose_nginx.yml - пример развертывания nginx сервера. Дополнительно следует сделать Dockerfile в котором мы прописываем дополнительные условия (пути, сертификаты, конфиг)
7. docker-compose_BitcoinCore.yml - пример развертывания ноды Биткоин, основнонной на образе kylemanna/bitcoind. Есть тестовая и основная конфигурация.  
8. docker-compose_network.json - пример развертывания внутренней сети bridge
