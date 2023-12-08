#C
 
**CANAL DE PAIMENT -** Dans le cadre du Lightning Network, un canal de paiement est une connexion bidirectionnelle entre deux nœuds Lightning et qui permet de faire des échanges de bitcoins off-chain. On-chain, un canal de paiement est représenté par une adresse multi-signatures 2/2 détenue par les deux participants. Le canal de paiement nécessite une transaction on-chain pour son ouverture et une transaction off-chain pour sa fermeture. Entre ces deux évènements, les utilisateurs du canal peuvent réaliser un très grand nombre d'échanges de bitcoins off-chain, sur le Lightning Network, sans nécessiter une activité on-chain. Sur Lightning, il est possible de router un paiement à travers plusieurs canaux de paiements et plusieurs nœuds, afin d'envoyer des bitcoins sans forcément ouvrir un canal direct avec le receveur.



**CHARGE UTILE (PAYLOAD) -** Dans le contexte général de l'informatique, une charge utile désigne les données essentielles transportées dans un paquet de données plus large. Par exemple, dans une adresse SegWit V0 sur Bitcoin, la charge utile correspond au hachage de la clé publique, sans les diverses métadonnées (le HRP, le séparateur, la version de SegWit et la somme de contrôle). Par exemple, sur l'adresse `bc1qc2eukw7reasfcmrafevp5dhv8635yuqays50gj`, nous avons :
 
 * `bc` : la partie lisible par l'homme (HRP) ;
 * `1` : le séparateur ;
 * `q` : la version de SegWit. Ici, c'est la version 0 ;
 * `c2eukw7reasfcmrafevp5dhv8635yuqa` : la charge utile, ici, le hachage de la clé publique ;
 * `ys50gj` : la somme de contrôle.



**CHIFFRER (CHIFFREMENT) -** Méthode cryptographique permettant de convertir une information brute en information chiffrée. Une information chiffrée masque la signification originale des données pour empêcher qu'elles ne soient connues. Le chiffrement consiste en une série de transformations effectuées sur l'information originale à l'aide d'une clé. Si ces transformations sont réversibles, le processus d'inversion correspondant est appelé « déchiffrement », et il permet de restaurer les informations à leur état brut.



**CIBLE DE DIFFICULTÉ -** Le facteur de difficulté, aussi connu sous le nom de cible de difficulté, est un paramètre crucial dans le mécanisme de consensus par preuve de travail (Proof of Work, PoW) utilisé par Bitcoin. La cible représente une valeur numérique qui détermine la difficulté pour les mineurs de résoudre un problème cryptographique spécifique, appelé preuve de travail, lors de la création d'un nouveau bloc dans la blockchain. La cible de difficulté est un nombre ajustable de 256 bits (64 octets) déterminant une limite d’acceptabilité pour le hachage de l’entête des blocs. Autrement dit, pour qu’un bloc soit valide, le hachage de son entête avec `SHA256d` (double `SHA256`) doit être numériquement inférieur ou égal à la cible de difficulté. La preuve de travail consiste à modifier le champ `nonce` de l'entête du bloc ou de la transaction coinbase jusqu'à ce que le hachage résultant soit inférieur à la valeur cible. Cette cible est ajustée tous les 2016 blocs (environ toutes les deux semaines), lors d'un évènement que l'on appelle « ajustement ». Le facteur de difficulté est recalculé en fonction du temps qu'il a fallu pour miner les 2016 blocs précédents. Si le temps total est inférieur à deux semaines, la difficulté augmente en ajustant la cible à la baisse. Si le temps total est supérieur à deux semaines, la difficulté diminue en ajustant la cible à la hausse. L’objectif est de conserver un temps de minage par bloc moyen à 10 minutes. Ce temps entre chaque bloc permet d'éviter les divisions du réseau Bitcoin, résultant en un gaspillage de la puissance de calcul. La cible de difficulté se trouve dans chaque entête de bloc, au sein du champ `nBits`. Puisque ce champ est réduit à 32 bits et que la cible fait en réalité 256 bits, la cible est compactée dans un format scientifique moins précis.
 
> _La cible de difficulté est parfois également nommée « facteur de difficulté ». Par extension, on peut l'évoquer avec son encodage dans les entêtes de bloc avec le terme « nBits »._



