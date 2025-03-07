---
name: Bitcoin Development Accelerator
goal: Acquisire tutte le basi per iniziare a sviluppare su Bitcoin
objectives:
  - Comprendere i concetti fondamentali e la tecnologia alla base di Bitcoin.
  - Acquisire competenze pratiche in sicurezza Bitcoin, sviluppo software e governance della rete.
  - Sviluppare una padronanza della Lightning Network e dei suoi protocolli associati.
---

# Introduzione

## Introduzione ai corsi di CUBO+

![Video](https://youtu.be/4VuI9we_XYM)

Filippo e Mario forniscono una presentazione introduttiva su CUBO+, preparando il terreno per il completo percorso di apprendimento che attende i partecipanti. Discutono la struttura dei corsi, gli obiettivi di apprendimento e come questi permetteranno agli studenti di svilupparsi nello spazio del Bitcoin.

### Obiettivi

Il corso mira a fornire ai partecipanti una profonda comprensione dei principi fondamentali di Bitcoin, competenze pratiche di sviluppo e la capacità di navigare ed apportare un contributo efficace all'ecosistema di Bitcoin. Attraverso una combinazione di conoscenze teoriche ed esercitazioni pratiche, gli studenti acquisiranno le basi della sicurezza di Bitcoin, le complessità del suo stack software e i meccanismi della sua governance.

### Prerequisiti

Si prevede che i partecipanti abbiano una forte curiosità, una volontà di apprendere a livello professionale e una conoscenza di base dello sviluppo. Sebbene non sia richiesta una conoscenza dettagliata di Bitcoin, è essenziale avere una comprensione di base dei principi di programmazione e una predisposizione ad affrontare concetti tecnici complessi per trarre il massimo vantaggio dall'acceleratore.

# Fondamenti di Bitcoin

## Pensiero sulla sicurezza in Bitcoin

![Video](https://youtu.be/2f_rK74MB3U)

Peter Todd approfondisce le considerazioni sulla sicurezza uniche di Bitcoin, insegnando agli sviluppatori come adottare una mentalità incentrata sulla sicurezza. La lezione mira a instillare una solida base nel riconoscere e mitigare le potenziali minacce nello sviluppo di Bitcoin, basandosi su un esercizio pratico di esplicitazione del modello di minaccia del software per l'indicizzazione delle elezioni.

## Software libero e open source (FLOSS) in Bitcoin
![Video](https://youtu.be/GM-ho5M5_mQ)

L'uso del software libero e open source (FLOSS) è fondamentale nell'ecosistema di Bitcoin. Peter Todd esplora l'importanza del FLOSS per Bitcoin, esaminando la storia del FLOSS e analizzando come Github ci permetta di costruire collaborativamente software open source come Bitcoin.

## Crittografia in Bitcoin
![Video](https://youtu.be/4Fw9xS7JlVU)

Adam Gibson guida i partecipanti attraverso le basi crittografiche di Bitcoin da una prospettiva matematica. La sessione copre le funzioni crittografiche essenziali presenti in Bitcoin, come gli hash e la loro sicurezza, gli alberi di Merkle, i protocolli di identità e firma, i log discreti e le curve ellittiche.

## Modello di governance di Bitcoin

![Video](https://youtu.be/KSpKwTFSOdc)

Peter Todd discute il modello di governance di Bitcoin, fornendo approfondimenti su come vengono prese le decisioni all'interno della comunità di Bitcoin e come questo approccio decentralizzato influisce sullo sviluppo e la stabilità del protocollo. In particolare, esplora come diversi tipi di modifiche possano portare a Fork Soft o Hard, come la governance differisce tra il cambiamento di politiche e le regole di consenso, e qual è il gioco politico del cambiamento in Bitcoin.

# Concetti di Layer One

## Componenti del nodo in Bitcoin

![Video](https://youtu.be/jdHc-pbDI9E)

Adam Gibson analizza i vari componenti di un nodo Bitcoin. Il capitolo si concentra sul ruolo che ogni componente svolge nel mantenere la funzionalità e l'integrità della rete. In particolare, si concentra su perché dovremmo eseguire un nodo Bitcoin, cosa fa un nodo Bitcoin e come funzionano i diversi componenti di un nodo Bitcoin.

## Strutture dati di Bitcoin

(il video sarà disponibile a breve)
Alekos Filini presenta un'analisi approfondita delle strutture dati di Bitcoin. Questo copre l'organizzazione dei dati all'interno della blockchain e come ciò permette la robustezza ed efficienza della rete.
## Stack Software di Bitcoin L1

![Video](https://youtu.be/L6FkntRwkOU)

Daniela Brozzoni offre una panoramica completa dello stack software di Bitcoin Layer 1, spiegando i livelli che compongono la base del protocollo di Bitcoin (cioè i nodi di Bitcoin e i portafogli di Bitcoin) e come costruire software di Bitcoin con un'introduzione alle librerie di Bitcoin e un'analisi approfondita del Bitcoin Development Kit (BDK).

# Lightning Network

## Storia dei Canali di Pagamento

![Video](https://youtu.be/0ZgE-LjHWvI)

Gabriel Comte fornisce una prospettiva storica sullo sviluppo dei canali di pagamento, che sono fondamentali per la Lightning Network. Questo capitolo esplora l'evoluzione dei canali di pagamento e la loro importanza nella scalabilità delle transazioni Bitcoin, dai canali di pagamento di Satoshi alle soluzioni di canali di pagamento bidirezionali come i canali di micro-pagamento Duplex o i canali di pagamento Lightning.

## Storia del Routing Atomico

![Video](https://youtu.be/RaMeYgSBJQ0)

Gabriel Comte ripercorre la storia del routing atomico, descrivendo diverse tecniche che sono state alla base del livello di routing della rete Lightning come il modello Hub-and-Spokes, il modello Ripple e i contratti Hashed TimeLocked (HTLC). Questa storia è stata fondamentale per consentire transazioni sicure e senza fiducia sulla Lightning Network.

## Revisione di BOLT

![Video](https://youtu.be/Fy5W_ryWrCY)

asi0 esamina BOLT, la Base of Lightning Technology, spiegando le specifiche che qualsiasi implementazione della Lightning Network deve rispettare. Questa sarà una prima analisi approfondita dei diversi livelli della Lightning Network.

## Principali Client LN

![Video](https://youtu.be/a0Q_5dzpqKw)

asi0 presenta i principali client della Lightning Network (LN), fornendo un'analisi delle loro caratteristiche e punti di forza basata su una matrice 2x2 che valuta il livello di custodia e gestione della liquidità che l'utente ha con i client LN.

# Le Sfide di LN

## Sfide Pratiche per LN

(il video sarà disponibile a breve)

asi0 affronta le sfide pratiche incontrate quando si lavora con la Lightning Network. Ciò include una discussione sulle limitazioni attuali e gli sforzi in corso per superarle basate su 4 sfide principali (gestione della liquidità, astrazione L1/L2, ricezione offline e gestione del backup) che vengono esplorate dal punto di vista dell'utente e dal punto di vista dello sviluppatore.

## Futura Evoluzione di LN

![Video](https://youtu.be/TIrAMFK6Peg)

Gabriel Comte specula sulla futura evoluzione della Lightning Network, esaminando sviluppi potenziali - come i canali dual-funded eltoo, BOLT 12, PTLC, Watchtowers e gli standard LSP - e come potrebbero trasformare il panorama delle transazioni Bitcoin.

## Protocolli sopra LN

![Video](https://youtu.be/OLTQLtQyoZE)

Alekos Filini esamina i protocolli costruiti sopra la Lightning Network, spiegando come contribuiscono alla scalabilità e funzionalità di Bitcoin.

# Bonus

## Mining in Bitcoin

![Video](https://youtu.be/22LadAWEMQo)

Ajelex approfondisce il mondo del mining di Bitcoin, dettagliando il processo e la sua importanza nel contesto della sicurezza della rete e nella creazione di nuovi bitcoin.

## Joinmarket

![Video](https://youtu.be/VFjccozVwc8)
Adam esplora Joinmarket, un'implementazione di CoinJoin che migliora la privacy e la fungibilità consentendo agli utenti di creare transazioni Bitcoin collaborative, senza fiducia e anonime.
## Protocolli sopra la Lightning Network

![Video](https://youtu.be/OLTQLtQyoZE)

Alekos discute dei vari protocolli che operano sopra la Lightning Network, migliorando le sue capacità oltre i semplici canali di pagamento. Questo capitolo esplora le innovazioni che questi protocolli portano alla rete, come interagiscono tra loro e il loro ruolo nell'ecosistema più ampio di Bitcoin, come Keysend, LNURL, Nostr, Lightning LSPs.

# Bonus

## Concetti essenziali del mining di Bitcoin

![Video](https://youtu.be/22LadAWEMQo)

Ajelex si concentra sull'aspetto commerciale del mining di Bitcoin, esaminando le strategie per mantenere la redditività in un mercato competitivo. La discussione include un'analisi dei costi operativi, delle misure di efficienza e dell'economia che guida l'industria mineraria.


## Comprensione di Joinmarket

![Video](https://youtu.be/VFjccozVwc8)

Adam Gibson offre una panoramica di Joinmarket, illustrando come questa implementazione di CoinJoin migliora la privacy e la fungibilità di Bitcoin. Discute di come Joinmarket facilita transazioni collaborative, senza fiducia e anonime all'interno dell'ecosistema di Bitcoin. Poi, in una seconda parte, mostra come eseguire Joinmarket in Signet.

## Cubo+ primo anno Hackathon

### Gruppo 1 Hackathon - The Satoshi Legacy

![Video](https://youtu.be/NiaahH57N1w)

Il gruppo di The Satoshi Legacy presenta il loro lavoro sulla costruzione di un e-commerce Lightning con Shopify, React JS e Hydrogen e il gateway di pagamento IBEX.

### Gruppo 2 Hackathon - Honey Badger

![Video](https://youtu.be/dds0-SV8ltE)

Il gruppo di Honey Badger presenta la loro soluzione per un blog con pagamenti micropagati Lightning integrati con l'uso di LnBits e Next.js, Node.js e Hydrogen.

### Gruppo 3 Hackathon

![Video](https://youtu.be/2YjrrDMGU9c)

Il terzo gruppo presenta una dashboard del nodo della Lightning Network tramite un'API personalizzata, LND, vue.js, node.js, Bootstrap.


### Gruppo 4 Hackathon - Satoshi Fellowship

![Video](https://youtu.be/mxLKiHa0mes#)

Il gruppo di Satoshi's Fellowship presenta un'app di gioco LN utilizzando LnBits e MongoDB, Poetry, Node.js.

### Gruppo 5 Hackathon - Lighting Walker

![Video](https://youtu.be/IiY5PmkGNVo)

Il gruppo di Lightning Walker presenta la loro soluzione per il servizio di rimessa utilizzando MySQL, JavaScript e l'API di ZDB.

# Riconoscimenti e Continua a Scavare la Tana del Coniglio

Desideriamo riconoscere i contributi dei nostri educatori:

- Peter Todd
- Adam Gibson
- Alekos Filini
- Daniela Brozzoni
- Ajelex
- asi0
- Gabriel Comte

La loro competenza è stata preziosa per il successo di questo corso. Questo è stato il primo corso basato sulla prima edizione dell'iniziativa Cubo+, condotto nel luglio 2023. Grazie a tutti i partecipanti ed educatori per essere stati parte di questo pionieristico percorso educativo. Segna l'inizio di ciò che speriamo sia un lungo e fruttuoso viaggio nel mondo dello sviluppo di Bitcoin. Come prima coorte, la vostra partecipazione ha stabilito lo standard per le future classi.

Continuate ad esplorare, imparare e contribuire all'ecosistema di Bitcoin. La conoscenza acquisita qui è solo un punto di partenza. Continua a scavare la tana del coniglio e scoprirai un mondo di opportunità in continua espansione.
