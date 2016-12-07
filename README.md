# E-health POC
Technical content for project E-health CMD (research)

Inleiding, wat wil je weten?

Ik wil weten hoe we pushnotificaties vanuit de app naar het mobiele device van de gebruiker kunnen sturen (voor ons Ios).
Is wat wij willen haalbaar en zo ja:
Hoe implementeren we deze functionaliteit, moeten we dit compleet zelf bouwen of kunnen we gebruik maken van een bestaand script, API?
Wat hebben we nodig, wat moet de developer weten?

Hoe heb ik onderzoek aangepakt? 
Dmv van deskresearch heb ik het bovenstaande technische aspect onderzocht van de toekomstige applicatie. 
Ik kwam verschillende websites tegen met informatie en tutorials.

Wat zijn de resultaten?

Wat kan je met een push notificatie:
-Een kort tekstbericht laten zien
-Een notificatie geluid afspelen
-Het mogelijk maken dat de gebruiker handelingen kan uitvoeren zonder openen van de app. (Push notificatie terwijl app niet geopend is).
-Het toestaan dat de app op de achtergrond een taak uitvoert.

3 dingen die moeten gebeuren om een push notificatie te verzenden en ontvangen:
- De app moet juist ingesteld en geregistreerd zijn met de Apple Push notification service (APNS) om push notificaties te ontvangen.
- Een server moet een push notificatie verzenden naar de APNS doorgestuurd naar een of meer specifieke devices.
- De app moet de push notificaties ontvangen. Dan kan het taken of gebruikershandelingen uitvoeren door callbacks te gebruiken.

Belangrijk:
Push notificaties betekent dat er goede beveiliging moet zijn, omdat je niet wil dat iemand anders push notificaties kan sturen naar gebruikers. Dit betekent dat er nog wel wat meer werk bij komt kijken om alles te configureren. (SSL certificaat)

Conclusie: antwoord op wat je wilde weten -tot-nu-toe-
Ja het is haalbaar, we hoeven niet alles zelf te bouwen.
Onderstaande websites (inhoud) zijn nodig:
https://www.raywenderlich.com/123862/push-notifications-tutorial (Beschreven in duidelijke stappen wat te doen!)
https://parse.com/tutorials/push-notifications (iOS -APNS-, Android -GCM-. "Scheduled push is not supported," so probably not for us)
https://developers.google.com/cloud-messaging/ (iOS, Android, web: chrome, firefox, opera. GCM/FCM).
https://www.quora.com/Push-Notifications/Push-Notifications-Which-is-best-to-use-Amazon-SNS-Google-Cloud-Messaging-or-Parse-Why (comparing)
http://stackoverflow.com/questions/17262511/how-do-ios-push-notifications-work (see img)
