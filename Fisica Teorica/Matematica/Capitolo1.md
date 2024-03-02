##Funzioni complesse
### 1.1 Richiami sui numeri complessi
**Coordinate polari:** Sono collegate alle coordinate cartesiane tramite le relazioni:
$$x = \rho\cos(\theta) \\ y = \rho\sin(\theta)$$
Dove $\rho$ è il modulo del numero complesso e $\theta$ è l'argomento(o fase) del numero complesso.
$$\rho = |z| = \sqrt{x^2 + y^2} \\ \theta = arg z = \arctan\left(\frac{y}{x}+ 2k\pi\right)$$
Pertanto un numero complesso può essere scritto come:
$$z = x + iy = \rho(\cos(\theta) + i\sin(\theta))$$
Il numero complesso di argomento $arg z = \theta + 2k\pi$ è lo stesso di $z$ per ogni $k \in \mathbb{Z}$, per la periodicità di seno e coseno. 
Ricordando le espansioni in sere di Taylor di seno e coseno:
$$\cos(\theta) = \sum_{k=0}^{\infty}\frac{(-1)^k\theta^{2k}}{(2k)!} \\ \sin(\theta) = \sum_{k=0}^{\infty}\frac{(-1)^k\theta^{2k+1}}{(2k+1)!}$$
Entrambe convergenti su tutto $\mathbb{R}$ e ricordando che $(-1)^k = i^{2k}$, possiamo scrivere:
$$\cos(\theta) + i\sin(\theta) = \sum_{k=0}^{\infty}\bigg(\frac{(i\theta)^{2k}}{(2k)!} + \frac{(i\theta)^{2k+1}}{(2k+1)!}\bigg) = \sum_{k=0}^{\infty}\frac{(i\theta)^k}{k!} = e^{i\theta}$$
Quindi vale la formula di Eulero:
$$e^{i\theta} = \cos(\theta) + i\sin(\theta)$$
Che ci dice che ogni numero compesso può essere espresso in forma polare come:
$$z = \rho e^{i\theta} = |z|e^{iarg z}$$
Il suo complesso coniugato è:
$$z^* = x - iy = \rho(\cos(\theta) - i\sin(\theta)) = \rho e^{-i\theta}$$
Se $\theta \in \mathbb{R}$, allora:
$$|e^{i\theta}| = e^{i\theta}e^{-i\theta} = 1$$
Infatti:
$$|e^{i\theta}| = |(\cos(\theta) + i\sin(\theta))| = \sqrt{\cos^2(\theta) + \sin^2(\theta)} = 1$$
La forma cartesiana è più comoda per le operazioni algebriche, mentre la forma polare è più comoda per le operazioni di moltiplicazione e divisione. Infatti:
$$z_1z_2 = \rho_1e^{i\theta_1}\rho_2e^{i\theta_2} = \rho_1\rho_2e^{i(\theta_1 + \theta_2)} \\ \frac{z_1}{z_2} = \frac{\rho_1e^{i\theta_1}}{\rho_2e^{i\theta_2}} = \frac{\rho_1}{\rho_2}e^{i(\theta_1 - \theta_2)}$$

**Esercizio 1:** Si esprimano i seguenti numeri in forma cartesiana e polare:
1. $(2 + 3i)^3$
2. $(\frac{\sqrt{2}}{2}(1 + i))^{40}$
3. $(3 + i)^4$

Invertendo la formula di Eulero, possiamo scrivere:
$$\cos(\theta) = \frac{e^{i\theta} + e^{-i\theta}}{2} \\ \sin(\theta) = \frac{e^{i\theta} - e^{-i\theta}}{2i}$$
Da cui possiamo dedurre la formula di de Moivre:
$$(\cos(\theta) + i\sin(\theta))^n = e^{in\theta} = \cos(n\theta) + i\sin(n\theta)$$
Che ci permette di calcolare seni e coseni dei multipli di un angolo. Più in generale, l'espansione binomiale di $(a + b)^n$ è:
$$(a + b)^n = \sum_{k=0}^{n}\binom{n}{k}a^{k}b^{n - k}$$
Applicando la formula di de Moivre, possiamo scrivere:
$$(\cos(\theta) + i\sin(\theta))^n = \cos(n\theta) + i\sin(n\theta) = \sum_{k=0}^{n}\binom{n}{k}\cos^{k}(\theta)(i\sin(\theta))^{n - k}$$

**Esercizio 2:** Si calcoli, usando la formula di de Moivre, $\cos(3\theta)$ e $\sin(3\theta)$ in funzione di $\cos(\theta)$ e $\sin(\theta)$.

