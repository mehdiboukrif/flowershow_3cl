---
dg-publish: true
dg-home: false
---

Données d'entrée principales :

Rendement de génération : $R g$ (sans dimension)

Rendement d'émission : Re (sans dimension)

Rendement de distribution : $R d$ (sans dimension)

Rendement de régulation : $\operatorname{Rr}$ (sans dimension)

Type d'installation de chauffage : avec ou sans solaire ; base + appoint...

Présence d'une ventouse (ou assistance par ventilateur) sur l'équipement

### 9.1 Installation de chauffage seule

Une installation de chauffage peut se composer d'un générateur ou de plusieurs générateurs couplés associés à un ou plusieurs émissions, régulations et distributions.

### 9.1.1 Consommation de chauffage

La consommation de chauffage est calculée pour une consigne de température à $19^{\circ} \mathrm{C}$ correspondant à un comportement conventionnel (ou $21^{\circ} \mathrm{C}$ pour un comportement dépensier).

Le besoin de chauffage sur le mois $\mathrm{j} \mathrm{Bch}_{\mathrm{j}}(\mathrm{kWh} \mathrm{PCl})$ est déterminé de la façon suivante :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-060.jpg?height=127&width=815&top_left_y=2375&top_left_x=626)

Avec :

- $B V_{j}$ : besoin de chauffage d'un logement par kelvin sur le mois $\mathrm{j}(W / K)$ (voir chapitre 2)
- $\mathrm{DH}_{\mathrm{j}}$ : degrés heures de chauffage sur le mois $\mathrm{j}\left({ }^{\circ} \mathrm{Ch}\right)$ (différents selon le comportement choisi) voir paragraphe 18.2 et 18.3
- $Q_{\text {rec_chauff_j }}$ : pertes récupérées de distribution d'ECS pour le chauffage sur le mois $\mathrm{j}$ (Wh)
- $Q_{g, w_{\_} \text {rec } \_j}$ : pertes récupérées de stockage d'ECS pour le chauffage sur le mois $\mathrm{j}(\mathrm{Wh})$
- $Q_{\text {gen_rec_j }}$ : pertes récupérées de génération pour le chauffage sur le mois $\mathrm{j}(\mathrm{Wh})$

Pertes récupérées de distribution d'ECS pour le chauffage sur le mois $\mathrm{j}(\mathrm{Wh})$ :

$$
Q_{\text {rec_chauff_j }}=0,48 * \text { Nref }_{j} * \frac{Q_{d, w \_ \text {ind }, v c_{\_} j}+Q_{d, w_{-} \text {col,vc_j }}}{8760}
$$

Avec :

- $Q_{d, w_{-} \text {ind, } v_{-j} j}$ : pertes de la distribution individuelle en volume chauffé pour le mois $\mathrm{j}$ (Wh) (voir paragraphe $15.2 .3)$
- $Q_{d, w_{-} \text {col,vc_j }}$ : pertes de la distribution collective en volume chauffé pour le mois $\mathrm{j}$ (Wh) (voir paragraphe 15.2.3) Pertes récupérées de stockage d'ECS pour le chauffage sur le mois $\mathrm{j}(\mathrm{Wh})$ :

$$
Q_{g, w_{\_} r e c \_j}=0,48 * N r e f_{j} * \frac{Q_{g, w}}{8760}
$$

Avec :

- $Q_{g, w}$ : pertes brutes annuelles de stockage (Wh) (voir paragraphe 14 ou 11.6)

Pertes récupérées de génération pour le chauffage sur le mois $j(W h):$

$$
Q_{\text {gen_rec_ } j}=0,48 * \text { Cper } * Q_{p 0} * \text { Dper }_{j}
$$

Avec :

- Cper : part des pertes par les parois égale à 0,75 pour les équipements à ventouse ou assistés par ventilateur et 0,5 pour les autres
- $Q_{p 0}:$ pertes à l'arrêt du générateur (W)
- $\quad$ Dper $_{j}:$ durée pendant laquelle les pertes sont récupérées sur le mois $\mathrm{j}(\mathrm{h}):$
- Pour les générateurs assurant le chauffage uniquement :

$$
\operatorname{Dper}_{j}=\min \left(N_{r e f} ; \frac{1,3 * B c h_{h p_{-}}}{0,3 * P n}\right)
$$

