# Rapport de la démarche pour l'analyse du document Mobycréa

## Étape 1 : Extraction du texte du PDF

Le document `Sujet-Mobycrea.pdf` est un fichier PDF binaire. Pour analyser son contenu, il est nécessaire de l'extraire sous forme de texte. Voici les étapes suivies :

1. **Vérification des outils disponibles** :
   - Vérification de la présence de `pdf2text` (non disponible).
   - Vérification de la présence de `pdftotext` (disponible).

2. **Extraction du texte** :
   - Utilisation de la commande `pdftotext` pour extraire le texte du PDF.
   - Commande utilisée : `pdftotext -layout "Sujet-Mobycrea.pdf" "Sujet-Mobycrea.txt"`.
   - Le fichier `Sujet-Mobycrea.txt` a été généré avec succès.

## Étape 2 : Analyse du contenu extrait

Le texte extrait du PDF a été analysé et contient les informations suivantes :

### Contexte du projet Mobycréa
- Le système Mobycréa est un berce-bébé automatisé destiné au grand public.
- Il est constitué de deux axes en série : un vertical et un horizontal.
- L'objectif est de limiter l'accélération au niveau de la tête de l'enfant pour son bien-être.

### Objectifs du TP
1. **Analyse cinématique** :
   - Déterminer la relation entre l'accélération au niveau de la tête de l'enfant et les paramètres de pilotage des moteurs (vitesse, accélération angulaire).
   - Mettre en œuvre une mesure du courant et la mise en forme du signal délivré par le capteur à l'aide d'un montage composé d'amplificateurs opérationnels.

2. **Projet de conception d'une chaîne d'acquisition** :
   - Concevoir et mettre en œuvre une chaîne de mesure complète pour connaître le courant moteur (image du couple fourni par le moteur).
   - Caractériser le fonctionnement du capteur et proposer une mise en forme du signal pour répondre à un cahier des charges spécifiques.

### Ressources disponibles
- Maquette pilotable du système.
- Webcam et logiciel Tracker.
- Capteur de courant.
- Documentation technique du capteur de courant MR003 (MICROBOT).
- Documentation technique de l'amplificateur opérationnel TL081.

### Partie 1 : Analyse cinématique proposée
- **Objectif** : Proposer une modélisation cinématique du Mobycréa et son exploitation.
- **Questions** :
  - Pourquoi est-il nécessaire de limiter l'accélération au niveau de la tête de l'enfant ?
  - Quel point du système permet d'étudier l'accélération au niveau de la tête de l'enfant ?
  - Quel schéma cinématique proposer ?
  - Quel protocole expérimental mettre en place pour comparer les résultats théoriques aux résultats expérimentaux ?
  - Pouvez-vous quantifier les écarts entre expérience et modélisation et les expliquer ?

### Partie 2 : Projet de conception d'une chaîne d'acquisition
- **Objectif** : Concevoir et mettre en œuvre une chaîne de mesure complète pour connaître le courant moteur.
- **Cahier des charges** :
  - Capter le courant moteur Im (lié au couple moteur Cem) circulant dans le moteur du Mobycréa.
  - Pour un courant évoluant entre 0 à Immax, la chaîne de mise en forme devra présenter une tension comprise entre 0 et 5V.
  - La tension délivrée par le capteur pour Immax est de 2V.
  - Les valeurs numériques relevées seront transmises par liaison série à un ordinateur pour afficher une courbe de l'évolution du couple dans le moteur.

### Étapes détaillées pour la mise en œuvre

#### 2.1 - Modéliser le capteur
- **Définir les grandeurs d'entrées et de sortie du capteur** :
  - Entrée : Courant moteur Im.
  - Sortie : Tension Vout.
  - Alimentation : À définir selon la documentation technique.

- **Tracer la caractéristique d'entrée/sortie Vout=f(Im)** :
  - Utiliser les informations de la documentation technique pour tracer la caractéristique théorique.
  - Déterminer l'équation de cette caractéristique.

- **Définir un protocole de mesure** :
  - Matériel utilisé : Capteur de courant, source de courant variable, multimètre, etc.
  - Démarche expérimentale : Mesurer la tension de sortie pour différentes valeurs de courant d'entrée.
  - Traitement des données : Tracer la caractéristique expérimentale et comparer avec la caractéristique théorique.

- **Faire valider le protocole expérimental** :
  - Présenter le protocole au professeur pour validation.
  - Mettre en œuvre le capteur et réaliser les tests nécessaires.

- **Comparer les différents modèles** :
  - Comparer les résultats théoriques et expérimentaux.
  - Conclure sur la pertinence des modèles.

#### 2.2 - Étude de la mise en forme du signal
- **Mettre en équation la structure proposée** :
  - Exprimer la tension de sortie VS en fonction de la tension d'entrée VE et des éléments du montage.
  - Utiliser les lois des circuits électriques pour établir les équations.

- **Déterminer le gain et l'offset nécessaire** :
  - Calculer le gain nécessaire pour adapter la tension de sortie du capteur à la plage 0-5V.
  - Déterminer l'offset pour ajuster la tension de décalage.

- **Proposer une adaptation de la structure** :
  - Choisir les valeurs des résistances RG et RO.
  - Choisir la tension d’alimentation du pont constitué par les résistances R1 et R0.
  - Valider les résultats par simulation à l'aide du logiciel Proteus.

- **Mettre en œuvre la structure et le capteur** :
  - Monter le circuit avec les composants choisis.
  - Valider par la mesure que la chaîne de mesure répond bien aux attentes du cahier des charges.

## Conclusion

Le document `Sujet-Mobycrea.pdf` décrit un projet de TP visant à analyser et concevoir une chaîne d'acquisition pour un berce-bébé automatisé. Les étapes détaillées ci-dessus permettent de comprendre la démarche à suivre pour réaliser ce projet, depuis l'analyse cinématique jusqu'à la mise en œuvre de la chaîne de mesure du courant moteur.

Pour plus de détails, vous pouvez consulter le fichier `Sujet-Mobycrea.txt` qui contient le texte extrait du PDF.