**CIOH (COMMON INPUT OWNERSHIP HEURISTIC) -** Heuristique utilisée dans le domaine de l'analyse et du traçage des transactions sur Bitcoin qui suppose que toutes les entrées d'une transaction appartiennent à une même entité ou à un même utilisateur. Lorsque l'on observe les données publiques d'une transaction Bitcoin, et que l'on y repère plusieurs entrées (inputs), alors, s'il n'y a pas de paternes où d'autres informations qui viendraient infirmer cela, on peut estimer que toutes les entrées de cette transaction appartenaient à une seule et même personne (ou entité). Cette heuristique d'analyse on-chain a été découverte par Satoshi Nakamoto lui-même, qui en parle dans la partie 10 du White Paper :
 
> « _Toutefois, la liaison est inévitable avec les transactions multi-entrées, qui révèlent nécessairement que leurs entrées étaient détenues par un même propriétaire. Le risque est que si le propriétaire d'une clef est révélé, les liaisons peuvent révéler d'autres transactions qui ont appartenu au même propriétaire._ » - Nakamoto, S. (2008). "Bitcoin: A Peer-to-Peer Electronic Cash System". Consulté à l'adresse https://bitcoin.org/bitcoin.pdf.
 
Encore aujourd'hui, le CIOH demeure le principal outil employé par les sociétés d'analyse de chaîne avec la réutilisation d'adresse.



**CLÉ ÉTENDUE -** Suite de caractère qui combine une clé (publique ou privée), son code de chaîne associé et une série de métadonnées. Une clé étendue rassemble en une seule chaîne de caractère tous les éléments nécessaires à la dérivation de clés enfants. Elles sont utilisées dans les portefeuilles déterministes et hiérarchiques, et peuvent être de deux types : une clé publique étendue (utilisée pour dériver des clés publiques enfants) ou une clé privée étendue (utilisée pour dériver à la fois des clés privées et des clés publiques enfants). Une clé étendue inclut donc plusieurs données différentes, décrites au sein du BIP32, dans l'ordre :
 
 * Le préfixe. `prv` et `pub` sont des HRP permettant d'indiquer si l'on a à faire à une clé privée étendue (`prv`) ou à une clé publique étendue (`pub`). La première lettre du préfixe permet, elle, de désigner la version de la clé étendue :
   
   * `x` permet d'indiquer un objectif Legacy ou SegWit V1 sur Bitcoin ;
   * `t` permet d'indiquer un objectif Legacy ou SegWit V1 sur Bitcoin Testnet ;
   * `y` permet d'indiquer un objectif Nested SegWit sur Bitcoin ;
   * `u` permet d'indiquer un objectif Nested SegWit sur Bitcoin Testnet ;
   * `z` permet d'indiquer un objectif SegWit V0 sur Bitcoin ;
   * `v` permet d'indiquer un objectif SegWit V0 sur Bitcoin Testnet.
 * La profondeur, qui indique le nombre de dérivations intervenues depuis la clé maîtresse pour arriver jusqu'à la clé étendue ;
 * L'empreinte du parent. Cela représente les 4 premiers octets du `HASH160` de la clé publique parent ;
 * L'index. C'est le numéro de la paire parmi ses sœurs dont est issue la clé étendue ;
 * Le code de chaîne ;
 * Un octet de rembourrage si c'est une clé privée `0x00` ;
 * La clé privée ou la clé publique ;
 * Une somme de contrôle. Elle incarne les 4 premiers octets du `HASH256` de tout le reste de la clé étendue.
 
Dans la pratique, la clé publique étendue est utilisée pour générer des adresses de réception et pour observer les transactions d'un compte, sans exposer les clés privées associées. Cela peut permettre, par exemple, la création d'un portefeuille dit « watch-only ». Il est toutefois important de noter que la clé publique étendue est une information sensible pour la confidentialité de l'utilisateur, car sa divulgation peut permettre à des tiers de tracer les transactions et de visualiser le solde du compte associé.



