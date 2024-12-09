
### 1. Concetti di Base

- **Codice rilocabile:** Quando un programma viene caricato in memoria (RAM), gli indirizzi relativi (logici) vengono trasformati in indirizzi assoluti (fisici). Questo processo è chiamato rilocazione e può essere **statica** (eseguita all'atto del caricamento) o **dinamica** (eseguita durante l'esecuzione del programma).
- **MMU (Memory Management Unit):** Un componente hardware che traduce gli indirizzi virtuali in indirizzi fisici, consentendo ai programmi di utilizzare uno spazio di indirizzamento virtuale più grande della memoria fisica disponibile.
- **Linking e Binding:** Il linking calcola gli indirizzi logici, mentre il binding li traduce in indirizzi fisici. Questo può avvenire durante la compilazione, il caricamento o l'esecuzione del programma.

### 2. Sfide della Gestione della Memoria

- **Dimensione dei Programmi:** I programmi moderni spesso superano la dimensione della RAM, richiedendo soluzioni per gestire lo spazio di memoria in modo efficiente.
- **Multiprocessing:** L'esecuzione simultanea di più processi può portare alla frammentazione della memoria, riducendo lo spazio disponibile per nuovi processi.
- **Efficienza:** Non tutte le istruzioni di un programma vengono eseguite, quindi caricare l'intero programma in memoria può essere inefficiente.

### 3. Soluzioni

- **Swapping:** Spostare temporaneamente i processi inattivi dalla RAM al disco per liberare spazio.
- **Caricamento Dinamico:** Caricare solo i moduli di programma necessari al momento dell'esecuzione.
- **Overlay:** Suddividere il programma in parti che possono essere caricate alternativamente nella stessa area di memoria.
- **Partizionamento:** Dividere la memoria in partizioni per allocare lo spazio ai processi. Può essere a **partizione fissa** (dimensioni definite staticamente) o **variabile** (dimensioni modificabili dinamicamente).

### 4. Frammentazione

- **Esterna:** Si verifica quando lo spazio libero totale è sufficiente per un processo, ma non è contiguo.
- **Interna:** Si verifica quando uno spazio allocato è più grande del necessario, sprecando memoria.

### 5. Strategie di Allocazione Dinamica

- **First-fit:** Alloca il processo nel primo spazio libero disponibile.
- **Best-fit:** Alloca il processo nello spazio libero più piccolo che può contenerlo.
- **Worst-fit:** Alloca il processo nello spazio libero più grande.
- **Next-fit:** Cerca lo spazio libero successivo all'ultimo processo allocato.

### 6. Memoria Virtuale

- Permette ai programmi di utilizzare uno spazio di indirizzamento più grande della memoria fisica disponibile, caricando solo le parti necessarie in memoria.
- Utilizza due tecniche principali: **paginazione** e **segmentazione**.

### 7. Paginazione

- Divide la memoria fisica e il programma in blocchi di dimensione fissa chiamati **frame** (fisici) e **pagine** (logiche).
- Usa una **tabella delle pagine** per mappare le pagine logiche ai frame fisici.
- Quando un processo fa riferimento a una pagina non presente in memoria, si verifica un **page fault**, che richiede il caricamento della pagina dal disco.

### 8. Segmentazione

- Divide lo spazio di indirizzamento del processo in **segmenti** di dimensione variabile, che corrispondono a unità logiche del programma.
- Usa una **tabella dei segmenti** per mappare i segmenti agli indirizzi fisici.
- Offre vantaggi come la condivisione di codice e la protezione, ma può portare alla frammentazione esterna.

### 9. Segmentazione con Paginazione

- Combina i vantaggi di entrambe le tecniche, usando la segmentazione per la gestione logica e la paginazione per la gestione fisica.
- Divide ogni segmento in pagine, che vengono caricate nei frame disponibili.
- Usa una tabella dei segmenti per mappare i segmenti e una tabella delle pagine per mappare le pagine ai frame.
