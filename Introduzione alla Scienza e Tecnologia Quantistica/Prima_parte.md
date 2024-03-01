##Prima Parte
**Stato:** Insieme di operazioni che puoi fare su un sistema. Può essere descritto anche la proprietà fisica di più sistemi preparati nello stesso modo, che creano una funzione d'onda.

**Misurazione:** Un'unico sistema non è misurabile, l'unico modo sarebbe attraverso la clonazione, che renderebbe possibile uno scambio di informazioni più veloce della luce attraverso il quantum entanglement.
Un sistema va misurato più volte, partendo dallo stesso stato iniziale, per avere una stima della probabilità di misurare un certo stato e ricostruire così lo stato iniziale. Questo metodo si chiama *tomografia quantistica*.

**Non clonabilità:** Una particella non è clonabile(a meno che il suo stato non sia ortogonale) perchè nel momento in cui si misura il suo stato collassa in uno stato 0 o 1, e quindi non è più possibile misurare il suo stato originale.

####Postulato 4: Sistemi Composti
Uno stato componente $\ket{\Psi}$ di un sistema composto contiene tutte le funzioni d'onda dei singoli sistemi se separabili.
$$\ket{\Psi} = \ket{\psi_1} \otimes \ket{\psi_2} \otimes \ket{\psi_3} \otimes \ket{\psi_4} \equiv \ket{\psi_1 \psi_2 \psi_3 \psi_4}$$
###3.0 Primitive della Quantum Information Processing
**Coerenza Quantistica:** Possibilità di avrere stati di sovrapposizione.

**Qubit:** Stato quantistico di un sistema quantistico a due livelli. Un qubit è un vettore di dimensione 2.
$$\ket{\psi} = \alpha \ket{0} + \beta \ket{1}$$
Dato dalla somma delle ampiezze di probabilità $\alpha$ e $\beta$. Soddisfano la condizione di normalizzazione $|\alpha|^2 + |\beta|^2 = 1$.

**Sfera di Bloch:** Rappresentazione geometrica di un qubit. Ogni punto sulla sfera rappresenta uno stato quantistico.
$$\ket{\psi} = \alpha \ket{0} + \beta \ket{1} = e^{i\gamma}(\cos(\theta/2)\ket{0} + e^{i\phi}\sin(\theta/2)\ket{1})$$    
Dove $\theta$ e $\phi$ sono le coordinate sferiche e $\gamma$ è la fase globale.
I corrispettivi intervalli di $\theta$, $\phi$ e $\gamma$ sono $[0,\pi]$, $[0,2\pi]$ e $[0,2\pi]$.
//TODO: Aggiungere immagine della sfera di Bloch
Si utilizzano 3 dimensioni per rappresentare uno stato quantistico, ma in realtà è un vettore di dimensione 2. Le prim due dimensione sono le ampiezze complesse di probabilità, mentre la terza è la fase locale.

**Fase globale:** Fase applicata uniformemente a tutto lo stato quantistico. Non ha effetti misurabili, perchè la probabilità di misurare un certo stato è data dal modulo quadro delle ampiezze di probabilità.

**Fase locale:** Fase applicata solo ad una parte dello stato quantistico. Puà influenzare la correlazione quantistica tra qubit, per esempio alterando le proprietà di entanglement.

**Informazione:** In un qubit può essere scritto anche tutto Wikipedia, ma non si può leggere perchè non si può clonare un qubit. Quindi l'informazione è la capacità di fare delle operazioni su un sistema. Un algoritmo deve sapere leggere senza effettuare una misurazione, altrimenti si perde l'informazione.
###3.2 2 Qubits
$$\ket{\psi} = \alpha_{00} \ket{00} + \alpha_{0} \ket{01} + \alpha_{10} \ket{10} + \alpha_{11} \ket{11}$$
Dove $\alpha_{00}$, $\alpha_{01}$, $\alpha_{10}$ e $\alpha_{11}$ sono le ampiezze di probabilità. Soddisfano la condizione di normalizzazione $|\alpha_{00}|^2 + |\alpha_{01}|^2 + |\alpha_{10}|^2 + |\alpha_{11}|^2 = 1$.

**Esempio:**
Misura del primo qubit con lo stato $\ket{0}$:
$$(\ket{0}_1 \bra{0} \otimes \mathbb{I_2})\ket{\psi} = \frac{\alpha_{00}\ket{00} + \alpha_{01}\ket{01}}{\sqrt{|\alpha_{00}|^2 + |\alpha_{01}|^2}}$$
Dove $\ket{0}_1 \bra{0}$ è l'operatore di proiezione sullo stato $\ket{0}$ del primo qubit e $\mathbb{I_2}$ è l'identità del secondo qubit.
Gli stati qualunque sia l'ampiezza di $\alpha_{00}$ e $\alpha_{01}$ non possono essere stati entangled perchè possono essere sempre scritti come il prodotto di due stati singoli.
$$
\ket{\psi} = \frac{1}{\sqrt{2}}\ket{0}(\ket{0} + \ket{1})
$$
Nel momento in cui ho una proiezione su uno stato non potrò mai avere uno stato entangled.

