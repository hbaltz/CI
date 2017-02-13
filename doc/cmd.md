# Commandes  

## Initilaisation de vagrant  
Créer le vagrant file :
```
vagrant init -m -f "nom_de_la_vm" "chemin_de_la_vm" 
vagrant init -m -f asi ./alpine2docker-1.0.0.box
```

## Démarrer la vm  

```
vagrant up
```

## Voir le statut de vagrant  
```
vagrant status
```

## Voir les ports utilisé par vagrant  
```
vagrant port
```

## Conncetion ssh 
```
vagrant ssh
```

## Aller sur la paghe de gestion  
[http://localhost:10000/](http://localhost:10000/)

# Commandes dans devbox (dans vm)

## Cloner le repository 
```
git clone http://localhost:10000/gitserver/butler/dw-demo-app.git
```

## Se placer dans le dossier
```
cd dw-demo-app/
```

## Compiler en nettoyant
```
mvn clean compile
```

## Tester l'application
```
mvn test
```

## Whole building process is as simple as
```bash
mvn clean install
```
## Just compiling classes:
```bash
mvn clean compile
```
## Running unit tests (implies compiling):
```bash
mvn test
```
## Running Integration tests (implies compiling but NO unit tests):
```bash
mvn verify
```

## Generating the standalone application:
```bash
mvn package
```

## "Installing" application in the local Maven repository:
```bash
mvn install
```

## How to run it ?

### Bare-metal

The [awesome DropWizard framework](http://www.dropwizard.io/1.0.0/docs/) makes the generated application a standalone one.

You can run it with just a Java JRE 8 installed:

```bash
java -jar ./target/demoapp.jar server ./hello-world.yml
```