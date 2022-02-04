# PANAMA PAPERS

*Fichier de réponse de l'exercice 1*

1. ***Combien la base de données contient-elle de sociétés offshores différentes dont la source est "Panama Papers" ?***

*Requête SQL*
> SELECT COUNT ( * ) FROM entity WHERE source = "Panama Papers"

*Réponse obtenue*
> 213634


2. ***Quel intermédiaire a créé le plus de sociétés offshores ? A-t-on son adresse et son pays ?***

*Requête SQL*
> SELECT DISTINCT E.inter, A.address, A.country_codes FROM address A JOIN intermediary I ON A.id_address = I.id_address JOIN assoc_inter_entity E ON I.id = E.inter WHERE E.inter = (SELECT inter FROM assoc_inter_entity GROUP BY inter ORDER BY COUNT( * ) DESC LIMIT 1);

*Réponse obtenue*
> 11001746 ; ORION HOUSE SERVICES (HK) LIMITED ROOM 1401; 14/F.; WORLD COMMERCE  CENTRE;[...] TSUI; KOWLOON; HONG KONG ; Hong Kong


3. ***Combien la base contient-elle de bénéficiaires avec un nom unique ? Quel est le bénéficiaire dont le nom revient le plus souvent ?***

*Requête SQL*
>

*Réponse obtenue*
> 


4. ***Donner la liste des juridictions avec le nombre d'entreprises offshores enregistrées sur chaque territoire, triée par ordre décroissant.***

*Requête SQL*
> 

*Réponse obtenue*
> 


5. ***Regrouper les sociétés offshores par statut, et trier la liste par ordre décroissant.***

*Requête SQL*
> 

*Réponse obtenue*
> 


6. ***Trouver la liste des bénéficiaires dont le nom contient "BNP" et ajouter, pour chaque bénéficiaire, le nom des sociétés offshores.***

*Requête SQL*
> 

*Réponse obtenue*
> 


7. ***Trouver la liste des sociétés dont la juridiction est "France", "Monaco" ou "Réunion".***

*Requête SQL*
> 

*Réponse obtenue*
> 


8. ***Trouver la liste des sociétés dont le pays de l'adresse et le pays de la juridiction sont différents.***

*Requête SQL*
> 

*Réponse obtenue*
> 


9. ***Trouver la liste des bénéficiaires qui ont des sociétés au même nom et enregistrée à la même date, trier la liste par odre décroissant.***

*Requête SQL*
> 

*Réponse obtenue*
> 


10. ***Donner la liste des intermédiaires qui ont aussi été bénéficiaires, en ajoutant leur nom de bénéficiaire et leur adresse.***

*Requête SQL*
> 

*Réponse obtenue*
> 


11. ***Donner le top 10 des bénéficiaires qui ont le plus d'identités différentes (similar name and address) et le nombre d'identités correspondant.***

*Requête SQL*
> 

*Réponse obtenue*
> 


12. ***Donner le top 10 des bénéficiaires qui ont le plus de parts toujours valides dans des entreprises offshores (dont la date de fin n'est pas encore passée).***

*Requête SQL*
> 

*Réponse obtenue*
> 


13. ***Question bonus : réussir à retrouver dans la base au moins 3 personnalités que tu connais***

*Requête SQL*
> 

*Réponse obtenue*
> 