- Pour les générateurs assurant l'ECS uniquement :

$$
\text { Dper }_{j}=\text { Nref }_{j} * \frac{1790}{8760}
$$

- Pour les générateurs assurant le chauffage et l'ECS :

$$
\operatorname{Dper}_{j}=\min \left(N r e f_{j} ; \frac{1,3 * \text { Bch }_{h p_{-} j}}{0,3 * \text { Pn }}+\text { Nref }_{j} * \frac{1790}{8760}\right)
$$

Avec :

- $\quad P n:$ puissance nominale du générateur (W)
- $B c h_{h p_{-} j}:$ besoin de chauffage hors pertes récupérées sur le mois $j(k W h)$ :

$$
B c h_{h p_{-} j}=\frac{B V_{j} * D H_{j}}{1000}
$$

Avec :

- $\mathrm{BV}_{\mathrm{j}}$ : besoin de chauffage d'un logement par kelvin sur le mois $\mathrm{j}(\mathrm{W} / \mathrm{K})$ (voir chapitre 2)
- $\mathrm{DH}_{j}:$ degrés heures de chauffage pour le mois $\mathrm{j}\left({ }^{\circ} \mathrm{Ch}\right)$

Ce calcul ne s'applique qu'au générateur pour lesquels des pertes à l'arrêt $Q_{p 0}$ sont prises en compte.

Seules les pertes des générateurs et des ballons de stockage en volume chauffé sont récupérables. Les pertes récupérées des générateurs d'air chaud sont nulles.

Le besoin annuel de chauffage ( $B c h$ ) est égal à la somme des besoins mensuels $\left(B c h_{j}\right)$ sur la période de chauffe :

$$
B c h=\sum_{j} B c h_{j}
$$

Les performances des équipements étant données sur une saison de chauffe complète, il n'est donc possible de calculer la consommation de chauffage $\mathrm{Cch}$ ( $\mathrm{kWh} \mathrm{PCI}$ ) que sur la saison complète de chauffe (donc sur l'année).

Les émetteurs sont classables en plusieurs catégories selon leur place dans l'installation :

- Emetteurs de base qui sont ceux assurant la plus grande partie du chauffage ;
- Emetteurs d'appoint qui apportent un complément à la base
- Emetteurs de salle de bain qui gèrent le chauffage dans les salles de bains.


### 9.1.2 Installation classique

Ce cas correspond à une installation simple avec un unique rendement de génération, de distribution, d'émission et de régulation pour tout le bâtiment.

$$
\text { Cch }=\text { Bch } * \text { Ich } * \text { INT }
$$

Avec :

- Bch et Cch sont respectivement les besoins et consommations annuels de chauffage ( $\mathrm{kWh} \mathrm{PCl}$ )
- INT : Facte d d'intermittence
- Ich : Inverse du rendement de l'installation :

$$
\operatorname{Ich}=\left(\frac{1}{\operatorname{Rg} * \operatorname{Re} * \operatorname{Rd} * \operatorname{Rr}}\right)
$$

$\mathrm{Rg}, \mathrm{Re}, \mathrm{Rd}$ et $\mathrm{Rr}$ sont respectivement le rendement annuel conventionnel du générateur ou le coefficient de performance des pompes à chaleur (COP), le rendement d'émission, le rendement de distribution et le rendement de régulation.

L'émetteur dans ce cas est défini comme un émetteur de base.

### 9.1.3 Installation avec plusieurs émissions pour un même générateur

Ce cas correspond aux installations centralisées avec plusieurs émetteurs de types différents

Les consommations associées à ces installations sont :

$$
C c h=\sum_{i}\left(\frac{S h_{i}}{S h} * I N T_{i} * I c h_{i}\right) * B c h
$$

La part de la consommation traitée par chaque émetteur est proratisé par le ratio des surfaces habitables.

Par exemple, pour un générateur alimentant un plancher chauffant au rez-de-chaussée et des radiateurs en étage d'une habitation, il faut considérer une installation avec deux émetteurs et éventuellement deux régulations et distributions.

- Surface chauffée par l'émission 1 (installation 1 ) : $\operatorname{Sh} 1(\mathrm{~m} 2)$
- Surface chauffée par l'émission 2 (installation 2 ) : Sh2 (m2)

