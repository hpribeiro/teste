
# **Documentação LabIOT Inatel- Software**

## Para instalar pacotes para o python será necessário a instalação do pip:

``` sudo apt-get install -y python-pip```

## Atualize o pip:

``` sudo pip install --upgrade pip```


## Para instalação do mongoDB no Ubuntu 16.04, dê os seguintes comandos:

- ``` sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927```

- ``` echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list```

- ``` sudo apt-get update```

- ``` sudo apt-get install -y mongodb-org```

- #### Em seguida crie o arquivo de configuração:
- > ```sudo nano /etc/systemd/system/mongodb.service```

- #### Copie o seguinte conteúdo para o arquivo, salve e feche.

- > [Unit]  
    Description=High-performance, schema-free document-oriented database
    After=network.target
    [Service]  
    User=mongodb
    ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf  
    [Install]  
    WantedBy=multi-user.target

- ``` sudo systemctl start mongodb```

- ```sudo systemctl enable mongodb```
