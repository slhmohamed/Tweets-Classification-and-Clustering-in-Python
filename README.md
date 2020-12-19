# Projet–Fouille de Données
 ## Thème : Classification des Tweets
 
## 1.Objectifs :
  • Maitriser l’API de twitter pour l’extraction des tweets
  • Maitriser la partie NLP (natural language processing) avec NLTK en Python
  • Appliquer les principes de nettoyage des données
  • Classer les tweets : regrouper ensemble les tweets qui sont similaires. C’est une étape qui peut
    être considérée comme une étape.
    
## 2.Introduction.
  Twitter est un service de réseautage social et de micro-blogging sur lequel les utilisateurs publient et interagissent les uns avec les autres via des messages appelés           «tweets».
  Grâce à l'analyse des sentiments, les parties intéressées peuvent comprendre de quoi parlent les utilisateurs et, à partir des informations, prendre les décisions appropriées.   Cet projet se concentre sur la classification des tweets en 4 grandes catégories:  economic , social , sport and health, puis sur la réalisation d'une analyse de cluster     KMeans sur les groupes.
  Les données utilisées sont extraites de Twitter à l'aide de Tweepy , une bibliothèque python permettant d'accéder à l'API Twitter.
  
## 3.Bibliothèques
  Les bibliothèques suivantes seront utilisées tout au long de la projet.
  ![c1](https://user-images.githubusercontent.com/41681230/102667276-48a48a80-4189-11eb-8a79-11e7ac39da99.PNG)
## 4.Preparation de DataFrame

## 5.Prétraitement
### Nettoyage des tweets
   Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme différents.

## 6.Tokenisation, lemmatisation et suppression des mots vides
   Les mots vides sont des mots couramment utilisés dont la présence dans une phrase a moins de poids que d'autres mots. Ils incluent des mots comme «et», «ou», «a» et.c.
   La tokenisation est le processus de division d'une chaîne en une liste de jetons. Une phrase peut être réduite en mots et un mot peut être réduit en lettres en utilisant      les tokenizers appropriés.
  Les langues utilisées dans les tweets sont principalement l'anglais et desautre lanngues. Ce dernier n'a aucun support donc nous ne travaillerons qu'avec le premier. Cela     rend l'analyse paralysée d'une certaine manière étant donné que les textes des autres langues seront ignorés.
  
 ## 7.Classification des tweets
   Cette approche utilise la technique de création d'un ensemble de mots qui peuvent être classés en toute confiance comme appartenant à une catégorie particulière pour          chacune des 4 classes. 

   -Les tweets sont chacun comparés aux 4 séries et attribués à un score de similitude. Pour calcule de score j'utilisé la similarité Jaccard .Ilprend uniquement un ensemble     unique de mots pour chaque phrase ou document, tandis que la similitude cosinus prend la longueur totale des vecteurs. La similitude Jaccard est bonne pour les cas où la     duplication n'a pas d'importance, la similitude cosinus est bonne pour les cas où la duplication est importante. Dans notre cas, le contexte compte plus que la               duplication, donc la similarité Jaccard est la technique idéale à utiliser.
   
 ## 8.DataFrame en cluster
   Je souhaitai créer une DatFrame contenant le nombre total de tweets par catégorie et par personne. Cela peut être réalisé d'abord en créant un bloc de données contenant      les scores Jaccard pour chaque tweet pour chaque catégorie, puis en attribuant un tweet à une catégorie en fonction du score le plus élevé et enfin en regroupant les          tweets par somme des tweets.
  
 ## 9.KMeans Clustering
 Pour determine le nombre optimal de cluster  j'utilisé le  méthode du coude.L'approche consiste à rechercher un coude dans le graphe WCSS. Habituellement, la partie du graphique avant le coude décroîtrait fortement, tandis que la partie après serait plus lisse.
 
 Dapres le graphe K=3
 
 
 ## 10.Conclusion
   Le traitement du langage naturel est un vaste domaine et il y a tellement plus à faire sur les données pour obtenir des informations plus précises et utiles.
 
  
  

  


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/slhmohamed/Tweets-Classification-and-Clustering-in-Python.git/HEAD)
