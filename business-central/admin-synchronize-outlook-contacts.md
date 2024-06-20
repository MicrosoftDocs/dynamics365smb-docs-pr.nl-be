---
title: Contacten delen tussen Business Central en Outlook
description: 'Deze service heeft diepe integratie met Microsoft 365, zodat u contacten kunt delen tussen Outlook en Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Contacten in Business Central synchroniseren met contacten in Microsoft Outlook

U kunt contactsynchronisatie instellen zodat uw contacten in [!INCLUDE[prod_short](includes/prod_short.md)] dezelfde informatie hebben als uw contacten in Microsoft Outlook. Als u bijvoorbeeld een verkoper bent, werkt u mogelijk in Outlook en [!INCLUDE[prod_short](includes/prod_short.md)] tegelijkertijd. Als de contactpersonen op beide plaatsen hetzelfde zijn, is uw werk eenvoudiger.  

Standaard worden de contacten die u synchroniseert, bewaard in een **Business Central**-map in uw favorieten in het mappenvenster in Outlook. De Business Central-map kan het gemakkelijker maken om te identificeren welke contacten u synchroniseert. U kunt filters instellen om alleen specifieke contacten te synchroniseren van [!INCLUDE[prod_short](includes/prod_short.md)] naar Outlook. Nadat u de synchronisatie hebt ingesteld, kunt u handmatig synchroniseren of het proces automatiseren om op geplande basis te synchroniseren.  

## <a name="prerequisites"></a>Vereisten

- Uw gebruikersprofiel in [!INCLUDE[prod_short](includes/prod_short.md)] moet uw Microsoft 365 e-mailaccount opgeven.

  U kunt dit controleren in de instelling **Microsoft 365-verificatie** van uw gebruikersprofiel in de lijst **Gebruikers**.
- Met [!INCLUDE[prod_short](includes/prod_short.md)] hebt u contactsynchronisatie ingesteld zoals beschreven in [Contactsynchronisatie instellen met Outlook voor Business Central On-premises](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a>Synchronisatie instellen

U stelt in hoe u contactpersonen wilt synchroniseren met Outlook op de pagina **Instelling van Exchange-synchronisatie** in [!INCLUDE[prod_short](includes/prod_short.md)]. 

Op de pagina **Instelling van Exchange-synchronisatie** kunt u controleren of de verbinding met Exchange werkt en vervolgens synchronisatie van contacten instellen. Vanaf de pagina **Instelling van Exchange-synchronisatie** kunt u de pagina **Instelling van contactsynchronisatie** openen en de synchronisatie starten. Stel optioneel een filter in om op te geven welke contacten moeten worden gesynchroniseerd. U kunt bijvoorbeeld een filter instellen op naam, type, bedrijf enzovoort. U kunt ook de standaardnaam wijzigen van de map in Outlook waarmee de contacten worden gesynchroniseerd.  

Elk van uw collega's kan tevens zijn of haar eigen Exchange-synchronisatie instellen en eigen filters instellen op basis waarvan contacten worden gesynchroniseerd.  

Nadat u de synchronisatie hebt ingesteld, kunt u de wijzigingen aan het contact handmatig synchroniseren of u kunt het proces automatiseren door een taakwachtrij in te stellen. Zie de volgende sectie in dit artikel voor meer informatie over automatisering.

### <a name="automate-synchronization"></a>Synchronisatie automatiseren

U kunt een taakwachtrij-item maken dat contacten synchroniseert volgens een schema dat u definieert. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md). 

In de volgende tabel staan de instellingen op de pagina **Kaart voor taakwachtrijpost** die zijn voor het synchroniseren van contacten:

|Veld|Instelling voor contactsynchronisatie|
|-----|-----|
|Uit te voeren objecttype|Codeunit|
|Id van uit te voeren object|6700|

## <a name="synchronize-contacts"></a>Contactpersonen synchroniseren

Als u gewend bent met contacten te werken in [!INCLUDE[prod_short](includes/prod_short.md)], is het gemakkelijk handmatig te synchroniseren vanuit de lijst **Contacten** wanneer het u uitkomt. U kunt contacten op twee manieren synchroniseren:

* **Synchroniseren met Microsoft 365**

  Synchroniseer alle wijzigingen van [!INCLUDE[prod_short](includes/prod_short.md)] naar Microsoft 365 die zijn aangebracht na de laatste synchronisatie, op basis van de datum van laatste wijziging. Nieuwe contacten vanuit Microsoft 365 worden ook gesynchroniseerd naar [!INCLUDE[prod_short](includes/prod_short.md)]. Dit gaat meestal sneller dan een hele synchronisatie. 

* **Volledig synchroniseren met Microsoft 365**

  Synchroniseer alle contacten in beide richtingen, ongeacht de datum van laatste synchronisatie en laatste wijziging.  

In beide gevallen worden contacten alleen gesynchroniseerd vanuit Outlook als ze de vereiste velden ingevuld hebben. De vereiste velden om te synchroniseren naar Microsoft 365 zijn **Naam** en **E-mailadres** en het contact moet van het type **Persoon** zijn. [!INCLUDE[prod_short](includes/prod_short.md)] is de bron van de contactgegevens, dus de contactgegevens van [!INCLUDE[prod_short](includes/prod_short.md)] worden opgeslagen als er duplicaten zijn.  

> [!NOTE]
> Als u een contact in Outlook verwijdert, maar deze in [!INCLUDE[prod_short](includes/prod_short.md)] behoudt, wordt het contact de volgende keer dat u synchroniseert opnieuw gemaakt in Outlook. 

## <a name="see-also"></a>Zie ook

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Financiën](finance.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Contactpersonen (personen) gebruiken in Outlook op het web](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