Il modulo permette di calcolare la distanza tra due punti del piano complesso:
$$|z_1 - z_2| = |(x_1 - x_2) + i(y_1 - y_2)| = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$$

### 1.2 Funzioni di variabile complessa
Si consideri un sottoinsieme $M \subset \mathbb{C}$. Una funzione complessa $f: M \rightarrow \mathbb{C}$ associa un numero $w \in \mathbb{C}$ ad un numero $z \in M$. Ponendo $z = x + iy$ e $w = u + iv$ possiamo scrivere:
$$f(z) = u(x, y) + iv(x, y)$$
Dove $u(x, y)$ e $v(x, y)$ sono funzioni reali di due variabili reali. Pertanto i concetti di limite e continuità sono derivati da quelli di funzione reale di due variabili reali.

**Definizione:** Sia $A \subset \mathbb{C}$ è detto *limite* di $f(z)$ per $z \rightarrow a \in \mathbb{C}$ se per ogni $\epsilon > 0$ esiste $\delta > 0$ tale che:
$$ 0 < |z - a| < \delta \Rightarrow |f(z) - A| < \epsilon$$
Con:
$$lim_{z \rightarrow a}f(z) = A \Leftrightarrow lim_{z \rightarrow a}Re(f(z)) = Re(A) \land lim_{z \rightarrow a}Im(f(z)) = Im(A)$$

**Definizione:** La funzione $f(z)$ è *continua* in *a* se:
$$lim_{z \rightarrow a}f(z) = f(a)$$
Le funzioni complesse sono definite generalizzando il caso reale. Per avere funzioni compleesse ben definite è necessario provare che le serie di potenze siano convergenti. Può essere dimostrato un criterio di convergenza di Cauchy per le serie di potenze.

**Teorema:** La successione delle ridotte di una serie è convergente se:
$$|S_{N} - S_{N - 1}| \leq \epsilon$$

**Esercizio 3:** La funzione esponenziale è definita come:
$$e^{x} = \sum_{n=0}^{\infty}\frac{x^n}{n!}$$
Per analogia, nel caso complesso, si definisce:
$$e^{z} = \sum_{n=0}^{\infty}\frac{z^n}{n!}$$
Si dimostri che la serie è convergente per ogni $z \in \mathbb{C}$.
Ovverosia che la successione delle ridotte è convergente.
$$|S_{N}(z) = \sum_{n=0}^{N}\frac{z^n}{n!} \rightarrow_{N \rightarrow \infty} e^{z} = w \in \mathbb{C}$$

### 1.3 Differenziabilità e Olomorifismo
Data che una funzione complessa è un caso particolare di una funzione $\mathbb{R}^2 \rightarrow \mathbb{R}^2$, si può definire un concetto di differenziabilità in $\mathbb{C}$ partendo da quello in $\mathbb{R}^2$. 

**Definizione:** Sia $\omega$ un aperto di $\mathbb{R}^2$ e sia $f(x,y)$ una funzione definita in $\omega$. La funzione $f(x,y)$ è *differenziabile* in $(x_0, y_0) \in \omega$ se esiste una forma lineare $\alpha\Delta x + \beta\Delta y$ detta differenziale tale che:
$$f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0) = \alpha\Delta x + \beta\Delta y + \omega(\Delta x, \Delta y)(\sqrt{\Delta x^2 + \Delta y^2})$$
Dove $\omega(\Delta x, \Delta y) \rightarrow 0$ per $\Delta x, \Delta y \rightarrow 0$. 
Se $f(x,y)$ è differenziabile in "$(x_0, y_0)$", allora esistono le derivate parziali:
$$\frac{\partial f}{\partial x}(x_0, y_0) = \alpha \\ \frac{\partial f}{\partial y}(x_0, y_0) = \beta$$
E scriviamo:
$$df_{(x_0, y_0)} = \frac{\partial f}{\partial x}(x_0, y_0)dx + \frac{\partial f}{\partial y}(x_0, y_0)dy$$
Nel caso complesso si definisce la differenziabilità in modo analogo, ma si richiede che la forma lineare sia lineare rispetto a $\Delta z = \Delta x + i\Delta y$.

