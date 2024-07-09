---
dg-publish: true
dg-home: false
---
## 3 Calcul des déperditions de l'enveloppe GV

## Données d'entrée :

Caractéristiques de l'enveloppe (linéaires, surfaces, $U$ )

Surface des parois déperditives i (murs, plafonds, planchers, baies, portes)

Linéaires de ponts thermiques

La somme GV des déperditions par les parois et par renouvellement d'air (W/K) s'exprime de la manière suivante :

$$
G V=\text { DPmur }+ \text { DPplancher_bas }+ \text { DPplancher_haut }+ \text { DPmenuiserie }+ \text { PT }+D R
$$

Avec :

- PT : déperditions par les ponts thermiques (W/K) (voir partie 3.4)
- DR : déperditions par le renouvellement d'air (W/K) (voir partie 4)
- DPparoi : déperdition par la paroi (W/K) :

$$
\begin{gathered}
\text { DPmur }=\sum_{i} b_{i} * \operatorname{Smur}_{i} * \operatorname{Umur}_{i} \\
\text { DPplancher_bas }=\sum_{i} b_{i} * \operatorname{Sp}_{i} * U p b_{i} \\
\text { DPplancher_haut }=\sum_{i} b_{i} * \operatorname{Sph}_{i} * U p h_{i} \\
\text { DPmenuiserie }=\sum_{i} \frac{\mathbb{V}}{b_{i}} * \text { Smenuiserie }_{i} * \text { Umensuiserie }_{i}
\end{gathered}
$$

Avec :

- $b_{i}$ : coefficient de réduction des déperditions pour la paroi i (voir partie 3.1)
- Sparoi $:$ : surface de la paroi déperditive $\mathrm{i}\left(\mathrm{m}^{2}\right)$
- Uparoi i: coefficient de transmission thermique de la paroi $\mathrm{i}\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$ (voir parties 3.2 et 3.3$)$

On appelle menuiserie l'ensemble vitrage-protection solaire des fenêtres, portes-fenêtres et portes.

Attention : Les parois donnant sur un bâtiment autre que d'habitation sont aussi considérées déperditives.

La surface prise en compte pour l'établissement du DPE est la surface habitable du bâtiment. Cette surface intègre les vérandas chauffées.

En présence d'un espace non habitable chauffé (par exemple un garage ou un sous-sol), cet espace est traité dans le DPE comme un espace non chauffé. Dans ce cas, le diagnostiqueur devra obligatoirement mentionner dans le rapport que cet espace ne doit pas être chauffé et intégrer ce commentaire dans la justification des écarts entre les factures et les consommations conventionnelles.

### 3.1 Détermination du coefficient de réduction des déperditions $\mathbf{b}$

## Données d'entrée :

Surface des parois séparant le local non chauffé des locaux chauffés : Aiu $\left(m^{2}\right)$

Surface des parois séparant le local non chauffé de l'extérieur ou du sol : Aue $\left(m^{2}\right)$

Type de local non chauffé (garage, comble, circulation...)

Etat d'isolation des parois du local non chauffé (isolées, non isolées)

Pour une paroi enterrée ou donnant sur l'extérieur, ou un plancher sur terre-plein, vide sanitaire ou sous-sol non chauffé, $b=1$.

Dans le cas de locaux non chauffés non accessibles (mitoyenneté, espace sans accès...), forfaitairement $\mathrm{b}=0,95$.

Les parois donnant sur un bâtiment ou un espace autre que d'habitation (occupation discontinue) sont considérées comme déperditives avec $b=0,2$.

Pour les circulations communes au niveau d'un appartement en bâtiment collectif d'habitation, le calcul de b se fait en considérant les parois situées au même niveau que le lot traité. Pour un calcul fait à l'immeuble, un seul b est pris pour toutes les circulations communes si elles ne sont pas en volume intérieur chauffé.

La méthode de caractérisation des espaces communs en volume chauffé ou non chauffé est détaillée au §17.1.1.3. Une paroi donnant sur un volume non intérieur ou sur un volume intérieur non chauffé sera considérée comme déperditive. Le b sera déterminé à l'aide de la méthode suivante.

Dans les autres cas, $b$ est déterminé à l'aide des tableaux suivants, en fonction du rapport des surfaces $A_{i u} / A_{u e}$ et du coefficient surfacique équivalent Uv,ue :

- Aue est la surface des parois du local non chauffé donnant sur l'extérieur ou en contact avec le sol (paroi enterrée, terre-plein)
- Aiu est la surface des parois du local non chauffé qui donnent sur des locaux chauffés

Il est considéré qu'il n'y a pas d'échange entre deux locaux non chauffés distincts (sans liaison aéraulique). La surface des parois du local non chauffé donnant sur un vide sanitaire ou un autre local non chauffé n'entre donc ni dans Aiu ni dans Aue.
![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-012.jpg?height=860&width=1508&top_left_y=316&top_left_x=272)

Calcul b1

Calcul b2

Vue en plan

## - ouverture non permanente <br> $-1+$ ouverture permanente <br> LNC local non chauffé

Le coefficient surfacique équivalent $U v$, ue est déterminé via le tableau ci-dessous :

| Locaux non chauffés types | $\mathrm{U}_{\mathrm{V}, \mathrm{ue}} \mathrm{W} /(\mathrm{m} 2 . \mathrm{K})$ |
| :---: | :---: |
| Maison individuelle <br> - Garage <br> - Cellier <br> - Comble <br> - fortement ventilé <br> $-\quad$ faiblement ventilé <br> - très faiblement ventilé | 3 <br> 3 <br> 9 <br> 3 <br> 0,3 |
| Logement collectif <br> - Circulations communes <br> - sans ouverture directe sur l'extérieur <br> - avec ouverture directe sur l'extérieur <br> - avec bouche ou gaine de désenfumage, ouverte en permanence <br> - halls d'entrée <br> - garage privé collectif <br> - Autres dépendances <br> - Comble <br> - fortement ventilé <br> - faiblement ventilé <br> - très faiblement ventilé | 0,0 <br> 0,3 <br> 3 <br> $3^{(1)}$ ou $0,3^{(2)}$ <br> 3 <br> 3 <br> 9 <br> 3 <br> 0,3 |

L'identification du niveau de ventilation des combles peut s'appuyer sur les définitions ci-dessous. Cependant, la présence d'ouvertures dans les parois des combles doit aussi être prise en compte pour déterminer leur niveau de ventilation :

- Combles fortement ventilés : combles couverts en tuiles ou autres éléments de couverture discontinus, sans support continu
- Combles faiblement ventilés : combles couverts avec éléments de couverture continus sur support discontinu, ou avec éléments de couverture discontinus sur support continu
- Combles très faiblement ventilés : combles couverts avec éléments de couverture continus sur support continu.

Dans le cas où Aue $=0$, alors $b=0$.

Dans les tableaux suivants :

- Inc désigne un local non chauffé ;
- Ic désigne le local chauffé.

Les parois du local non chauffé sont considérées comme isolées si plus de $50 \%$ de leur surface est isolée.

Les parois en double vitrage et les portes seront considérées comme non isolées pour le calcul de b. Les parois en triple vitrage seront considérées isolées.

Les parois déperditives dont l'état d'isolation n'est pas connu sont considérées :

- Pour les bâtiments d'avant 1975, la paroi est considérée comme non isolée ;
- Pour les bâtiments construits à partir de 1975 :
- Les murs sont considérés comme isolés par l'intérieur ;
- Les plafonds sont considérés isolés par l'extérieur ;
- Les planchers sur terre-plein sont considérés isolés par l'extérieur (en sous face) à partir de 2001.

On en déduit la valeur de $b$ en fonction des différents cas suivants :
![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-013.jpg?height=144&width=1170&top_left_y=1598&top_left_x=450)

| Aiu/Aue | Uv,ue |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  | $\mathbf{0 , 0}$ | $\mathbf{0 , 3}$ | $\mathbf{3 , 0}$ | $\mathbf{9 , 0}$ |  |
|  | $\leq 0,25$ | 0,95 | 0,95 | 1,00 | 1,00 |
| $0,25<$ | $\leq 0,50$ | 0,95 | 0,95 | 0,95 | 1,00 |
| $0,50<$ | $\leq 0,75$ | 0,90 | 0,95 | 0,95 | 1,00 |
| $0,75<$ | $\leq 1,00$ | 0,85 | 0,90 | 0,95 | 0,95 |
| $1,00<$ | $\leq 1,25$ | 0,85 | 0,90 | 0,90 | 0,95 |
| $1,25<$ | $\leq 2,00$ | 0,80 | 0,80 | 0,90 | 0,95 |
| $2,00<$ | $\leq 2,50$ | 0,75 | 0,80 | 0,85 | 0,90 |
| $2,50<$ | $\leq 3,00$ | 0,70 | 0,75 | 0,85 | 0,90 |
| $3,00<$ | $\leq 3,50$ | 0,65 | 0,75 | 0,80 | 0,90 |
| $3,50<$ | $\leq 4,00$ | 0,65 | 0,70 | 0,80 | 0,90 |
| $4,00<$ | $\leq 6,00$ | 0,55 | 0,60 | 0,70 | 0,85 |
| $6,00<$ | $\leq 8,00$ | 0,45 | 0,55 | 0,65 | 0,80 |
| $8,00<$ | $\leq 10,00$ | 0,40 | 0,50 | 0,60 | 0,75 |
| $10,00<$ | $\leq 25,00$ | 0,35 | 0,40 | 0,50 | 0,70 |
| $25,00<$ | $\leq 50,00$ | 0,20 | 0,25 | 0,35 | 0,50 |
| $50,00<$ |  | 0,10 | 0,15 | 0,20 | 0,30 |


