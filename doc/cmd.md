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