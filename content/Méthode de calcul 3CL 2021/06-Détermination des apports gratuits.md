---
dg-publish: true
dg-home: false
---
## 6 Détermination des apports gratuits

### 6.1 Calcul de $F$

Données d'entrée :

Département

Altitude

$F_{j}$ est la fraction des besoins de chauffage du mois $\mathrm{j}$ couverts par les apports gratuits, elle s'exprime en fonction de l'inertie du bâtiment :

| Inertie              |         $\mathbf{F}_{\mathbf{j}}$         |
| :------------------- | :---------------------------------------: |
| Lourde / Très Lourde | $\frac{X_{j}-X_{j}^{3,6}}{1-X_{j}^{3,6}}$ |
| Moyenne              | $\frac{X_{j}-X_{j}^{2,9}}{1-X_{j}^{2,9}}$ |
| Légère               | $\frac{X_{j}-X_{j}^{2,5}}{1-X_{j}^{2,5}}$ |

Avec :

$$
X_{j}=\frac{A s_{j}+A i_{j}}{G V * D H_{j}}
$$

- GV : déperditions de l'enveloppe en W/K (calculées dans la partie 3)
$\mathrm{DH}_{\mathrm{j}}$ : degrés-heures de chauffage sur le mois $\mathrm{j}\left({ }^{\circ} \mathrm{Ch}\right)$, déterminés à partir des tableaux des paragraphes 18.2 et $18.3:$
- DH19 pour une consigne de chauffage à $19^{\circ} \mathrm{C}$ (comportement conventionnel)
- DH21 pour une consigne de chauffage à $21^{\circ} \mathrm{C}$ (comportement dépensier)

$A i_{j}$ : apports internes dans le logement sur le mois $\mathrm{j}(\mathrm{Wh}):$

Les apports internes de chaleur dus aux équipements prennent en compte l'ensemble des équipements «mobiliers» (cuisson, audiovisuel, informatique, lavage, froid, appareils ménagers). Pour distinguer le fonctionnement permanent du fonctionnement lié à l'occupation, on considère que la puissance de chaleur dégagée par l'ensemble des équipements est conventionnellement de :

- $5,7 \mathrm{~W} / \mathrm{m}^{2}$ en occupation hors période de sommeil
- $1,1 \mathrm{~W} / \mathrm{m}^{2}$ en inoccupation et pendant le sommeil

Le scénario conventionnel d'occupation hebdomadaire des logements est le suivant :

- De 0 h à 9 h et de 17 h à 24 h avec une période de sommeil allant de 0 h et de 6 h et de 22 h à $24 \mathrm{~h}$ les lundi, mardi, jeudi et vendredi
- De $0 \mathrm{~h}$ à $9 \mathrm{~h}$ et de $13 \mathrm{~h}$ à $24 \mathrm{~h}$ avec une période de sommeil allant de $0 \mathrm{~h}$ à $6 \mathrm{~h}$ et de $22 \mathrm{~h}$ à $24 \mathrm{~h}$ le mercredi
- De 0 h à $24 \mathrm{~h}$ les samedi et dimanche avec une période de sommeil allant de 0 h à $6 \mathrm{~h}$ et de $22 \mathrm{~h}$ à $24 \mathrm{~h}$

Soit sur une semaine :

- $132 \mathrm{~h}$ d'occupation dont $56 \mathrm{~h}$ de sommeil
- 36h d'inoccupation

Les apports internes moyens dus aux équipements sur une semaine type sont donc de $3,18 \mathrm{~W} / \mathrm{m}^{2}$.

À ces apports il faut ajouter :

- Ceux de l'éclairage, qui correspondent à une puissance moyenne de $1,4 \mathrm{~W} / \mathrm{m}^{2}$ en fonctionnement. Les apports d'éclairage sont des moyennes annuelles sur toutes les zones climatiques. Cette valeur est pondérée par le nombre d'heures moyen d'éclairage (voir paragraphe 16.1) sur l'année c'est-à-dire $2123 \mathrm{~h}$ sur $8760 \mathrm{~h}$.

Les apports moyens annuels d'éclairage correspondent donc à $1,4 * \frac{2123}{8760}=0,34 \mathrm{~W} / \mathrm{m}^{2}$.

