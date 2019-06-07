# GraphBotLP
pràctica de python per LP Q2 2019

# Introducció
Aquest arxiu descriu les comandes que tracta el GraphBotLP, exemple:

![Foto](https://github.com/007kof/LP/blob/master/foto1.png)

# Prerequisits
Per poder executar el codi, calen les següents llibreries i tenir `python3` instalat:
* `networkx` per manipular grafs.
* `haversine` per calcular distàncies entre dos coordenades
* `fuzzywuzzy` per calcular semblances entre textos
* `staticmap` per pintar mapes
* `pandas` per baixar fitxers
* `python-telegram-bot` per interactuar amb Telegram

Per millorar la eficiència de calcular semblances entre textos, es recomanable instalar-se la llibreria `python-levenshtein`.

# Instalació
Per instalar totes les llibreries anteriors, només caldrà executar la següent comanda per la terminal:
`pip3 install -r requirements.txt`

# Execcució
Per executar el script, cal introduir la següent comanda via terminal:
`./GraphBotLP.py` o `python3 GraphBotLP.py`

# Comandes del Bot
* `/start`
El Bot contesta amb una salutació.

* `/help`
El Bot contesta amb una llista de totes les possibles comandes amb una breu documentació

* `/author`
El Bot contesta amb el nom complet de l'autor i el seu correu electrònic.

* `/graph [<distance> <population>]`
El Bot crea un nou graf amb les ciutats del món que tenen una població major o igual a `<population>` i amb distància menor o igual a `<distance>`.
Si l'usuari no introdueix els paràmetres es crearà una graf amb `<distance>` = 300 i `<population>` = 100000.

* `/nodes`
El Bot escriu el nombre de nodes en el graf, si el graf no s'ha creat, es crearà un nou graf amb distance = 300 i population = 100000.

* `/edges`
El Bot escriu el nombre de arestes en el graf, si el graf no s'ha creat, es crearà un nou graf amb distance = 300 i population = 100000.

* `/components`
El Bot escriu el nombre de components connexs en el graf, si el graf no s'ha creat, es crearà un nou graf amb distance = 300 i population = 100000.

* `Enviar ubicació`
El Bot es guarda la ubicació rebuda.

    Per exemple:
    ![foto](https://github.com/007kof/LP/blob/master/foto2.png)

* `/plotpop <dist> [<lat> <lon>]`
Mostra una mapa amb totes les ciutats del graf a distància menor o igual que `⟨dist⟩` de` ⟨lat⟩,⟨lon⟩`. Les coordenades són opcionals: si no es dónen, es refereixen a la posició de l'usuari (aquest l'ha enviar prèviament). El format de les coordenades és el mateix que al fitxer de dades. Cada ciutat es mostra amb un cercle, de radi proporcional a la seva població.
Si l'usuari no ha creat el graf prèviament, es crearà el graf amb distance = 300 i population = 100000.

    Per exemple:
    ![foto](https://github.com/007kof/LP/blob/master/foto3.png)

* `/plotgraph <dist> [<lat> <lon>]`
Mostra una mapa amb totes les ciutats del graf a distància menor o igual que `⟨dist⟩` de `⟨lat⟩,⟨lon⟩` i les arestes que es connecten. Les coordenades són opcionals: si no es dónen, es refereixen a la posició de l'usuari.
Si l'usuari no ha creat el graf prèviament, es crearà el graf amb distance = 300 i population = 100000.

    Per exemple:
    ![foto](https://github.com/007kof/LP/blob/master/foto4.png)

* `/route <src> <dst>`
Mostra una mapa amb les arestes del camí més curt per anar entre dues ciutats `⟨src⟩` i `⟨dst⟩`.
La sintàxi de les ciutats és `"Nom, codi_país"`. En cas de múltiples ocurrències, trieu-ne una d'arbitrària. Podeu utilitzar la distància de Lavenstein per cercar de forma més robusta en presència d'errors ortogràfics.
Si l'usuari no ha creat el graf prèviament, es crearà el graf amb distance = 300 i population = 100000.

    Per exemple, aquesta podria ser la sortida de `/route "Barcelona, es" "Zurich, ch"`:
    ![foto](https://github.com/007kof/LP/blob/master/foto5.png)

# Autors
* **Junjie Ji Chen** [email](junjie.ji@est.fib.upc.edu)

# Comentaris
Al executar el codi, pot trigar una estona en respondre, perquè primer llegeix el fitxer que conté totes les ciutats del món.
