# LocalizationTool

Stocker les textes d'un projet Unity dans un fichier csv pour le lire sur Excel.
Le système est plutôt adapté pour les petits projets Unity.

path du fichier : Assets/Resources/localization.csv

# TUTORIEL

Pour fonctionner correctement, la scène Unity a besoin d'un component LocalizationManager

POUR ENREGISTRER UN TEXTE DANS LE CSV :
* Selectionner le gameobject avec le component __Text__ ou __TextMeshPro__
* Attacher un component __TextLocalizer__ et renseigner une clé ID
* Clic droit sur le component et cliquez sur __AddToCSV__ :

![Sans titre-1](https://user-images.githubusercontent.com/55829314/162481878-4b0e2928-51d7-4d7e-a54e-879868385749.jpg)

Le fichier .csv a été update !

il faut maintenant entrer dans le fichier de localization et effectuer la traduction :

![image](https://user-images.githubusercontent.com/55829314/178805191-dcb4c79a-0622-4c7e-933b-c2d241faa5d4.png)


Dans le script __LocalizationSystem__ vous pouvez ajouter une langue dans l'enum et son dictionnaire associé :

![image](https://user-images.githubusercontent.com/55829314/178803207-8c52d3e9-2e17-4884-8fbe-45035f4ed47d.png)


__LE COMPONENT TEXTLOCALIZER N'EST QU'UN OUTIL SIMPLIFIÉ POUR TRADUIRE RAPIDEMENT__

Vous pouvez effectuer des traductions dans vos script sans passer par lui

#CHEAT SHEET

* __LocalizationSystem.GetLocalisedValue(string key)__

récupère la traduction associée à une clé

* __LocalizationSystem.Add(string key,string value)__

ajoute une nouvelle traduction au fichier .csv

* __LocalizationSystem.Remove(string key)__

retire la traduction correspondante du .csv

* __LocalizationSystem.Sort()__

arrange le fichier .csv avec ses clés dans l'ordre alphabétique