- Ceux dus aux occupants : on considère un apport de chaleur de 90W par adulte équivalent (variable $N_{\text {adeq }}$ déterminée au paragraphe 11.1). Le nombre d'adultes équivalent est calculé en fonction de la surface habitable. Les apports de chaleur dus aux occupants sont donc à $90 * \mathrm{~N}_{\text {adeq }} * \frac{132}{7 * 24}$.

En période de chauffe :

Les apports internes sur le mois $\mathrm{j}$ (en Wh) en période de chauffe sont donc :

$$
A i_{j}=\left[(3,18+0,34) * S h+90 * \frac{132}{168} * N_{\text {adeq }}\right] * \text { Nref }_{j}
$$

- Sh : surface habitable du logement $\left(m^{2}\right)$
- $N_{\text {adeq }}$ : nombre d'adultes équivalent (voir paragraphe 11.1)
- Nref $\mathrm{f}_{\mathrm{j}}$ : nombre d'heures de chauffage pour le mois $\mathrm{j}$, déterminé à partir des tableaux des paragraphes 18.2 et 18.3 :
- $\operatorname{Nref}\left(19^{\circ} \mathrm{C}\right)$ pour une consigne de chauffage à $19^{\circ} \mathrm{C}$ (comportement conventionnel)
- $\operatorname{Nref}\left(21^{\circ} \mathrm{C}\right)$ pour une consigne de chauffage à $21^{\circ} \mathrm{C}$ (comportement dépensier)

Pour une année complète, Nref est évalué seulement sur la saison de chauffe avec :

$$
N r e f=\sum_{j} N r e f_{j}
$$

$\mathrm{As}_{j}$ : apports solaires sur le mois $\mathrm{j}$ durant la période de chauffe $(\mathrm{Wh})$ :

$$
A s_{j}=1000 * S s e_{j} * E_{j}
$$

En présence d'une véranda ou autre espace solarisé non chauffé, à ces apports solaires s'ajoutent ceux à travers cet espace. Le calcul des apports solaires à travers un espace solarisé non chauffé est détaillé au paragraphe 6.3.

- Sse $_{\mathrm{j}}$ : «Surface transparente sud équivalente » du logement, c'est-à-dire la surface de paroi, fictive, exposée au sud, totalement transparente et sans ombrage, qui provoquerait les mêmes apports solaires que les parois du logement, pour le mois $j\left(m^{2}\right)$ (voir partie 6.2)
- $\mathrm{E}_{\mathrm{i}}$ : ensoleillement reçu, sur le mois $\mathrm{j}$, par une paroi verticale orientée au sud en absence d'ombrage $\left(\mathrm{kWh} / \mathrm{m}^{2}\right)$


### En période de refroidissement :

De la même manière, les apports internes sur le mois $\mathrm{j}$ (en Wh) en période de refroidissement sont donc :

$$
A i_{-} f r_{j}=\left[(3,18+0,34) * S h+90 * \frac{132}{168} * N_{\text {adeq }}\right] * N r e f_{j}
$$

Avec :

- Nref $f_{j}$ : nombre d'heures de chauffage pour le mois j, déterminé à partir des tableaux des paragraphes 18.2 et $18.3:$
- Nref $\left(28^{\circ} \mathrm{C}\right)$ pour une consigne de refroidissement à $28^{\circ} \mathrm{C}$ (comportement conventionnel)
- $\operatorname{Nref}\left(26^{\circ} \mathrm{C}\right)$ pour une consigne de refroidissement à $26^{\circ} \mathrm{C}$ (comportement dépensier)

Pour une année complète, Nref est évalué seulement sur la saison de refroidissement avec :

$$
N r e f=\sum_{j} N r e f_{j}
$$

Les apports solaires sur le mois $\mathrm{j} \mathrm{As}_{-} \mathrm{fr}_{\mathrm{j}}$ (en Wh) durant la période de refroidissement sont :

$$
A s_{-} f r_{j}=1000 * S s e_{j} * E_{-} f r_{j}
$$

Avec :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-047.jpg?height=399&width=1752&top_left_y=2179&top_left_x=126)

Annexe 1 - Méthode de calcul 3CL-DPE 2021

### 6.2 Détermination de la surface Sud équivalente

Données d'entrée:

Inclinaison des baies (verticale, pente, horizontale)

Orientation des baies (Nord, Sud, Est, Ouest)

Position des baies en flanc de loggias