**CLÉ PRIVÉE -** Une clé privée est un élément fondamental de la cryptographie asymétrique. Il s'agit d'une chaîne de caractères alphanumériques de 256 bits qui représente un secret cryptographique. Cette clé est utilisée pour signer numériquement des transactions et prouver la possession d'une clé publique Bitcoin (et par extension, d'une adresse de réception). Les clés privées permettent donc de dépenser des bitcoins en débloquant les UTXO associés à la clé publique correspondante. Les clés privées doivent être conservées strictement confidentielles, car leur divulgation pourrait permettre à des tiers malveillants de prendre le contrôle des fonds associés. Dans le système Bitcoin, la clé privée est liée à une clé publique par le biais d'un algorithme de signature numérique à courbes elliptiques (ECDSA ou Schnorr). La clé publique est dérivée de la clé privée, mais l'inverse est pratiquement impossible à réaliser en raison de la difficulté computationnelle inhérente à la résolution du problème mathématique sous-jacent (problème du logarithme discret). La clé publique est généralement utilisée pour générer une adresse Bitcoin, qui sert à bloquer des bitcoins à l'aide d'un script. En cryptographie, les clés privées sont souvent des nombres aléatoires ou pseudo-aléatoires. Dans le contexte spécifique des portefeuilles déterministes et hiérarchiques Bitcoin, les clés privées sont dérivées de manière déterministe depuis la graine (seed). Les clés privées sont fréquemment confondues avec la graine (seed) ou avec la phrase de récupération (mnémonique). Pourtant, ces éléments sont bien différents.
 
> _En anglais, une clé privée se dit « private key »._



**CLÉ PUBLIQUE -** La clé publique est un élément essentiel de la cryptographie asymétrique. Elle est générée à partir d'une clé privée en utilisant une fonction mathématique irréversible. Sur Bitcoin, les clés publiques sont dérivées depuis leur clé privée associée grâce aux algorithmes de signature numérique à courbes elliptiques ECDSA ou Schnorr. La clé publique, contrairement à la clé privée, peut être partagée librement sans compromettre la sécurité des fonds. Dans le cadre du protocole Bitcoin, la clé publique sert de base pour créer une adresse Bitcoin, qui est ensuite utilisée pour créer des conditions de dépense sur un UTXO. Les clés publiques sont fréquemment confondues avec la clé maîtresse ou avec les clés étendues (xpub...). Pourtant, ces éléments sont bien différents.
 
> _En anglais, une clé publique se dit « public key ». Ce terme est parfois abrégé avec « pubkey », ou « PK »._



**CLI -** Acronyme de « Command Line Interface », ou « interface en ligne de commande » en français. C'est une méthode d'interaction avec des logiciels qui repose sur la saisie de commandes textuelles dans un terminal ou une console. La CLI se différencie de la GUI (interface graphique utilisateur) qui dispose de méthodes d'interactions de pointage (avec la souris) et d'éléments visuels interactifs.



**CODE DE CHAÎNE -** Dans le contexte de la dérivation hiérarchique et déterministe (HD) des portefeuilles Bitcoin, le code de chaîne est une valeur de sel cryptographique de 256 bits utilisée pour générer des clés enfants à partir d'une clé parent, selon le standard BIP32. Le code de chaîne est utilisé en combinaison avec la clé parente et l’index de l’enfant pour générer de manière sécurisée et déterministe une nouvelle paire de clés (clé privée et clé publique) sans révéler la clé parente ou les autres clés enfants dérivées. Il existe donc un code de chaîne unique pour chaque paire de clés. Le code de chaîne est obtenu soit en hachant la graine du portefeuille, et en prenant la moitié des bits à droite. Dans ce cas, on parle d'un code de chaîne maître, associé à la clé privée maîtresse. Ou bien, il peut être obtenu en hachant une clé parent avec son code de chaîne parent et un index, et en conservant les bits à droite. On parle alors de code de chaîne enfant. Cette approche permet aux utilisateurs de gérer plusieurs adresses Bitcoin à partir d'une seule graine (seed), améliorant ainsi la confidentialité dans les transactions Bitcoin. Il est impossible de dériver des clés sans avoir la connaissance du code de chaîne associé à chaque paire parent. Il permet d'introduire des données pseudo-aléatoires dans le processus de dérivation pour garantir que la génération des clés cryptographiques reste imprévisible pour les attaquants tout en étant déterministe pour le détenteur du portefeuille.
 
> _En anglais, un code de chaîne se dit « chain code », et un code de chaîne maître se dit « master chain code »._



