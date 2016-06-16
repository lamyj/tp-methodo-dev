Mise en place
=============

Cette première étape a pour but d'installer et de configurer `Git`_ puis de créer un premier dépôt vide.

Installation et configuration de Git
------------------------------------

Des binaires précompilés sont disponibles pour `Mac`_ et `Windows`_. Sous OS X, il est également possible de passer par un gestionnaire de paquet si vous en avez déjà un d'installé (`Homebrew`_, `MacPorts`_). Sous Linux, il est recommandé d'utiliser les paquets de la distribution ; un `récapitulatif`_ des différentes commandes selon les distributions est donné sur le site de Git.

Une fois Git installé, il est recommandé de configurer son identité (nom et adresse e-mail) qui sera associée à chaque commit :

.. code-block:: shell

  git config --global user.name "Georges Brouchard"
  git config --global user.email "brouchard@unistra.fr"

À l'aide de la commande `git config`_, vérifiez que cette configuration a été correctement prise en compte. Une `référence`_ de toutes les commandes de Git est disponible sur leur site web ; une aide peut également être obtenue en ligne de commande avec les options ``-h`` ou ``--help``.

Création d'un dépôt
-------------------

Créez un dépôt qui contiendra les sources de votre projet (`git init`_). Il est possible, par dépôt, de modifier la configuration de Git, en omettant l'option ``--global`` utilisée ci-dessus. Essayez de modifier le nom ou l'email *uniquement pour ce dépôt*. Vérifiez que le découplage entre la configuration globale et la configuration locale fonctionne.

En fonction des langages et des éventuelles méthodes de compilation, il peut être intéressant d'exclure automatiquement certains fichiers du dépôt (e.g. ``.o`` en C et C++, ``.class`` en Java, ``.pyc`` en Python). Dans votre dépôt, créez un fichier nommé `.gitignore`_ qui contient les motifs des fichiers que vous voulez exclure.

Infrastructure de tests
-----------------------

L'infrastructure de tests étant très dépendante du langage, seuls quelques outils seront mentionnés. N'hésitez pas à nous aider à compléter cette liste.

* C++ : `Boost.Test`_, `tutoriel <http://www.alittlemadness.com/2009/03/31/c-unit-testing-with-boosttest/>`_
* Java : `JUnit`_, `tutoriel <http://www.jmdoudoux.fr/java/dej/chap-junit.htm>`_
* Python : `unittest`_, tutoriel sur la page du module

A minima, les tests peuvent être réalisés par un ensemble d'exécutables ou de scripts isolés, même si les outils ci-dessus apportent une plus-value en terme de reproductibilité et de génération de rapport.

.. _Boost.Test: http://www.boost.org/doc/libs/1_61_0/libs/test/doc/html/index.html
.. _.gitignore: https://git-scm.com/docs/gitignore
.. _Git: https://git-scm.com/
.. _git config: https://git-scm.com/docs/git-config
.. _git init: https://git-scm.com/docs/git-init
.. _JUnit: http://junit.org/junit4/
.. _Homebrew: http://brew.sh/
.. _Mac: https://git-scm.com/download/mac
.. _MacPorts: https://www.macports.org/
.. _récapitulatif: https://git-scm.com/download/linux
.. _référence: https://git-scm.com/docs
.. _unittest: https://docs.python.org/3/library/unittest.html
.. _Windows: https://git-scm.com/download/win
