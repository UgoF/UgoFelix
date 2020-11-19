# UgoFelix  
Virtual Reality Glove/ force Feedback

# REMERCIEMENTS  
La réalisation de ce projet a été possible grâce au concours de plusieurs personnes à qui nous voudrions témoigner
toute notre reconnaissance.
Tout d’abord, nous voudrions remercier notre tuteur de projet Mr Bareggi pour sa patience et sa disponibilité à notre
égard. Nous souhaitons aussi remercier le corps enseignant pour avoir mis à notre disposition les moyens essentiels à notre
projet, en particulier Mr Ferret pour ses judicieux conseils ainsi que pour avoir soutenu notre projet depuis le début, et Mr Grève
pour son aide pour le management de notre équipe.
Enfin, nous remercions nos amis et collègues pour leur support intellectuel et moral, un grand merci à Fabien Félix pour
ses conseils concernant Unity.

    

# INTRODUCTION  
Ce projet a été réalisé dans le cadre du projet semestriel du parcours « Biotech et Santé » de notre 3ème année à l’école
d’ingénieur ESME Sudria au campus de Lyon. Objectif : offrir à l’utilisateur la possibilité de ressentir les sensations de toucher,
de contact et de saisie d’un objet en réalité virtuelle à l’aide d’un gant. L’utilisateur a ainsi grâce au gant un retour haptique qui
lui donnera des perceptions tactiles concentrées sur les doigts. Lorsque l’utilisateur touchera ou saisira un objet en réalité
virtuelle, il ressentira, à l’aide du gant, des sensations telles que lorsqu’on saisit un objet réel.
Le gant fonctionne grâce à la proprioception de la main et grâce à un système de blocage des mouvements de flexions
des doigts. Ce système est une armature légère sur le dos de la main qui se raidit pour imiter la saisie d’un objet par une main.
L’utilisateur peut ainsi ressentir différentes sensations telles que le toucher d’un doigts sur un objet rigide, mou ou déformable,
d’une taille de l’ordre de grandeur d’objets saisissables par une main humaine.

# LE PRODUIT  
## NAISSANCE D’UNE IDÉE  
L’idée du projet nous est venue d’une façon assez inattendue. Lors de notre 2ème année en cycle ingénieur, un film liant
la réalité virtuelle et le monde réelle est apparu. Celui-ci, réalisé par Steven Spielberg, se nomme : Ready Player One.
Une question commune a soudain surgi à la suite du visionnage : ont-ils les sensations du toucher ? Nous nous sommes
alors lancés dans ce projet consistant à reproduire les sensations du touché en Réalité Virtuelle.
Notre première idée reposait sur la déformation d’un matériau traversé par un champ magnétique. Celui-ci se
contracterait plus ou moins, empêchant ou non les mouvements de la main. Malheureusement, après une multitude de
recherches, un problème fut confirmé… Le voltage minimum pour souhaiter contracter un matériau appelé « polymère électroactif
diélectrique » est de plusieurs milliers de volts. L’ampérage étant très petit, celui-ci n’était pas problématique. Un voltage
aussi élevé que celui nécessaire pouvait avoir des répercussions mortelles sur l’utilisateur. Déçu à l’idée que le projet pouvait
s’arrêtait là, nous n’avons pas pour autant abandonné complètement nos recherches. Après plusieurs semaines de lectures et
renseignements, nous nous penchions sur une idée en particulier, celle de réaliser un muscle en prenant exemple sur le corps
humain. On appelle cela « le biomimétisme », et s’accorde parfaitement avec notre parcours « Biotech et Santé ».
L’idée était donc de placer un muscle artificiel, sur le doigt, dont la contraction agirait contre celle du muscle de
l’utilisateur. Une sensation de blocage sera donc ressentie. Pour cela, notre muscle serait composé d’une forme réalisée à partir
d’origamis, d’une enveloppe plastique et d’une pompe à air activant ou non la contraction du muscle.  
## DESCRIPTION GÉNÉRALE  
Notre projet comprend une boite prête à être branchée et utilisée, et un gant, prêt lui aussi à être branché à la boite et au
tuyau pour utiliser comme il se doit notre gant Midas, notre Virtual Reality Reacting Glove. Attendez-vous à des sensations hors
du commun mêlées à une ambiance innovante et confortable, avec une ergonomie à couper le souffle. Enfilez votre gant, lancez
le logiciel et touchez un objet : vous sentez alors une sensation de force qui vous empêche de plier le doigt : notre muscle
artificiel se contracte. Relevez votre doigt et la sensation de force s’annule : la main virtuelle ne retouche plus l’objet et vous
n’avez plus de sensation de toucher. C’est ce qu’on appelle un retour haptique.