**CODE DE PAIMENT RÉUTILISABLE -** Dans le BIP47, un code de paiement réutilisable est une information générée à partir d'un portefeuille Bitcoin permettant d'engager une transaction de notification et de dériver des adresses uniques. Cela permet de ne pas faire de réutilisation d'adresses, qui mènent à une perte de la confidentialité, sans pour autant devoir dériver et transmettre manuellement de nouvelles adresses vierges à chaque paiement. Dans le BIP47, les codes de paiement réutilisables sont construits de la manière suivante :
 
 * L'octet 0 correspond à la version ;
 * L'octet 1 est un champ de bits permettant d'ajouter des informations en cas d'utilisation spécifique ;
 * L'octet 2 permet d'indiquer la parité du `y` de la clé publique ;
 * De l'octet 3 à l'octet 34, on retrouvera la valeur `x` de la clé publique ;
 * De l'octet 35 à l'octet 66, il y a le code de chaîne associé à la clé publique ;
 * De l'octet 67 à l'octet 79, c'est du rembourrage de zéros.
   On ajoute généralement un HRP au départ du code de paiement et une somme de contrôle à la fin, puis on l'encode en base58. La construction d'une code de paiement est donc assez proche de celle d'une clé étendue. Voici mon propre code de paiement BIP47 en base58 : `PM8TJSBiQmNQDwTogMAbyqJe2PE2kQXjtgh88MRTxsrnHC8zpEtJ8j7Aj628oUFk8X6P5rJ7P5qDudE4Hwq9JXSRzGcZJbdJAjM9oVQ1UKU5j2nr7VR5`. Dans l'implémentation PayNym du BIP47, les codes de paiement peuvent également être exprimés sous la forme d'identifiants associés à l'image d'un robot. Voici le mien : `+throbbingpond8B1`. L'utilisation de codes de paiements avec l'implémentation PayNym est actuellement disponible sur Sparrow Wallet sur PC et sur Samourai Wallet sur mobile.



**COINJOIN -** Le CoinJoin est une technique permettant de casser le traçage des bitcoins. Il repose sur une transaction collaborative à la structure spécifique de même nom : la transaction CoinJoin. Les transactions CoinJoin permettent d'améliorer la protection de la vie privée des utilisateurs de Bitcoin en rendant l'analyse des transactions plus difficile pour les observateurs extérieurs. Cette structure permet la combinaison de plusieurs transactions indépendantes en une seule transaction, rendant difficile la détermination des liens entre les adresses d'entrée et de sortie. Le fonctionnement général du CoinJoin est le suivant : différents utilisateurs souhaitant mixer déposent un montant en input d'une transaction. Ces inputs ressortiront en différents outputs de même montant. À la sortie de la transaction, il est donc impossible de déterminer quel output appartient à quel utilisateur. Il n'y a techniquement aucun lien entre les entrées et les sorties de la transaction CoinJoin. Le lien entre chaque utilisateur et chaque UTXO est cassé, de la même manière que l'historique de chaque pièce.
 
<img alt="" width="600" src="/dictionnaire/images/Sch%C3%A9ma%20coinjoin%20wp.png">
Pour permettre le CoinJoin sans qu'aucun utilisateur ne perde la main sur ses fonds à aucun moment, la transaction est d'abord construite par un coordinateur puis transmise à chaque utilisateur. Chacun d'eux signe alors la transaction de son côté en vérifiant qu'elle lui convient, puis toutes les signatures sont ajoutées à la transaction. Si un utilisateur ou le coordinateur tente de voler les fonds des autres en modifiant les outputs de la transaction CoinJoin, alors les signatures seront invalides et la transaction sera refusée par les nœuds. Ce mécanisme augmente la confidentialité des transactions sans nécessiter de modifications du protocole Bitcoin. Des implémentations spécifiques de CoinJoin, telles que Whirlpool, JoinMarket ou Wabisabi, proposent des solutions pour faciliter le processus de coordination entre les participants et renforcer l'efficacité de la transaction CoinJoin. Exemple de transaction coinjoin : https://mempool.space/fr/tx/323df21f0b0756f98336437aa3d2fb87e02b59f1946b714a7b09df04d429dec2
 
