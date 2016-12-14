# E-health POC
Technical content for project E-health CMD (research)

<b>Inleiding, wat wil ik weten?</b></br>
Ik wil weten hoe we pushnotificaties vanuit de app naar het mobiele device van de gebruiker kunnen sturen (voor ons iOS).
Is wat wij willen haalbaar en zo ja:
Hoe implementeren we deze functionaliteit, moeten we dit compleet zelf bouwen of kunnen we gebruik maken van een bestaand script, API?
Wat hebben we nodig, wat moet de developer weten?

<b>Hoe heb ik onderzoek aangepakt?</b></br>
Dmv van deskresearch heb ik het bovenstaande technische aspect onderzocht van de toekomstige applicatie. 
Ik kwam verschillende websites tegen met informatie en tutorials.

<b>Wat zijn de resultaten?</b></br>
Wat kan je met een push notificatie:
- Een kort tekstbericht laten zien.
- Een notificatie geluid afspelen.
- Het mogelijk maken dat de gebruiker handelingen kan uitvoeren zonder openen van de app. (Push notificatie terwijl app niet geopend is).
- Het toestaan dat de app op de achtergrond een taak uitvoert.

3 dingen die moeten gebeuren om een push notificatie te verzenden en ontvangen:
- De app moet juist ingesteld en geregistreerd zijn met de Apple Push notification service (APNS) om push notificaties te ontvangen.
- Een server moet een push notificatie verzenden naar de APNS doorgestuurd naar een of meer specifieke devices.
- De app moet de push notificaties ontvangen. Dan kan het taken of gebruikershandelingen uitvoeren door callbacks te gebruiken.

Belangrijk:<br>
Push notificaties betekent dat er goede beveiliging moet zijn, omdat je niet wil dat iemand anders push notificaties kan sturen naar gebruikers. Dit betekent dat er nog wel wat meer werk bij komt kijken om alles te configureren. (SSL certificaat)

<b>Conclusie -tot-nu-toe-:</b></br>
Ja het is haalbaar, we hoeven niet alles zelf te bouwen. 
Onderstaande websites (inhoud) zijn nodig:
- https://www.raywenderlich.com/123862/push-notifications-tutorial (Beschreven in duidelijke stappen wat te doen!)</br>
- https://parse.com/tutorials/push-notifications (iOS -APNS-, Android -GCM-. "Scheduled push is not supported," so probably not for us)</br>
- https://developers.google.com/cloud-messaging/ (iOS, Android, web: chrome, firefox, opera. GCM/FCM)</br>
- https://www.quora.com/Push-Notifications/Push-Notifications-Which-is-best-to-use-Amazon-SNS-Google-Cloud-Messaging-or-Parse-Why (comparing)</br>
- http://stackoverflow.com/questions/17262511/how-do-ios-push-notifications-work (see img)</br>

<b>Tentamenvragen</b>
1. Waarom is veiligheid, security, belangrijk met betrekking tot sturen van push notificaties naar je gebruiker? En wat is er nodig om deze security te realiseren?</br>
    http://www.w3.org/TR/push-api/#dfn-push-message</br>
    "User agents must implement the Push API to be HTTPS-only. SSL-only support provides better protection for the user against man-in-the-middle attacks intended to obtain push subscription data. Browsers may ignore this rule for development purposes only."
    
2. Noem minimaal drie mogelijkheden/eigenschappen van een push notificatie.
   https://www.raywenderlich.com/123862/push-notifications-tutorial
   "In iOS 9, push notifications can:</br>
- Display a short text message
- Play a notification sound
- Set a badge number on the app’s icon
- Provide actions the user can take without opening the app
- Be silent, allowing the app to wake up in the background and perform a task"
   
