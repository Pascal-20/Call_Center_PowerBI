# Power BI Call_Center
###  Introduction
Ce projet de fin d'etudes se concentre sur l'utilisation de la puissance de Microsoft Power BI pour l'analyse et la visualisation des données. Notre objectif est de créer un tableau de bord complet qui fournit des informations précieuses sur les performances des employés du centre d'appel et facilite les prises de décision futures.

Tout au long de ce projet, nous explorerons divers aspects de l'analyse des données à l'aide de Power BI. De la connexion et de la transformation des données à la conception de visualisations interactives, nous apprendrons à présenter efficacement des informations complexes de manière significative.


Rejoignez-moi dans cette aventure captivante à la découverte de l'analyse de données, où nous explorons les possibilités offertes par Power BI et révélons tout le potentiel des insights basés sur les données. Préparez-vous à faire la différence et à renforcer vos compétences en veille stratégique et en visualisation de données.

### Preparation des Données
Avant de plonger dans l'analyse des données avec Power BI, il est essentiel de réaliser des tâches de préparation des données. Initialement, les données anonymisées qui nous ont été fournies étaient dans un format particulier :

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/b2cb2294-a54b-43da-bc24-c899f717d58f">
</p>

Lors de la phase de préparation des données, nous avons nettoyé et transformé les données à l'aide de Power Query. Par exemple, nous avons supprimé la colonne "Call Abandoned" dans les fichiers de données. De plus, nous avons créé une colonne **SLA Compliance**. Cette colonne inclut une déclaration logique selon laquelle le temps d'attente des appels **Waittime** est inférieur à 35 secondes. Les résultats de la colonne incluent Within SLA (Dans les normes de niveau de service) ou Outside SLA (Hors des normes de niveau de service). Ces étapes sont essentielles pour garantir que nos données sont dans un format adapté à l'analyse dans Power BI.

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/8f829192-e9fb-4d92-9fcf-8655ae96e4e1">
</p>

Au cours de ce travail, nous allons prioriser les KPI suivants pour guider la conception de notre tableau de bord :
1. Une vision globale du service client : Calculer le nombre total d'appels à différents niveaux, le taux d'appels **Within SLA** ou **Outside SLA**, et le temps d'appel moyen. Ces KPIs permettront d'analyser les performances par manager et par employé, avec une visualisation mensuelle sur l'année.
2. Une vision des revenus par appels : Nous allons analyser l'évolution des revenus en observant la variation d'une année à l'autre et en décomposant les revenus par secteur et par équipe.
3. Une vision des performances des managers et des employés : Et enfin, nous allons étudier le comportement des managers en évaluant leurs performances individuelles et en analysant le temps d'attente par équipe et par employé.

Notons que ces KPIs ne sont qu'un point de départ. Nous pouvons explorer des indicateurs et des dimensions supplémentaires qui pourraient fournir des informations précieuses pour l'activité.

Exploitons maintenant la puissance de Power BI et créons un tableau de bord dynamique qui présente les indicateurs clés de performance et les mesures, permettant à l'entreprise anonymisée de prendre des décisions éclairées, de faire progresser son chiffre d'affaire et optimiser ses methodes de travail. Préparez-vous à plonger et à libérer votre créativité !


*💡 Les étapes suivantes mettent en évidence les points clés pour créer le graphique de la tâche 1, en se concentrant sur les aspects fondamentaux et non sur les éléments de conception généraux comme les polices, les couleurs, les arrière-plans et les légendes. Ces instructions détaillées sont données à titre d'exemple spécifique à la tâche 1, qui concerne la création d'un tableau de bord.*

### Création de Mesures Essentielles pour l'analyse des KPIs
Après avoir nettoyé et préparé nos données à l'aide de Power Query, nous avons décidé de commencer par créer toutes les mesures que nous estimions pertinentes pour notre analyse.

Par exemple, en exploitant notre nouvelle colonne **Call Duration**, nous avons créé une mesure pour calculer la durée moyenne des appels en utilisant la formule **DAX** suivante :

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/07073af4-5a83-464c-88ce-da34ad1a1e87">
</p>