## Fonctionnement global de notre virtual reality glove :  
Pour commencer, nous avons créé une main en 3D sur un logiciel de 3D : Unity 3D
#
Ensuite, nous avons créé un « collider » qui est la petite sphère verte que vous voyez cidessous.
Cela permet au logiciel de reconnaître lorsque notre main virtuelle touche le cube
et d’envoyer un signal à la carte Arduino. Notre carte Arduino reçoit donc le signal que notre
main virtuel a touché le cube et transmet alors un autre signal à notre électrovanne qui
s’ouvre ainsi qu’à notre pompe qui va se mettre à aspirer l’air à l’intérieur de notre muscle.
L’air à l’intérieur de notre muscle se faisant aspirer, celui-ci se contracte et se raidit afin
d’avoir une force opposée au mouvement de notre doigt ce qui nous permet de donner
l’impression de toucher le cube.  


# COMPOSANTS
Liste du Matériel :  
500g de Silicone RTV 181 (prix : 30€80)  
1 Pompe : AIRPO Model D2028B (prix : 15€)  
2 Electrovannes US SOLID Model USS2-00051 (prix unitaire : 15€)  
4 Mamelons en laiton égal mâle 3/8’’ (prix : 0€30)  
1m Tuyau diamètre 3/8’’  
Moule : imprimé par nos soins (voir travaux associés au moule dans nos rapports)  
Fils de connections  
Transformateur 12V (pour la pompe et l’électrovalve)  
Carte Arduino Uno  
Logiciel Unity3D installé sur Mac, Windows 8  
Logiciel Autodesk Fusion 360  
Logiciel DEFORM-3D  
Transistors MOSFET  
5 Flex Sensors  
Résistances diverses  
Plaques Plexiglas (transparent et mate)  
Quelques LEDs  
Boite plastique 30*20*15 cm  