| Aiu/Aue |  | $U_{v, \text { ue }}$ |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  |  | 0,0 | 0,3 | 3,0 | 9,0 |
|  | $\leq 0,25$ | 0,80 | 0,85 | 0,90 | 0,95 |
| $0,25<$ | $\leq 0,50$ | 0,65 | 0,75 | 0,80 | 0,90 |
| $0,50<$ | $\leq 0,75$ | 0,55 | 0,65 | 0,75 | 0,85 |
| $0,75<$ | $\leq 1,00$ | 0,50 | 0,55 | 0,70 | 0,80 |
| $1,00<$ | $\leq 1,25$ | 0,45 | 0,50 | 0,65 | 0,80 |
| $1,25<$ | $\leq 2,00$ | 0,35 | 0,40 | 0,50 | 0,70 |
| $2,00<$ | $\leq 2,50$ | 0,30 | 0,35 | 0,45 | 0,65 |
| $2,50<$ | $\leq 3,00$ | 0,25 | 0,30 | 0,40 | 0,60 |
| $3,00<$ | $\leq 3,50$ | 0,20 | 0,30 | 0,40 | 0,55 |
| $3,50<$ | $\leq 4,00$ | 0,20 | 0,25 | 0,35 | 0,50 |
| $4,00<$ | $\leq 6,00$ | 0,15 | 0,20 | 0,25 | 0,40 |
| $6,00<$ | $\leq 8,00$ | 0,10 | 0,15 | 0,20 | 0,35 |
| $8,00<$ | $\leq 10,00$ | 0,10 | 0,10 | 0,20 | 0,30 |
| $10,00<$ | $\leq 25,00$ | 0,05 | 0,10 | 0,15 | 0,25 |
| $25,00<$ | $\leq 50,00$ | 0,05 | 0,05 | 0,05 | 0,15 |
| $50,00<$ |  | 0,00 | 0,00 | 0,05 | 0,05 |

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-014.jpg?height=154&width=623&top_left_y=314&top_left_x=405)

$A_{i u}:$ isolée

$A_{u e}$ : isolée

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-014.jpg?height=152&width=389&top_left_y=318&top_left_x=1256)

| A | $\mathbf{U}_{\mathbf{i u}}$ Aue |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  |  |  |  |  |  |  |
|  |  | $\mathbf{0 , 3}$ | $\mathbf{3 , 0}$ | $\mathbf{9 , 0}$ |  |
|  |  | 0,35 | 0,50 | 0,85 | 0,95 |
| $0,25<$ | $\leq 0,50$ | 0,20 | 0,35 | 0,70 | 0,90 |
| $0,50<$ | $\leq 0,75$ | 0,15 | 0,25 | 0,65 | 0,85 |
| $0,75<$ | $\leq 1,00$ | 0,15 | 0,20 | 0,55 | 0,80 |
| $1,00<$ | $\leq 1,25$ | 0,10 | 0,15 | 0,50 | 0,75 |
| $1,25<$ | $\leq 2,00$ | 0,05 | 0,10 | 0,40 | 0,65 |
| $2,00<$ | $\leq 2,50$ | 0,05 | 0,10 | 0,35 | 0,60 |
| $2,50<$ | $\leq 3,00$ | 0,05 | 0,10 | 0,30 | 0,55 |
| $3,00<$ | $\leq 3,50$ | 0,05 | 0,05 | 0,25 | 0,50 |
| $3,50<$ | $\leq 4,00$ | 0,05 | 0,05 | 0,25 | 0,45 |
| $4,00<$ | $\leq 6,00$ | 0,00 | 0,05 | 0,20 | 0,35 |
| $6,00<$ | $\leq 8,00$ | 0,00 | 0,05 | 0,15 | 0,30 |
| $8,00<$ | $\leq 10,00$ | 0,00 | 0,05 | 0,10 | 0,25 |
| $10,00<$ | $\leq 25,00$ | 0,00 | 0,00 | 0,10 | 0,20 |
| $25,00<$ | $\leq 50,00$ | 0,00 | 0,00 | 0,05 | 0,10 |
| $50,00<$ |  | 0,00 | 0,00 | 0,00 | 0,05 |


| Aiu/Aue | U $_{\mathbf{v}, \mathbf{u e}}$ |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  | $\mathbf{0 , 0}$ | $\mathbf{0 , 3}$ | $\mathbf{3 , 0}$ | $\mathbf{9 , 0}$ |  |
|  | $\leq 0,25$ | 0,80 | 0,90 | 0,95 | 1,00 |
| $0,25<$ | $\leq 0,50$ | 0,65 | 0,80 | 0,95 | 1,00 |
| $0,50<$ | $\leq 0,75$ | 0,55 | 0,70 | 0,90 | 0,95 |
| $0,75<$ | $\leq 1,00$ | 0,50 | 0,65 | 0,90 | 0,95 |
| $1,00<$ | $\leq 1,25$ | 0,45 | 0,60 | 0,90 | 0,95 |
| $1,25<$ | $\leq 2,00$ | 0,35 | 0,45 | 0,80 | 0,95 |
| $2,00<$ | $\leq 2,50$ | 0,30 | 0,40 | 0,80 | 0,90 |
| $2,50<$ | $\leq 3,00$ | 0,25 | 0,35 | 0,75 | 0,90 |
| $3,00<$ | $\leq 3,50$ | 0,20 | 0,35 | 0,70 | 0,90 |
| $3,50<$ | $\leq 4,00$ | 0,20 | 0,30 | 0,70 | 0,85 |
| $4,00<$ | $\leq 6,00$ | 0,15 | 0,25 | 0,60 | 0,80 |
| $6,00<$ | $\leq 8,00$ | 0,10 | 0,20 | 0,55 | 0,75 |
| $8,00<$ | $\leq 10,00$ | 0,10 | 0,15 | 0,45 | 0,70 |
| $10,00<$ | $\leq 25,00$ | 0,05 | 0,10 | 0,40 | 0,65 |
| $25,00<$ | $\leq 50,00$ | 0,05 | 0,05 | 0,25 | 0,45 |
| $50,00<$ |  | 0,00 | 0,05 | 0,10 | 0,30 |

Les espaces tampons solarisés (vérandas, loggias fermées) non chauffés bénéficient d'apports solaires qui y génèrent des températures supérieures à celles atteintes dans les espaces non solarisés.

## Rappelons que les vérandas chauffées sont traitées en surface habitable.

Dans le cas de vérandas ou loggias fermées non chauffées, les coefficients de réduction de température pris sont donnés dans le tableau ci-dessous :

| Zone climatique | Orientation de la véranda | Paroi donnant sur la véranda | $\mathrm{b}_{\text {ver }}$ |
| :---: | :---: | :---: | :---: |
| H1 | Nord | Isolé | 0.95 |
|  |  | Non isolé | 0.85 |
|  | Est / Ouest | Isolé | 0.63 |
|  |  | Non isolé | 0.6 |
|  | Sud | Isolé | 0.58 |
|  |  | Non isolé | 0.55 |
| H2 | Nord | Isolé | 0.95 |
|  |  | Non isolé | 0.85 |
|  | Est / Ouest | Isolé | 0.6 |
|  |  | Non isolé | 0.58 |
|  | Sud | Isolé | 0.57 |
|  |  | Non isolé | 0.55 |
| H3 | Nord | Isolé | 0.95 |
|  |  | Non isolé | 0.85 |
|  | Est / Ouest | Isolé | 0.53 |
|  |  | Non isolé | 0.53 |
|  | Sud | Isolé | 0.48 |
|  |  | Non isolé | 0.55 |

Les orientations Nord intègrent les limites Nord-Est et Nord-Ouest.

Les orientations Sud intègrent les limites Sud-Est et Sud-Ouest.

L'orientation de la véranda prise en compte est celle de sa façade principale (avec la plus grande surface de vitrages

verticaux), S'il existe plusieurs façades principales, c'est-à-dire qu'au moins deux façades d'orientation présentent de façon égale les surfaces vitrées les plus importantes, b ber est la moyenne des buer sur ces orientations.

### 3.2 Calcul des U des parois opaques

Données d'entrée:

Caractéristiques des parois (type, épaisseur, mitoyenneté, matériaux traditionnels)

Caractéristique isolation (épaisseur, résistance, année d'isolation)

Nombre d'appartements

Retour d'isolation autour des menuiseries (avec ou sans)

Hauteur moyenne sous plafond

On considère qu'un logement est chauffé par effet joule lorsque la chaleur est fournie par une résistance électrique.

Une paroi opaque (hors plancher bas) est considérée comme un mur dès lors que l'angle par rapport à l'horizontal est supérieur ou égal à $75^{\circ}$. Dans les autres cas, il s'agit d'un plancher haut.

### 3.2.1 Calcul des Umur

### 3.2.1.1 Schéma du calcul de Umur

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-016.jpg?height=1947&width=1470&top_left_y=500&top_left_x=310)

### 3.2.1.2 Calcul des Umur0

Umur0 est le coefficient de transmission thermique du mur non isolé $\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$.

| Epaisseur (en cm) |  | $\leq 20$ | 25 | 30 | 35 | 40 | 45 | 50 | 55 | 60 | 65 | 70 | 75 | $\geq 80$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en pierre de taille et <br> moellons (granit, gneiss, porphyres, <br> pierres calcaires, grès, meulières, <br> schistes, pierres volcaniques) | Murs constitués d'un <br> seul matériau / inconnu | 3,2 | 2,85 | 2,65 | 2,45 | 2,3 | 2,15 | 2,05 | 1,90 | 1,80 | 1,75 | 1,65 | 1,55 | 1,50 |
|  | Murs avec remplissage <br> tout venant | - | - | - | - | - | - | 1,90 | 1,75 | 1,60 | 1,50 | 1,45 | 1,30 | 1,25 |


| Epaisseur connue (en cm) | $\leq 40$ | 45 | 50 | 55 | 60 | 65 | 70 | 75 | $\geq 80$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en pisé ou béton de terre <br> stabilisé | 1,75 | 1,65 | 1,55 | 1,45 | 1,35 | 1,25 | 1,2 | 1,15 | 1,1 |


| Epaisseur connue (en cm) |  | $\leq 8$ | 10 | 13 | 18 | 24 | $\geq 32$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en pans de bois | Sans remplissage tout venant | 3 | 2,7 | 2,35 | 1,98 | 1,65 | 1,35 |
|  |  | Avec remplissage tout venant | 1,7 |  |  |  |  |


| Epaisseur connue (en cm) | $\leq 10$ | 15 | 20 | $\geq 25$ |
| :---: | :---: | :---: | :---: | :---: |
| Murs bois (rondins) | 1,6 | 1,2 | 0,95 | 0,8 |


