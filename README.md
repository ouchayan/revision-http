## What is HTTP :
- Http : Hyper Text transfer protocol. Il fait partie de la couche applicatiotion du réseau.
- Http est un protocole qui permet de faire des échanges entre un client(Pc, téléphone, tablette) et un serveur.
- Http  est obligatoire pour créer du contenu pour le web.
- Une application web traite sans arrêt des appels client < > serveur.
- Le client envoi une requête et le serveur retourne une reponse.
- HTTPS est la version sécurisé de HTTP.
- Le Port par défaut de HTTP : 80 exemple 63.172.111.128:80
- Le Port par défaut de HTTPS : 443 exemple 216.58.198.196:443
## request Headers detail :
- authority: www.google.fr
- User-agent : Firefox Chrome
- Méthode : GET POST DELETE PUT PATCH ..
- Path : /user
- Scheme : Https
- Cookie : 
- cache-control: max-age=0
- accept-language: fr-FR,fr;q=0.9,en-US;q=0.8,en;q=0.7,ar;q=0.6,de;q=0.5 Language attendu par le navigateur.
- Accept : Text/html image/png …. La ressource que le user s’attends de recevoir (fichier html image fichier pdf zip ..)
- accept-encoding: gzip, deflate, br
- ……..
## Response Headers detail :
- Server : gws (Google web server) cloudflare, was
- Date
- expires
- content-encoding: br
- content-length: 41780
- content-type: text/html; charset=UTF-8
- set-cookie
- …………..
## Http versions :
> HTTP/0.9 : 1991 ; Protocole simple , il envoie juste du html , il supporte juste la méthode GET et il ne retourne pas les code statuts (200 ….).
> HTTP/1.0 : 1996, il retourne les codes status, Http headers, il envoie du document non html (exemple page html avec image pour afficher l’image on fait un autre appel)
> HTTP/1.1 : 1997 , l’ajout de HEADER Host, cache control mecanism, 
> HTTP/2.0 : 2015 , 
> HTTP/3.0 : future.
## HTTP méthodes (Versbes)
> Get : retourner un objet ou liste des objets. (Juste pr recuperer)
> HEAD : c’est comme GEt mais elle retourne juste le header et pas le corps (exemple content-type json html xml ) URL dynamique.
> POST : Créer ou modifier un objet : retourn l’objet avec l’id.
> PUT : créer ou modifier une ressource en passant l’id dans url épisode/3434
> Patch : Modification partiel d’une ressource (Modifier par exemple juste un champ d’une ressource).
> Delete : suppression en passant l’id dans url
> Options : pour connaîtrez les méthodes autorisé par la ressource.
> connect : Pour établir une connexion directe est protégé via un proxy.
> trace : elle est utilisé pr tracer une requête http.
## Code statut : 
un entier composé de 3 chiffres qui pour nous dire est ce que la requête est passée ou pas.( contient 5 classes 1xx 2xx 3xx 4xx 5xx)
> 1xx : information (100, 101, 102 et 103)
> 2xx : success (200 : 0k requests c’est bien passé, 201 : created et retourne la ressource crée, 202 : accepted et en cours de traitement pas encore fini, 204 : requête traitée mais ne retourne rien)
> 3xx : Redirection
> 4xx : Client error ( 400 : bad request, 401 : unauthorized, 403 : forbidden, 404 : not found, 406 : not acceptable)
> 5xx : Serveur error (500 : internal error serveur le serveur ne peut pas traité la requête, 501 , 502 : bad getaway
## LEs différents type de cache HTTP :
> Cache-Control: no-store
> Cache-Control: no-cache
> Cache-Control: private
> Cache-Control: public
> Cache-Control: max-age=31536000 (expiration).
> Cache-Control: must-revalidate (Validation).
