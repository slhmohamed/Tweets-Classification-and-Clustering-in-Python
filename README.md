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
## 4.Prétraitement
### Nettoyage des tweets
    Les tweets contiennent des objets inutiles tels que des hashtags, des mentions, des liens et des signes de ponctuation qui peuvent affecter les performances d'un algorithme     et doivent donc être supprimés. Tous les textes sont convertis en minuscules pour éviter que les algorithmes n'interprètent les mêmes mots avec des cas différents comme         différents.

  
  

  


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/slhmohamed/Tweets-Classification-and-Clustering-in-Python.git/HEAD)