| Epaisseur connue (en cm) | $\leq 9$ | 12 | 15 | 19 | 23 | 28 | 34 | 45 | 55 | 60 | $\geq 70$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en briques pleines simples | 3,9 | 3,45 | 3,05 | 2,75 | 2,5 | 2,25 | 2 | 1,65 | 1,45 | 1,35 | 1,2 |


| Epaisseur connue (en cm) | $\leq 20$ | 25 | 30 | 35 | 45 | 50 | $\geq 60$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en briques pleines doubles avec lame d'air | 2 | 1,85 | 1,65 | 1,55 | 1,35 | 1,25 | 1,2 |


| Epaisseur connue (en cm) | $\leq 15$ | 18 | 20 | 23 | 25 | 28 | 33 | 38 | $\geq 43$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en briques creuses | 2,15 | 2,05 | 2 | 1,85 | 1,7 | 1,68 | 1,65 | 1,55 | 1,4 |


| Epaisseur connue | $\leq 20$ | 23 | 25 | 28 | 30 | 33 | 35 | 38 | $\geq 40$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en blocs de béton pleins | 2,9 | 2,75 | 2,6 | 2,5 | 2,4 | 2,3 | 2,2 | 2,1 | 2,05 |


| Epaisseur connue (en cm) | $\leq 20$ | 23 | $\geq 25$ |
| :---: | :---: | :---: | :---: |
| Murs en blocs de béton creux | 2,8 | 2,65 | 2,3 |


| Epaisseur connue (en cm) | $\leq 20$ | 22,5 | 25 | 28 | 30 | 35 | 40 | $\geq 45$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en béton banché | 2,9 | 2,75 | 2,65 | 2,5 | 2,4 | 2,2 | 2,05 | 1,9 |
| Murs en béton de mâchefer | 2,75 | 2,5 | 2,4 | 2,25 | 2,15 | 1,95 | 1,8 | - |


| Epaisseur connue (en cm) | 30 | 37,5 |
| :---: | :---: | :---: |
| Brique terre cuite alvéolaire | 0,47 | 0,40 |


|  | Mur en béton cellulaire |  |  |  |  |  |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Epaisseur (cm) | 15 | 17,5 | 20 | 22,5 | 25 | 27,5 | 30 | 32,5 | 35 | 37,5 |
| Construction $<2013$ | 0,90 | 0,79 | 0,70 | 0,63 | 0,57 | 0,53 | 0,49 | 0,45 | 0,42 | 0,40 |
| Construction $\geq 2013$ | 0,69 | 0,60 | 0,53 | 0,48 | 0,43 | 0,40 | 0,36 | 0,30 | 0,28 | 0,22 |


| Epaisseur connue (en cm) | $\leq 15$ | 20 | $\geq 25$ |
| :---: | :---: | :---: | :---: |
| Murs sandwich béton/isolant/béton (sans isolation rapportée) | 0,9 | 0,48 | 0,45 |


|                      Epaisseur connue (en cm)                      |  10  |  15  |  20  |  25  |  30  |  35  |  40  | $\geq 45$ |
| :----------------------------------------------------------------: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :-------: |
| Murs en ossature bois avec isolant en <br> remplissage $\geq 2006$ | 0,45 | 0,35 | 0,26 | 0,21 | 0,17 | 0,15 | 0,13 |   0,11    |


|                     Epaisseur connue (en cm)                     |  10  |  15  | 20  |  25  | 30  |  35  |  40  | $\geq 45$ |
| :--------------------------------------------------------------: | :--: | :--: | :-: | :--: | :-: | :--: | :--: | :-------: |
| Murs en ossature bois avec isolant en <br> remplissage 2001-2005 | 0,52 | 0,41 | 0,3 | 0,24 | 0,2 | 0,17 | 0,15 |   0,13    |


|                   Epaisseur connue (en cm)                   |  10  |  15  |  20  |  25  |  30  | 35  |  40  |  45  |
| :----------------------------------------------------------: | :--: | :--: | :--: | :--: | :--: | :-: | :--: | :--: |
| Murs en ossature bois avec isolant en <br> remplissage <2001 | 0,65 | 0,45 | 0,34 | 0,28 | 0,23 | 0,2 | 0,18 | 0,16 |


|                Epaisseur connue (en cm)                 | $\leq 8$ | 10  | 13  | 18  | 24  | $\geq 32$ |
| :-----------------------------------------------------: | :------: | :-: | :-: | :-: | :-: | :-------: |
| Murs en ossature bois avec remplissage tout <br> venant |   1,7    |     |     |     |     |           |


| Epaisseur connue (en cm) | $\leq 8$ | 10 | 13 | 18 | 24 | $\geq 32$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Murs en ossature bois sans remplissage | 3 | 2,7 | 2,35 | 1,98 | 1,65 | 1,35 |

Cloison de plâtre : Umur0 $=3,33 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Pour les parois dites «anciennes ", c'est-à-dire constituées de matériaux traditionnels à savoir pierres, terre, mur à colombage, brique ancienne, la présence d'un enduit isolant n'est pas considérée comme une isolation. Cependant, cet enduit apporte une correction d'isolation qu'il faut prendre en compte en considérant :

$$
\text { Umur } 0=\frac{1}{\frac{1}{\text { Umur0_sansEnduit }}+R_{\text {enduit }}}
$$

Avec :

- $R_{\text {enduit }}=0,7 m^{2} . \mathrm{K} / \mathrm{W}$

Pour l'ensemble des parois, la présence d'un doublage apporte une résistance thermique supplémentaire calculée comme suit :

$$
\text { Umur }_{\text {doublage }}=\frac{1}{\frac{1}{\text { Umur } 0}+R_{\text {doublage }}}
$$

Avec les valeurs de résistances suivantes :

- Pour un mur avec un doublage rapporté de nature indéterminée ou avec lame d'air de moins de $15 \mathrm{~mm}: R_{\text {doublage }}=$ $0,1 \mathrm{~m}^{2} . \mathrm{K} / \mathrm{W}$
- Pour un mur avec un doublage rapporté avec une lame d'air de plus de $15 \mathrm{~mm}$ ou avec un matériau de doublage connu (plâtre, brique, bois) : $R_{\text {doublage }}=0,21 \mathrm{~m}^{2} . \mathrm{K} / \mathrm{W}$

Les murs en pavés de verre sont traités comme des parois vitrées (voir paragraphe 3.3).

Pour les murs non répertoriés, saisir directement les coefficients de transmission thermique quand ils sont justifiés.

Pour les murs doubles ou de composants multiples connus et justifiés, saisir directement le $\cup$ du mur calculé.

### 3.2.2 Calcul des Uplancher bas (Upb)

### 3.2.2.1 Schéma du calcul de Upb

Si le plancher donne sur l'extérieur ou un local non chauffé (hors sous-sol) :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-020.jpg?height=1851&width=1402&top_left_y=568&top_left_x=356)

Pour les vides sanitaires, les sous-sol non chauffés et terre-plein, le calcul des déperditions se fait avec un coefficient Ue en remplacement de Upb. Le calcul de Upb est toutefois nécessaire pour obtenir la valeur du coefficient Ue, selon les tableaux ci-dessous.

Upb est le coefficient de transmission thermique de la partie du plancher située entre l'ambiance intérieure et le vide sanitaire, le sous-sol ou le terre-plein. Il est calculé selon le schéma précédent (voir « plancher donnant sur l'extérieur ou un local non chauffé "), en $W /\left(m^{2} . K\right)$.

Les données ne figurant pas dans le tableau peuvent être obtenues par interpolation et extrapolation en traçant des droites entre les valeurs les plus proches présentes dans le tableau.

- P : périmètre ou linéaire du plancher déperditif du bâtiment ou du lot sur terre-plein, vide sanitaire ou soussol non chauffé donnant sur l'extérieur ou un local non chauffé ( $\mathrm{m}$ )
- : surface du plancher du bâtiment ou du lot sur terre-plein, vide sanitaire ou sous-sol non chauffé ( $m^{2}$ )
- $25 / P$ est arrondi à l'entier le plus proche

Le Ue d'un plancher est un Umoyen pour tout le plancher du bâtiment. Il prend en compte l'isolation périphérique du plancher bas. Dès lors, tous les appartements d'un immeuble donnant sur un même terre-plein ont le même Ue.

Le Ue d'un plancher bas d'immeuble est toujours calculé à l'immeuble, même dans le cas d'un DPE seulement sur un appartement.

Valeurs de Ue $\left(W /\left(m^{2} . K\right)\right)$ selon Upb et $2 S / P$ :

Si le plancher est sur vide sanitaire ou sous-sol non chauffé :

| Upb | 3,33 | 1,43 | 0,83 | 0,45 | 0,41 | 0,37 | 0,34 | 0,31 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 3 | 0,45 | 0,42 | 0,39 | 0,36 | 0,33 | 0,3 | 0,28 | 0,26 |
| 4 | 0,43 | 0,4 | 0,37 | 0,34 | 0,31 | 0,29 | 0,27 | 0,25 |
| 5 | 0,38 | 0,36 | 0,34 | 0,32 | 0,3 | 0,28 | 0,26 | 0,25 |
| 6 | 0,37 | 0,35 | 0,33 | 0,31 | 0,29 | 0,27 | 0,25 | 0,24 |
| 7 | 0,36 | 0,34 | 0,32 | 0,3 | 0,28 | 0,26 | 0,24 | 0,23 |
| 8 | 0,35 | 0,33 | 0,31 | 0,29 | 0,27 | 0,25 | 0,24 | 0,22 |
| 9 | 0,34 | 0,32 | 0,3 | 0,28 | 0,26 | 0,24 | 0,23 | 0,22 |
| 10 | 0,33 | 0,31 | 0,29 | 0,27 | 0,25 | 0,24 | 0,22 | 0,21 |
| 12 | 0,28 | 0,27 | 0,26 | 0,25 | 0,24 | 0,22 | 0,21 | 0,2 |
| 14 | 0,28 | 0,27 | 0,26 | 0,24 | 0,23 | 0,21 | 0,2 | 0,19 |
| 16 | 0,28 | 0,27 | 0,25 | 0,23 | 0,21 | 0,2 | 0,19 | 0,18 |
| 18 | 0,28 | 0,26 | 0,24 | 0,22 | 0,2 | 0,19 | 0,19 | 0,18 |
| 20 | 0,24 | 0,23 | 0,22 | 0,21 | 0,2 | 0,19 | 0,18 | 0,17 |

