Sur les features :


Side Scroller :

- J'ai repris le ThirdPersonController de base et j'ai modifié la caméra pour qu'elle ne suive pas les rotations du personnage
- Le joueur a donc un simple saut
- Le joueur meurt bien quand il tombe dans un trou (lorsque que sa position Z est en dessous de 0)

Objets ramassables :

- Le joueur peut ramasser des objets (des coins ici) qui lui incrémente son nombre de coin
- Le nombre est alors affiché en printText à chaque récupération
- Le joueur a aussi de la Life (à 100 de base) et il en perd lorsqu'il trigger des piques
- La vie qui lui reste est aussi affiché à chaque fois qu'il prend des dégats

Autre :

- Feedbacks en text pour les coins et la life
- Lorsque l'avatar n'a plus de vie, s'il tombe, ou s'il rencontre un ennemi, il est considéré comme mort et
  la scène se reload

Variantes :

IA :

- Implémentation d'un Behaviour Tree, d'un Blackboard et d'un Ai_Controller pour que l'IA soit attirée par le
  joueur lorsque ce dernier se trouve à moins de 400 unités de distance.
- Si l'IA attrape et touche le joueur, ce dernier meurt et la scène est reload

Objets ramassable ++ :

- Création d'un Blueprint mère PickupObject, qui lance une fonction commune lorsqu'il overlap avec le joueur.
- Création grâce à cette classe de 2 "PickupObject : les Coin qui appelle une fonction du PlayerController qui
  incrémente le nombre de coin, et les piques que j'ai considéré par limite de temps comme des PickupObject
  (objet qui lance une fonction lorsque le joueur overlap). Le nom de la classe mère est alors à revoir mais ces
  derniers lance une fonction du PlayerController qui lui enlève de la vie (nombre de pv éditable directement depuis l'objet pique)


+ :

Ajout d'une box que le joueur doit pousser pour accéder à une hauteur (elle est bof, pas gravité m'enfin...)