**Definizione:** Olomorfismo. Una funzione su un aperto $D \subset \mathbb{C}$ è *olomorfa* in $z_0 \in D$ se è differenziabile in $z_0$, cioè se esiste $\gamma \in \mathbb{C}$ tale che:
$$f(z_0 + \Delta z) - f(z_0) = \gamma\Delta z + \omega(\Delta z)|\Delta z|$$
Con $\omega(\Delta z) \rightarrow 0$ per $\Delta z \rightarrow 0$. 
Che mi dice che $\alpha = \gamma$ e $\beta = i\gamma$.
Se $f(z)$ è olomorfa in $z_0$, allora esiste la derivata complessa:
$$\gamma = lim_{\Delta z \rightarrow 0}\frac{f(z_0 + \Delta z) - f(z_0)}{\Delta z} = \frac{\partial f}{\partial z}(z_0)$$
$z_0$ è detto *punto regolare* di $f(z)$. Se $f(z)$ è olomorfa in ogni punto di $D$, allora $f(z)$ è detta *olomorfa* in $D$. In tal caso $D$ è detto *dominio olomorfo*.
I punti non appartenenti a $D$ sono detti *punti singolari* di $f(z)$.

Da qui capiamo che ci sono condizioni aggiuntive a quelle del caso di $\mathbb{R}^2$ per la differenziabilità. Infatti, se $f(z)$ è olomorfa in $z_0$, allora $f(z)$ è continua in $z_0$. Infatti $\alpha = \frac{\partial f}{\partial x}(z_0) = \gamma$ e $\beta = \frac{\partial f}{\partial y}(z_0) = i\gamma$, sono dipendenti, overro:
$$\frac{\partial f}{\partial x}(z_0) = i\frac{\partial f}{\partial y}(z_0) = 0$$
Quindi se $f(z) = u(x,y) + iv(x,y)$:
$$\frac{\partial f}{\partial x}(z_0) = \frac{\partial u}{\partial x}(z_0) + i\frac{\partial v}{\partial x}(z_0) = 0 \\ \frac{\partial f}{\partial y}(z_0) = \frac{\partial u}{\partial y}(z_0) + i\frac{\partial v}{\partial y}(z_0) = 0$$
Che ci fa diventare la condizione di prima:
$$\frac{\partial u}{\partial x} + i\frac{\partial v}{\partial y} + i(\frac{\partial u}{\partial y} + i\frac{\partial v}{\partial x}) = (\frac{\partial u}{\partial x} - \frac{\partial v}{\partial y}) + i(\frac{\partial v}{\partial x} - \frac{\partial u}{\partial y}) = 0$$
Che è la condizione di Cauchy-Riemann:
$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y} \\ \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x}$$
Cerchiamo di capire meglio le condizioni facendo i cambiamenti di variabili $(x,y) \rightarrow (z, \bar{z})$:
$$z = x + iy \rightarrow x = \frac{z + \bar{z}}{2} \\ \bar{z} = x - iy \rightarrow y = \frac{z - \bar{z}}{2i}$$
E quindi:
$$\frac{\partial f}{\partial z} = \frac{\partial f}{\partial x}\frac{\partial x}{\partial z} + \frac{\partial f}{\partial y}\frac{\partial y}{\partial z} = \frac{1}{2}(\frac{\partial f}{\partial x} - i\frac{\partial f}{\partial y}) = \frac{\partial f}{\partial x} \\ \frac{\partial f}{\partial \bar{z}} = \frac{\partial f}{\partial x}\frac{\partial x}{\partial \bar{z}} + \frac{\partial f}{\partial y}\frac{\partial y}{\partial \bar{z}} = \frac{1}{2}(\frac{\partial f}{\partial x} + i\frac{\partial f}{\partial y}) = 0$$
QUindi $f(z)$ è olomorfa se $\frac{\partial f}{\partial \bar{z}} = 0$, perciò può dipendere solo da $z$ e non da $\bar{z}$.
In particolare $f(z) = \bar{z}$ e $f(z) = |z|$ non sono olomorfe.
Date due funzioni $f(z)$ olomorfa in un domnio $F$ e $g(z)$ olomorfa in un dominio $G$, utilizzando Cauchy-Riemann possiamo scrivere:
- $f(z) + g(z)$ è olomorfa in $F \cap G$
- $P(z) = f(z)g(z)$ è olomorfa in $F \cap G$
- il dominio di $P(z)$ è in alcuni casi più grande di $F \cap G$(per esempio se $f(z) = \frac{1}{z}$ e $g(z) = z$)
- se $f(z)$ è olomorfa in $F$, allora $\frac{1}{f(z)}$ è olomorfa in $F - \{z \in F | f(z) = 0\}$

**Esercizio 4:** Si dimostri che $f(z) = z^2$ è olomorfa in $\mathbb{C}$ e si calcoli la sua derivata.

### 1.4 Integrali nel piano complesso

