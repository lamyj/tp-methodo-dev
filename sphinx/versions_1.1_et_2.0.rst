Versions 1.1 et 2.0
===================

Documentation du code
---------------------

Ajoutez deux nouvelles fonctionnalités : le cosinus et le sinus. Ces deux opérateurs (respectivement ``cos`` et ``sin``) prennent une seule opérande, l'angle, et renvoient le sinus ou le cosinus de cet angle. Comme pour les étapes précédentes, n'oubliez pas les tests et le commit.

Avez-vous choisi d'exprimer l'angle en degré ou en radian ? Est-ce documenté (au moins au niveau des fonctions, la documentation utilisateur n'étant pas abordée ici) ?

Gestion de bug
--------------

La valeur de π n'est pas assez précise : sin(3.14 rad) vaut 0.0016 alors que la valeur attendue de sin(π rad) est 0. Ceci peut être considéré comme un bug. Revenez sur la version ``v1.0`` (`git checkout`_), créez une nouvelle branche nommée ``maintenance-1.0`` (`git branch`_) et corrigez le bug en remplaçant la valeur approchée de π par une plus précise (n'hésitez pas à vous servir d'une valeur présente dans le langage). Ajoutez une étiquette à ce nouveau commit (``v1.1``), repassez sur la branche principale et fusionnez la branche de maintenance à la branche principale (`git merge`_).

Version 2.0
-----------

Ajoutez la dernière opération avant la version 2.0 : la tangente (opérateur ``tan``). Une fois tous les bugs résolus, créez une nouvelle étiquette (``v2.0``). Vous pouvez obtenir une représentation du graphe de l'historique par ``git log --graph --oneline`` (ou par toute interface graphique de votre choix).

Git permet également de créer des archives du dépôt à partir de la référence d'un commit ou d'une étiquette. À l'aide de la commande `git archive`_, créez des archives (au format ``.zip`` ou ``.tar.gz``) de vos trois version (v1.0, v1.1 et v2.0). Réglez les options de telle manière que ces archives contiennent un dossier nommé ``calculatrice-<VERSION>``, où ``<VERSION>`` vaut l'étiquette, privée de son ``v`` initial (e.g. ``calculatrice-1.1``).

.. _git archive: https://git-scm.com/docs/git-archive
.. _git branch: https://git-scm.com/docs/git-branch
.. _git checkout: https://git-scm.com/docs/git-checkout
.. _git merge: https://git-scm.com/docs/git-merge