Soit dans notre cas :

$$
C c h=C c h 1+C c h 2
$$

Avec :

$$
\begin{aligned}
& C c h 1=\frac{S h 1}{S h} * B c h * I N T 1 * I c h 1 \\
& C c h 2=\frac{S h 2}{S h} * B c h * I N T 2 * I c h 2
\end{aligned}
$$

Avec :

$$
\begin{aligned}
& \mathrm{Ich} 1=\left(\frac{1}{\mathrm{Rg} * \mathrm{Re} 1 * \mathrm{Rd} * \mathrm{Rr} 1}\right) \\
& \mathrm{Ich} 2=\left(\frac{1}{\mathrm{Rg} * \mathrm{Re} 2 * \mathrm{Rd} * \mathrm{Rr} 2}\right)
\end{aligned}
$$

Dans cette configuration, tous les émetteurs sont définis en base car ils sont des émetteurs principaux du chauffage.

Les consommations sont mensualisées de la façon suivante :

$$
C c h_{j}=C c h * \frac{B c h_{j}}{B c h}
$$

$\mathrm{Cch}_{j}$ et $\mathrm{Bch}_{\text {j }}$ respectivement les consommations et besoins de chauffage sur le mois $\mathrm{j}$ ( $\mathrm{kWh} \mathrm{PCl}$ ).

### 9.1.4 Installation avec plusieurs générateurs pour une même émission

Notons qu'en présence de plusieurs émissions, les consommations assurées par chaque générateur dans ce paragraphe doivent être proratisées selon les règles du paragraphe précédent.

9.1.4.1 Installation de chauffage avec une chaudière ou une PAC en relève d'une chaudière bois

Cette installation correspond à une chaudière bois assurant principalement le chauffage sauf par temps doux ou en mi-saison où une PAC ou chaudière prend le relais de la chaudière bois.

La consommation annuelle de chauffage Cch1 liée à la chaudière bois ( $\mathrm{kWh} \mathrm{PCl}$ ) est donnée par la formule :

$$
\operatorname{Cch} 1=0,75 * B \operatorname{ch} * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage Cch2 liée à la PAC ou chaudière (kWh PCI) est donnée par la formule :

$$
\text { Cch } 2=0,25 * B \operatorname{ch} * I N T 2 * I \operatorname{ch} 2
$$

Dans cette configuration, les générateurs sont multiples et couplés, les émetteurs sont de base et peuvent aussi être multiples.

### 9.1.4.2 Installation de chauffage avec chaudière en relève de PAC

Cette installation correspond à une PAC assurant principalement le chauffage sauf par temps de grand froid où la PAC s'arrête pour laisser le relais à la chaudière.

La consommation annuelle de chauffage Cch1 liée à la PAC (kWh PCI) est donnée par la formule :

$$
\operatorname{Cch} 1=0,8 * B \operatorname{ch} * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage liée à la chaudière (kWh PCI) est donnée par la formule :

$$
\operatorname{Cch} 2=0,2 * B \operatorname{ch} * I N T 2 * I \operatorname{ch} 2
$$

Dans cette configuration, les générateurs sont multiples et couplés, les émetteurs sont de base et peuvent aussi être multiples.

### 9.1.4.3 Les pompes à chaleur hybrides

Une pompe à chaleur (PAC) hybride est l'association d'une chaudière à condensation (gaz ou fioul) et d'une PAC air/eau ou eau/eau. Le système de régulation permet selon les conditions climatiques de produire la chaleur avec le générateur le plus performant. La modélisation choisie pour la PAC hybride correspond à une gestion des besoins de chauffage du bâtiment selon la répartition suivante entre les deux systèmes :

| \% du besoin de chauffage assuré par chaque équipement |  |  |
| :---: | :---: | :---: |
| Zone | PAC | Chaudière |
| H1 | 80 | 20 |
| H2 | 83 | 17 |
| H3 | 88 | 12 |

61

Annexe 1 - Méthode de calcul 3CL-DPE 2021

La fourniture d'ECS est considérée assurée à $100 \%$ par la chaudière.

Dans cette configuration, tous les émetteurs associés au générateur sont de base.

### 9.2 Installation de chauffage avec du chauffage solaire

Cette installation est valable seulement pour les maisons individuelles. Une partie de l'énergie destinée au chauffage est apportée par une installation de panneaux solaires thermiques.

