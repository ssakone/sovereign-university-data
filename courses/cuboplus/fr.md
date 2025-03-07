---
name: Accélérateur de développement Bitcoin
goal: Acquérir toutes les bases pour commencer à développer sur Bitcoin
objectives:
  - Comprendre les concepts fondamentaux et la technologie sous-jacente à Bitcoin.
  - Acquérir des compétences pratiques en matière de sécurité Bitcoin, de développement logiciel et de gouvernance du réseau.
  - Maîtriser le Lightning Network et ses protocoles associés.
---

# Introduction

## Introduction aux cours CUBO+

![Vidéo](https://youtu.be/4VuI9we_XYM)

Filippo et Mario présentent une conférence introductive sur CUBO+, préparant le terrain pour le parcours d'apprentissage complet qui attend les participants. Ils discutent de la structure des cours, des objectifs d'apprentissage et de la manière dont ceux-ci permettront aux étudiants de se développer dans le domaine du développement Bitcoin.

### Objectifs

Le cours vise à doter les participants d'une compréhension approfondie des principes sous-jacents de Bitcoin, de compétences pratiques en développement et de la capacité à naviguer et à contribuer efficacement à l'écosystème Bitcoin. Grâce à un mélange de connaissances théoriques et d'exercices pratiques, les étudiants maîtriseront les bases de la sécurité Bitcoin, les subtilités de sa pile logicielle et les mécanismes de sa gouvernance.

### Prérequis

Les participants doivent faire preuve d'une grande curiosité, d'un désir d'apprendre à un niveau professionnel et de connaissances de base en développement. Bien qu'une expérience détaillée de Bitcoin ne soit pas requise, une compréhension de base des principes de codage et une ouverture à l'exploration de concepts techniques complexes sont essentielles pour tirer le meilleur parti de l'accélérateur.

# Fondamentaux de Bitcoin

## La réflexion sur la sécurité dans Bitcoin

![Vidéo](https://youtu.be/2f_rK74MB3U)

Peter Todd explore les considérations de sécurité propres à Bitcoin, enseignant aux développeurs comment adopter une approche axée sur la sécurité. La conférence vise à instaurer une base solide pour reconnaître et atténuer les menaces potentielles dans le développement Bitcoin, en se basant sur un exercice pratique consistant à expliciter le modèle de menace d'un logiciel de chronométrage des élections.

## Logiciel libre et open source (FLOSS) dans Bitcoin
![Vidéo](https://youtu.be/GM-ho5M5_mQ)

L'utilisation de logiciels libres et open source (FLOSS) est essentielle dans l'écosystème de Bitcoin. Peter Todd explore l'importance du FLOSS pour Bitcoin, en examinant l'histoire du FLOSS et en montrant comment Github nous permet de construire collectivement des logiciels open source comme Bitcoin.

## Cryptographie dans Bitcoin
![Vidéo](https://youtu.be/4Fw9xS7JlVU)

Adam Gibson guide les participants à travers les bases cryptographiques de Bitcoin d'un point de vue mathématique. La session couvre les fonctions cryptographiques essentielles présentes dans Bitcoin, telles que les hachages et leur sécurité, les arbres de Merkle, les protocoles d'identité et de signature, les logarithmes discrets et les courbes elliptiques.

## Le modèle de gouvernance de Bitcoin

![Vidéo](https://youtu.be/KSpKwTFSOdc)

Peter Todd discute du modèle de gouvernance de Bitcoin, en fournissant des informations sur la manière dont les décisions sont prises au sein de la communauté Bitcoin et sur la manière dont cette approche décentralisée influence le développement et la stabilité du protocole. Il explore notamment comment différents types de changements peuvent entraîner des forks doux ou durs, comment la gouvernance différencie les changements de politique des règles de consensus, et quel est le jeu politique du changement dans Bitcoin.

# Concepts de la couche un

## Les composants d'un nœud Bitcoin

![Vidéo](https://youtu.be/jdHc-pbDI9E)

Adam Gibson décrit les différents composants d'un nœud Bitcoin. Le chapitre se concentre sur le rôle de chaque composant dans le maintien de la fonctionnalité et de l'intégrité du réseau. En particulier, il met l'accent sur pourquoi nous devrions exécuter un nœud Bitcoin, ce que fait un nœud Bitcoin et comment les différents composants d'un nœud Bitcoin fonctionnent.

## Les structures de données de Bitcoin

(La vidéo sera bientôt disponible)
Alekos Filini présente un aperçu approfondi des structures de données de Bitcoin. Cela couvre l'organisation des données au sein de la blockchain et comment cela permet la robustesse et l'efficacité du réseau.
## Stack logiciel Bitcoin L1

![Vidéo](https://youtu.be/L6FkntRwkOU)

Daniela Brozzoni offre un aperçu complet de la pile logicielle Bitcoin Layer 1, expliquant les couches qui composent les fondements du protocole Bitcoin (c'est-à-dire les nœuds Bitcoin et les portefeuilles Bitcoin) et comment construire un logiciel Bitcoin avec une introduction aux bibliothèques Bitcoin et une plongée profonde dans le Bitcoin Development Kit (BDK).

# Lightning Network

## Histoire des canaux de paiement

![Vidéo](https://youtu.be/0ZgE-LjHWvI)

Gabriel Comte offre une perspective historique sur le développement des canaux de paiement, qui sont fondamentaux pour le Lightning Network. Ce chapitre explore l'évolution des canaux de paiement et leur importance dans la mise à l'échelle des transactions Bitcoin, des canaux de paiement de Satoshi aux solutions de canaux de paiement bidirectionnels comme les canaux de micropaiement Duplex ou les canaux de paiement Lightning.

## Histoire du routage atomique

![Vidéo](https://youtu.be/RaMeYgSBJQ0)

Gabriel Comte raconte l'histoire du routage atomique, détaillant plusieurs techniques qui ont été à la base de la couche de routage du réseau Lightning, comme le modèle Hub-and-Spokes, le modèle Ripple et les contrats verrouillés par hachage dans le temps (HTLC). Cette histoire a été cruciale pour permettre des transactions sécurisées et sans confiance sur le Lightning Network.

## Examen de BOLT

![Vidéo](https://youtu.be/Fy5W_ryWrCY)

asi0 examine BOLT, la Base de la technologie Lightning, expliquant les spécifications que tout réseau Lightning doit respecter. Cela sera une première plongée approfondie dans les différentes couches du Lightning Network.

## Principaux clients LN

![Vidéo](https://youtu.be/a0Q_5dzpqKw)

asi0 présente les principaux clients du Lightning Network (LN), en fournissant une analyse de leurs fonctionnalités et de leurs points forts basée sur une matrice 2x2 qui évalue le niveau de garde et de gestion de la liquidité que l'utilisateur a avec les clients LN.

# Les défis du LN

## Défis pratiques pour LN

(la vidéo sera bientôt disponible)

asi0 aborde les défis pratiques auxquels on est confronté lorsqu'on travaille avec le Lightning Network. Cela inclut une discussion sur les limitations actuelles et les efforts en cours pour les surmonter, basés sur 4 principaux défis (gestion de la liquidité, abstraction L1/L2, réception hors ligne et gestion des sauvegardes) qui sont explorés du point de vue de l'utilisateur et du point de vue du développeur.

## Évolution future du LN

![Vidéo](https://youtu.be/TIrAMFK6Peg)

Gabriel Comte spécule sur l'évolution future du Lightning Network, examinant les développements potentiels - tels que les canaux à financement double eltoo, BOLT 12, PTLCs, Watchtowers et les normes LSP - et comment ils pourraient transformer le paysage des transactions Bitcoin.

## Protocoles sur le LN

![Vidéo](https://youtu.be/OLTQLtQyoZE)

Alekos Filini examine les protocoles construits sur le Lightning Network, expliquant comment ils contribuent à la scalabilité et à la fonctionnalité de Bitcoin.

# Bonus

## Minage dans Bitcoin

![Vidéo](https://youtu.be/22LadAWEMQo)

Ajelex plonge dans le monde du minage de Bitcoin, détaillant le processus et son importance dans le contexte de la sécurité du réseau et de la création de nouveaux bitcoins.

## Joinmarket

![Vidéo](https://youtu.be/VFjccozVwc8)
Adam explore Joinmarket, une implémentation de CoinJoin qui améliore la confidentialité et la fongibilité en permettant aux utilisateurs de créer des transactions Bitcoin collaboratives, sans confiance et anonymes.
## Protocoles sur le réseau Lightning

![Vidéo](https://youtu.be/OLTQLtQyoZE)

Alekos discute des différents protocoles qui fonctionnent sur le réseau Lightning, améliorant ses capacités au-delà des simples canaux de paiement. Ce chapitre explore les innovations que ces protocoles apportent au réseau, comment ils interagissent entre eux et leur rôle dans l'écosystème plus large de Bitcoin, comme Keysend, LNURL, Nostr, Lightning LSPs.

# Bonus

## Principes essentiels du minage de Bitcoin

![Vidéo](https://youtu.be/22LadAWEMQo)

Ajelex se concentre sur l'aspect commercial du minage de Bitcoin, examinant les stratégies permettant de maintenir la rentabilité sur un marché concurrentiel. La discussion comprend une analyse des coûts opérationnels, des mesures d'efficacité et de l'économie qui anime l'industrie minière.

## Comprendre Joinmarket

![Vidéo](https://youtu.be/VFjccozVwc8)

Adam Gibson offre un aperçu de Joinmarket, expliquant comment cette implémentation de CoinJoin améliore la confidentialité et la fongibilité de Bitcoin. Il explique comment Joinmarket facilite les transactions collaboratives, sans confiance et anonymes au sein de l'écosystème Bitcoin. Ensuite, dans une deuxième partie, il montre comment exécuter Joinmarket dans Signet.

## Hackathon de la première année de Cubo+

### Groupe 1 Hackathon - L'Héritage de Satoshi

![Vidéo](https://youtu.be/NiaahH57N1w)

Le groupe L'Héritage de Satoshi présente son travail sur la construction d'un commerce électronique Lightning avec Shopify, React JS et Hydrogen, ainsi que la passerelle de paiement IBEX.

### Groupe 2 Hackathon - Honey Badger

![Vidéo](https://youtu.be/dds0-SV8ltE)

Le groupe Honey Badger présente sa solution pour un blog avec des micropaiements Lightning intégrés à l'aide de LnBits et Next.js, Node.js et Hydrogen.

### Groupe 3 Hackathon

![Vidéo](https://youtu.be/2YjrrDMGU9c)

Le troisième groupe présente un tableau de bord de nœud Lightning Network via une API personnalisée, LND, vue.js, node.js, Bootstrap.

### Groupe 4 Hackathon - Satoshi Fellowship

![Vidéo](https://youtu.be/mxLKiHa0mes#)

Le groupe de Satoshi Fellowship présente une application de jeu LN utilisant LnBits et MongoDB, Poetry, Node.js.

### Groupe 5 Hackathon - Lighting Walker

![Vidéo](https://youtu.be/IiY5PmkGNVo)

Le groupe Lighting Walker présente sa solution pour un service de transfert d'argent utilisant MySQL, JavaScript et l'API de ZDB.

# Remerciements et continuez à creuser le terrier du lapin

Nous tenons à remercier nos éducateurs :

- Peter Todd
- Adam Gibson
- Alekos Filini
- Daniela Brozzoni
- Ajelex
- asi0
- Gabriel Comte

Leur expertise a été inestimable pour le succès de ce cours. Il s'agit du premier cours basé sur la 1ère édition de l'initiative Cubo+, réalisé en juillet 2023. Merci à tous les participants et éducateurs d'avoir fait partie de ce voyage éducatif pionnier. Cela marque le début de ce que nous espérons être un long et fructueux voyage dans le monde du développement Bitcoin. En tant que première cohorte, votre participation a fixé la norme pour les futures classes.

Continuez à explorer, apprendre et contribuer à l'écosystème Bitcoin. Les connaissances acquises ici ne sont qu'un point de départ. Continuez à creuser le terrier du lapin et vous découvrirez un monde d'opportunités en constante expansion.
