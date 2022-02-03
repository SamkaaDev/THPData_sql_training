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
> SELECT A.Title FROM albums A JOIN artists S ON S.ArtistId = A.ArtistId WHERE S.Name = 'AC/DC';  

*Réponse obtenue*
> For Those About To Rock We Salute You ; Let There Be Rock



7. ***Récupérer la liste des titres de l'album "Let There Be Rock"***

*Requête SQL*
> SELECT T.Name FROM tracks T JOIN albums A ON T.AlbumId = A.AlbumId WHERE A.Title = "Let There Be Rock"; 


*Réponse obtenue*
> Go Down ; Dog Eat Dog ; Let There Be Rock ; Bad Boy Boogie ; Problem Child ; Overdose ; Hell Ain't A Bad Place To Be ; Whole Lotta Rosie



8. ***Afficher le prix de cet album ainsi que sa durée totale***

*Requête SQL*
> SELECT SUM(T.UnitPrice), SUM(T.Milliseconds) FROM tracks T JOIN albums A ON T.AlbumId = A.AlbumId WHERE A.Title = "Let There Be Rock";

*Réponse obtenue*
> prix = 7.92$ ; durée = 2453259ms



9. ***Afficher le coût de l'intégralité de la discographie de "Deep Purple"***

*Requête SQL*
> SELECT SUM(T.UnitPrice) FROM tracks T JOIN albums A ON T.AlbumId = A.AlbumId JOIN artists S ON S.ArtistId = A.ArtistId WHERE S.Name = "Deep Purple"; 

*Réponse obtenue*
> 91.079$



10. ***Créer l'album de ton artiste favori en base, en renseignant correctement les trois tables albums, artists et tracks***

*Requête SQL*
> INSERT INTO albums (AlbumId, Title, ArtistId)
> VALUES(348, "Human After All", 276);
> INSERT INTO artists (ArtistId, Name)
> VALUES (276, "Daft Punk");
> INSERT INTO tracks (TrackId, Name, AlbumId, Milliseconds, Bytes, UnitPrice)
> VALUES (1001, "Robot Rock", 348, 286000, 5510424, 0.99);


*Réponse obtenue*
> ajout des infos dans la db