Nature des menuiseries (bois, $P V C$...)

Type de vitrage (Simple, double...)

Positionnement de la menuiserie (tunnel, nu intérieur...)

Type de masque

Masques proches (balcon, loggias...)

Masques lointains

Profondeur des masques proches (profondeur balcon)

Largeur des baies

Positionnement des masques (Nord, Sud...)

Angle de vue des masques lointains

Type de fenêtre ou de porte fenêtre (coulissante, battante, avec ou sans soubassement...)

La prise en compte des apports solaires exige à minima une saisie par façade des fenêtres du bâtiment. Le calcul de la surface sud équivalente se fait en sommant les valeurs de Sse pour chaque paroi vitrée i :

$$
S_{s e_{j}}=\sum_{i} A_{i} * S w_{i} * F e_{i} * C 1_{i, j}
$$

Avec :

- $A_{i}:$ surface de la baie $\mathrm{i}\left(\mathrm{m}^{2}\right)$
- $S w_{i}$ : proportion d'énergie solaire incidente qui pénètre dans le logement par la paroi vitrée i
- $F e_{i}$ : facteur d'ensoleillement, qui traduit la réduction d'énergie solaire reçue par une paroi vitrée du fait des masques
- $C 1_{i, j}$ : coefficient d'orientation et d'inclinaison pour la paroi vitrée i pour le mois j, voir paragraphe 18.5

La surface vitrée des portes n'est pas prise en compte dans le calcul de Sse $_{\mathrm{j}}$.

### 6.2.1 Détermination du facteur solaire

La proportion d'énergie solaire incidente qui pénètre dans le logement à travers une paroi est donnée par :

- Pour les parois en polycarbonate $: S w=0,4$
- Pour les parois en brique de verre pleine ou creuse : $S w=0,4$
- Pour les doubles-fenêtres composées de deux fenêtres de facteur solaire Sw1 et Sw2, le facteur solaire de la double-fenêtre est : $S w=S w 1 * S w 2$
- Dans le cas d'un survitrage, on prendra en compte le Sw du double vitrage équivalent.

Si les facteurs solaires des menuiseries sont connus et justifiés, les saisir directement. Sinon, les tableaux suivants donnent des valeurs par défaut des facteurs solaires en fonction des caractéristiques des menuiseries :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-049.jpg?height=1427&width=1807&top_left_y=660&top_left_x=250)

|  | Sw | Fenêtr | ou por | fenêtre : <br> tunne | u nu int | rieur ou en |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Menuiserie | Type de fenêtre | Simple <br> vitrage | Double <br> vitrage | Double <br> vitrage <br> VIR | Triple <br> vitrage | Triple <br> vitrage VIR |
|  |  |  |  |  |  |  |
|  | Fenêtre battante | 0,52 | 0,47 | 0,40 | 0,41 | 0,37 |
|  | Fenêtre coulissante | 0,52 | 0,47 | 0,40 | 0,41 | 0,37 |
| BoIs / Bois- <br> métal | Porte-fenêtre battante ou coulissante sans <br> soubassement | 0,56 | 0,50 | 0,43 | 0,44 | 0,40 |
|  | Porte-fenêtre battante avec soubassement | 0,48 | 0,43 | 0,37 | 0,38 | 0,34 |
|  |  |  |  |  |  |  |
|  | Fenêtre battante | 0,49 | 0,44 | 0,38 | 0,39 | 0,35 |
|  | Porte-fenêtre battante sans soubassement | 0,51 | 0,46 | 0,39 | 0,40 | 0,36 |
| PVC | Porte-fenêtre battante avec soubassement | 0,45 | 0,40 | 0,35 | 0,36 | 0,32 |
|  | Fenêtre coulissante | 0,54 | 0,48 | 0,41 | 0,43 | 0,38 |
|  | Porte-fenêtre coulissante | 0,57 | 0,51 | 0,44 | 0,45 | 0,41 |
| Métal avec | Fenêtre battante | 0,53 | 0,48 | 0,41 | 0,42 | 0,38 |
| rupture de | Porte-fenêtre battante | 0,56 | 0,51 | 0,44 | 0,45 | 0,40 |
| pont | Fenêtre coulissante | 0,58 | 0,52 | 0,45 | 0,46 | 0,42 |
| thermique | Porte-fenêtre coulissante | 0,63 | 0,56 | 0,48 | 0,50 | 0,45 |
|  |  |  |  |  |  |  |
|  | Fenêtre battante | 0,55 | 0,49 | 0,43 | 0,44 | 0,40 |
| HN | Porte-fenêtre battante | 0,58 | 0,52 | 0,45 | 0,46 | 0,42 |
| Nitetal | Fenêtre coulissante | 0,60 | 0,54 | 0,47 | 0,48 | 0,43 |
|  | Porte-fenêtre coulissante | 0,64 | 0,57 | 0,49 | 0,51 | 0,46 |

