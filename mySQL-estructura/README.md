# We will model several entity-relationship diagrams.
# 2.1: MySQL data structure

## Level 1
### - Exercise 1 - Optics
An optician called Cul d'Ampolla wants to computerize customer management and the sale of glasses:

First of all the optician wants to know which is the supplier of each of the glasses. Specifically, you want to know the name, address (street, number, floor, door, city, postal code and country) of each provider, telephone, fax, NIF.

The optical purchasing policy is based on the fact that glasses from one brand will be bought from a single supplier (so you can get better prices), but they can buy glasses from several brands from one supplier. From the glasses you want to know, the brand, the graduation of each of the glasses, the type of frame (floating, paste or metal), the color of the frame, the color of the glasses and the price.

Customers want to store their name, mailing address, phone number, email, and registration date. We are also asked, when a new customer arrives, to store the customer who has recommended the establishment (as long as someone has recommended it). Our system will need to indicate who and when the employee has sold each pair of glasses.


### - Exercises 2 - Pizzeria
A customer has hired you to design a website that allows you to place food orders online:

Please note the following instructions for modeling the project database: We store a unique identifier for each client, first name, last name, address, zip code, location, province, and phone number. Location and province data will be stored in separate tables. We know that a locality belongs to a single province, and that a province can have many localities. For each location we store a unique identifier and a name. We store a unique identifier and name for each province.

A customer can place many orders, but a single order can only be placed by a single customer. Each order stores a unique identifier, date and time, if the order is for home delivery or in-store collection, the number of products selected for each type and the total price. An order may consist of one or more products.

Products can be pizzas, burgers and drinks. Each product is stored: a unique identifier, name, description, image and price. In the case of pizzas, there are several categories that can change their name throughout the year. A pizza can only be in one category, but one category can have many pizzas.

A unique identifier and a name are stored for each category. An order is handled by a single store, and one store can handle many orders. Each store has a unique identifier, address, zip code, location, and province. Many employees can work in one store and one employee can only work in one store. Each employee is stored a unique identifier, name, surname, nif, telephone and whether he works as a cook or delivery man. For home delivery orders, it is important to save the delivery person who delivers the order and the date and time of delivery.

## Level 2
### - Exercise 1 - Youtube
We'll try to make a simple model of what the database would look like for a reduced version of YouTube:


De cada usuari guardem un identificador únic, email, password, nom d'usuari, data de naixement, sexe, país, codi postal. Un usuari publica vídeos. De cada vídeo guardem un identificador únic, un títol, una descripció, una grandària, el nom de l'arxiu de vídeo, durada del vídeo, un thumbnail, el nombre de reproduccions, el número de likes, el número de dislikes.

Un vídeo pot tenir tres estats diferents: públic, ocult i privat. Un vídeo pot tenir moltes etiquetes. Una etiqueta s'identifica per una Identificador únici un nom d'etiqueta. Interessa guardar qui és l'usuari que publica el vídeo i en quina data/hora el fa. Un usuari pot crear un canal. Un canal té un identificador únic, un nom, una descripció i una data de creació. Un usuari es pot subscriure als canals d'altres usuaris. Un usuari pot donar-li un like o un dislike a un vídeo una única vegada. Caldrà portar un registre dels usuaris que li han donat like i dislike a un determinat vídeo i en quina data/hora ho van fer. Un usuari pot crear playlists amb els vídeos que li agraden. Cada playlist té un identificador únic, un nom, una data de creació, i un estat que indica que pot ser pública o privada. Un usuari pot escriure comentaris en un vídeo determinat.

Cada comentari està identificat per un identificador únic, el text del comentari i la data/hora en la qual es va realitzar. Un usuari pot marcar un comentari com m'agrada o no m'agrada. Caldrà portar un registre dels usuaris que han marcat un comentari com m'agrada/no m'agrada, i en quina data/hora ho van fer.

## Nivell 3
### - Exercici 1 - Spotify
Provarem de fer un model senzill de com seria la base de dades necessària per a Spotify:

Existeixen dos tipus d'usuaris: usuari free i usuari premium. De cada usuari guardem un identificador únic, email, password, nom d'usuari, data de naixement, sexe, país, codi postal.

Els usuaris premium realitzen subscripcions. Les dades necessàries que caldrà guardar per a cada subscripció són: data d'inici de la subscripció, data de renovació del servei i una forma de pagament, que pot ser mitjançant targeta de crèdit o PayPal.

De les targetes de crèdit guardem el número de targeta, mes i any de caducitat i el codi de seguretat. Dels usuaris que paguen amb PayPal guardem el nom d'usuari de PayPal. Ens interessa portar un registre de tots els pagaments que un usuari premium ha anat realitzant durant el període que està subscrit. De cada pagament es guarda la data, un número d'ordre (que és únic) i un total.

Un usuari pot crear moltes playlists. De cada playlist guardem un títol, el nombre de cançons que conté, un identificador únic i una data de creació. Quan un usuari esborra una playlist no s'esborra del sistema, sinó que es marca com que ha estat eliminada. D'aquesta manera l'usuari pot tornar a recuperar els seus playlists en cas que les hagi eliminat per error. És necessari emmagatzemar la data en la qual uneixi playlist ha estat marcada com eliminada.

Podem dir que existeixen dos tipus de playlists: actives i esborrades. Una playlist que està activa pot ser compartida amb altres usuaris, això vol dir que altres usuaris poden afegir cançons en ella. En una llista compartida ens interessa saber quin usuari ha estat el que ha afegit cada cançó i en quina data ho va fer. Una cançó només pot pertànyer a un únic àlbum. Un àlbum pot contenir moltes cançons. Un àlbum ha estat publicat per un únic artista. Un artista pot haver publicat molts àlbums. De cada cançó guardem un identificador únic, un títol, una durada i el nombre de vegades que ha estat reproduïda pels usuaris de Spotify.

De cada àlbum guardem un identificador únic, títol, any de publicació i una imatge amb la portada. De cada artista guardem un identificador únic, nom i una imatge de l'artista. Un usuari pot seguir a molts artistes. Un artista pot estar relacionat amb altres artistes que facin música semblant. De manera que Spotify pugui mostrar-nos un llistat d'artistes relacionats amb els artistes que ens agraden. També ens interessa guardar quins són els àlbums i les cançons favorites d'un usuari. Un usuari pot seleccionar molts àlbums i moltes cançons com a favorites. 

Per verificar el teu disseny, omple les taules amb dades de prova per tal de verificar que les relacions són correctes i efectua les següents consultes i comprova'n els resultats:

## Verificació
### Optica:
Llista el total de factures d'un client en un període determinat
Llista els diferents models d'ulleres que ha venut un empleat durant un any
Llista els diferents proveïdors que han subministrat ulleres venudes amb èxit per l'òptica

### Pizzeria:
Llista quants productes de la categoria 'begudes' s'han venut en una determinada localitat
Llista quantes comandes ha efectuat un determinat empleat
