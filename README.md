# Решения для docker-compose на разные жизненные случаи
Поставить себе docker CE stable в одну строку (UBUNTU 16-18-20).  Рекомендуется выполнять через оболочку bash

    $ sudo apt-get remove docker docker-engine docker.io -y && sudo apt-get update -y && sudo apt-get install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo apt-key fingerprint 0EBFCD88 && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs)  stable" && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get update -y && sudo apt-get install docker-ce -y && docker --version

Поставить себе docker-compose 1.29.1 в одну строку (UBUNTU 16-18-20). Рекомендуется выполнять через оболочку bash

    $ sudo curl -L https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose && docker-compose --version

1. docker-compose_ethereum_go.yml - развертывание локальной клиентской ноды сети Ethereum с примерами для основной сети, тестовых сетей Ropsten n Rinkeby
2. docker-compose_rabbitMQ.yml - пример развертывания брокера сообщений RabbitMQ с загрузкой модуля отложенных сообщений.
3. docker-compose_postgresql.yml - пример развертывания на хосте postgresql 13.2
4. docker-compose_wordpress.yml - пример развертывания системы wordpress включающей mysql:5.7 и сам wordpress
5. docker-compose_aerospike.yml - пример развертывания системы aerospike

