EmailService
============
It's self learning project to get knowledge with microservices.
Microservice architecture, or simply microservices, is a distinctive method of developing software systems.

Micro Framework for Microservices - it's simple!
------------------------------------------------
Micro Framework gives us the opportunity to take advantage of the basic components and create their own application architecture (with all its consequences).

Symfony Microkernel
-------------------
The best thing about the Symfony microframework is that you are building your application on the shoulders of Symfony, meaning that you won't face any of the usual restrictions of the microframeworks. All the incredible Symfony features and bundles are ready to use in case you need them as your application grows.

###Getting started

In order to set up this application you need clone this repo:

```git clone https://github.com/tarnawski/symfony-microkernel.git```

And you have to install dependencies:

```
cd symfony-microkernel

composer install
```

####1. The quickest way to set up

Just run PHP server:

```
php -S localhost:8001
```

####2. Run with Vagrant and prepared environment:

```
cd vagrant && vagrant up 
```


When the process is complete, get into the machine:
```
vagrant ssh
cd /var/www/emailservice/
```

Creating schema:
```
php bin/console doctrine:schema:create --force
```  

Add to your hosts:
```
10.0.0.200 emailservice.dev
```



####3. Do you like Docker? Me too!

Just run this command in project catalog:
```
docker-compose run
```


###That's all! Now you can start to use app!!!

Endpoint documentation:
-----------------------

| Method | Path         |  Description                     |
|--------|--------------|----------------------------------|
| GET    | /emails      |  Return list of email addres     |             
| GET    | /emails/{id} |  Return single email address     |             
| POST   | /emails      |  Create new email address        |             
| DELETE | /emails/{id} |  Delete email address            |             