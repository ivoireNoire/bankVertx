# bankVertx

BankVertx, a backend app using Vertx for serving bank operation via HTTP calls

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What you need to have configured on your machine


##### JDK
##### Apache Maven
##### Mysql

In *Mysql CLI* or *phpMyAdmin*, you'll have just to create a database named ```Banca_v1``` and configure for this database one user with a password.
Fyi, the app uses, (`bancaDBUser` - `12345`), but you can use a different user & pwd.
If so, DO NOT FORGET to reconfigure the [persistence.xml](./src/main/resources/META-INF/persistence.xml) for DB connection. You can also change to generation strategy for the DB there.



### Installing

First, clone or download this project on your local machine. After moving in the project folder at the pom.xml level, run
```
$ mvn clean package
```
This command will compile the files, download all the dependencies needed, run the maven goals for the project and also create a fat-jar at *target/bankVertx-1.0-SNAPSHOT-fat.jar*

## Deployment

Now, you will have to run the next command to get running the app by creating and HTTP Server to listen on port 8040
```
$ java -jar target/bankVertx-1.0-SNAPSHOT-fat.jar
```
#### The Supported Urls

``POST`` : */register*

``GET`` : */authentificate/:username/:password*

``GET`` : */accounts*

``POST`` : */accounts*

``DELETE`` : */accounts/:id*

``POST`` : */transactions*

## License

This project is licensed under the MIT License - see the [license.md](license.md) file for details