## Si le plancher donne sur terre-plein :

- Bâtiment construit avant 2001

| Usp | 3,4 | 1,5 | 0,85 | 0,6 | 0,46 | 0,37 | 0,31 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 3 | 0,78 | 0,56 | 0,43 | 0,35 | 0,3 | 0,78 | 0,56 |
| 4 | 0,68 | 0,51 | 0,4 | 0,33 | 0,28 | 0,68 | 0,51 |
| 5 | 0,6 | 0,46 | 0,38 | 0,32 | 0,27 | 0,6 | 0,46 |
| 6 | 0,54 | 0,43 | 0,35 | 0,3 | 0,26 | 0,54 | 0,43 |
| 7 | 0,49 | 0,39 | 0,33 | 0,28 | 0,25 | 0,49 | 0,39 |
| 8 | 0,45 | 0,37 | 0,31 | 0,27 | 0,24 | 0,45 | 0,37 |
| 9 | 0,42 | 0,34 | 0,29 | 0,26 | 0,23 | 0,42 | 0,34 |
| 10 | 0,39 | 0,32 | 0,28 | 0,24 | 0,22 | 0,39 | 0,32 |
| 12 | 0,35 | 0,29 | 0,25 | 0,22 | 0,2 | 0,35 | 0,29 |
| 14 | 0,31 | 0,26 | 0,23 | 0,2 | 0,19 | 0,31 | 0,26 |
| 16 | 0,28 | 0,24 | 0,21 | 0,19 | 0,17 | 0,28 | 0,24 |
| 18 | 0,26 | 0,22 | 0,2 | 0,18 | 0,16 | 0,26 | 0,22 |
| 20 | 0,24 | 0,21 | 0,18 | 0,17 | 0,15 | 0,24 | 0,21 |

- Bâtiments à partir de 2001

| Upb | 3,4 | 1,5 | 0,85 | 0,59 | 0,46 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 3 | 0,7 | 0,6 | 0,49 | 0,39 | 0,33 |
| 4 | 0,65 | 0,55 | 0,45 | 0,36 | 0,31 |
| 5 | 0,58 | 0,5 | 0,42 | 0,34 | 0,29 |
| 6 | 0,52 | 0,45 | 0,38 | 0,32 | 0,27 |
| 7 | 0,48 | 0,42 | 0,36 | 0,3 | 0,26 |
| 8 | 0,45 | 0,39 | 0,33 | 0,28 | 0,25 |
| 9 | 0,39 | 0,35 | 0,31 | 0,27 | 0,24 |
| 10 | 0,38 | 0,34 | 0,3 | 0,26 | 0,23 |
| 12 | 0,35 | 0,31 | 0,27 | 0,23 | 0,21 |
| 14 | 0,3 | 0,27 | 0,24 | 0,21 | 0,19 |
| 16 | 0,26 | 0,24 | 0,22 | 0,2 | 0,18 |
| 18 | 0,25 | 0,24 | 0,21 | 0,18 | 0,17 |
| 20 | 0,23 | 0,21 | 0,19 | 0,17 | 0,16 |

### 3.2.2.2 Calcul des Upb0

Upb0 est le coefficient de transmission thermique du plancher bas non isolé ( $\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$ ).

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=1106&width=1591&top_left_y=692&top_left_x=238)

| Plancher avec ou sans <br> remplissage |
| :--- |
|  |
|  |
| Upb0 $=1,45$ |

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=523&width=463&top_left_y=978&top_left_x=251)

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=274&width=480&top_left_y=962&top_left_x=822)
![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=542&width=466&top_left_y=1246&top_left_x=818)

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=568&width=466&top_left_y=958&top_left_x=1345)

Plancher bois sur solives bois

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-023.jpg?height=163&width=451&top_left_y=1603&top_left_x=260)

Plancher à entrevous isolant $\mathrm{Upb0}=0,45 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Pour les planchers bas non répertoriés, saisir directement les coefficients de transmission thermique Upb0 quand ils sont justifiés. Les données des règles TH-U peuvent être utilisées.

### 3.2.3 Calcul des Uplancher haut (Uph)

### 3.2.3.1 Schéma du calcul de Uph

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-024.jpg?height=1836&width=1005&top_left_y=481&top_left_x=320)

Uph tab :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-024.jpg?height=1844&width=397&top_left_y=497&top_left_x=1366)

Lorsque le local au-dessus du logement est un local non chauffé ou un local autre que d'habitation., Uph_tab est pris dans la catégorie "Terrasse ».

3.2.3.2 Calcul des Uph0

Uph0 est le coefficient de transmission thermique du plancher haut non isolé ( $\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$ ).

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-025.jpg?height=760&width=1634&top_left_y=454&top_left_x=248)

Combles aménagés sous rampant : Uph $0=2,5 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Toiture en chaume $: U p h 0=0,24 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Plafond en plaque de plâtre : Uph $0=2,5 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Les toitures en bac acier sont traités comme des combles aménagés sous rampants : Uph $0=2.5 \mathrm{~W} / \mathrm{m}^{2}$. $\mathrm{K}$ Pour les murs, plafonds, planchers non répertoriés, saisir directement les coefficients de transmission thermique quand ceux si peuvent être justifiés. Les données des règles TH-U peuvent être utilisées à défaut.

Attention : Les valeurs par défaut des caractéristiques des parois dépendent des années de construction dans certains cas. Pour les bâtiments ayant fait l'objet d'extension, les valeurs par défaut des caractéristiques des parois peuvent donc être différentes entre l'extension et le bâtiment originel.

### 3.3 Calcul des $U$ des parois vitrées et des portes

Données d'entrée :

Type de vitrage (simple, double...)

Epaisseur lame d'air

Présence d'une couche peu émissive

Gaz de remplissage

Inclinaison vitrage

Type de menuiserie

Type de volets

## Type de porte

Les grandes surfaces vitrées des vérandas chauffées seront traitées comme des portes-fenêtres avec des menuiseries au nu extérieur.

Les parois en brique de verre sont traitées comme des parois vitrées avec :

- $\quad$ Brique de verre pleine $U w=3,5 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$
- Brique de verre creuse $U w=2 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Les parois en polycarbonate sont traitées comme des parois vitrées avec : Uw $=3 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$

Définition de l'inclinaison des baies pour le calcul des $U$ :

- $\quad$ Paroi verticale $=$ angle par rapport à l'horizontal $\geq 75^{\circ}$
- $\quad$ Paroi horizontale $=$ angle par rapport à l'horizontal $<75^{\circ}$

Le coefficient U des fenêtres est connu : saisir Uw et caractériser les occultations pour déterminer Ujn.

Si Uw est inconnu alors suivre la démarche suivante :

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-026.jpg?height=386&width=1194&top_left_y=1166&top_left_x=411)

Avec :

- Ug : coefficient de transmission thermique du vitrage $\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$
- Uw : coefficient de transmission thermique de la fenêtre ou de la porte-fenêtre (vitrage + menuiserie) $\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$
- Ujn : coefficient de transmission thermique de la fenêtre ou de la porte-fenêtre avec les protections solaires $\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$


### 3.3.1 Détermination de la performance du vitrage $U_{\mathrm{g}}$ <br> - Simple vitrage et survitrage

Pour un simple vitrage, quelle que soit l'épaisseur du verre, prendre :

- $\mathrm{U}_{\mathrm{g}}=5,8 \mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$ pour un vitrage vertical ou horizontal

Le $U_{\mathrm{g}}$ d'un survitrage est déterminé en apportant une majoration de $0,1 \mathrm{~W} /\left(\mathrm{m}^{2} . K\right)$ au $\mathrm{U}_{\mathrm{g}}$ du double vitrage rempli à l'air sec ayant la même épaisseur de lame d'air. Les épaisseurs des lames d'air pour le survitrage sont plafonnées à $20 \mathrm{~mm}$. C'est-à-dire que toute lame d'air d'un survitrage d'épaisseur supérieure à $20 \mathrm{~mm}$ sera traitée dans les calculs comme une lame d'air de $20 \mathrm{~mm}$ d'épaisseur.

## - Double vitrage vertical

Remplissage air sec ou inconnu

| Remplissage air sec |  |  |
| :---: | :---: | :---: |
| Epaisseur de lame <br> d'air $(\mathrm{mm})$ | Ug W/(m². $\mathrm{K})$ |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 3,3 | 2,45 |
| 8 | 3,1 | 2,1 |
| 10 | 2,9 | 1,8 |
| 12 | 2,8 | 1,6 |
| 14 | 2,8 | 1,5 |
| 15 | 2,7 | 1,4 |
| 16 | 2,7 | 1,4 |
| 18 | 2,7 | 1,4 |
| 20 | 2,7 | 1,4 |

Remplissage Argon ou Krypton

| Remplissage argon ou krypton |  |  |
| :---: | :---: | :---: |
| Epaisseur de <br> lame d'air (mm) | Ug W/(m².K) |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 3 | 2 |
| 8 | 2,9 | 1,7 |
| 10 | 2,8 | 1,4 |
| 12 | 2,7 | 1,3 |
| 14 | 2,6 | 1,2 |
| 15 | 2,6 | 1,1 |
| 16 | 2,6 | 1,1 |
| 18 | 2,6 | 1,1 |
| 20 | 2,6 | 1,1 |

## - Double vitrage horizontal

## Remplissage air sec ou inconnu

| Remplissage air sec |  |  |
| :---: | :---: | :---: |
| Epaisseur de lame <br> d'air (mm) | Ug W/( $\left.\mathrm{m}^{2} . \mathrm{K}\right)$ |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 3,7 | 2,6 |
| 8 | 3,4 | 2,2 |
| 10 | 3,2 | 1,9 |
| 12 | 3,1 | 1,7 |
| 14 | 3,1 | 1,6 |
| 15 | 2,9 | 1,5 |
| 16 | 2,9 | 1,5 |
| 18 | 2,9 | 1,5 |
| 20 | 2,9 | 1,5 |

## Remplissage Argon ou Krypton