Dans cette partie, nous parlerons essentiellement des composants électriques. Les composants tels que le silicone ou le
Plexiglas seront expliqués dans la partie « matériaux ».
Notre pompe AIRPO (achetée sur Amazon) est une simple pompe pour aquarium (à la base) mais elle reste très
polyvalente, elle s’alimente en 12V et possède une entrée d’air forcée (c'est à dire une entrée d’air par un embout adaptable
pour un tuyaux assez fin) ainsi qu’une sortie d’air aussi adaptable pour placer un tuyau. Sa puissance nous suffit amplement
pour notre prototype actuel puisqu’il n’y a qu’un seul muscle à faire fonctionner. Sa taille nous satisfait pour le moment, mais
nous pensons à la changer bientôt pour opter pour une pompe plus petite et plus puissante, avec une sortie d’air généralisée,
non forcée (pour optimiser la taille et la puissance).
Les vannes US SOLID ont été elles aussi achetées sur Amazon, ce sont des composants essentiels pour réguler la sortie
d’air/l’entrée d’air des muscles artificiels afin de contrôler la contraction du muscle. Ces 2 vannes sont spécialisées pour la
haute pression et sont compatibles pour de l’eau ou de l’air. La taille de ces vannes ne nous satisfait pas, nous pensons qu’elles
seront les prochains composants à remplacer pour gagner en poids et en volume dans notre boite. Effectivement, nous avons
juste besoin d’une vanne contrôlable électriquement et pas forcément apte à supporter de la très haute pression ou plusieurs
fluides. Pour le circuit général (assembler les vannes avec les pompes et le muscle) nous avons eu besoin de matériels de haute
pression tels que des embouts en laiton et des tuyaux fins.
Nos muscles et la structure du gant sont moulés en silicone, nous avons nous-même conçu nos moules, d’abord
modélisés en 3D sur le logiciel Fusion 360, puis importé sur Tinkercad pour créer le négatif de la pièce, et transféré en fichier .stl
sur le logiciel CURA pour le rendre compatible avec les imprimantes 3D du Fablab (fichier .gcode).
Notre système électrique est constitué d’une carte Arduino, de fils de connexion, de 3 transistors MOSFET, de
résistances diverses (3 de 27 kOhm, 3 de 1 kOhm) ainsi que 5 Flex Sensors. Ce circuit électrique permet de réguler
automatiquement la contraction du muscle lorsque Unity l’ordonne. Les vannes et la pompe sont alimentés en 12V avec un
transformateur branché en secteur.
Pour l’esthétisme général de notre projet, nous avons fabriqué une boite en Plexiglas découpé au laser au Fablab, et
nous avons placé des LEDs dans la boite de la carte Arduino.

# UTILISATION  

Vous venez d’acquérir le gant de Réalité Virtuelle Midas de la société Alva Tech, avant de profiter des nombreuses activités
permises grâce à ce gant vous devez tout d’abord connecter tous les éléments.  
1. Branchez le système au secteur  
2. Vérifier si les LEDs s’allument, si non merci de nous contacter  
3. Mettez le gant à votre main gauche et votre casque de Réalité Virtuelle  
4. Allumez votre programme  
5. Vous pouvez maintenant profiter des meilleures sensations possibles en Réalité Virtuelle  
6. N’oubliez pas de manger, dormir, sortir et de garder une hygiène de vie saine nous ne prenons aucune responsabilité sur  
la santé du client  
RECOMMANDAT I O N S  
• Veuillez ne pas trop plier les flex-sensors, ce sont des matériaux fragiles qui peuvent se casser  
• Veuillez éviter de forcer trop violemment sur les muscles, le but de ce projet n’est pas de calculer la force de votre poigne  
• Ne desserrez pas totalement les bagues  
• N’essayez pas d’enlever les flex-sensors, si vous devez remplacer un des composants merci de nous contacter  
• Si vous voulez remplacer un des muscles artificiels, enlevez les grâce au système de scratch, de plus, nos muscles sont
consignés, renvoyez-les-nous et nous vous offrons une réduction sur le remplacement de votre muscle.  
• Ne débranchez pas la pompe ou les vannes lorsqu’elles sont alimentées  
• Ne touchez pas les composants électriques lorsqu’ils sont allumés  
• Ne débranchez pas le circuit lorsqu’il est en cours d’utilisation  
## NORMES EN VIGUEUR  
Notre cahier des charges détaille très bien toutes les normes que nous avons prises en compte (taille, poids, sécurité,
compatibilité etc). Notre cahier des charges se trouve à la fin de ce dossier, en annexe. Rappelons les besoins et contraintes du
projet :  
Le gant doit pouvoir être compatible avec le logiciel Unity3D et Arduino afin de fonctionner et d’être utilisé pour la réalité
virtuelle.  
La taille du gant doit convenir à un large panel d’utilisateur, notre prototype sera conçu à partir d’un gant de taille 9, voire de
taille adaptable (de 7 à 11) (taille européenne).  
L’alimentation se doit d’être pratique et de pouvoir s’adapter aux prises secteurs de France.  
Les matériaux qui composent le gant doivent pouvoir résister à plusieurs centaines d’utilisations avant de commencer à se
déformer irréversiblement.  
