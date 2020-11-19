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

    # SOMMAIRE  
    Remerciements 2   
    Introduction 4   
    L’équipe 5  
    Le produit 6  
    Naissance d’une idée 6  
    Description générale 6  
    Composants 7  
    Avantages de notre gant 9  
    Utilisation 10  
    Utilisation 10  
    Recommandations 10  
    Normes en vigueur 10  
    Réparations 11  
    Technologie 12  
    Unity 12  
    Arduino 13  
    Flex sensors 15  
    Alimentation 15  
    Le muscle 15  
    Choix des matériaux 20  
    Assemblage général 22  
    Esthétisme 25  
    Gant, câblage et boîte 25  
    Conclusion 27  
    Annexes 28  
    Cahier des charges 28  
    Organisation de travail 29  
    Représentation de l’avancée du travail 32  
    Tutoriel Unity 34  
    Tutoriel DEFORM-3D 42  
    Bibliographie 52  

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