| Remplissage argon ou krypton |  |  |
| :---: | :---: | :---: |
| Epaisseur de lame <br> d'air (mm) | Ug W/(m². K) |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 3,3 | 2,1 |
| 8 | 3,2 | 1,8 |
| 10 | 3,1 | 1,5 |
| 12 | 2,9 | 1,4 |
| 14 | 2,8 | 1,2 |
| 15 | 2,8 | 1,1 |
| 16 | 2,8 | 1,1 |
| 18 | 2,8 | 1,1 |
| 20 | 2,8 | 1,1 |

Attention : si la valeur de l'épaisseur de la lame d'air n'est pas dans le tableau présenté, prendre la valeur directement inférieure qui s'y trouve.

- Triple vitrage vertical

Remplissage air sec ou inconnu

| Remplissage air sec |  |  |
| :---: | :---: | :---: |
| Epaisseur de lame <br> d'air (mm) | Ug W/( $\left.m^{2} . \mathrm{K}\right)$ |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 2,3 | 1,7 |
| 8 | 2,1 | 1,4 |
| 10 | 2,0 | 1,2 |
| 12 | 1,9 | 1,1 |
| 14 | 1,8 | 1,0 |
| 15 | 1,8 | 0,9 |
| 16 | 1,8 | 0,9 |
| 18 | 1,7 | 0,8 |
| 20 | 1,7 | 0,8 |

Remplissage Argon ou Krypton

| Remplissage argon ou krypton |  |  |
| :---: | :---: | :---: |
| Epaisseur de lame <br> d'air (mm) | Ug W/( $\left.\mathrm{m}^{2} . \mathrm{K}\right)$ |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 2,1 | 1,5 |
| 8 | 1,9 | 1,2 |
| 10 | 1,8 | 1,0 |
| 12 | 1,8 | 0,9 |
| 14 | 1,7 | 0,8 |
| 15 | 1,7 | 0,7 |
| 16 | 1,7 | 0,7 |
| 18 | 1,6 | 0,6 |
| 20 | 1,6 | 0,6 |

## - Triple vitrage horizontal

Remplissage air sec ou inconnu

| Remplissage air sec |  |  |
| :---: | :---: | :---: |
| Epaisseur d'une <br> lame d'air $(\mathrm{mm})$ | Ug W/( $\left.\mathrm{m}^{2} . \mathrm{K}\right)$ |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 2,5 | 1,8 |
| 8 | 2,2 | 1,5 |
| 10 | 2,1 | 1,2 |
| 12 | 2,0 | 1,1 |
| 14 | 1,9 | 1,0 |
| 15 | 1,9 | 0,9 |
| 16 | 1,9 | 0,9 |
| 18 | 1,8 | 0,8 |
| 20 | 1,8 | 0,8 |

Remplissage Argon ou Krypton

| Remplissage argon ou krypton |  |  |
| :---: | :---: | :---: |
|  | Ug W/(m².K) |  |
|  | Vitrages non traités | Vitrages peu émissifs |
| 6 | 2,2 | 1,6 |
| 8 | 2,0 | 1,2 |
| 10 | 1,9 | 1,0 |
| 12 | 1,9 | 0,9 |
| 14 | 1,8 | 0,8 |
| 15 | 1,8 | 0,7 |
| 16 | 1,8 | 0,7 |
| 18 | 1,7 | 0,6 |
| 20 | 1,7 | 0,6 |

Attention : Si un triple vitrage a des épaisseurs de lame d'air différentes, considérer que c'est un triple vitrage dont l'épaisseur de chaque lame d'air est la moitié de l'épaisseur totale des deux lames d'air (ou la valeur consignée dans les tableaux précédents la plus proche de la moitié de l'épaisseur).

Exemple : pour un triple vitrage 4/10/4/12/4, considérer que c'est équivalent à un 4/10/4/10/4.

Par défaut, les doubles et triples vitrages installés à partir de 2006 sont tous considérés remplis à l'Argon ou au Krypton.

Si le Ug d'un vitrage est connu et justifié, le saisir directement.

### 3.3.2 Coefficients Uw des fenêtres / portes-fenêtres

Les baies sans ouverture possible (ni battantes ni coulissantes) et les baies oscillantes seront traitées comme battantes dans toute la suite.

Dans la suite, les Uw associés à des Ug non présents dans les tableaux peuvent être obtenus par interpolation ou extrapolation avec les deux Ug tabulés les plus proches.

## - Menuiserie métallique à rupture de pont thermique

| Ug | Uw $\left(W /\left(m^{2} . K\right)\right)$ |  |  |  |
| :---: | :---: | :---: | :---: | :---: |
|  | Fenêtre <br> battante | Fenêtre <br> coulissante | Porte-Fenêtre <br> battante | Porte-Fenêtre <br> coulissante |
| 0,5 | 1,3 | 1,4 | 1,0 | 1,2 |
| 0,6 | 1,4 | 1,5 | 1,1 | 1,3 |
| 0,7 | 1,5 | 1,6 | 1,2 | 1,4 |
| 0,8 | 1,6 | 1,6 | 1,3 | 1,5 |
| 0,9 | 1,6 | 1,7 | 1,4 | 1,6 |
| 1 | 1,7 | 1,8 | 1,5 | 1,6 |
| 1,1 | 1,8 | 1,9 | 1,6 | 1,7 |
| 1,2 | 1,9 | 2,0 | 1,7 | 1,8 |
| 1,3 | 2,0 | 2,0 | 1,7 | 1,9 |
| 1,4 | 2,1 | 2,1 | 1,8 | 2,0 |
| 1,5 | 2,1 | 2,2 | 1,9 | 2,1 |
| 1,6 | 2,2 | 2,3 | 2,0 | 2,2 |
| 1,7 | 2,3 | 2,4 | 2,1 | 2,3 |
| 1,8 | 2,4 | 2,4 | 2,2 | 2,4 |
| 1,9 | 2,5 | 2,5 | 2,3 | 2,5 |
| 2 | 2,6 | 2,6 | 2,4 | 2,5 |
| 2,1 | 2,7 | 2,8 | 2,5 | 2,6 |
| 2,2 | 2,7 | 2,9 | 2,6 | 2,7 |
| 2,3 | 2,8 | 2,9 | 2,6 | 2,8 |
| 2,4 | 2,9 | 3,0 | 2,7 | 2,9 |
| 2,5 | 3,0 | 3,1 | 2,8 | 3,0 |
| 2,6 | 3,1 | 3,2 | 2,9 | 3,1 |
| 2,7 | 3,2 | 3,3 | 3,0 | 3,2 |
| 2,8 | 3,3 | 3,3 | 3,1 | 3,3 |
| 2,9 | 3,3 | 3,4 | 3,2 | 3,4 |
| 3 | 3,4 | 3,5 | 3,3 | 3,4 |
| 3,1 | 3,5 | 3,6 | 3,4 | 3,5 |
| 3,2 | 3,6 | 3,7 | 3,5 | 3,6 |
| 3,3 | 3,7 | 3,7 | 3,5 | 3,7 |
| 3,4 | 3,8 | 3,8 | 3,6 | 3,8 |
| 3,5 | 3,8 | 3,9 | 3,7 | 3,9 |
| 3,6 | 3,9 | 4,0 | 3,8 | 3,9 |
| 3,7 | 4,0 | 4,1 | 3,9 | 4,1 |
| 3,8 | 4,1 | 4,1 | 4,0 | 4,2 |
| 3,9 | 4,2 | 4,2 | 4,1 | 4,3 |
| 4 | 4,3 | 4,3 | 4,2 | 4,3 |
| 5,7 | 5,7 | 5,7 | 5,7 | 5,8 |


| 5,8 | 5,8 | 5,8 | 5,8 | 5,9 |
| :---: | :---: | :---: | :---: | :---: |
| 5,9 | 5,9 | 5,9 | 5,9 | 6,0 |
| 6 | 6,0 | 6,0 | 6,0 | 6,1 |

Menuiserie métallique sans rupture de pont thermique

| ug | $U w\left(W /\left(m^{2} \cdot K\right)\right)$ |  |  |  |
| :---: | :---: | :---: | :---: | :---: |
|  | Fenêtre <br> battante | Fenêtre <br> coulissante | Porte-Fenêtre <br> battante | Porte-Fenêtre <br> coulissante |
| 0,5 | 1,9 | 2,2 | 1,4 | 1,5 |
| 0,6 | 2,0 | 2,3 | 1,5 | 1,6 |
| 0,7 | 2,1 | 2,4 | 1,6 | 1,7 |
| 0,8 | 2,2 | 2,4 | 1,7 | 1,8 |
| 0,9 | 2,2 | 2,5 | 1,8 | 1,9 |
| 1 | 2,3 | 2,6 | 1,9 | 1,9 |
| 1,1 | 2,4 | 2,7 | 2,0 | 2,0 |
| 1,2 | 2,5 | 2,8 | 2,1 | 2,1 |
| 1,3 | 2,6 | 2,8 | 2,1 | 2,2 |
| 1,4 | 2,7 | 2,9 | 2,2 | 2,3 |
| 1,5 | 2,7 | 3,0 | 2,3 | 2,4 |
| 1,6 | 2,8 | 3,1 | 2,4 | 2,5 |
| 1,7 | 2,9 | 3,2 | 2,5 | 2,6 |
| 1,8 | 3,0 | 3,2 | 2,6 | 2,7 |
| 1,9 | 3,1 | 3,3 | 2,7 | 2,8 |
| 2 | 3,2 | 3,4 | 2,8 | 2,8 |
| 2,1 | 3,3 | 3,5 | 2,9 | 2,9 |
| 2,2 | 3,3 | 3,6 | 3,0 | 3,0 |
| 2,3 | 3,4 | 3,6 | 3,0 | 3,1 |
| 2,4 | 3,5 | 3,7 | 3,1 | 3,2 |
| 2,5 | 3,6 | 3,8 | 3,2 | 3,3 |
| 2,6 | 3,7 | 3,9 | 3,3 | 3,4 |
| 2,7 | 3,8 | 4,0 | 3,4 | 3,5 |
| 2,8 | 3,9 | 4,0 | 3,5 | 3,6 |
| 2,9 | 3,9 | 4,1 | 3,6 | 3,7 |
| 3 | 4,0 | 4,2 | 3,7 | 3,7 |
| 3,1 | 4,1 | 4,3 | 3,8 | 3,8 |
| 3,2 | 4,2 | 4,4 | 3,9 | 3,9 |
| 3,3 | 4,3 | 4,4 | 3,9 | 4,0 |
| 3,4 | 4,4 | 4,5 | 4,0 | 4,1 |
| 3,5 | 4,4 | 4,6 | 4,1 | 4,2 |
| 3,6 | 4,5 | 4,7 | 4,2 | 4,3 |
| 3,7 | 4,6 | 4,8 | 4,3 | 4,4 |
| 3,8 | 4,7 | 4,8 | 4,4 | 4,5 |
| 3,9 | 4,8 | 4,9 | 4,5 | 4,6 |
| 4 | 4,9 | 5,0 | 4,6 | 4,6 |
| 5,7 | 6,3 | 6,4 | 6,1 | 6,2 |
| 5,8 | 6,4 | 6,4 | 6,2 | 6,3 |
| 5,9 | 6,5 | 6,5 | 6,3 | 6,4 |

Annexe 1 - Méthode de calcul 3CL-DPE 2021

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-031.jpg?height=65&width=965&top_left_y=316&top_left_x=543)

