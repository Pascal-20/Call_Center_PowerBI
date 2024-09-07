# Power BI Call_Center
###  Introduction
Ce projet de fin d'etude se concentre sur l'utilisation de la puissance de Microsoft Power BI pour l'analyse et la visualisation des données. Notre objectif est de créer un tableau de bord complet qui fournit des informations précieuses sur les performances des employés du centre d'appel et facilite les prise de décision futures.

Tout au long de ce projet, nous explorerons divers aspects de l'analyse des données à l'aide de Power BI. De la connexion et de la transformation des données à la conception de visualisations interactives, nous apprendrons à présenter efficacement des informations complexes de manière significative.


Rejoignez-moi dans cette aventure captivante à la découverte de l'analyse de données, où nous explorons les possibilités offertes par Power BI et révélons tout le potentiel des insights basés sur les données. Préparez-vous à faire la différence et à renforcer vos compétences en veille stratégique et en visualisation de données.

### Preparation des Données
Avant de plonger dans l'analyse des données avec Power BI, il est essentiel de réaliser des tâches de préparation des données. Initialement, les données anonymisées qui nous ont été fournies étaient dans un format particulier :

![Capture d’écran 2024-09-07 181727](https://github.com/user-attachments/assets/b2cb2294-a54b-43da-bc24-c899f717d58f)

Lors de la phase de préparation des données, nous avons nettoyé et transformé les données à l'aide de Power Query. Par exemple, nous avons supprimé la colonne "Call Abandoned" dans les fichiers de données. De plus, nous avons créer une colonne "SLA Compliance". Cette colonne inclue une déclaration logique selon laquelle le temps d'attente des appels (Waittime) est inférieur à 35 secondes. Les résultats de la colonne incluent Within SLA (Dans les normes de niveau de service) ou Outside SLA (Hors des normes de niveau de service). Ces étapes sont essentielles pour garantir que nos données sont dans un format adapté à l'analyse dans Power BI.

![Capture d’écran 2024-09-07 191822](https://github.com/user-attachments/assets/8f829192-e9fb-4d92-9fcf-8655ae96e4e1)

Au cours de ce travail, nous allons prioriser les KPI suivants pour guider la conception de notre tableau de bord :
1. Une vision globale du service client : Calculer le nombre total d'appels à différents niveaux, le taux d'appels "Within SLA" ou "Outside SLA", et le temps d'appel moyen. Ces KPI permettront d'analyser les performances par manager et par employé, avec une visualisation mensuelle sur l'année.
2. Une vision des revenus par appels : Nous allons Analyser l'évolution des revenus en observant la variation d'une année à l'autre et en décomposant les revenus par secteur et par équipe.
3. Une vision des performances des managers et des employés : Et enfin, Nous allons étudier le comportement des managers en évaluant leurs performances individuelles et en analysant le temps d'attente par équipe et par employé.

Notons que ces KPIs ne sont qu'un point de départ. Nous pouvons explorer des indicateurs et des dimensions supplémentaires qui pourraient fournir des informations précieuses pour l'activité.

Exploitons maintenant la puissance de Power BI et créons un tableau de bord dynamique qui présente les indicateurs clés de performance et les mesures, permettant l'entreprise de prendre des décisions éclairées, de faire progresser son chiffre d'affaire et optimiser ses methodes de travail. Préparez-vous à plonger et à libérer votre créativité !


*💡 Les étapes suivantes mettent en évidence les points clés pour créer le graphique de la tâche 1, en se concentrant sur les aspects fondamentaux et non sur les éléments de conception généraux comme les polices, les couleurs, les arrière-plans et les légendes. Ces instructions détaillées sont données à titre d'exemple spécifique à la tâche 1, qui concerne la création d'un tableau de bord.*

### Création de mesures essentielles pour l'analyse des KPI
Après avoir nettoyé et préparé nos données à l'aide de Power Query, nous avons décidé de commencer par créer toutes les mesures que nous estimions pertinentes pour notre analyse.

Par exemple, en exploitant notre nouvelle colonne « Call Duration », nous avons créé une mesure pour calculer la durée moyenne des appels en utilisant la formule DAX suivante :

![Capture d’écran 2024-09-07 201833](https://github.com/user-attachments/assets/07073af4-5a83-464c-88ce-da34ad1a1e87)

Nous avons répété ce processus jusqu'à obtention de toutes les mesures dont nous avions besoin :

![measures](https://github.com/user-attachments/assets/5ca62e58-3162-4368-b1b4-1a1b8a37b79b)

### Visualisation des données
Après avoir créé nos mesures, nous allons maintenant procéder à la conception des visualisations que nous avons jugées les plus pertinentes pour l’analyse.

#### Revenues total mensuelle par manager sur l'année 2018

![measure2](https://github.com/user-attachments/assets/85e8c30b-3345-418a-96ba-a1d7570deac5)

J'ai créé une visualisation de graphique en courbe.
J'ai utilisé la colonne **Year** comme entrée pour l'axe X, représentant la chronologie sur l'année 2018.
J'ai utilisé la colonne **Total revenue** comme entrée pour l'axe Y, affichant le revenue total de 2018 à 2021.
Enfin, j'ai utilisé en legende la colonne **Manager Name** qui contient le nom des differents manager d'equipe.

![Capture d’écran 2024-09-07 213449](https://github.com/user-attachments/assets/44e2f7dc-a632-4cf2-9b58-f576cd5d0906)


