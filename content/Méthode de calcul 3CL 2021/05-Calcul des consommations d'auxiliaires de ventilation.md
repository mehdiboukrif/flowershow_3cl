---
dg-publish: true
dg-home: false
---
## 5 Calcul des consommations d'auxiliaires de ventilation

## Données d'entrée :

Type de VMC

Type de bâtiment

## Surface habitable

La consommation annuelle d'auxiliaires de ventilation (kWhef/an) est donnée par la formule :

$$
\text { Caux }=8760 * \frac{\text { Pvent }_{\text {moy }}}{1000}
$$

Avec :

- $\quad$ Pvent $_{\text {moy }}$ : puissance moyenne des auxiliaires (W)
- Pvent $_{\text {mov }}$ en maison individuelle :

| Puent $_{\text {moy }}$ | jusqu'à 2012 | Après 2012 |
| :---: | :---: | :---: |
| Simple Flux Auto | 65 W-ThC | 35 W-ThC |
| Simple Flux hygro | 50 W-ThC | 15 W-ThC |
| Double Flux | 80 W-ThC | 35 W-ThC |

Les puissances d'auxiliaires tabulées ci-dessus pour les VMC double flux intègrent les puissances du soufflage et de l'extraction

- Pvent $_{\text {mov }}$ en immeuble collectif:

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-044.jpg?height=53&width=558&top_left_y=1938&top_left_x=769)

![](https://cdn.mathpix.com/cropped/2024_05_08_6c6a39962cbc46e343eag-044.jpg?height=35&width=1379&top_left_y=2030&top_left_x=424)
4)

- Sh : surface habitable $\left(m^{2}\right)$
- Pvent : puissance des auxiliaires $\left(W /\left(m^{3} / h\right)\right)$ :

|  | Jusqu'à 2012 | Après 2012 |
| :---: | :---: | :---: |
| Simple Flux Auto réglable | $0,46 \mathrm{~W}-\mathrm{ThC} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ | $0,25 \mathrm{~W}-\mathrm{Th} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ |
| Simple Flux hygro réglable | $0,46 \mathrm{~W}-\mathrm{ThC} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ | $0,25 \mathrm{~W}-\mathrm{Th} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ |
| Double Flux Auto réglable | $1,1 \mathrm{~W}-\mathrm{Th} \mathrm{Th} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ | $0,6 \mathrm{~W}-\mathrm{Th} \mathrm{C} /\left(\mathrm{m}^{3} / \mathrm{h}\right)$ |

Les puissances d'auxiliaires des VMC basse pression sont les mêmes que pour les VMC classiques.

41

Annexe 1 - Méthode de calcul 3CL-DPE 2021

Les puissances d'auxiliaires tabulées ci-dessus pour les VMC double flux intègrent les puissances du soufflage et de l'extraction.

- Ventilation Hybride :

On considère que le système bascule d'un mode mécanique à un mode naturel et inversement. Les consommations d'auxiliaire ont lieu pendant le mode de fonctionnement mécanique.

Par défaut la durée de fonctionnement de l'extracteur mécanique est prise pour le mode grand débit :

|  | Durée d'utilisation en grand débit <br> (en $\mathrm{h} /$ semaine) |
| :---: | :---: |
| Collectif | 28 |
| individuel | 14 |

Les consommations d'auxiliaires pour une VMC hybride correspondent aux consommations d'une VMC classique autoréglable de 2001 à 2012 multipliées par le ratio du temps d'utilisation :

|  | Ratio du temps d'utilisation du <br> mode mécanique |
| :---: | :---: |
| Collectif | 0,167 |
| individuel | 0,083 |