La consommation de chauffage annuelle ( $\mathrm{kWh} \mathrm{PCl}$ ) s'exprime donc de la manière suivante :

$$
C c h=B c h * I N T *(1-F c h) * I c h
$$

Avec :

- Bch le besoin annuel de chauffage ( $\mathrm{kWh} \mathrm{PCl}$ )
- Fch : facteur de couverture solaire pour le chauffage, déterminé à partir du tableau du paragraphe 18.4
- Ich : Inverse du rendement de l'installation

Dans cette configuration, tous les émetteurs sont définis en base car ils sont des émetteurs principaux du chauffage. L'appoint apporté par le solaire se fait en amont de l'émission.

En présence de plusieurs générateurs et émetteurs, la part de la consommation de chauffage assurée par l'installation est calculée en appliquant les règles du paragraphe 9.1.

En présence de plusieurs émissions, les consommations assurées par chaque générateur dans ce paragraphe doivent être proratisées selon les règles du paragraphe 9.1.3.

### 9.3 Installation de chauffage avec insert ou poêle bois en appoint

Configuration correspondant à un insert ou à un poêle en appoint dans le logement en plus d'un système principal chauffant tout le logement. Cela signifie que le chauffage principal peut assurer $100 \%$ du besoin mais qu'il y a un poêle ou un insert à la place du système principal qui est de temps en temps utilisé dans l'habitation (en mi-saison par exemple).

La consommation annuelle de chauffage Cch1 liée au système principal de chauffage ( $\mathrm{kWh} \mathrm{PCI}$ ) est donnée par la formule :

$$
C c h 1=0,75 * B c h * I N T 1 * I \operatorname{ch} 1
$$

En présence de plusieurs générateurs et émetteurs, la part de la consommation de chauffage assurée par l'installation est calculée en appliquant les règles du paragraphe 9.1.

La consommation annuelle de chauffage Cch2 liée à l'insert ou au poêle (kWh PCI) est donnée par la formule :

$$
C c h 2=0,25 * B c h * I N T 2 * I c h 2
$$

Avec :

- $\quad \mathbf{I c h}_{i}$ : inverse du rendement de l'installation alimentée par l'équipement i (voir partie 9.1)

L'émetteur de base dans ce cas est celui associé au chauffage principal. Il peut être associé à une installation centralisée (planchers chauffants, radiateurs, bouches de soufflage...) ou à une installation divisée (effet joules, radiateurs gaz...). L'émetteur traité en appoint est le poêle bois ou l'insert.

Le poêle bois ou l'insert peuvent être traités en émetteur de base dans les situations où ce sont les seuls équipements de chauffage du local.

### 9.4 Installation de chauffage par insert, poêle bois (ou biomasse) avec un chauffage électrique dans la salle de bains

Dans cette configuration, valable que pour les maisons individuelles, tout le bâtiment est chauffé par un poêle bois. Seule la salle de bains est chauffée par un système électrique.

