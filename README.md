# Analyse Météorologique

Ce projet utilise les données météorologiques de Nice pour analyser les précipitations journalières. L'analyse est réalisée en R en utilisant les packages **tibble**, **dplyr**, et **ggplot2** pour la manipulation et la visualisation des données. Ce README détaille les étapes principales du traitement et de l'analyse des données.

## Prérequis

- R version 4.3.3 ou supérieure
- Les packages R suivants doivent être installés :
  - `tibble`
  - `dplyr`
  - `ggplot2`

Vous pouvez installer ces packages via `install.packages("nom_du_package")`.

## Étapes de l'analyse

1. **Préparation des données** : Importer les données météorologiques à partir d'un fichier CSV, puis les convertir en format adapté pour la manipulation dans R (tibble).

2. **Sélection et renaming des variables** : Extraire les variables pertinentes (comme les précipitations sur les trois dernières heures) et renommer les colonnes pour les rendre plus claires.

3. **Manipulation des dates** : Conversion de la colonne `Date` en format date (POSIXct) et ordonnancement des observations par ordre croissant.

4. **Création d'une variable "Jour"** : Ajout d'une colonne pour indiquer le jour de l'année de chaque observation.

5. **Calcul des précipitations journalières** : Agrégation des précipitations sur une base journalière pour obtenir le cumul des précipitations par jour.

6. **Fréquence des jours avec précipitations** : Calcul de la proportion des jours avec des précipitations non nulles pour chaque mois.

7. **Précipitation maximale** : Identification du jour avec la précipitation journalière la plus élevée.

8. **Visualisation graphique** : Création de graphiques pour visualiser les précipitations journalières, avec mise en avant des précipitations maximales.

9. **Somme glissante** : Calcul des précipitations cumulées sur des périodes de 2 jours et de 7 jours pour observer les tendances de précipitations sur des périodes plus longues.

10. **Extraction des dates maximales** : Identification des dates correspondant aux cumuls maximaux des précipitations sur 2 jours et sur 7 jours.

11. **Affichage des séries de dates** : Visualisation des dates correspondant aux cumuls maximaux obtenus précédemment.

## Résultats obtenus

- **Fréquence des précipitations** : La fréquence des jours avec précipitation est calculée pour chaque mois. Cela permet d'identifier les périodes de l'année avec des précipitations plus fréquentes.

- **Précipitation maximale** : L'analyse met en évidence la journée avec la plus forte précipitation enregistrée sur la période étudiée.

- **Cumuls maximaux sur plusieurs jours** : Grâce au calcul des sommes glissantes, nous avons identifié les périodes de 2 jours et de 7 jours avec les plus fortes précipitations cumulées. 

- **Dates des cumuls maximaux** : Les dates associées aux précipitations maximales sur ces périodes ont été extraites pour un examen plus approfondi.

## Visualisation

Un graphique montre la distribution des précipitations journalières tout au long de l'année. Les précipitations maximales sont également représentées visuellement pour mieux comprendre leur répartition dans le temps.

## Conclusion

Cette analyse fournit des informations précieuses sur la répartition des précipitations à Nice au cours de l'année, en mettant en lumière les périodes les plus humides et les événements de précipitations les plus intenses. L'utilisation des fonctions de manipulation de données et de visualisation en R permet de traiter efficacement ces données et de les rendre interprétables pour l'analyse météorologique.
