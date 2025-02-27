# Ecrans AndroidAPS

## Écran d'accueil

![Écran d'accueil V2.5](../images/Screenshot_Home_screen_V2_5_1.png)

Ceci est le premier écran que vous verrez quand vous ouvrirez AndroidAPS et il contient la plupart des informations dont vous aurez besoin au jour le jour.

### Section A

* naviguer entre les différents modules AndroidAPS en balayant à gauche ou à droite

### Section B

* changer le statut de la boucle (boucle ouverte, boucle fermée, suspendre la boucle etc)
* voir votre profil actif et faire un [changement de profil](../Usage/Profiles.md)
* voir votre niveau actuel de cible glycémique et définir une [cible temporaire](../Usage/temptarget.md).

Un appui long sur n’importe lequel de ces boutons permet de modifier les paramètres. Par ex. un appui long sur la cible en haut à droite ("110" dans la copie d'écran ci-dessus) pour définir une cible temp.

### Section C

* dernière glycémie reçue de votre MGC
* depuis combien de temps elle a été reçue
* les changements dans les 15 et 40 dernières minutes
* votre débit de basal - y compris les débits de base temporaires (DBT) programmés par le système
* Insuline Active (IA)
* Glucides Actifs (GA)

Les [voyants d'état optionnels](../Configuration/Preferences#overview) (CAN | INS | RES | SEN | BAT) donnent un avertissement visuel pour un réservoir bas et le niveau de batterie ainsi que le changement de site en retard.

Le chiffre de l’insuline active serait à 0 s’il n’y avait que votre basal standard en cours et qu’il ne restait plus d’insuline active d’un précédent bolus. Les chiffres entre parenthèses indiquent le niveau d’insuline restant d’un bolus précédent et de combien est la variation de basal due à un précédent débit basal temporaire (DBT) programmé par AndroidAPS (AAPS). Ce second chiffre peut être négatif s’il y a eu récemment des périodes de basal réduit.

### Section D

Cliquez sur la flèche située à droite de l'écran de la section D pour sélectionner les informations à afficher dans les graphiques ci-dessous.

### Section E

Graphique montrant votre glycémie (GLY) lue à partir de votre capteur de glycémie (MGC), il montre également des notifications Nightscout telles que les glycémies capillaires de calibrations et des entrées de glucides.

Une pression longue sur le graphique permet de changer l'échelle de temps. Vous pouvez choisir 6, 8, 12, 18 ou 24 heures.

Le prolongement des lignes indique la glycémie prévue, et la tendance, si vous avez sélectionné cette option.

* Ligne **orange** : [Glucides Actifs (GA)](../Usage/COB-calculation.rst) (la couleur est généralement utilisée pour représenter les Glucides)
* Ligne **bleu foncé** : Insuline Active (IA) (la couleur est généralement utilisée pour représenter l'insuline)
* Ligne **bleu clair** ligne : zéro-temp (glycémie prévisionnelle si un débit de base temporaire à 0% était défini)
* Ligne **jaune foncé**: [RNS](../Configuration/Sensitivity-detection-and-COB#sensitivity-oref1) (Repas Non Signalés)

These lines show you the different predictions based on current carb absorption (COB); insulin only (IOB); showing how long it will take BG to level off at/above target if deviations suddenly cease and we run a zero temp until then (zero-temp) and unannounced meal/effect detection where carbs are detected but have not been entered into the system by the user (UAM).

La ligne **bleu continu** indique le débit de base de votre pompe. La ligne **bleue pointillée** correspond au débit de basal du profil sélectionné sans débits de basal temporaires (DBT) et la ligne bleue continue est le débit réel distribué au fil du temps.

La ligne **fine jaune** indique l'activité de l'insuline, calculée par votre profil d'insuline (elle n'est pas dérivée de l'IA). La valeur est plus élevée quand l'insuline délivrée est proche de son pic d'activité. It would mean to be negative when IOB is decreasing.

### Section F

Cette section est aussi configurable en utilisant les options de la section D.

* **Insuline Active (IA)** (diagramme bleu) : affiche l'insuline que vous avez dans le corps. S'il n'y avait pas de DBT, de SMB et plus de bolus restants, elle serait nulle. La diminution dépend de votre DAI et de vos paramètres de profil d'insuline. 
* **Glucides Actifs (GA)** (diagramme orange) : affiche les glucides que vous avez dans le corps. La diminution dépend des écarts que l'algorithme détecte. S'il détecte une absorption de glucide inférieure à ce qui est prévu, de l'insuline est administrée et cela augmente l'IA (plus ou moins, selon vos paramètres de sécurité). If it detects a higher carb absorption than expected, it will fall back to the value that is calculated by the min_5min_carbimpact.
* **Déviations**: 
   * barres **GRISES** montrent un écart dû aux glucides. 
   * barres **VERTES** montrent que la Gly est supérieure à l'attendu de l'algorithme 
   * barres **ROUGES** montrent que la Gly est inférieur à l'attendu de l'algorithme.
* **Sensibilité** (ligne blanche) : Elle montre la sensibilité détectée par Autosense. C'est le résultat d'un calcul de la sensibilité à l'insuline suite à de l'exercice, aux hormones, etc.
* **Activité** (ligne jaune) : indique l'activité de l'insuline, calculée par votre profil d'insuline (elle n'est pas dérivée de l'IA). La valeur est plus élevée quand l'insuline délivrée est proche de son pic d'activité. It would mean to be negative when IOB is decreasing. 

### Section G

Enables you to administer a bolus (normally you would use the Calculator button to do this) and to add a fingerstick CGM calibration. Un bouton d'assistant rapide s'affiche également ici s'il est configuré dans le [Générateur de configuration](../Configuration/Config-Builder#quickwizard-settings).

## Calculatrice

![Calculatrice](../images/Screenshot_Bolus_calculator.png)

Quand vous voulez faire un bolus de repas, c'est normalement d'ici que vous le ferez.

### Section A

zone où vous renseignez les informations concernant le bolus que vous voulez. Le champ de la glycémie (Gly) est normalement déjà renseigné avec la dernière lecture de votre MGC. Si vous n'avez pas de MGC, il sera vide. Dans le champ Glucides, vous indiquez votre estimation de la quantité de glucides pour laquelle vous voulez faire le bolus. The CORR field is if you want to modify the end dosage for some reason, and the CARB TIME field is for pre-bolusing so you can tell the system that there will be a delay before the carbs are to be expected and the bolus will be delayed. Vous pouvez mettre un nombre négatif dans ce champ si vous faites un bolus pour des glucides déjà consommés.

SUPER BOLUS : permet d'ajouter l'insuline basale des 2 prochaines heures au bolus immédiat, et un débit basal temporaire (DBT) à 0 est défini pour les 2 prochaines heures afin de ne pas avoir d'insuline supplémentaire. L'idée est de fournir l'insuline plus tôt et, espérons-le, de réduire les pointes.

### Section B

affiche le bolus calculé et permet de renseigner une note. Si la quantité d'insuline active dépasse déjà le bolus calculé, elle affichera simplement la quantité de glucides encore nécessaire.

### Section C

montre les différents éléments qui ont été utilisées pour calculer le bolus. Vous pouvez décocher tout ce que vous ne souhaitez pas inclure mais vous ne voudrez normalement pas faire cela.

### Combinaisons de GA (Glucides Actifs) et IA (Insuline Active) et leur signification

<ul>
    <li>Si vous cochez GA et IA, les glucides non absorbés qui ne sont pas couverts par de l'insuline + toute l'insuline qui a été délivrée en DBT (basal temporaire) ou SMB seront pris en compte</li>
    <li>Si vous cochez GA sans IA vous courez le risque d'avoir trop d'insuline car AAPS ne comptera pas ce qui a déjà été diffusé. </li>
    <li>Si vous cochez l’IA sans GA, AAPS prendra en compte l’insuline déjà délivrée, mais pas les glucides absorbés. Cela conduit à un avis de « manque de glucides ».
</ul>

Si vous faites un bolus aditionnel rapidement après un bolus de repas (par exemple pour un dessert supplémentaire) il peut être utile de décocher toutes les cases. De cette façon, les nouveaux glucides seront juste additionnés car le repas principal ne sera pas nécessairement absorbé et l'IA ne correspondra pas avec le GA aussi prêt d'un bolus de repas.

### Détection incorrecte des GA

![Absorption lente des glucides](../images/Calculator_SlowCarbAbsorbtion.png)

Si vous voyez l'avertissement ci-dessus après avoir utilisé l'assistant bolus, AndroidAPS a détecté que la valeur de GA calculée est peut-être incorrecte. Donc si vous voulez un nouveau bolus après un précédent repas avec des GA, vous devez être conscient du risque de surdose ! Pour plus d'informations, voir les conseils sur la [page de calcul des GA](../Usage/COB-calculation.html#detection-of-wrong-cob-values).

## Profil d'Insuline

![Profil d'Insuline](../images/Screenshot_insulin_profile.png)

Ceci montre le profil d'activité de l'insuline que vous avez choisie. La ligne MAUVE indique la quantité d’insuline restante après son injection car elle décroît avec le temps, tandis que la ligne BLEUE indique son activité.

Vous utiliserez normalement l'un des profils Oref, et il est important de noter que la décroissance dure longtemps. Si vous êtes habitué à utiliser la pompe manuellement, vous êtes probablement habitué à supposer que l'insuline se désintègre en environ 3,5 heures. Toutefois, lorsque vous bouclez, la fin de l'action de l'insuline est importante, car les calculs sont beaucoup plus précis et ces petites quantités s’additionnent lorsqu’elles sont soumises aux calculs récursifs de l’algorithme AndroidAPS.

Pour plus d'informations sur les différents types d'insuline, leurs profils d'activité et l'importance de tout cela, vous pouvez lire un article ici sur [Comprendre les nouvelles courbes IA basées sur des courbes d'activité exponentielles](https://openaps.readthedocs.io/en/latest/docs/While%20You%20Wait%20For%20Gear/understanding-insulin-on-board-calculations.html#understanding-the-new-iob-curves-based-on-exponential-activity-curves)

Et vous pouvez lire un excellent article de blog à ce sujet ici : [Pourquoi nous avons régulièrement tort dans la durée d'action de l'insuline (DAI) que nous utilisons, et pourquoi c'est important…](http://www.diabettech.com/insulin/why-we-are-regularly-wrong-in-the-duration-of-insulin-action-dia-times-we-use-and-why-it-matters/)

Et plus encore : [Courbes d’insuline exponentielle + Fiasp](http://seemycgm.com/2017/10/21/exponential-insulin-curves-fiasp/)

## Statut de la pompe

![Statut de la pompe](../images/Screenshot_pump_Combo.png)

Nous voyons ici l'état de la pompe à insuline - dans ce cas, un Accu-Chek Combo. Les informations affichées sont explicites. Un appui long sur le bouton HISTORIQUE lira les données de votre historique de pompe, y compris votre profil basal. Mais n'oubliez pas qu'un seul profil de basal est supporté sur la pompe Combo.

## Careportal

![Careportal](../images/Screenshot_care_portal.png)

Ceci reproduit les fonctions que vous trouverez sur votre écran Nightscout sous le symbole "+" qui vous permet d'ajouter des notes à vos enregistrements. Les fonctions telles que l'enregistrement lorsque vous modifiez de site d'injection ou une cartouche d'insuline doivent être explicites. MAIS cette section n'émet aucune commande à votre pompe. Donc, si vous ajoutez un bolus à l'aide de cet écran, cela ajoutera simplement une note dans vos enregistrements Nightscout, la pompe ne délivrera pas de bolus.

## Boucle, AR, AAR, SMB

Vous n'avez pas besoin de vous en inquiéter, ils montrent les résultats de l'algorithme OpenAPS qui s'exécute chaque fois que le système obtient une nouvelle lecture de la MGC. Ces fonctions sont expliquées ailleurs.

## Profil

![Profil](../images/Screenshot_profile.png)

AndroidAPS peut s'exécuter avec différentes configurations de profil. Typiquement - comme ici - le profil Nightscout a été téléchargé via le Client NS intégré et il est présenté ici en lecture seule. Si vous souhaitez effectuer des modifications, vous pouvez le faire à partir de votre interface utilisateur Nightscout, puis faire un [Changement de Profil](../Usage/Profiles.md) dans AndroidAPS pour activer les modifications. Les données telles que les débits de base du profil seront automatiquement copiés sur votre pompe.

** DAI : ** représente la Durée d'Action de l'Insulin et il est détaillé plus haut dans la section sur les profils d'insuline.

** G/I : ** est le rapport quantité de glucides divisé par le nombre d'unité d'insuline. Ce profil comporte un certain nombre de valeurs différentes définies pour différentes périodes de la journée.

** SI :** est la Sensibilité à l'Insuline, elle correspond à la réduction de glycémie que permettra d'obtenir une unité d'insuline en supposant que rien d'autre ne change par ailleurs.

**Basal : ** est le profil de basal programmé dans votre pompe.

**Cible :** est l'objectif glycémique que vous souhaitez atteindre. Si vous le souhaitez, vous pouvez définir différents niveaux pour différentes heures de la journée. Vous pouvez même définir des limites supérieure et inférieure afin que le l'algorithme ne commence à effectuer des modifications que lorsque la valeur de glycémie prévue est en dehors dela plage, mais si vous le faites, la boucle réagira moins vite et il est peu probable que vous obteniez une glycémie aussi stable.

## Traitement, xDrip, NSClient

Il s'agit simplement des journaux de traitements (bolus et glucides), des messages xDrip et des messages envoyés à Nightscout via le client intégré Nightscout. Vous n'avez normalement pas besoin de vous en inquiéter à moins qu'il y ait un problème.

## Générateur de configuration

![Générateur de configuration](../images/Screenshot_config_builder.png)

C'est ici que vous allez paramétrer la configuration de votre plate-forme AndroidAPS. Cette capture d'écran montre une configuration typique utilisant une pompe Combo, un capteur MGC Dexcom G5 géré par xDrip+ et fonctionnant avec de l'insuline NovoRapid sur un profil Oref et connecté à un serveur Nightscout hébergé sur le cloud.

La case à cocher à droite détermine si ce module sera affiché dans la barre de menu en haut (voir la section A dans Ecran d'accueil) et la roue crantée permet d'accèder aux paramètres du module, s'il y en a.

## Réglages et Préférences

En haut à droite de la barre de navigation, vous trouverez trois petits points verticaux. En appuyant dessus, vous aurez accès aux préférences de l'application, préférences des plugins, l'historique, l'assistant de configuration, les informations de l'application (à propos de) et le bouton quitter pour fermer AAPS.