## Menuiserie PVC

| Ug | $\operatorname{Uw}\left(W /\left(m^{2} \cdot k\right)\right)$ |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  | Fenêtre battante | Fenêtre <br> coulissante | Porte-Fenêtre <br> battante | Porte-Fenêtre <br> coulissante | Porte-Fenêtre <br> battante aved <br> soubassemen |
| 0,5 | 0,9 | 1,3 | 0,8 | 1,1 | 0,9 |
| 0,6 | 1,0 | 1,4 | 0,9 | 1,2 | 1,0 |
| 0,7 | 1,1 | 1,5 | 1,0 | 1,2 | 1,1 |
| 0,8 | 1,2 | 1,5 | 1,0 | 1,3 | 1,1 |
| 0,9 | 1,2 | 1,6 | 1,1 | 1,4 | 1,2 |
| 1 | 1,3 | 1,7 | 1,2 | 1,5 | 1,3 |
| 1,1 | 1,4 | 1,7 | 1,3 | 1,6 | 1,4 |
| 1,2 | 1,5 | 1,8 | 1,4 | 1,6 | 1,4 |
| 1,3 | 1,5 | 1,9 | 1,4 | 1,7 | 1,5 |
| 1,4 | 1,6 | 2,0 | 1,5 | 1,8 | 1,6 |
| 1,5 | 1,7 | 2,0 | 1,6 | 1,9 | 1,6 |
| 1,6 | 1,8 | 2,1 | 1,7 | 2,0 | 1,7 |
| 1,7 | 1,8 | 2,2 | 1,8 | 2,0 | 1,8 |
| 1,8 | 1,9 | 2,2 | 1,8 | 2,1 | 1,8 |
| 1,9 | 2,0 | 2,3 | 1,9 | 2,2 | 1,9 |
| 2 | 2,1 | 2,4 | 2,0 | 2,3 | 2,0 |
| 2,1 | 2,1 | 2,4 | 2,1 | 2,4 | 2,1 |
| 2,2 | 2,2 | 2,5 | 2,2 | 2,4 | 2,1 |
| 2,3 | 2,3 | 2,6 | 2,2 | 2,5 | 2,2 |
| 2,4 | 2,4 | 2,7 | 2,3 | 2,6 | 2,3 |
| 2,5 | 2,4 | 2,7 | 2,4 | 2,7 | 2,3 |
| 2,6 | 2,5 | 2,8 | 2,5 | 2,8 | 2,4 |
| 2,7 | 2,6 | 2,9 | 2,6 | 2,8 | 2,5 |
| 2,8 | 2,7 | 2,9 | 2,6 | 2,9 | 2,5 |
| 2,9 | 2,7 | 3,0 | 2,7 | 3,0 | 2,6 |
| 3 | 2,8 | 3,1 | 2,8 | 3,1 | 2,7 |
| 3,1 | 2,9 | 3,1 | 2,9 | 3,2 | 2,8 |
| 3,2 | 3,0 | 3,2 | 3,0 | 3,2 | 2,8 |
| 3,3 | 3,0 | 3,3 | 3,0 | 3,3 | 2,9 |
| 3,4 | 3,1 | 3,4 | 3,1 | 3,4 | 3,0 |
| 3,5 | 3,2 | 3,4 | 3,2 | 3,5 | 3,0 |
| 3,6 | 3,3 | 3,5 | 3,3 | 3,6 | 3,1 |
| 3,7 | 3,3 | 3,6 | 3,4 | 3,6 | 3,2 |
| 3,8 | 3,4 | 3,6 | 3,4 | 3,7 | 3,2 |
| 3,9 | 3,5 | 3,7 | 3,5 | 3,8 | 3,3 |
| 4 | 3,6 | 3,8 | 3,6 | 3,9 | 3,4 |
| 5,7 | 4,8 | 5,0 | 5,0 | 5,2 | 4,6 |
| 5,8 | 4,9 | 5,0 | 5,0 | 5,3 | 4,6 |
| 5,9 | 5,0 | 5,1 | 5,1 | 5,4 | 4,7 |

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-032.jpg?height=63&width=1399&top_left_y=314&top_left_x=334)

## - Menuiserie bois ou bois métal

Dans tous les calculs, les menuiseries mixtes bois métal prendront les caractéristiques du bois.

