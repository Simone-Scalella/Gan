# Gan
Implementazione di una GAN (Generative Adversarial Network).
Per ottenere risultati migliori è necessario addestrare i modelli per molte epoche.
L'ideale sarebbe 2000, su architetture dotate di GPU per ridurre i tempi di addestramento.

## Cosa sono le GAN ?

Le GAN, o Generative Adversarial Networks, sono un tipo di architettura di reti neurali artificiali introdotta da Ian Goodfellow e i suoi colleghi nel 2014. Le GAN sono progettate per generare nuovi dati realistici, apprendendo le distribuzioni dei dati esistenti durante il processo di addestramento.

Ecco una descrizione delle principali componenti e del funzionamento delle GAN:

1. **Generatore (Generator):**
   - Il generatore è una rete neurale che prende in input un vettore casuale (rumore) e cerca di generare dati artificiali che assomiglino il più possibile ai dati reali.
   - In termini più tecnici, il generatore trasforma un punto in uno spazio latente (di solito un vettore di numeri casuali) in un punto nello spazio dei dati.

2. **Discriminatore (Discriminator):**
   - Il discriminatore è un'altra rete neurale che agisce come un classificatore binario. Riceve in input sia dati reali che dati generati dal generatore e cerca di distinguere tra essi.
   - Il discriminatore assegna probabilità che un dato dato sia reale o generato. Addestrando il discriminatore, si fornisce un feedback al generatore per migliorare la qualità delle sue generazioni.

3. **Funzionamento dell'addestramento:**
   - Durante l'addestramento, il generatore e il discriminatore vengono addestrati simultaneamente in un gioco a somma zero.
   - Il generatore cerca di generare dati che il discriminatore classifica come reali, mentre il discriminatore cerca di migliorare la sua capacità di distinguere tra dati reali e generati.
   - L'obiettivo è raggiungere uno stato in cui il generatore è così bravo a generare dati che il discriminatore non può più distinguere tra dati reali e generati.

4. **Loss Function (Funzione di Perdita):**
   - La GAN utilizza una funzione di perdita che è una combinazione di due componenti principali:
     - La loss del generatore: Misura quanto bene il generatore inganna il discriminatore.
     - La loss del discriminatore: Misura quanto bene il discriminatore distingue tra dati reali e generati.

5. **Convergenza:**
   - L'addestramento delle GAN può essere complesso, e il successo dipende dalla ricerca di un equilibrio tra generatore e discriminatore.
   - Quando le GAN convergono, si raggiunge uno stato in cui il generatore genera dati che sono difficili da distinguere dai dati reali.

6. **Applicazioni:**
   - Le GAN sono utilizzate in una varietà di campi, tra cui la generazione di immagini, il miglioramento delle immagini, la traduzione delle immagini da uno stile all'altro, la generazione di testo realistico, la creazione di nuovi design, e altro ancora.

Le GAN sono una potente architettura che ha portato a progressi significativi nel campo della generazione di contenuti realistici e nella creazione di dati sintetici utili per una serie di applicazioni.
