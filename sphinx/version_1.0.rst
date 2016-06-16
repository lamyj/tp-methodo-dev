Version 1.0
===========

Premier commit
--------------

En appliquant ce qui a été présenté concernant l'écriture du code et le *test-driven development*, ajoutez une première fonctionnalité : la lecture de deux nombres et l'affichage de leur somme. Pour cette fonctionnalité, trois tests doivent être validés :

* l'addition de deux entiers positifs différents
* l'addition d'un entier positif et d'un entier négatif (de préférence différent de l'opposé du premier)
* l'addition de deux réels

La commande `git status`_ permet de vérifier l'état des fichiers dans le dépôt (inconnu, propre, modifié, supprimé, etc.). Vérifiez le statut courant de votre dépôt ; si des fichiers surnuméraires apparaissent, pensez à ajuster votre ``.gitignore``.

En vérifiant le statut du dépôt entre chaque étape,

1. Ajoutez le fichier au dépôt (`git add`_)
2. Sauvegardez vos modifications (`git commit`_) avec un message concis et informatif

Vérifiez que votre commit a bien été pris en compte (`git log`_).

Ajout de fonctionnalités
------------------------

Ajoutez deux nouvelles fonctionnalités : la soustraction et la multiplication. L'application doit désormais commencer par lire l'opérateur (``+``, ``-`` ou ``*``), puis les deux opérandes ; si l'opérateur est inconnue, une erreur doit être remontée à l'utilisateur. Étendez les tests de l'étape précédente pour ces nouvelles opérations, et ajoutez un test vérifiant qu'une erreur se produit bien dans le cas d'un opérateur non reconnu.

Votre application contient-elle actuellement du code dupliqué ? Si oui, supprimez-le. Vérifiez que les différentes sont documentées (a minima, une brève description de leur utilité), puis faitez un nouveau commit. En cas d'erreur dans un commit (fichier oublié, erreur dans le message, etc.), il est possible de modifier le dernier commit (``git commit --amend``).

Contrôle d'erreur
-----------------

Ajoutez la division de deux nombres à votre application, en vérifiant qu'il n'y a pas de régression introduite par cet ajout, et en ajoutant deux nouveaux tests :

* la division de deux réels
* la division d'un réel par 0

Faites un nouveau commit. Dans cet exercice, un commit a été réalisé pour chaque fonctionnalité : quels sont les avantages et les inconvénients de cette approche par rapport à l'utilisation d'un unique commit pour cette section ?

Étiquetage de version
---------------------

Dernier ajout avant l'étiquetage d'une version : la saisie d'une constante. Au lieu de saisr un nombre, l'utilisateur peut également saisir la valeur ``pi`` qui sera pour l'instant approximée à 3.14 (cette valeur est *très* approximative, mais ce choix est utilisé dans la suite du TP). Comme pour les fonctionnalités précédentes, vérifiez l'absence de régression, mettez à jour les tests, et faites un commit.

La première version de votre application est désormais prête : ajoutez une étiquette (de valeur ``v1.0``) au dernier commit (`git tag`_). Lors du travail avec un dépôt distant (ce qui n'est pas le cas dans ce TP), il ne faut pas oublier que les étiquettes ne sont pas transmises par défaut : il faut ajouter l'option ``--tags`` à la commande `git push`_. La documentation mentionne que les étiquettes peuvent être déplacées ou supprimées, mais dans la pratique il faut éviter de modifier une étiquette qui a été transmise à un autre dépôt ou un autre développpeur : pourquoi ?

Les étiquettes peuvent avoir un contenu sémantique : une des conventions possibles est la `Gestion sémantique de version`_, mais l'utilisation de cette convention ou d'une autre reste, comme d'habitude, une décision à prendre pour chaque projet.

.. _Gestion sémantique de version: http://semver.org/lang/fr/
.. _git add: https://git-scm.com/docs/git-add
.. _git commit: https://git-scm.com/docs/git-commit
.. _git log: https://git-scm.com/docs/git-log
.. _git push: https://git-scm.com/docs/git-push
.. _git status: https://git-scm.com/docs/git-status
.. _git tag: https://git-scm.com/docs/git-tag
