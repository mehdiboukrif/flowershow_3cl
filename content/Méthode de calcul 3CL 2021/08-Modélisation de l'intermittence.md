---
dg-publish: true
dg-home: false
---
## 8 Modélisation de l'intermittence

## Données d'entrée :

Type de bâtiment

Type de chauffage (divisé, central)

Type de régulation (par pièce ou non)

Equipement d'intermittence (absent, central sans minimum de température, ...)

Type d'émetteur (air soufflé, convecteurs,

Présence d'un comptage

Hauteur moyenne sous plafond

Le facteur d'intermittence traduit les baisses temporaires de température, réalisées pour différentes raisons, absence, ralenti de nuit et éventuellement de façon inégale dans les pièces.

Il est égal au rapport entre les besoins réels, compte tenu d'un comportement moyen des occupants, et les besoins théoriques. Le facteur d'intermittence est donné par la formule :

$$
I N T=\frac{I o}{1+0,1 *(G-1)}
$$

Avec :

$$
G=\frac{G V}{H s p * S h}
$$

- GV : déperditions annuelles de l'enveloppe (W/K) (déterminé en partie 3)
- Sh : surface habitable $\left(m^{2}\right)$
- Hsp : hauteur moyenne sous plafond ( $m$ )

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-058.jpg?height=754&width=1688&top_left_y=1782&top_left_x=184)

|  | pièce par <br> pièce | Plancher chauffant | 0,92 | 0,91 | 0,90 | - |  | 0,94 | 0,93 | 0,92 |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |

Une maison individuelle branchée sur un réseau collectif de fourniture d'énergie pour le chauffage sera traitée comme une maison individuelle avec un chauffage individuel central.

| {10 <br> Pour les immeubles collectifs avec chauffage <br> individuel} |  |  | Équipements d'intermittence |  |  |  |  |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  |  |  | Absent <br> 0,90 | Central sans <br> minimum de <br> température <br> 0,89 | Central avec <br> minimum de <br> température <br> 0,88 | Par pièce avec <br> minimum de <br> température <br> 0,86 | Par pièce avec minimum <br> de température et <br> détection de présence <br> 0,83 |
| Chauffage <br> divisé | Avec régulation <br> pièce par pièce | Air soufflé |  |  |  |  |  |
|  |  | Radiateur/Convecteur | 0,90 | 0,89 | 0,88 | 0,86 | 0,83 |
|  |  | Plafond chauffant | 0,90 | 0,89 | 0,88 | 0,86 | 0,83 |
|  |  | Plancher chauffant | 0,95 | 0,94 | 0,93 | 0,91 | - |
| Chauffage <br> central | Avec régulation <br> pièce par pièce | Air soufflé | 0,91 | 0,90 | 0,89 | 0,87 | 0,84 |
|  |  | Radiateur | 0,93 | 0,92 | 0,91 | 0,89 | 0,86 |
|  |  | Plafond chauffant | 0,93 | 0,92 | 0,91 | 0,89 | 0,86 |
|  |  | Plancher chauffant | 0,95 | 0,94 | 0,93 | 0,91 | - |
|  | Sans régulation <br> pièce par pièce | Air soufflé | 0,95 | 0,94 | 0,93 | - |  |
|  |  | Radiateur | 0,96 | 0,95 | 0,94 | - |  |
|  |  | Plafond chauffant | 0,96 | 0,95 | 0,94 | - |  |
|  |  | Plancher chauffant | 0,97 | 0,96 | 0,95 | - |  |

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-059.jpg?height=565&width=1671&top_left_y=1274&top_left_x=201)

En immeuble collectif, le chauffage mixte, c'est-à-dire dont une partie est facturée collectivement et une autre individuellement, est traité au niveau de l'intermittence comme un système collectif avec comptage individuel.

Seule l'intermittence de l'appoint est prise en compte sur les installations base + appoint. Une régulation zonale peut être considérée comme une régulation pièce par pièce.

L'équipement d'intermittence peut être :

- En chauffage individuel
- Absent : pas d'équipement permettant de programmer des réduits de température ;
- Central sans minimum de température : équipements permettant une programmation seulement de la fonction marche arrêt et donc ne garantissant pas un minimum de température ;
- Central avec un minimum de température : équipement pouvant assurer :
- Centralement un ralenti ou un abaissement de température fixe, non modifiable par l'occupant, ainsi que la fonction hors gel ;
- Centralement un ralenti ou un abaissement de température au choix de l'occupant ;
- Pièce par pièce avec minimum de température : équipement permettant d'obtenir par pièce un ralenti ou un abaissement de température fixe, non modifiable par l'occupant.
- En chauffage collectif
- Absent : pas de réduit de nuit ;
- Central collectif : possibilité de ralenti de nuit.

Un plancher chauffant avec une régulation zone jour/zone nuit peut être associée à une régulation pièce par pièce.

Un poêle sera modélisé comme un radiateur/convecteur pour la détermination de l'intermittence.

Un système de chauffage divisé est un système pour lequel la génération et l'émission sont confondues. C'est le cas des convecteurs électriques, planchers chauffants électriques, $\ldots$

Un système de chauffage central comporte un générateur central, individuel ou collectif, et une distribution par fluide chauffant : air ou eau.