| Ug | $\operatorname{Uw}\left(\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$ |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  | Fenêtre <br> battante | Fenêtre <br> coulissante | Porte-Fenêtre <br> battante | Porte-Fenêtre <br> coulissante | Porte-Fenêtre battante <br> avec soubassement |
| 0,5 | 1,1 | 1,2 | 0,9 | 1,0 | 1,1 |
| 0,6 | 1,2 | 1,3 | 1,0 | 1,1 | 1,2 |
| 0,7 | 1,3 | 1,4 | 1,1 | 1,2 | 1,2 |
| 0,8 | 1,4 | 1,4 | 1,2 | 1,2 | 1,3 |
| 0,9 | 1,4 | 1,5 | 1,2 | 1,3 | 1,4 |
| 1 | 1,5 | 1,6 | 1,3 | 1,4 | 1,4 |
| 1,1 | 1,6 | 1,7 | 1,4 | 1,5 | 1,5 |
| 1,2 | 1,7 | 1,8 | 1,5 | 1,6 | 1,6 |
| 1,3 | 1,8 | 1,9 | 1,6 | 1,7 | 1,7 |
| 1,4 | 1,8 | 2,0 | 1,7 | 1,7 | 1,7 |
| 1,5 | 1,9 | 2,1 | 1,8 | 1,8 | 1,8 |
| 1,6 | 2,0 | 2,1 | 1,8 | 1,9 | 1,9 |
| 1,7 | 2,1 | 2,2 | 1,9 | 2,0 | 1,9 |
| 1,8 | 2,2 | 2,3 | 2,0 | 2,1 | 2,0 |
| 1,9 | 2,2 | 2,4 | 2,1 | 2,2 | 2,1 |
| 2 | 2,3 | 2,4 | 2,2 | 2,3 | 2,1 |
| 2,1 | 2,4 | 2,5 | 2,3 | 2,3 | 2,2 |
| 2,2 | 2,5 | 2,6 | 2,3 | 2,4 | 2,3 |
| 2,3 | 2,6 | 2,7 | 2,4 | 2,5 | 2,4 |
| 2,4 | 2,6 | 2,7 | 2,5 | 2,6 | 2,4 |
| 2,5 | 2,7 | 2,8 | 2,6 | 2,7 | 2,5 |
| 2,6 | 2,8 | 2,9 | 2,7 | 2,8 | 2,6 |
| 2,7 | 2,9 | 3,0 | 2,8 | 2,9 | 2,6 |
| 2,8 | 3,0 | 3,0 | 2,9 | 2,9 | 2,7 |
| 2,9 | 3,0 | 3,1 | 2,9 | 3,0 | 2,8 |
| 3 | 3,1 | 3,2 | 3,0 | 3,1 | 2,8 |
| 3,1 | 3,2 | 3,3 | 3,1 | 3,2 | 2,9 |
| 3,2 | 3,3 | 3,3 | 3,2 | 3,3 | 3,0 |
| 3,3 | 3,4 | 3,4 | 3,3 | 3,4 | 3,1 |
| 3,4 | 3,4 | 3,5 | 3,4 | 3,4 | 3,1 |
| 3,5 | 3,5 | 3,6 | 3,5 | 3,5 | 3,2 |
| 3,6 | 3,6 | 3,6 | 3,5 | 3,6 | 3,3 |
| 3,7 | 3,7 | 3,7 | 3,6 | 3,7 | 3,3 |
| 3,8 | 3,8 | 3,8 | 3,7 | 3,8 | 3,4 |
| 3,9 | 3,8 | 3,9 | 3,8 | 3,9 | 3,5 |
| 4 | 3,9 | 3,9 | 3,9 | 4,0 | 3,5 |
| 5,7 | 5,3 | 5,3 | 5,3 | 5,4 | 4,7 |

29

Annexe 1 - Méthode de calcul 3CL-DPE 2021

| 5,8 | 5,4 | 5,4 | 5,4 | 5,5 | 4,8 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 5,9 | 5,4 | 5,4 | 5,5 | 5,6 | 4,9 |
| 6 | 5,5 | 5,5 | 5,6 | 5,7 | 4,9 |

## - Traitement des doubles fenêtres

$$
U w=\frac{1}{\frac{1}{U w 1}+\frac{1}{U w 2}+0,07}
$$

$U w 1$ et $U w 2$ sont respectivement le coefficient de transmission thermique des fenêtres 1 et $2\left(\mathrm{~W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)\right)$

Chaque fenêtre du complexe doit donc être caractérisée pour déterminer la performance de la double fenêtre.

Si le Uw d'une menuiserie est connu et justifié, le saisir directement.

### 3.3.3 Coefficients Ujn des fenêtres/portes-fenêtres

La présence de volets aux fenêtres et portes-fenêtres leur apporte un supplément d'isolation avec une résistance additionnelle $\Delta R$.

| Fermetures | $\Delta R\left(m^{2} . \mathrm{K} / \mathrm{W}\right)$ |
| :--- | :---: |
| Jalousie accordéon, fermeture à lames orientables y compris les vénitiens <br> extérieurs tout métal, volets battants ou persiennes avec ajours fixes | 0,08 |
| Fermeture sans ajours en position déployée, volets roulants alu | 0,15 |
| Volets roulants PVC ou bois ( $e \leq 12 \mathrm{~mm})$ | 0,19 |
| Persienne coulissante et volet battant PVC ou bois $(e \leq 22 \mathrm{~mm})$ | 0,19 |
| Volets roulants PVC ou bois ( $e>12 \mathrm{~mm})$ | 0,25 |
| Persienne coulissante et volet battant PVC ou bois $(e>22 \mathrm{~mm})$ | 0,25 |
| Fermeture isolée sans ajours en position déployée | 0,25 |
| Note : $e$ est l'épaisseur du tablier. |  |

Dans la suite, les Ujn associés à des Uw non présents dans les tableaux peuvent être obtenus par interpolation ou extrapolation avec les deux Uw tabulés les plus proches.

|  | Ujn pour une valeur de résistance supplémentaire $\Delta R\left(\right.$ en $^{2} \mathrm{~m}^{2} . \mathrm{K} / \mathrm{W}$ ) de : |  |  |  |
| :---: | :---: | :---: | :---: | :---: |
| Uw <br> $\mathrm{W} /\left(\mathrm{m}^{2} . \mathrm{K}\right)$ | 0,08 | 0,15 | 0,19 | 0,25 |
| 0,8 | 0,8 | 0,8 | 0,7 | 0,7 |
| 0,9 | 0,9 | 0,8 | 0,8 | 0,8 |
| 1 | 1,0 | 0,9 | 0,9 | 0,9 |
| 1,1 | 1,1 | 1,0 | 1,0 | 1,0 |
| 1,2 | 1,1 | 1,1 | 1,1 | 1,1 |
| 1,3 | 1,2 | 1,2 | 1,2 | 1,1 |
| 1,4 | 1,3 | 1,3 | 1,3 | 1,2 |
| 1,5 | 1,4 | 1,4 | 1,3 | 1,3 |
| 1,6 | 1,5 | 1,5 | 1,4 | 1,4 |


| 1,7 | 1,6 | 1,5 | 1,5 | 1,4 |
| :---: | :---: | :---: | :---: | :---: |
| 1,8 | 1,7 | 1,6 | 1,6 | 1,5 |
| 1,9 | 1,8 | 1,7 | 1,6 | 1,6 |
| 2 | 1,9 | 1,8 | 1,7 | 1,7 |
| 2,1 | 1,9 | 1,9 | 1,8 | 1,7 |
| 2,2 | 2,0 | 1,9 | 1,9 | 1,8 |
| 2,3 | 2,1 | 2,0 | 2,0 | 1,9 |
| 2,4 | 2,2 | 2,1 | 2,0 | 2,0 |
| 2,5 | 2,3 | 2,2 | 2,1 | 2,0 |
| 2,6 | 2,4 | 2,3 | 2,2 | 2,1 |
| 2,7 | 2,5 | 2,3 | 2,2 | 2,2 |
| 2,8 | 2,5 | 2,4 | 2,3 | 2,2 |
| 2,9 | 2,6 | 2,5 | 2,4 | 2,3 |
| 3 | 2,7 | 2,6 | 2,5 | 2,4 |
| 3,1 | 2,8 | 2,6 | 2,5 | 2,4 |
| 3,2 | 2,9 | 2,7 | 2,6 | 2,5 |
| 3,3 | 3,0 | 2,8 | 2,7 | 2,6 |
| 3,4 | 3,0 | 2,9 | 2,7 | 2,6 |
| 3,5 | 3,1 | 2,9 | 2,8 | 2,7 |
| 3,6 | 3,2 | 3,0 | 2,9 | 2,7 |
| 3,7 | 3,3 | 3,1 | 2,9 | 2,8 |
| 3,8 | 3,4 | 3,1 | 3,0 | 2,9 |
| 3,9 | 3,4 | 3,2 | 3,1 | 2,9 |
| 4 | 3,5 | 3,3 | 3,1 | 3,0 |
| 4,1 | 3,6 | 3,4 | 3,2 | 3,1 |
| 4,2 | 3,7 | 3,4 | 3,3 | 3,1 |
| 4,3 | 3,7 | 3,5 | 3,3 | 3,2 |
| 4,4 | 3,8 | 3,6 | 3,4 | 3,2 |
| 4,5 | 3,9 | 3,6 | 3,5 | 3,3 |
| 4,6 | 4,0 | 3,7 | 3,5 | 3,4 |
| 4,7 | 4,1 | 3,8 | 3,6 | 3,4 |
| 4,8 | 4,1 | 3,8 | 3,7 | 3,5 |
| 4,9 | 4,2 | 3,9 | 3,7 | 3,6 |
| 5 | 4,3 | 4,0 | 3,8 | 3,6 |
| 5,1 | 4,4 | 4,0 | 3,8 | 3,7 |
| 5,2 | 4,4 | 4,1 | 3,9 | 3,7 |
| 5,3 | 4,5 | 4,2 | 4,0 | 3,8 |
| 5,4 | 4,6 | 4,2 | 4,0 | 3,8 |
| 5,5 | 4,7 | 4,3 | 4,1 | 3,9 |
| 5,6 | 4,7 | 4,4 | 4,2 | 4,0 |
| 5,7 | 4,8 | 4,4 | 4,2 | 4,0 |
| 5,8 | 4,9 | 4,5 | 4,3 | 4,1 |
| 5,9 | 5,0 | 4,6 | 4,3 | 4,1 |
| 6 | 5,0 | 4,6 | 4,4 | 4,2 |
| 6,1 | 5,1 | 4,7 | 4,5 | 4,3 |
| 6,2 | 5,2 | 4,8 | 4,5 | 4,3 |
| 6,3 | 5,2 | 4,8 | 4,6 | 4,4 |
| 6,4 | 5,3 | 4,9 | 4,6 | 4,4 |


| 6,5 | 5,4 | 5,0 | 4,7 | 4,5 |
| :--- | :--- | :--- | :--- | :--- |
| 6,6 | 5,5 | 5,0 | 4,8 | 4,5 |

Si le Ujn d'une menuiserie est connu et justifié, le saisir directement.

### 3.3.4 Coefficients $U$ des portes

Si le coefficient U des portes est connu et justifié, le saisir directement. Sinon, prendre les valeurs tabulées ci-dessous :

| Nature de la menuiserie | Type de porte | Uporte $W /\left(m^{2} . K\right)$ |
| :---: | :---: | :---: |
| Porte simple en bois ou <br> PVC | Porte opaque pleine | 3,5 |
|  | Porte avec moins de $30 \%$ de vitrage <br> simple | 4 |
|  | Porte avec $30-60 \%$ de vitrage simple | 4,5 |
|  | Porte avec double vitrage | 3,3 |
| Porte simple en métal | Porte opaque pleine | 5,8 |
|  | Porte avec vitrage simple | 5,8 |
|  | Porte avec moins de $30 \%$ de double <br> vitrage | 5,5 |
|  | Porte avec $30-60 \%$ de double vitrage | 4,8 |
| Toute menuiserie | Porte opaque pleine isolée | 1,5 |
|  | Porte précédée d'un SAS | 1,5 |
|  | Porte isolée avec double vitrage | 1,5 |

Attention : une porte vitrée avec plus de $60 \%$ de vitrage est traitée comme une porte-fenêtre avec soubassement.

### 3.4 Calcul des déperditions par les ponts thermiques

## Données d'entrée :

Type d'isolation (ITI, ITE, ITR)

Nombre de niveaux

Nombre d'appartements

Retour d'isolation autour des menuiseries (avec ou sans)

Hauteur moyenne sous plafond

Linéaires de pont thermique

Position des menuiseries (nu extérieur, nu intérieur, tunnel)

$$
\begin{aligned}
& P T=\sum_{i, j} k_{p b_{-} i / m_{-} j} * l_{p b_{-} i / m_{-} j}+\sum_{i, j} k_{p i_{-} i / m_{-} j} * l_{p i_{-} i / m_{-} j}+\sum_{j} k_{r f / m_{-} j} * l_{r f / m_{-} j}+\sum_{i, j} k_{p h_{-} i / m_{-} j} * l_{p h_{-} i / m_{-} j} \\
&+\sum_{i, j} k_{m e n_{-} i / m_{-} j} * l_{m e n_{-} i / m_{-} j}
\end{aligned}
$$

Avec :

- $\quad \mathrm{k}_{\mathrm{pb} \_} \mathrm{i} / \mathrm{m}_{j}$ : valeur du pont thermique de la liaison plancher bas i mur $\mathrm{j}$ (W/(m.K)) (définie ci-après)
- $\quad \mathrm{k}_{\text {pi_i }} / \mathrm{m} \mathrm{j}$ : valeur du pont thermique de la liaison plancher intermédiaire i mur $\mathrm{j}$ (W/(m.K)) (définie ci-après)
- $\quad \mathrm{k}_{\mathrm{rf} / \mathrm{m} j}:$ valeur du pont thermique de la liaison refend mur $\mathrm{j}(W /(m . K))$ (définie ci-après)

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-036.jpg?height=46&width=1339&top_left_y=474&top_left_x=301)

- $\quad k_{\text {men_ } / \mathrm{m} j}$ : valeur du pont thermique de la liaison menuiserie i mur $j(W /(m . K))$ (définie ci-après)
- $I_{p b ~} / / m j$ : longueur du pont thermique plancher bas i mur $j(m)$. Il prend en compte les seuils des portes et portefenêtre
- $\quad I_{\text {pi_i } / m \jmath}:$ longueur du pont thermique plancher intermédiaire i mur j $(m)$
- $\quad I_{\text {ph_i/mj }}:$ longueur du pont thermique plancher haut i mur $j(m)$
- $I_{\mathrm{rf} / \mathrm{m} j}:$ longueur du pont thermique refend mur $\mathrm{j}(\mathrm{m})$ En immeuble collectif d'habitation, la longueur totale forfaitaire du pont thermique refend mur est :