**Esempio:**
$\alpha_{00} = \frac{1}{\sqrt{2}} = \alpha_{11}$
$$\ket{\psi} = \frac{1}{\sqrt{2}}(\ket{00} + \ket{11}) \neq \ket{\psi_1} \otimes \ket{\psi_2}$$
Questa formula è importante perchè mostra che non è possibile scrivere uno stato composto come il prodotto di due stati singoli. Questo è un esempio di entanglement, poichè non è possibile scrivere uno stato composto come il prodotto di due stati singoli.
###3.3 Porte Logiche
Tutte le trasformazioni su un qubit possono essere descritte da una matrice unitaria 2x2. 
$$U^\dagger U = \mathbb{I}$$
**Porta NOT:** Cambia lo stato di un qubit.
$$\ket{0} \rightarrow \ket{1} \\\ket{1} \rightarrow \ket{0}$$
Più in generale:
$$\ket{\psi} = \alpha \ket{0} + \beta \ket{1} \rightarrow \ket{\psi'} = \alpha' \ket{1} + \beta' \ket{0}$$
Dove l'operatore NOT è rappresentato dalla matrice:
$$X = \sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$$
**Porta Hadamard:** Crea uno stato di sovrapposizione.
$$\ket{0} \rightarrow \frac{1}{\sqrt{2}}(\ket{0} + \ket{1}) \equiv {\ket +} \\ \ket{1} \rightarrow \frac{1}{\sqrt{2}}(\ket{0} - \ket{1}) \equiv {\ket -}$$
Più in generale:
$$\ket{\psi} = \alpha \ket{0} + \beta \ket{1} \rightarrow \ket{\psi'} = \frac{1}{\sqrt{2}}(\alpha + \beta) \ket{0} + \frac{1}{\sqrt{2}}(\alpha - \beta) \ket{1}$$
Dove l'operatore Hadamard è rappresentato dalla matrice:
$$H = \frac{1}{\sqrt{2}}\begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$$
**Trasformazione unitaria:**
$$U = e^{i\alpha} \begin{pmatrix} e^{\frac{- i\beta}{2}} & 0 \\ 0 & e^{\frac{i\beta}{2}} \end{pmatrix} \begin{pmatrix} \cos(\frac{\gamma}{2}) & -\sin(\frac{\gamma}{2}) \\ \sin(\frac{\gamma}{2}) & \cos(\frac{\gamma}{2}) \end{pmatrix} \begin{pmatrix} e^{\frac{- i\delta}{2}} & 0 \\ 0 & e^{\frac{i\delta}{2}} \end{pmatrix}$$
Dove $\alpha$ è la fase globale(non interessante), la prima matrice cambia la fase relativa tra qubit 0 e 1 ed effettua una rotazione intorno a z, la seconda matrice effettua una rotazione sul piano ortogonale.
Una trasformaizone su singolo bit si chiama quindi *rotazione*.

**Porte a 2 qubit:**
La NAND è una porta logica a 2 bit chiamata universale perchè ci permette di scrivere tutte le altre porte.
In meccanica quantistica si utilizza la porta CNOT.
La porta CNOT effettua un controllo sul primo qubit e se è 1 effettua una NOT sul secondo qubit(che è il target), il not è descritto come $b \rightarrow a \oplus b$.
//TODO: Aggiungere immagine della porta CNOT
$$U_{CNOT} = \begin{pmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{pmatrix}$$
$U_{CNOT}^\dagger U_{CNOT} = \mathbb{I}$

La porta CNOT(X) può essere anche descritta con una porta Hadamard, la matrice $\delta_z$ e un'altra porta Hadamard.
//TODO: Aggiungere immagine della porta CNOT con le porte Hadamard
$$\ket{0} \rightarrow \ket{1} \equiv \ket{0} \rightarrow \ket{+} \rightarrow \ket{-} \rightarrow \ket{1} \\ \ket{1} \rightarrow \ket{0} \equiv \ket{1} \rightarrow \ket{-} \rightarrow \ket{+} \rightarrow \ket{0}$$
### 3.5 Logica Classica con Qubit
**Porta Toffoli:** Porta logica a 3 bit che effettua una NAND sul terzo bit se i primi due sono 1, dove la NAND è descritta come $c \rightarrow c \oplus ab$.
//TODO: Aggiungere immagine della porta Toffoli
//TODO: Aggiungere tabella di verità della porta Toffoli
Si può rappresentare il NAND con la porta Toffoli
//TODO: Aggiungere immagine NAND con la porta toffoli
Lo stato di input è quindi reversibile perchè manteniamo a e b nell'output.

**Copy(FANOUT):** Non è possibile copiare un qubit, ma è possibile copiare un qubit classico.
//TODO: Aggiungere immagine della porta copy

**Esempio Copy di un qubit non ortogonale:**
//TODO: Aggiungere esempio di copy di un qubit non ortogonale

**Numeri Casuali:**
L'output è un bit classico con probabilità 0.5 di essere 0 o 1.
//TODO: Aggiungere immagine della porta random