### 6.2.2 Détermination du facteur d'ensoleillement

On considère successivement les obstacles liés au bâtiment (balcons, loggias, avancées, ...) et les obstacles liés à I'environnement (autres bâtiments, reliefs, végétation, ...). On obtient ainsi deux coefficients, Fe1 et Fe2, dont on fait le produit, soit :

$$
F e=F e 1 * F e 2
$$

En l'absence d'obstacles liés au bâtiment et pour les configurations non présentées ci-dessous, Fe1 = 1;

En l'absence d'obstacles liés à l'environnement, $\mathrm{Fe} 2=1$;

Conventionnellement, les orientations Nord, Sud, Est et Ouest correspondent aux secteurs situés de part et d'autre de ces orientations dans un angle de $45^{\circ}$. Pour respectivement le Nord et le Sud, les orientations incluent les limites NordEst, Nord-Ouest et Sud-Est, Sud-Ouest.

### 6.2.2.1 Masques proches

### 6.2.2.1.1 Baie en fond de balcon ou fond et flanc de loggias

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-051.jpg?height=386&width=1334&top_left_y=471&top_left_x=386)

Configuration du masque

Le tableau ci-dessous donne les valeurs de Fe1 en fonction de l'orientation de la façade et de l'avancée I de la loggia ou du balcon :

|  | Orientation de la façade |  |  |
| :---: | :---: | :---: | :---: |
| Avancée I $(\mathrm{m})$ | Nord | Sud | Est ou Ouest |
| $<1$ | 0,4 | 0,5 | 0,45 |
| $1 \leq \ldots<2$ | 0,3 | 0,4 | 0,35 |
| $2 \leq \ldots<3$ | 0,2 | 0,3 | 0,25 |
| $3 \leq$ | 0,1 | 0,2 | 0,15 |

L'orientation Nord va du Nord-Est au Nord-Ouest bornes comprises.

L'orientation Sud va du Sud-Est au Sud-Ouest bornes comprises.

L'orientation Est va du Nord-Est au Sud-Est bornes exclues.

L'orientation Ouest va du Nord-Ouest au Sud-Ouest bornes exclues.

### 6.2.2.1.2 Baie sous un balcon ou auvent

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-051.jpg?height=494&width=363&top_left_y=1832&top_left_x=869)

Le tableau ci-dessous donne les valeurs de Fe1 quelle que soit l'orientation de la façade en fonction de l'avancée I.

| Avancée $\mathrm{I}(\mathrm{m})$ | Fe1 |
| :---: | :---: |
| $<1$ | 0,8 |
| $1 \leq \ldots<2$ | 0,6 |
| $2 \leq \ldots<3$ | 0,5 |
| $\geq 3$ | 0,4 |

6.2.2.1.3 Baie masquée par une paroi latérale

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-052.jpg?height=462&width=642&top_left_y=657&top_left_x=707)

Configuration du masque

Une paroi latérale est considérée faire obstacle si les angles $\beta$ et $\gamma$ sont supérieurs à $30^{\circ}$. Les angles sont pris au centre des baies.

Le tableau ci-dessous donne les valeurs de Fe1 selon la position de l'obstacle latéral :

| Le retour ne fait pas obstacle au Sud | 0,7 |
| :---: | :---: |
| Le retour fait obstacle au Sud | 0,5 |

Attention : en présence de plusieurs types de masques proches, seul l'impact du masque le plus pénalisant est pris en compte.

### 6.2.2.2 Masques lointains

### 6.2.2.2.1 Obstacle d'environnement homogène

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-052.jpg?height=509&width=642&top_left_y=1847&top_left_x=707)

Configuration du masque

Les masques lointains s'appliquent à toute une façade. Les angles sont mesurés à partir du centre de la façade.