$$
l_{r f / m_{-} j}=2 * H s p *\left(N b_{l g t}-N i v\right)
$$

Avec :

- Hsp : hauteur moyenne sous plafond
- $\mathrm{Nb}_{\text {lgt }}:$ nombre d'appartements
- Niv : nombre de niveaux de logements
- $\quad I_{\text {men_i/mj }}:$ longueur du pont thermique menuiserie i mur j $(m)$
- ITI, ITE, ITR respectivement isolation thermique intérieure, extérieure et répartie.

Si l'état d'isolation d'une paroi est inconnu :

- Pour les bâtiments d'avant 1975, la paroi est considérée comme non isolée ;
- $\quad$ Pour les bâtiments construits à partir de 1975 :
- Les murs sont considérés comme isolés par l'intérieur ;
- Les plafonds sont considérés isolés par l'extérieur ;
- Les planchers sur terre-plein sont considérés non isolés avant 2001 et isolés par l'extérieur (en sous face) à partir de 2001 ;
- Les autres planchers sont considérés isolés par l'extérieur.

Dans la suite, les murs en ossature bois sont traités comme des murs à isolation répartie.

Si les valeurs des ponts thermiques sont connues et justifiées, les saisir directement pour le calcul, à l'exception des ponts thermiques négligés dans les valeurs par défaut. Sinon les valeurs par défaut proposées dans la suite peuvent être utilisées.

Les ponts thermiques des parois au niveau des circulations communes ne sont pas pris en compte.

Aucun coefficient de réduction des températures (b) n'est appliqué aux ponts thermiques.

Seuls les ponts thermiques entre parois lourdes ou entre une paroi et une menuiserie sont conservés.

Le schéma ci-dessous permet d'identifier les différents types de ponts thermiques.

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-037.jpg?height=1862&width=1422&top_left_y=385&top_left_x=317)

Pth Plancher intermédiaire / mur

Exemple de représentations de ponts thermiques

### 3.4.1 Mur Plancher bas / mur

$\mathbf{k}_{\text {pb } \_/ \mathrm{m} j}$ : Valeur du pont thermique de la liaison Plancher bas $\mathrm{i} /$ Mur j j (W/(m.K))

| kpb_i/mj |  | Plancher Bas |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
|  |  | Non Isolé | $\|T\|$ | ITE | ITI + ITE |
| Mur <br> extérieur | Non Isolé | 0,39 | 0,47 | 0,8 | 0,47 |
|  | ITI | 0,31 | 0,08 | 0,71 | 0,08 |
|  | ITE | 0,49 | 0,48 | 0,64 | 0,48 |
|  | ITR | 0,35 | 0,1 | 0,45 | 0,1 |
|  | ITI + ITE | 0,31 | 0,08 | 0,45 | 0,08 |
|  | ITI + ITR | 0,31 | 0,08 | 0,45 | 0,08 |
|  | ITE + ITR | 0,35 | 0,1 | 0,45 | 0,1 |

Seuls les murs et planchers bas constitués d'un matériau lourd (béton, brique, ...) sont considérés ici. Pour les autres cas ce pont thermique est pris nul.

Pour les murs, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITI.

Pour les planchers bas, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITE.

Pour un plancher bas, ITI correspond à une isolation sous chape et ITE à une isolation en sous face.

Les planchers en hourdis polystyrène sont traités comme des planchers avec ITE.

### 3.4.2 Plancher intermédiaire / mur

$\mathbf{k}_{\text {pi_ } 1 / \mathrm{m} j} \mathbf{j}$ Valeur du pont thermique de la liaison Plancher intermédiaire i/Mur j (W/(m.K))

|  | $\mathrm{k}_{\text {pi_i_i_m_j }}$ |  |
| :---: | :---: | :---: |
|  | Non Isolé | 0,86 |
|  | ITI | 0,92 |
|  | ITE | 0,13 |
|  | ITR | 0,24 |
|  | ITI + ITE | 0,13 |
|  | ITI + ITR | 0,24 |
|  | ITE + ITR | 0,13 |

Seuls les murs et planchers constitués d'un matériau lourd (béton, brique, ...) sont considérés ici. Pour les autres cas ce pont thermique est pris nul.

Pour les murs, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITI.

Les ponts thermiques des planchers intermédiaires en structure légère (ossature bois ou autre matériau) / murs sont négligés.

Lorsque le plancher intermédiaire ne sépare pas deux niveaux du lot faisant l'objet du DPE, il faut prendre en compte dans les calculs seulement la moitié de la valeur tabulée ci-dessus.

### 3.4.3 Plancher haut / mur

$\mathbf{k}_{\text {ph } \_ \text {i/m } j}$ : Valeur du pont thermique de la liaison Plancher haut i/Mur j (W/(m.K))

Terrasse ou plancher haut lourd :

|  |  | Plancher Haut |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: |
| $\mathrm{k}_{\text {ph_i/m }}$ j |  |  |  |  |  |
|  |  | $\frac{\text { Non Isolé }}{0,3}$ | ![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-039.jpg?height=97&width=85&top_left_y=653&top_left_x=1100) | ITE <br> 0,4 | $\frac{\mathrm{ITI}+\mathrm{ITE}}{0,4}$ |
| Mur <br> extérieur | Non Isolé |  |  |  |  |
|  | ITI | 0,27 | 0,07 | 0,75 | 0,07 |
|  | ITE | 0,55 | 0,76 | 0,58 | 0,58 |
|  | ITR | 0,4 | 0,3 | 0,48 | 0,3 |
|  | ITI + ITE | 0,27 | 0,07 | 0,58 | 0,07 |
|  | ITT + ITR | 0,27 | 0,07 | 0,48 | 0,07 |
|  | ITE + ITR | 0,4 | 0,3 | 0,48 | 0,3 |

Pour les murs, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITI.

Pour les planchers haut, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITE.

Pour un plancher haut, ITI correspond à une isolation sous plancher haut et ITE à une isolation sur plancher haut.

Les ponts thermiques des planchers haut en structure légère sont négligés.

### 3.4.4 Refend / mur

$\mathbf{k}_{\mathrm{r} / \mathrm{m} j}$ : Valeur du pont thermique de la liaison Refend/Mur $\mathrm{j}(\mathrm{W} /(\mathrm{m} . \mathrm{K}))$

|  | $\mathrm{k}_{\mathrm{rf} / \mathrm{m} j}$ |  |
| :---: | :---: | :---: |
|  | Non Isolé | 0,73 |
|  | ITI | 0,82 |
|  | ITE | 0,13 |
|  | ITR | 0,2 |
|  | ITI + ITE | 0,13 |
|  | ITI ITR | 0,2 |
|  | ITE + ITR | 0,13 |

Seuls les murs et refends constitués d'un matériau lourd (béton, brique, ...) sont considérés ici. Pour les autres cas, ce pont thermique est pris nul.

Pour les murs, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITI.

Les ponts thermiques des parois sur circulation sont négligés pour les appartements et les immeubles.

Lorsque le refend ne sépare pas deux volumes du même lot faisant l'objet du DPE, il faut prendre en compte dans les calculs seulement la moitié de la valeur tabulée ci-dessus.

### 3.4.5 Menuiserie / mur

$\mathbf{k}_{\text {men_i } \mathbf{i} / \mathrm{j}}:$ Valeur du pont thermique de la liaison Menuiserie i/Mur j $(W /(m . K))$

On entend par menuiserie les fenêtres, portes ou portes-fenêtres.

|  | $\mathrm{k}_{\text {men_i }} / \mathrm{m} \mathrm{j}$ | Menuiserie |  |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  |  | Au nu <br> extérieur |  | En tunnel |  | Au nu <br> intérieur |  |
|  |  | $L p=5$ | $L p=10$ | $L p=5$ | $L p=10$ | $\mathrm{Lp}=5$ | $L p=10$ |
| Mur | Non isolé | 0,43 | 0,29 | 0,31 | 0,19 | 0,38 | 0,25 |
|  | ITI avec retour d'isolant | 0,22 | 0,18 | 0,16 | 0,13 | 0 | 0 |
|  | ITI sans retour d'isolant | 0,43 | 0,29 | 0,31 | 0,19 | 0 | 0 |
|  | ITE avec retour d'isolant | 0 | 0 | 0,19 | 0,15 | 0,25 | 0,2 |
|  | ITE sans retour d'isolant | 0 | 0 | 0,45 | 0,4 | 0,9 | 0,8 |
|  | ITR | 0,2 |  |  |  |  |  |
|  | ITI+ITE avec retour d'isolant | 0 | 0 | 0,16 | 0,13 | 0 | 0 |
|  | ITI+ITE sans retour d'isolant | 0 | 0 | 0,31 | 0,19 | 0 | 0 |
|  | ITI+ITR avec retour d'isolant | 0,2 | 0,18 | 0,16 | 0,13 | 0 | 0 |
|  | ITI+ITR sans retour d'isolant | 0,2 | 0,2 | 0,2 | 0,19 | 0 | 0 |
|  | ITE+ITR avec retour d'isolant | 0 | 0 | 0,19 | 0,15 | 0,2 | 0,2 |
|  | ITE+ITR sans retour d'isolant | 0 | 0 | 0,2 | 0,2 | 0,2 | 0,2 |

Avec :

- Lp est la largeur approximative (arrondie à la valeur la plus proche apparaissant dans le tableau) du dormant de la menuiserie $(\mathrm{cm})$.

En cas de double-fenêtre, la largeur du dormant est la plus importante des deux.

Pour les murs, s'il n'est pas possible de distinguer le type d'isolation (ITI, ITE...), prendre par défaut ITI.

Ces valeurs de pont thermique sont valables pour les appuis, tableaux et le linteau de la menuiserie.

Les ponts thermiques au niveau des seuils de porte et de porte-fenêtre ne sont pas pris en compte.

Les ponts thermiques avec les parois en structure bois (ossature bois, rondin de bois, pans de bois) sont négligés.

Les ponts thermiques au niveau des fenêtres de toit sont négligés.

Les ponts thermiques pour la liaison mur / pavés de verre, plancher pavé de verre et plafond pavés de verre ne sont pas pris en compte.