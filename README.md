# Extension directus

## Step-1: Posizione della cartella 'kdm-upload'
La cartella 'kdm-upload' va copata allo stesso livello del progetto directus "compilato"

**- ESEMPIO**

![image](https://i.ibb.co/rxHvttx/1.jpg)

Supponiamo che il progetto directus(in questo caso **example-project**), la cartella kdm-upload va in questa posizione

## Step-2: Inserire path progetto directus'
Cambiare nel file 'package.json', la stringa del path come in figura, sostituire **"example-project"** con il nome della cartella del progetto directus

![image](https://i.ibb.co/bm5ZKpj/2.jpg)

## Step-3: Comando di creazione cartella extension

Questo comando crea la cartella kdm dentro extensions
```
mkdir ./<nome-cartella-directus>/extensions/endpoints/kdm
```

**P.S**:  In questa cartella verrà generato il 'comiplato' della estensione

## Step-4: Build estensione

```
cd <nome-cartella-directus>
npm --prefix ../kdm-upload/ run build && npx directus start
```

1. Il primo comando (**npm --prefix ../kdm-upload/ run build**), builda l'estensione nella cartella specificata allo step-2

2.Il secondo comando (**npx directus start**) starta l'app directus, **QUESTO COMANDO PUO' ESSERE SOSTITUITO CON QUELLO CHE SI USAVA IN PRECEDENZA PER FAR PARTIRE L'APP DIRECTUS**