49

Annexe 1 - Méthode de calcul 3CL-DPE 2021

Le tableau ci-dessous donne les valeurs de Fe2 selon la hauteur du masque et l'orientation de la façade :

|  | Orientation de la façade |  |  |
| :---: | :---: | :---: | :---: |
| Hauteur $\alpha\left({ }^{\circ}\right)$ | Sud | Est ou Ouest | Nord |
| $<15$ | 1 | 1 | 1 |
| $15 \leq \ldots<30$ | 0,8 | 0,77 | 0,82 |
| $30 \leq \ldots<60$ | 0,3 | 0,4 | 0,5 |
| $60 \leq \ldots<90$ | 0,1 | 0,2 | 0,3 |

### 6.2.2.2.2 Obstacle d'environnement non homogène

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-053.jpg?height=346&width=962&top_left_y=818&top_left_x=547)

Configuration du masque

$$
F e 2=1-\sum \frac{O m b}{100}
$$

Avec :

- Omb :l'ombrage créé par l'obstacle sur la paroi

La méthode d'évaluation est la suivante :

1. on découpe le champ de vision en quatre secteurs égaux ;
2. on détermine, pour chacun d'eux, la hauteur moyenne des obstacles ;
3. on lit dans le tableau ci-dessous les valeurs correspondantes de l'ombrage, Omb :

|  | Façade au Sud ou Nord |  | Façade Est ou Ouest |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Hauteur moyenne de <br> l'obstacle $\alpha, \beta\left({ }^{\circ}\right)$ | Pour les 2 <br> secteurs latéraux | Pour les 2 secteurs <br> centraux | Pour le secteur <br> latéral vers le sud | Pour le secteur <br> central vers le sud | Pour les 2 autres <br> secteurs |
| $<15$ | 0 | 0 | 0 | 0 | 0 |
| $15 \leq \ldots .<30$ | 4 | 14 | 14 | 17 | 5 |
| $30 \leq \ldots .<60$ | 13 | 35 | 27 | 40 | 17 |
| $60 \leq \ldots .<90$ | 15 | 40 | 30 | 45 | 25 |

Les masques lointains sont évalués au niveau de la baie la plus proche du centre de la façade avant de s'appliquer à toutes les baies de cette façade.

### 6.3 Traitement des espaces tampons solarisés

Un logement donnant sur un espace tampon solarisé (véranda, loggia fermée) est influencé dans son bilan énergétique par les apports solaires. Il en existe deux types :

- Les apports solaires indirects qui sont associés au rayonnement solaire qui rentre dans le logement après de multiples réflexions dans l'espace tampon solarisé
- Les apports solaires directs qui sont associés au rayonnement solaire qui rentre directement dans le logement après avoir traversé l'espace tampon solarisé pour pénétrer dans le logement (en direct ou diffus).

Les apports solaires à travers un espace tampon solarisé sont donnés sur un mois j par :

$$
A s_{\text {ver }_{j}}=1000 * \text { Sse }_{\text {veranda }, j} * E_{j}
$$

Avec :

- $\mathrm{E}_{\mathrm{j}}$ : ensoleillement reçu par une paroi verticale orientée au sud en l'absence d'ombrage sur le mois $\mathrm{j}\left(\mathrm{kWh} / \mathrm{m}^{2}\right)$, déterminé à partir des tableaux des paragraphes 18.2 et 18.3
- Dans le cas de baies vitrées séparant l'espace tampon solarisé de la partie habitable du logement, l'impact de l'espace tampon solarisé sur les apports solaires à travers ces baies vitrées est modélisé par une surface sud équivalente pour le mois $j$ Sse $_{\text {veranda } j}$ :

$$
\text { Sse }_{\text {veranda }, j}=\text { Ssd }_{j}+\text { Ssind }_{j} * b_{v e r}
$$

- Ssd : Surface sud équivalente représentant l'impact des apports solaires associés au rayonnement solaire traversant directement l'espace tampon pour arriver dans la partie habitable du logement (apports directs) :

$$
S s d_{j}=T * \sum_{i} A_{i} * S w_{i} * F e_{i} * C 1_{i, j}
$$

Avec :