Nous avons répété ce processus jusqu'à obtention de toutes les mesures dont nous avions besoin :

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/5ca62e58-3162-4368-b1b4-1a1b8a37b79b">
</p>

### Visualisation des données
Après avoir créé nos mesures, nous allons maintenant procéder à la conception des visualisations que nous avons jugés les plus pertinentes pour l’analyse.

#### Revenus Total Mensuelle par Manager sur l'année 2018

<p align="center">
  <img width="300" " src="https://github.com/user-attachments/assets/85e8c30b-3345-418a-96ba-a1d7570deac5">
</p>

J'ai créé une visualisation avec un graphique en courbe.
J'ai utilisé la colonne **Year** comme entrée pour l'axe X, représentant la chronologie sur l'année 2018.
J'ai utilisé la colonne **Total revenue** comme entrée pour l'axe Y, affichant le revenue total de 2018 à 2021.
Enfin, j'ai utilisé en legende la colonne **Manager Name** qui contient le nom des differents manager d'equipe.

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/44e2f7dc-a632-4cf2-9b58-f576cd5d0906">
</p>
#### Temps d'Attente par Equipe

<p align="center">
  <img width="300" " src="https://github.com/user-attachments/assets/9e9b651e-5067-4496-b1ad-bcc0901a1b86">
</p>

J'ai créé une visualisation avec un graphique en diagramme.
J'ai utilisé la colonne **Manager Name** comme entrée pour l'axe X, représentant le nom des responsables d'equipe.
J'ai utilisé la colonne **Wait Time** comme entrée pour l'axe Y, affichant la somme totale du temps d'attente de 2018 à 2021.

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/3fa245bc-a53a-458e-a4a3-4b490939dcb8">
</p>

#### Revenue Total par Site

<p align="center">
  <img width="300" " src="https://github.com/user-attachments/assets/d305495b-a885-4ac5-8853-446cb7507305">
</p>

Pour la visualisation suivante, j'ai opté pour un diagramme circulaire.
J'ai choisi la colonne **Site** pour la legende, elle contient le nom des villes.
J'ai aussi choisi pour la legende des valeurs la colonne **Global Total Revenue** 

<p align="center">
  <img width="400" " src="https://github.com/user-attachments/assets/caaa2be2-5364-4301-8155-57f9f2795a5a">
</p>

#### Performances Comparative par Periode Similaire

<p align="center">
  <img width="300" " src="https://github.com/user-attachments/assets/2cc24223-a550-4318-8543-9c173162095d">
</p>

Pour cette visualisation, j'ai fait un comparatif par periode de chaque année sur la periode 2018-2021. Pour une visualisation facile à interpreter, j'ai opté pour un tableau.
Les colonnes choisies pour la legende rows sont les colonnes temporelles : **Quater**, **Year** et **Month**.
Pour la legende value, j'ai choisi les mesures du total des revenues : **Global Total Revenue**, **Revenue YTD YoY Growth**, **Total Revenue YTD**, **Total Revenue YTD LY**, **Total Revenue YTD YoY growth**.

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/00898eb3-3be5-4534-b602-b2ae0c53f396">
</p>

#### Slicer 
Enfin, nous avons ajouté des sliccers à notre tableau de bord, ce qui nous permet de filtrer les données en fonction de la date, des équipes et des agents individuels. Cela nous permet d'analyser les données en fonction de périodes de temps spécifiques et d'examiner les performances de chaque agent individuellement. Voici deux exemples ci-dessous.

<p align="center">
  <img width="100" " src="https://github.com/user-attachments/assets/19f2a64c-6abf-4724-92d3-63781b06b816">
</p>

#### Tableau de bord
Et pour conclure, voici l'analyse des tendances des centres d'appels. Vous trouverez ci-dessous le tableau de bord complet représentant l'analyse complète des tendances du centre d'appel et les revenus generés.

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/3edf6f28-d8cb-412c-af86-51e253c5f401">
</p>

#### Analyse detaillée des revenus généres 

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/b9c92744-d13e-4339-a3d9-173832cf279f">
</p>

#### Performances realisées individuellement et par equipe

<p align="center">
  <img width="600" " src="https://github.com/user-attachments/assets/7fa60e0e-b52b-4a14-86d9-f31af6e2fcda">
</p>








