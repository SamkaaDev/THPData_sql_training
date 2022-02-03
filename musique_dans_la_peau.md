# LA MUSIQUE DANS LA PEAU

*Fichier de réponse de l'exercice 1*


1. ***Récupérer tous les albums***

*Requête SQL*
> SELECT * FROM albums;

*Réponse obtenue*
> 347


2. ***Récupérer tous les albums dont le titre contient "Great" (indice)***

*Requête SQL*
> SELECT * FROM albums WHERE Title LIKE '%Great%';

*Réponse obtenue*
> 13



3. ***Donner le nombre total d'albums contenus dans la base (sans regarder les id bien sûr)***

*Requête SQL*
> SELECT COUNT( * ) FROM albums;

*Réponse obtenue*
> 347



4. ***Supprimer tous les albums dont le nom contient "music"***

*Requête SQL*
> DELETE FROM albums WHERE Title LIKE '%music%';

*Réponse obtenue*
> Suppression des albums en question




5. ***Récupérer tous les albums écrits par AC/DC***

*Requête SQL*
> SELECT * FROM albums JOIN artists ON artists.ArtistId = albums.ArtistId WHERE artists.name = 'AC/DC';

*Réponse obtenue*
> 2



6. ***Récupérer tous les titres des albums de AC/DC***

*Requête SQL*
> SELECT A.Title FROM albums A
> JOIN artists S ON S.ArtistId = A.ArtistId
> WHERE S.Name = 'AC/DC';  

*Réponse obtenue*
> For Those About To Rock We Salute You
> Let There Be Rock



7. ***Récupérer la liste des titres de l'album "Let There Be Rock"***

*Requête SQL*
> 

*Réponse obtenue*
> 



8. ***Afficher le prix de cet album ainsi que sa durée totale***

*Requête SQL*
> 

*Réponse obtenue*
> 



9. ***Afficher le coût de l'intégralité de la discographie de "Deep Purple"***

*Requête SQL*
> 

*Réponse obtenue*
> 



10. ***Créer l'album de ton artiste favori en base, en renseignant correctement les trois tables albums, artists et tracks***

*Requête SQL*
> 

*Réponse obtenue*
> 


