TP Méthodologies de développement
=================================

Prétexte : Réalisation d'une calculatrice simple, langage/outils au choix

Buts :

* Utilisation de Git
* Tests
* Gestion de versions et de bugs
* Documentation du code

1. Mise en place

  * Création d'un dépôt Git : config, .gitignore

2. Opérations basiques

  * Addition : lecture de deux nombres, affichage de leur somme. 
  
    * Tests : deux entiers positifs, un entier positif et un négatif, deux réels
    * Commit
    
  * Soustraction, multiplication : lecture de l'opération (+, -, *), des 
    opérandes, affichage du résultat.
    
    * Tests : id. ci-dessus pour chacune des opérations, opération inconnue
    * Y a-t-il du code dupliqué ? Si oui, le supprimer.
    * Commit

  * Division : id. ci-dessus, gestion de la division par 0.
    
    * Tests
    * Commit

  * Constantes : en plus lieu d'un nombre, l'utilisateur peut saisir la valeur
    d'une constante (π, valant 3.14)
    
    * Tests
    * Version 1.0

3. Opérations trigonométriques

  * Nouvelles opérations : cosinus et sinus
  
    * Avez-vous choisi l'angle en degré ou en radian ? Est-ce documenté ?
    * Tests, commit

  * Bug : valeur de π pas assez précise
  
    * Retour sur la version 1.0, nouvelle branche, correction, test, commit, 
      version 1.1
    * Correction de la version courante

  * Nouvelle opération : tan
  
    * Gestion des erreurs
    * Tests, version 2.0
