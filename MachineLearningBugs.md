# L’utilisation de l’apprentissage automatique pour détecter des ravageurs volants en champ

## Table des matières
- [L’utilisation de l’apprentissage automatique pour détecter des ravageurs volants en champ](#lutilisation-de-lapprentissage-automatique-pour-d%C3%A9tecter-des-ravageurs-volants-en-champ)
  * [Comment l’apprentissage automatique peut-il être utilisé pour identifier des insectes ravageurs à partir d’images digitales?](#comment-lapprentissage-automatique-peut-il-%C3%AAtre-utilis%C3%A9-pour-identifier-des-insectes-ravageurs-%C3%A0-partir-dimages-digitales)
  * [Qu’est-ce qu’un piège à phéromones régulier?](#quest-ce-quun-pi%C3%A8ge-%C3%A0-ph%C3%A9romones-r%C3%A9gulier)
  * [Qu’est-ce qu’un piège à phéromones automatisé?](#quest-ce-quun-pi%C3%A8ge-%C3%A0-ph%C3%A9romones-automatis%C3%A9)
  * [Quels sont les défis d’un concepteur de piège à phéromones automatisé?](#quels-sont-les-d%C3%A9fis-dun-concepteur-de-pi%C3%A8ge-%C3%A0-ph%C3%A9romones-automatis%C3%A9)
    + [Les insectes ne sont pas toujours collés dans la même position](#les-insectes-ne-sont-pas-toujours-collés-dans-la-même-position)
    + [Les captures secondaires](#les-captures-secondaires)
    + [Les changements de condition du piège](#les-changements-de-condition-du-piège)
* [Bibliographie](#bibliographie)
  

___
## Comment l’apprentissage automatique peut-il être utilisé pour identifier des insectes ravageurs à partir d’images digitales?
Les algorithmes de classification doivent être aptes à séparer les insectes du fond de l’image et de classer cet insecte. On doit donc soumettre un très grand nombre d’images aux algorithmes de classification choisis pour leur permettre de diminuer le nombre de faux positifs et faux négatifs. Les images doivent être passés à travers un série de filtres visant d'abord à isoler les insectes du fond de l’image. Ces insectes potentiels doivent être sélectionnés sur la base de leur forme, taille, couleur ou degré de complexité et d'irrégularité. Ensuite, dépendamment des besoins du concepteur de la méthode d'apprentissage machine, les insectes seront attribué à une classe. Parfois, le système de classification sera binaire et ne détectera que la présence ou l’absence de l’insecte recherché. Dans d’autres cas, il pourrait y avoir une dizaine d’insectes ravageurs à différencier du fond de l’image et des insectes qui ne sont pas nuisibles. La base de donnée d’image soumise aux filtres de classification doit contenir un nombre d’images suffisant pour permettre aux algorithmes de classification de s’améliorer suite aux confirmations (ou infirmations) d’un observateur humain. Cette base de donnée d’image doit être représentative des différentes classes à détecter et des objets non-recherchés que l’algorithme pourrait identifier à tort comme faisant partie d'une des classes d'intérêt.

![Image1](https://github.com/Cocoricoco/BIO6033/blob/master/Image1.jpg)

*Exemple de système de détection bien ajusté.*

___
## Qu’est-ce qu’un piège à phéromones régulier?
Des pièges à phéromones sont utilisés pour détecter la présence de la forme ailée de nombreuses espèces de ravageurs. Une capsule de phéromones est ajoutée à un piège contenant une base collante où les insectes attirés iront se coller. Les pièges réguliers doivent être inspectés manuellement par un dépisteur qui devra compter le nombre d’insectes d'intérêts collés à la base collante pour ensuite la changer. Ce dépisteur devra être capable de distinguer les espèces d'intérêts des captures involontaires.
___

## Qu’est-ce qu’un piège à phéromones automatisé?
Un piège à phéromones automatisé inclus une caméra prenant des photos de la base collante à des intervalles pré-déterminés. Ces photos peuvent être envoyé par le réseau cellulaire aux propriétaires du champ surveillé. En théorie, une série de filtres de classification bien entraînés par apprentissage machine pourra alors envoyer une alerte au fermier l’informant du nombre d’insectes ravageurs de chaque classe d'intérêt détectés.

![Image2](https://github.com/Cocoricoco/BIO6033/blob/master/SemiosTraps.jpg)

*Exemple de l'interface utilisateur d'un fermier surveillant son champ à l'aide de pièges automatisés*
___
## Quels sont les défis d’un concepteur de piège à phéromones automatisé?

### Les insectes ne sont pas toujours collés dans la même position
Les images utilisées pour entraîner les filtres de classification doivent être représentatives des différentes positions dans lesquelles peuvent se coller les insectes. Elles doivent par exemple inclure des insectes collés de face ainsi que de profil.

### Les captures secondaires
Malgré que les phéromones des insectes ravageurs sont souvent très spécifiques, il y aura souvent des captures secondaires qui iront se coller au hasard sur la base collante. Les filtres de classification devront être entraînés sous des conditions réelles pour différencier les captures secondaires du ravageur d'intérêt. De plus, le système doit être entraîné pour prendre en compte la superposition d’insectes lorsque de nombreux insectes y seront collés. Une superposition d’insectes peut mener à une sous-estimation de leur nombre.

![Image3](https://github.com/Cocoricoco/BIO6033/blob/master/Image3.jpg)

*Exemple de système d'apprentissage automatique entrainé à distinguer des papillons par un technicien*


### Les changements de condition du piège
Les conditions météorologiques ou la présence de plantes créant de l’ombre autour du piège peuvent en changer le niveau de luminosité. La base de donnée d’images utilisées pour entraîner le système d’apprentissage automatique doit être représentative des changements de luminosité tout au long de la saison de culture.
___

### Bibliographie

- Barbedo, J.G.A., 2020. *Detecting and Classifying Pests in Crops Using Proximal Images and Machine Learning: A Review.* AI, 1(2), pp.312-328.

- Ding, W. and Taylor, G., 2016. *Automatic moth detection from trap images for pest management. Computers and Electronics in Agriculture*, 123, pp.17-28.



