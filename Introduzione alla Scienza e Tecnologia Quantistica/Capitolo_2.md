##2.1.3 Le matrici di Pauli
Sono quattro matrici 2x2 che formano una base per lo spazio delle matrici 2x2. Sono:
$$
\sigma_0 \equiv I \equiv \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \quad \sigma_1 \equiv \sigma_x \equiv X \equiv \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad \sigma_2 \equiv \sigma_y \equiv Y \equiv \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad \sigma_3 \equiv \sigma_z \equiv Z \equiv \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}.
$$
##2.1.4 Inner product
L'operatore duale è un operatore da *V* a *C* utilizzando un inner product. L'operatore duale di un operatore *A* è definito come:
$$
A^{\dagger} \equiv \left( A^T \right)^*.
$$
Lo spazio di Hilbert è uno spazio vettoriale complesso con un inner product definito. L'inner product di due vettori *v* e *w* è definito come:
$$
\left \langle v | w \right \rangle \equiv v^{\dagger} w \equiv [v_1^*, v_2^*, \ldots, v_n^*] \begin{pmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{pmatrix}
$$
Questo ci darà sempre un numero complesso.
L'inner product da due vettori mi produce uno scalare.
Invece l'outer product di due vettori mi produce una matrice. E' definito come:
$$
| v \rangle \langle w | \equiv \begin{pmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{pmatrix} [w_1^*, w_2^*, \ldots, w_n^*].
$$
####2.1 L'inequalià di Cauchy-Schwarz
L'inequalità di Cauchy-Schwarz è una disuguaglianza importante in matematica che coinvolge l'inner product in uno spazio vettoriale. Per due vettori *v* e *w* in uno spazio vettoriale complesso, l'inequalità di Cauchy-Schwarz afferma che:
$$
\left | \left \langle v | w \right \rangle \right |^2 \leq \left \langle v | v \right \rangle \left \langle w | w \right \rangle.
$$
L'uguaglianza si verifica solo quando i due vettori sono linearmente dipendenti.
##2.1.5 Eigevalues e Eigevalues
La rappresentazione diagonale di un operatore *A* su uno spazio vettoriale *V* è data da:
$$
A = \sum_{i=1}^n \lambda_i | i \rangle \langle i |,
$$
dove *λ*<sub>*i*</sub> sono gli autovalori di *A* e  i vettori |*i*⟩ formano una base ortonormale di *V*.
Ortonormale significa che:
$$
\left \langle i | j \right \rangle = \delta_{ij}.
$$
Un operatore è diagonalizzabile se rappresentabile in forma diagonale.
Rappresentaizoni diagonali sono chiamate anche *decomposizioni ortonormali*.
Se un eigenspace è multidimensionale, l'operatore non è diagonalizzabile, si dice che lo spazio è *degenere*.
##2.1.6 Adjoint e Operatori Hermitiani
Un operatore *A* è detto *hermitiano* se:
$$
A^{\dagger} = A.
$$
Un operatore hermitiano ha solo autovalori reali.
Un operatore *P* è detto di proiezione e serve a proiettare un vettore *v* su un sottospazio *W* di dimensione *n < m* di *V* di dimensione *m*.
In pratica data una base ortonormale di *W*, |1⟩, |2⟩, ..., |n⟩, la proiezione di *v* su *W* è data da:
$$
P = \sum_{i=1}^n | i \rangle \langle i |,
$$
Un operatore *A* è detto *normale* se commuta con il suo adjoint:
$$
AB = BA \Rightarrow A^{\dagger} B = B A^{\dagger}.
$$
Un operatore *A* è detto *unitario* se:
$$
A^{\dagger} A = I.
$$
##2.1.7 Prodotto tensoriale
Il prodotto tensoriale di due spazi vettoriali *V* e *W* è uno spazio vettoriale *V* ⊗ *W* di dimensione *n* × *m*.
Se ho una base ortonormale di *V* data da |1⟩, |2⟩, ..., |n⟩ e una base ortonormale di *W* data da |a⟩, |b⟩, ..., |m⟩, allora una base ortonormale di *V* ⊗ *W* è data da |1⟩ ⊗ |a⟩, |1⟩ ⊗ |b⟩, ..., |n⟩ ⊗ |a⟩, |n⟩ ⊗ |b⟩, ..., |n⟩ ⊗ |m⟩.
Il prodotto tensoriale di due operatori *A* e *B* è dato da:
$$
A \otimes B = \begin{pmatrix} A_{11} B & A_{12} B & \ldots & A_{1n} B \\ A_{21} B & A_{22} B & \ldots & A_{2n} B \\ \vdots & \vdots & \ddots & \vdots \\ A_{n1} B & A_{n2} B & \ldots & A_{nn} B \end{pmatrix}.
$$
#2.2 Postulati della meccanica quantistica
##2.2.1 Spazio di stato
**Postulato 1**: Associato ad un sistema fisico isolato c'è uno spazio vettoriale complesso con prodotto interno(di Hilbert) conosciuto come lo spazio di stato del sistema. Lo stato del sistema è descritto da un vettore unitario nello spazio di stato.

Il più semplice sistema in meccanica quantistica è il qubit. Un qubit è un sistema quantistico con due stati di base |0⟩ e |1⟩. Un qubit generico è dato da:
$$
| \psi \rangle = \alpha | 0 \rangle + \beta | 1 \rangle,
$$
dove *α* e *β* sono numeri complessi tali che |*α*|<sup>2</sup> + |*β*|<sup>2</sup> = 1.
Ogni combinaizone lineare $\sum_{i=1}^n \alpha_i | \psi \rangle$ è una superposizione di stati $| \psi_i \rangle$ con ampiezze $\alpha_i$.
##2.2.2 Evoluzione temporale
**Postulato 2**: l'evoluzione di un sistema quantistico chiuso è descritta da una trasformazione unitaria. Cioè, il vettore di stato $| \psi \rangle$ di un sistema al tempo $t_1$ è legato al vettore di stato $| \psi\prime \rangle$ al tempo $t_2$ da un operatore unitario *U* che dipende solo da $t_1$ e $t_2$:
$$
| \psi\prime \rangle = U | \psi \rangle.
$$
**Postulato 2.1**: L'evoluzione temporale di un sistema quantistico è descritta dall'equazione di Schrödinger:
$$
i \hbar \frac{d}{dt} | \psi \rangle = H | \psi \rangle,
$$
dove *H* è l'operatore Hamiltoniano del sistema.
##2.2.3 Misura
**Postulato 3**: Le misurazioni quanistiche sono descritte da una collezione di operatori *M*<sub>*m*</sub> che agiscono sullo spazio di stato del sistema. Gli indici *m* etichettano i possibili esiti della misura. Se la misura restituisce il risultato *m*, lo stato del sistema subisce un collasso a:
$$
| \psi \rangle \rightarrow \frac{M_m | \psi \rangle}{\sqrt{\left \langle \psi | M_m^{\dagger} M_m | \psi \right \rangle}}.
$$
La probabilità che la misura restituisca il risultato *m* è data da:
$$
p(m) = \left \langle \psi | M_m^{\dagger} M_m | \psi \right \rangle.
$$
Gli operatori di misura devono soddisfare la condizione di completezza:
$$
\sum_m M_m^{\dagger} M_m = I.
$$
La condizione di completezza esprime che le probabilità di tutti i possibili risultati della misura devono sommare a 1.
$$
\sum_m p(m) = 1 = \sum_m \left \langle \psi | M_m^{\dagger} M_m | \psi \right \rangle.
$$
##2.2.4 Distinzione tra stati quantistici
