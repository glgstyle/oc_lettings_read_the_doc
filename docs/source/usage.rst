Usage
=====

.. _installation:

Installation
------------

Pour installer Orange County Lettings, veuillez suivre les instructions suivantes:

1. Créer un répertoire pour le projet et se placer à l'intérieur

.. code-block:: console

   mkdir in
   cd /path/to/put/project/in

2. Cloner le repository

.. code-block:: console

   git clone https://github.com/OpenClassrooms-Student-Center/Python-OC-Lettings-FR.git

3. Créer l'environnement virtuel

.. code-block:: console

   cd /path/to/Python-OC-Lettings-FR
   python -m venv venv

Si l'étape précédente comporte des erreurs avec un paquet non trouvé sur Ubuntu

.. code-block:: console

   apt-get install python3-venv

4. Activer l'environnement, puis vérifier que python exécute l'interpréteur Python dans l'environnement virtuel

.. code-block:: console

   source venv/bin/activate
   which python

5. Confirmer que la version de l'interpréteur Python est la version 3.6 ou supérieure

.. code-block:: console

   python --version

6. Confirmer que la commande pip exécute l'exécutable pip dans l'environnement virtuel

.. code-block:: console

   which pip

Pour désactiver l'environnement

.. code-block:: console

   deactivate

7. Créer un fichier .env à la racine du projet

.. code-block:: console
   mkdir .env

8. Copier le contenu du fichier.env_sample et le coller dans le fichier .env 

.. code-block:: console


.. _utilisation:

Utilisation du site en local
-----------------------------

1. Aller dans le répertoire contenant le projet

.. code-block:: console

   cd /path/to/Python-OC-Lettings-FR

2. Activer l'environnement

.. code-block:: console

   source venv/bin/activate

3. Installer les packages

.. code-block:: console

   pip install --requirement requirements.txt`

4. Démarrer le serveur

.. code-block:: console

   python manage.py runserver

5. Aller à l'adresse suivante dans un navigateur

.. code-block:: console
   
   http://localhost:8000

6. Confirmer que le site fonctionne et qu'il est possible de naviguer (vous devriez voir plusieurs profils et locations)


Recherche d'erreurs (linting)
------------------------------
1. Aller dans le répertoire contenant le projet

.. code-block:: console

   cd /path/to/Python-OC-Lettings-FR

2. Activer l'environnement

.. code-block:: console

   source venv/bin/activate

3. Chercher les erreurs et violations des conventions et normes PEP8

.. code-block:: console

   flake8

4. Générer un rapport html pour plus de lisibilité sur les erreurs

.. code-block:: console

   flake8 --format=html --htmldir=flake-report

5. Ouvrir dans un navigateur l'index.html qui se trouve dans le dossier flake-report 


Tests unitaires
----------------

1. Aller dans le répertoire contenant le projet

.. code-block:: console

   cd /path/to/Python-OC-Lettings-FR

2. Activer l'environnement

.. code-block:: console

   source venv/bin/activate

3. Lancer les tests

.. code-block:: console
   
   pytest


Tests de couverture
--------------------

Générer un rapport html des tests

.. code-block:: console

   coverage html --skip-covered


Base de données
----------------

1. Aller dans le répertoire contenant le projet

.. code-block:: console

   cd /path/to/Python-OC-Lettings-FR

2. Activer l'environnement

.. code-block:: console

   source venv/bin/activate

3. Ouvrir une session shell 

.. code-block:: console

   sqlite3

4. Se connecter à la base de données

.. code-block:: console

   .open oc-lettings-site.sqlite3

5. Afficher les tables dans la base de données

.. code-block:: console
   
   .tables

6. Afficher les colonnes dans le tableau des profils

.. code-block:: console
   pragma table_info(Python-OC-Lettings-FR_profile);

7. Lancer une requête sur la table des profils

.. code-block:: console

   select user_id, favorite_city from Python-OC-Lettings-FR_profile where favorite_city like 'B%';

8. Quitter

.. code-block:: console

   .quit