- $A_{i}:$ Surface de la baie i séparant le logement de l'espace tampon solarisé $\left(m^{2}\right)$
- $S w_{i}$ : Facteur solaire de la baie i séparant le logement de l'espace tampon solarisé
- $F e_{i}$ : Facteur d'ensoleillement, qui traduit la réduction d'énergie solaire reçue par la baie i du fait des masques (la présence de l'espace tampon solarisé n'est pas prise en compte pour déterminer ce coefficient)
- $C 1_{i, j}$ : Coefficient d'orientation et d'inclinaison de la baie i séparant le logement de l'espace tampon solarisé pour le mois j, voir paragraphe 18.5
- $\mathrm{T}$ : Coefficient représentant la transparence de l'espace tampon solarisé. II correspond à l'atténuation du rayonnement solaire arrivant directement dans le logement par la traversée de l'espace tampon solarisé. Il prend les valeurs du tableau suivant selon les caractéristiques des parois vitrées de l'espace tampon solarisé :

| Menuiserie | Type de Vitrage | Transparence T |
| :---: | :--- | :---: |
| Bois / Bois métal | 0,62 |  |
|  | Simple vitrage | 0,55 |
|  | Double vitrage | 0,48 |
|  | Double vitrage peu émissif | 0,49 |
|  | Triple vitrage | 0,44 |
|  | Triple vitrage peu émissif | 0,5 |
| PVC | Simple vitrage | 0,45 |
|  | Double vitrage | 0,39 |
|  | Double vitrage peu émissif | 0,4 |
|  | Triple vitrage |  |

51

Annexe 1 - Méthode de calcul 3CL-DPE 2021

|  | Triple vitrage peu émissif | 0,36 |
| :---: | :--- | :---: |
| Métal avec rupture <br> de pont thermique | Simple vitrage | 0,63 |
|  | Double vitrage | 0,56 |
|  | Double vitrage peu émissif | 0,48 |
|  | Triple vitrage | 0,5 |
|  | Triple vitrage peu émissif | 0,45 |
| Métal | Simple vitrage | 0,64 |
|  | Double vitrage | 0,58 |
|  | Double vitrage peu émissif | 0,5 |
|  | Triple vitrage | 0,52 |
|  | Triple vitrage peu émissif | 0,47 |

Pour les parois en polycarbonate, on prendra $T=0,4$.

Dans le cas où les vitrages séparant l'espace tampon solarisé de l'extérieur sont hétérogènes, le coefficient $T$ est celui du vitrage majoritaire, Dans le cas où aucun vitrage n'est majoritaire, le coefficient $T$ est proratisé à la surface.

- $b_{\text {ver }}:$ Coefficient de réduction des déperditions(voir partie 3.1)
- Ssindj : Surface sud équivalente représentant l'impact des apports solaires associés au rayonnement solaire entrant dans la partie habitable du logement après de multiples réflexions dans l'espace tampon solarisé (apports indirects) pour le mois $j$.

La surface sud équivalente représentant les apports solaires indirects dans le logement pour le mois $\mathrm{j}$ Ssind ${ }_{\mathrm{j}}$, correspond à la surface sud équivalente des apports totaux dans la véranda Stt $_{\mathrm{j}}$, à laquelle il faut déduire celle des apports directs $\mathrm{Ssd}_{\mathrm{j}}:$

$$
\begin{gathered}
S \operatorname{sind}_{j}=S s t_{j}-S s d_{j} \\
S s t_{j}=\sum_{k} A_{k} *(0,8 * T+0,024) * F e_{k} * C 1_{k, j}
\end{gathered}
$$

Avec :

- $A_{k}:$ Surface de la baie $\mathrm{k}$ séparant la véranda de l'extérieur $\left(\mathrm{m}^{2}\right)$
- $T$ : Coefficient de transparence des baies séparant la véranda de l'extérieur $\left(\mathrm{m}^{2}\right)$
- $F e_{k}$ : Facteur d'ensoleillement, qui traduit la réduction d'énergie solaire reçue par la baie $k$ du fait des masques lointains. Pour les espaces tampons solarisés, $F e_{k}=1$ car l'impact des masques sera négligé.
- $C 1_{k, j}$ : Coefficient d'orientation et d'inclinaison de la baie $k$ séparant la véranda de l'extérieur pour le mois j, voir paragraphe 18.5

Les grandes surfaces vitrées séparant la véranda de l'extérieur seront traitées comme des portes-fenêtres avec des menuiseries au nu extérieur.