La consommation annuelle de chauffage Cch1 liée au poêle bois ( $(\mathrm{WWh} \mathrm{PCI}$ ) est donnée par la formule :

$$
C \operatorname{ch} 1=0,9 * B c h * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage Cch2 liée au chauffage électrique de la salle de bains (kWh PCI) est donnée par la formule :

$$
C c h 2=0,1 * B c h * I N T 2 * I \operatorname{ch} 2
$$

L'émetteur poêle bois ou insert est traité ici comme un émetteur de base. Le chauffage électrique dans la salle de bain est saisi comme un émetteur de SDB. En présence de plusieurs salles de bain avec un chauffage électrique différent, la part de la consommation apportée par l'appoint est répartie entre les deux équipements par un prorata de surface habitable. C'est-à-dire pour le cas d'un logement avec deux salles de bains de surface $S_{\mathrm{sdbb}_{1}}$ et $\mathrm{Sh}_{\mathrm{sdb} 2}$ :

$$
\begin{aligned}
& C c h 2_{s b d 1}=0,1 * \frac{S h_{s d b 1}}{S h_{s d b 1}+S h_{s d b 2}} * B c h * I N T_{s d b 1} * I c h_{s d b 1} \\
& C c h 2_{s b d 2}=0,1 * \frac{S h_{s d b 2}}{S h_{s d b 1}+S h_{s d b 2}} * B c h * I N T_{s d b 2} * I c h_{s d b 2}
\end{aligned}
$$

Avec :

$$
C c h 2=C c h 2_{s d b 1}+C c h 2_{s d b 2}
$$

### 9.5 Installation de chauffage avec en appoint un insert ou poêle bois et un chauffage électrique dans la salle de bains (différent du chauffage principal)

Configuration, valable que pour les maisons individuelles, correspond à un insert ou à un poêle en appoint dans le logement en plus d'un système principal qui chauffe presque tout le logement. La salle de bains est chauffée uniquement par un équipement électrique.

La consommation annuelle de chauffage Cch1 liée au système principal de chauffage ( $\mathrm{kWh} \mathrm{PCI}$ ) est donnée par la formule:

$$
C \operatorname{ch} 1=0,75 * 0,9 * B \operatorname{ch} * I N T 1 * I \operatorname{ch} 1
$$

En présence de plusieurs générateurs et émetteurs, la part de la consommation de chauffage assurée par l'installation est calculée en appliquant les règles du paragraphe 9.1.

La consommation annuelle de chauffage Cch2 liée à l'insert ou au poêle bois ( $\mathrm{kWh} \mathrm{PCl}$ ) est donnée par la formule :

$$
C \operatorname{ch} 2=0,25 * 0,9 * B \operatorname{ch} * I N T 2 * I \operatorname{ch} 2
$$

La consommation annuelle de chauffage Cch3 liée au chauffage électrique de la salle de bains ( $\mathrm{kWh} \mathrm{PCl}$ ) est donnée par la formule :

$$
\text { Cch3 }=0,1 * B c h * I N T 3 * I \operatorname{ch} 3
$$

L'émetteur de base dans ce cas est celui associé au chauffage principal. Il peut être associé à une installation centralisée (planchers chauffants, radiateurs, bouches de soufflage...) ou à une installation divisée (effet joules, radiateurs gaz...). L'émetteur traité en appoint est le poêle bois ou l'insert. Le chauffage électrique dans la salle de bain est saisi comme un émetteur de salle de bain.

En présence de plusieurs salles de bain avec un chauffage électrique différent, la part de la consommation apportée par l'appoint est répartie entre les deux équipements par un prorata de surface habitable.

### 9.6 Installation de chauffage avec chauffage solaire et insert ou poêle bois en appoint

Cette configuration, valable seulement pour les maisons individuelles, correspond à un insert ou à un poêle en appoint dans le logement en plus d'un système général composé d'un équipement principal accompagné par du chauffage solaire chauffant presque tout le logement.

La consommation annuelle de chauffage Cch1 liée au système principal de chauffage ( $\mathrm{kWh} \mathrm{PCI}$ ) est donnée par la formule :

$$
\text { Cch } 1=0,75 * B c h * I N T 1 *(1-F c h) * I c h 1
$$

En présence de plusieurs générateurs et émetteurs, la part de la consommation de chauffage assurée par l'installation est calculée en appliquant les règles du paragraphe 9.1.

La consommation annuelle de chauffage Cch2 liée à l'insert ou au poêle bois (kWh PCI) est donnée par la formule :

$$
C c h 2=0,25 * B c h * I N T 2 *(1-F c h) * I c h 2
$$

La production annuelle de chauffage solaire Prod $_{\text {chauff_sol }}(\mathrm{kWh} \mathrm{PCI})$ est donnée par la formule :

$$
\text { Prod }_{\text {chauff_sol }}=B c h * F c h *(0,75 * I N T 1 * I c h 1+0,25 * I N T 2 * I c h 2)
$$

L'émetteur traité en appoint est le poêle bois ou l'insert.

### 9.7 Installation de chauffage avec chaudière en relève de PAC avec insert ou poêle bois en appoint

Cette installation correspond à une PAC assurant principalement le chauffage sauf par temps de grand froid où la PAC s'arrête pour laisser le relais à la chaudière. Dans le bâtiment, il y a un poêle bois ou un insert qui est utilisé de temps en temps en remplacement du système principal.

La consommation annuelle de chauffage liée à la PAC (kWh PCI) est donnée par la formule :

$$
\operatorname{Cch} 1=0,8 * 0,75 * B c h * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage liée à la chaudière (kWh PCI) est donnée par la formule :

$$
C \operatorname{ch} 2=0,2 * 0,75 * B \operatorname{ch} * I N T 2 * I \operatorname{ch} 2
$$

La consommation annuelle de chauffage lié à l'insert ou au poêle en appoint ( $\mathrm{kWh} \mathrm{PCl}$ ) est donnée par la formule :

$$
\operatorname{Cch} 3=0,25 * B c h * I N T 3 * I \operatorname{ch} 3
$$

Dans cette configuration, les générateurs sont multiples et couplés, les émetteurs sont de base et peuvent aussi être multiples.

L'émetteur traité en appoint est le poêle bois ou l'insert.

En présence de plusieurs générateurs et émetteurs, la part de la consommation de chauffage assurée par l'installation est calculée en appliquant les règles du paragraphe 9.1.

### 9.8 Installation de chauffage collectif avec base + appoint

La base fonctionne seule tant que la température extérieure est supérieure à une température de dimensionnement $\mathrm{T}\left({ }^{\circ} \mathrm{C}\right)$. A cette température $\mathrm{T}$, le besoin instantané du bâtiment est égal à la puissance utile du générateur en base :

$$
T=14-\frac{P e * D H 14}{B c h}
$$

Avec :

- DH14 : degrés heures de base 14 sur la saison de chauffe complète ( ${ }^{\circ} \mathrm{Ch}$ ) (voir paragraphes 18.2 et 18.3)
- $\quad \mathrm{Pe}:$ puissance émise utile par le générateur en base $(\mathrm{kW})$ :

$$
P e=P n * R d * R r * R e
$$

Avec :

- Pn : puissance nominale du générateur en base (kW)
- $\mathrm{Rd}, \mathrm{Rr}$ et $\mathrm{Re}$ : respectivement les rendements annuels de distribution, de régulation et d'émission de l'installation de chauffage de base

Le besoin de chauffage assuré par la base Bch_base ( $_{\text {( }}$ Whef) est calculé pour le mois j par :

$$
\text { Bch_base }_{j}=B c h_{j} *\left(1-\frac{D H T_{j}}{D H 14_{j}}\right)
$$

Avec :

- $\mathrm{DHT}_{\mathrm{j}}$ : degré heure base $\mathrm{T}$ sur le mois $\mathrm{j}$

$$
D H T_{j}=\text { Nref }_{j} *\left(\text { Text }_{j}-\text { Tbase }\right) * X_{j}^{5} *\left(14-28 * X_{j}+20 * X_{j}^{2}-5 * X_{j}^{3}\right)
$$

Avec :

$$
X_{j}=0,5 * \frac{T-\text { Tbase }}{\text { Text }_{j}-\text { Tbase }}
$$

- Nref $f_{j}$ : Nombre d'heures de chauffage sur le mois $\mathrm{j}$
- Tbase : Température extérieure de base dans la zone climatique $\left({ }^{\circ} \mathrm{C}\right)$
- Text $\mathrm{T}_{\mathrm{j}}:$ Température extérieure moyenne dans la zone climatique sur le mois $\mathrm{j}\left({ }^{\circ} \mathrm{C}\right)$

Le besoin annuel est la somme des besoins mensuels :

$$
\text { Bch_base }=\sum_{j} \text { Bch_base }_{j}
$$

La consommation annuelle de chauffage Cch1 liée à la base (kWhef PCI) est :

$$
\text { Cch1 }=\text { Bch_base } * I N T 1 * I c h 1
$$

La consommation annuelle de chauffage Cch2 liée à l'appoint (kWhef $\mathrm{PCl}$ ) est :

$$
\text { Cch2 } 2=(\text { Bch }- \text { Bch_base }) * I N T 2 * \text { Ich } 2
$$

L'appoint est supposé être dimensionné pour assurer $50 \%$ du besoin.

La base constitué d'un ou plusieurs générateurs collectifs associés à un ou plusieurs émetteurs peut correspondre à I'une des installations décrite dans ce paragraphe 9.

L'appoint constitué d'un ou plusieurs générateurs individuels associés à un ou plusieurs émetteurs peut correspondre à l'une des installations décrite dans ce paragraphe 9 .

### 9.9 Convecteur bi-jonction

La base et l'appoint sont assurés par un même convecteur disposant d'un circuit collectif alimentant la base et un circuit individuel pour l'appoint.

La consommation annuelle de chauffage Cch1 liée au circuit collectif assurant la base ( $\mathrm{WWh} \mathrm{PCI}$ ) est donnée par la formule :

$$
C c h 1=0,6 * B c h * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage Cch2 liée au circuit individuel assurant l'appoint ( $\mathrm{kWh} \mathrm{PCI}$ ) ) est donnée par la formule :

$$
\text { Cch2 }=0,4 * B c h * I N T 2 * I \operatorname{ch} 2
$$

### 9.10 Chauffage avec plusieurs installations différentes et indépendantes et/ou plusieurs installations différentes et indépendantes couplées

Une installation de chauffage correspond à un générateur avec les émissions, distributions et régulations associées.

Surface chauffée par l'installation $1: \operatorname{Sh} 1(\mathrm{~m} 2)$

Surface chauffée par l'installation $3: \operatorname{Sh} 3(\mathrm{~m} 2)$

Surface chauffée par l'installation $5:$ Sh5 (m2)
Surface chauffée par l'installation $2: \operatorname{Sh} 2(\mathrm{~m} 2)$

Surface chauffée par l'installation $4: \operatorname{Sh} 4(\mathrm{~m} 2)$

Surface chauffée par l'installation $6:$ Sh6 $(\mathrm{m} 2)$

Surface chauffée par l'installation i : Shi (m2) (la saisie de 6 installations minimum doit être possible)

Les consommations associées à ces installations sont :

$$
C c h=\sum_{i}\left(\frac{S h_{i}}{S h} * I N T_{i} * I c h_{i}\right) * B c h
$$

Soit dans notre cas :

$$
\begin{array}{lll}
C c h 1=\frac{S h 1}{S h} * B c h * I N T 1 * I c h 1 & C c h 2=\frac{S h 2}{S h} * B c h * I N T 2 * I c h 2 & C c h 3=\frac{S h 3}{S h} * B c h * I N T 3 * I c h 3 \\
C c h 4=\frac{S h 4}{S h} * B c h * I N T 4 * I c h 4 & C c h 5=\frac{\text { Sh } 5}{S h} * B c h * I N T 5 * I c h 5 & C c h 6=\frac{S h 6}{S h} * B c h * I N T 6 * I c h 6
\end{array}
$$

L'intermittence sera déterminée pour chaque installation i associée à la surface $\mathrm{Sh}_{\mathrm{j}}$.

Dans le cas particulier où plusieurs équipements différents cohabitent dans une même pièce, avec des caractéristiques différentes (c'est le cas parfois avec des émetteurs à effet joule ou des convecteurs et panneaux rayonnants ainsi que des PAC air/air) on notera :

Pour la pièce $j$ de surface $S h_{j}$ avec $N$ équipements de puissance $P_{i}$ (en $W$ ) la consommation devient :

$$
C c h_{j}=\sum_{i=1}^{N} \frac{P_{i}}{\sum_{i} P_{i}} * I c h_{i} * I N T_{i} * \frac{S h_{j}}{S h} * B c h
$$

Dans le cas où les puissances $\mathrm{P}_{\mathrm{i}}$ des équipements partageant la même pièce ne sont pas connues, la consommation devient :

$$
C c h_{j}=\sum_{i=1}^{N} \frac{1}{N} * I c h_{i} * I N T_{i} * \frac{S h_{j}}{S h} * B c h
$$

Dans cette configuration, tous les émetteurs associés aux différents générateurs sont de base.

### 9.11 Installation de chauffage avec un générateur bi-énergie

Pour les générateurs pouvant fonctionner avec deux énergies différentes (selon le choix de l'occupant), il est considéré que chaque énergie couvre $50 \%$ du besoin.

La consommation annuelle de chauffage Cch1 pour l'énergie 1 est donnée par la formule :

$$
C c h 1=0,5 * B c h * I N T 1 * I \operatorname{ch} 1
$$

La consommation annuelle de chauffage Cch2 pour l'énergie 2 est donnée par la formule :

$$
C \operatorname{ch} 2=0,5 * B \operatorname{ch} * I N T 2 * I \operatorname{ch} 2
$$

Dans cette configuration, tous les émetteurs associés au générateur sont de base.