> _Le terme de « CoinJoin » ne dispose pas de traduction française. Certains bitcoiners utilisent également les termes de « mix », de « mixing » ou encore de « mixage » pour évoquer la transaction CoinJoin. Selon moi, cette utilisation est une erreur puisque le « mixage » évoque plutôt l'activité d'un acteur central qui mélange des pièces. Cela n'a rien à voir avec le CoinJoin où l'utilisateur ne perd à aucun moment la main sur ses bitcoins durant le processus. Toutefois, ces termes sont globalement admis, même s'ils peuvent parfois porter à confusion._



**CONCATÉNATION -** La concaténation, dans le contexte de la cryptographie et des systèmes informatiques, désigne le processus d'assemblage de deux opérandes, en les mettant bout à bout, formant ainsi une nouvelle chaîne de caractères ou de données. Cette opération se note généralement avec un symbole de deux barres verticales ‖, ou avec le symbôle ∘. Par exemple, la concaténation de 45 avec 87 sera égale à 4587. Nous noterons : 45‖87=4587. On a mis bout à bout les deux opérandes.



**CONDENSAT (HASH) -** Le condensat, dans le contexte de la cryptographie, désigne le résultat (ou l'output) produit par l'application d'une fonction de hachage cryptographique à un ensemble de données. Le condensat est une chaîne de caractères de taille fixe généralement représentée sous forme d'une série de chiffres et de lettres en notation hexadécimale (base 16). Ce résultat a la particularité d'être presque unique et spécifique aux données d'entrée, de sorte qu'un changement minime dans l'entrée produira un condensat complètement différent. Les fonctions de hachage cryptographiques sont conçues pour être unidirectionnelles et résistantes aux collisions, rendant très difficile de retrouver les données initiales à partir du condensat ou de trouver deux entrées distinctes produisant le même condensat.
 
> _Voir la définition de « fonction de hachage » pour plus de précisions sur ce sujet._



**CONFIRMATION -** Correspond au nombre de blocs dont pour lesquels une transaction bénéficie de leurs sécurité. Lorsque l'on diffuse une transaction au réseau Bitcoin, celle-ci est d'abord en attente dans les mempools des nœuds. Elle est ensuite incluse dans un bloc valide par un mineur. À ce stade, la transaction vient d'être ajoutée à la blockchain, elle bénéficie donc d'une première confirmation. Lorsqu'un nouveau bloc sera trouvé par dessus le bloc où se trouve la transaction en question, elle bénéficiera d'une seconde confirmation, et ainsi de suite. Chaque nouveau bloc miné par dessus le bloc contenant la transaction constitue une nouvelle confirmation. Grâce au comptage du nombre de confirmations pour une transaction, on peut estimer le risque qu'elle puisse être finalement annulée. Le nombre de confirmation nous permet de juger du niveau d'immuabilité d'une transaction sur la blockchain.



**CONSENSUS -** Mécanisme par lequel tous les nœuds du réseau Bitcoin parviennent à s'accorder sur l'état partagé de la blockchain. Le consensus permet que tous les utilisateurs s'alignent sur un même historique des transactions Bitcoin, afin notamment d'éviter la double dépense. Le mécanisme de consensus de Bitcoin est parfois appelé « Consensus de Nakamoto ». Il s'appuie sur la preuve de travail et spécifie que tous les nœuds du réseau acceptent la chaîne disposant de la plus grande quantité de travail accumulé.
 
> _Par extension, certaines personnes appellent par « Consensus » les règles tacites du protocole Bitcoin._



**COURBE ELLIPTIQUE -** Dans le contexte de la cryptographie, une courbe elliptique est une courbe algébrique définie par une équation de la forme y2=x3+ax+b. Ces courbes sont utilisées dans la cryptographie à courbes elliptiques (ECC), qui est une méthode de cryptographie à clé publique permettant de créer des algorithmes de chiffrement, de signature numérique et d'échange de clés. Dans le contexte de Bitcoin, l'algorithme ECDSA (Elliptic Curve Digital Signature Algorithm) ou le protocole de Schnorr sont utilisés avec la courbe `secp256k1`. Cette courbe a été choisie pour ses propriétés de performance et de sécurité. Ces algorithmes sont utilisés pour générer des clés publiques à partir de clés privées, ainsi que pour signer des transactions, et donc débloquer des bitcoins. '''