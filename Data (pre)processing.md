# Foodboost

## Data exploration/cleaning/visualisation etc.

Tijdens de eerste weken waren we bezig met het foodboost project. Aangezien dit voor mij de eerste keer was waar ik iets data science gerelateerd deed, was ik vooral in het begin bezig met bekend worden met de data en hoe deze uitgelezen, aangepast, verwerkt, gevisualizeerd etc. kan worden.
Het was vooral een beetje vragen bedenken en data verkennen in het begin. Daarna ging ik doelgerichter werken en data cleanen, verwerken, visualizeren etc. Ook ben ik bezig geweest met data in csv's stoppen en csv's uitlezen
Hieronder een aantal bewijzen van datgeen wat ik hierboven genoemd heb. Dit is natuurlijk niet alles, het lijkt mij redundant om van alles een screenshot bij te voegen.
![image](https://user-images.githubusercontent.com/80320867/215437027-f18757f3-162c-4d48-8368-022168a983ec.png)
![image](https://user-images.githubusercontent.com/80320867/215437947-2b53bb59-7d0c-4c8b-ba50-9f1401773598.png)
![image](https://user-images.githubusercontent.com/80320867/215438492-8d6dbf5f-103c-4066-9dff-57e6b7e7a73c.png)

## Change of plans

We kozen er later voor om van data set te veranderen en hadden een grotere van het internet gehaald. Uiteindelijk zijn we op deze dataset verdergegaan.
Deze bevatten onder andere reviews van van mensen, waardoor dit handig was voor een recommender system. Hier heb ik me vooral bezig gehouden met het schoonmaken van data, zodat we deze kunnen gebruiken in het model.
![image](https://user-images.githubusercontent.com/80320867/215441912-5d62e153-5ed8-45bf-99a1-7cf45b4a8f1d.png)
![image](https://user-images.githubusercontent.com/80320867/215442308-4c1b5c46-35d0-4864-a95f-023d6cd88f4b.png)
![image](https://user-images.githubusercontent.com/80320867/215442708-47337944-ec05-47f9-9113-0ee1b62ca1fe.png)



# IV_Infra

Dit project was veel veelzijdiger en het proces verliep ook netter, dus zal ik hier gebruik maken van meerdere kopjes

## Data exploration & cleaning

Ik begon met het verkennen en bekend raken met de data die we tot onze beschikking hadden, dit waren in het begin voornamelijk de foto's van IV-Infra. Toen we besloten hadden wat we gingen doen met de foto's van IV-Infra kozen wij ervoor om een aantal van de foto's, zoals deze die zijn gemaakt door camera 6 te discarden.
Uiteindelijk hebben we alleen de foto;s van camera 1 en 2 gebruikt. De foto's waren in eerste instantie ook te groot, deze zijn gereduceerd naar 640x640.
![image](https://user-images.githubusercontent.com/80320867/215440656-0f3e0386-33d7-4ebb-98d8-a4daea389550.png)
![image](https://user-images.githubusercontent.com/80320867/215440831-70aa4744-c54c-4552-bde5-73d3fe069d41.png)
![image](https://user-images.githubusercontent.com/80320867/215440905-f137ed51-ca10-4bfd-8676-e1564d62880d.png)

## Pyslam & camera calibratie

Mohamed en ik zijn aan de gang gegeaan met PySlam v2. Hier hebben wij het voor elkaar gekregen om de reeks foto's van de foto's van IV-Infra als input te gebruiken.
Het programma schiet dan herkenningspunten op deze foto's. De bedoeling was dat we hiermee uiteindelijk de verkeersborden in kaart zouden brengen, maar we hebben dit uiteindelijk op een andere manier gedaan.
We hebben ook geprobeerd pyslam runnend te krijgen op de server. We hebben het uiteindelijk erop gekregen, maar konden het niet visueel in onze notebooks te zien krijgen.
We hebben ook geprobeerd de gegevens van de calibratie van de camera te gebruiken, om te kijken of pyslam hierdoor nog accuratere herkenningspunten zou schieten.
We zijn bezig geweest met het onderzoeken van de camera, hoe camera calibratie werkt en de hugin tool. We hebben dit beide als individuen op onze eigen laptop gedaan.
![image](https://user-images.githubusercontent.com/80320867/215448947-36ac240f-2b7f-4cc1-9906-a6507586f961.png)
![image](https://user-images.githubusercontent.com/80320867/215449019-aca06bb9-f1ec-4d29-a615-320552e5fd82.png)


Hier heb ik een aantal waardes aangepast, zodat deze overeen kwamen met die van de camera.
![image](https://user-images.githubusercontent.com/80320867/215447533-165099f4-0712-43bd-b70f-97a15b7cacd1.png)


## Annotaten
De volgende stap was annotaten in roboflow. We hebben alleen foto's gebruikt van camera 1 en camera 2. Hier ben ik door 1398 foto's gegaan en heb de foto's die verkeersborden bevatten geannoteerd. Deze hebben wij daarna gebruikt om ons model te trainen in YOLOv5.
![image](https://user-images.githubusercontent.com/80320867/215446338-7d21ecdf-8669-4f5c-b716-fe12044b6c7d.png)
![image](https://user-images.githubusercontent.com/80320867/215447009-0ac50d96-29d6-4077-ac6c-ace58f833dce.png)
![image](https://user-images.githubusercontent.com/80320867/215449089-2449aac1-c7d8-427f-8913-f50a1c3e0859.png)


Deze geannoteerde afbeeldingen hebben zijn daarna ook ge-augment en gebruikt om YOLO mee te trainen.
![image](https://user-images.githubusercontent.com/80320867/215446695-a0da6e00-fec7-4411-84a6-7b91a64daddf.png)

## Lidar
Samen met Mohamed heb ik de taak op mij genomen de lidar data bruikbaar te maken. We kregen deze in een .las format, wat neerkomt op compressed lidar data. Hier een aantal screenshots van de code waarmee ik deze probeerde uit te lezen en uit te pakken.
![image](https://user-images.githubusercontent.com/80320867/215448540-fc3258c2-8428-4839-a9db-38853cbc5541.png)
![image](https://user-images.githubusercontent.com/80320867/215448829-33896aee-cdcb-4e8c-84ba-0e91c1bba8b6.png)





