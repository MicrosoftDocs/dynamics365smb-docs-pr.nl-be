---
title: Business Central gebruiken met Outlook | Microsoft Docs
description: Deze service is nauw geïntegreerd met Microsoft 365. U kunt al uw bedrijfs- en e-mailcommunicatie met klanten en leveranciers rechtstreeks in Outlook beheren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589645"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Business Central gebruiken als uw bedrijfsinbox in Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] biedt een invoegtoepassing waarmee u bedrijfsinteracties kunt beheren met uw klanten en leveranciers, rechtstreeks in Microsoft Outlook. Met de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing voor Outlook kunt u financiële gegevens bekijken met betrekking tot klanten en leveranciers, en financiële documenten maken en verzenden, zoals offertes en facturen.

De [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing bestaat uit twee afzonderlijke invoegtoepassingen die de volgende mogelijkheden bieden:

- Contactinzichten

   Met deze invoegtoepassing kunt u [!INCLUDE[prod_short](includes/prod_short.md)]-klant- of leveranciersinformatie opzoeken in Outlook-e-mails en agenda-afspraken. Het stelt u ook in staat om [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijfsdocumenten te maken en te verzenden, zoals een verkoopofferte of factuur aan een contact.

- Documentweergave

   Wanneer een bedrijfsdocument wordt verzonden in een e-mail, biedt de invoegtoepassing een directe, in-line koppeling van de hoofdtekst van de e-mail naar het eigenlijke bedrijfsdocument in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Aan de slag

1. Het eerste dat u moet doen, is de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing geïnstalleerd krijgen in Outlook. Uw beheerder heeft de invoegtoepassing mogelijk al voor u geïnstalleerd. Dus als u het niet zeker weet, neem dan contact op met uw beheerder of bekijk de volgende stap om te controleren of het is geïnstalleerd.

    Als de invoegtoepassing niet voor u is geïnstalleerd, zie [De invoegtoepassing installeren voor eigen gebruik](admin-outlook.md#install). 

2. Als de invoegtoepassing is geïnstalleerd, hebt u toegang tot de **[!INCLUDE[prod_short](includes/prod_short.md)]**-toepassing vanuit elk nieuw of bestaand e-mailbericht of agenda-afspraak in Outlook.

    Begin door in te loggen op Outlook en een e-mailbericht te openen. Als u de Outlook-app gebruikt, ga dan naar het lint en zoek naar **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Of als u Outlook op het web gebruikt, zoekt u boven of onder aan het e-mailbericht naar ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) of gaat u naar de Meer-acties ![Meer acties voor een e-mail weergeven in Outlook.](media/outlook-more-actions-button.png)  

    ![Business Central-invoegtoepassingen in Outlook openen.](media/outlook-business-central-addin.png)

   Als u de invoegtoepassing zelf hebt geïnstalleerd en ervoor hebt gekozen om een voorbeeld-e-mail te ontvangen, controleer dan uw inbox voor de welkomst-e-mail. Deze e-mail bevat informatie om u op weg te helpen.

De eerste keer dat u de invoegtoepassing gebruikt, wordt u in het deelvenster van de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing, mogelijk gevraagd om in te loggen. Kies in dit geval **Nu aanmelden** en volg de instructies op het scherm om u aan te melden bij Business Central met uw account.

> [!TIP]
> Als u de nieuwe versie van Outlook op het web gebruikt, kunt u **[!INCLUDE[prod_short](includes/prod_short.md)]** vastzetten, zodat het altijd direct zichtbaar is, in plaats van dat u naar de knop Meer acties moet gaan, waardoor het handig is om contactinzichten te bekijken terwijl u door verschillende e-mails bladert.

Zie voor meer informatie [Invoegtoepassingen gebruiken in Outlook op het web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Werken met contacten en documenten met behulp van de invoegtoepassing Contactinzichten

Stel u eens voor dat u een e-mailbericht ontvangt van een klant die een offerte voor enkele artikelen wil. U kunt rechtstreeks in Outlook de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing openen, die de afzender als een klant herkent en de klantkaart voor dat bedrijf opent. Vanuit dit dashboard kunt u overzichtsinformatie voor de klant zien, evenals inzoomen voor meer details over specifieke documenten. U kunt ook de verkoophistorie van de klant bekijken. Als dit een nieuw contact is, kunt u het als nieuwe klant toevoegen in [!INCLUDE[prod_short](includes/prod_short.md)] zonder Outlook te verlaten.  

In de invoegtoepassing kunt u een verkoopofferte maken en deze naar de klant verzenden zonder Outlook te verlaten. Alle informatie die u in de verkoopofferte moet verzenden, is beschikbaar in uw bedrijfsinbox in Outlook. Nadat u de gegevens hebt ingevoerd, kunt u de offerte boeken en per e-mail verzenden. [!INCLUDE[prod_short](includes/prod_short.md)] genereert een .pdf-bestand met de verkoopofferte en koppelt dat aan het e-mailbericht dat u opstelt in de invoegtoepassing.  

En als u een e-mail van een leverancier ontvangt, kunt u net zo de invoegtoepassing gebruiken om met leveranciers en inkoopfacturen te werken.  

Soms wilt u meer velden bekijken dan u in de invoegtoepassing kunt weergeven, zoals wanneer u regels in een factuur wilt invullen. Als u wat meer ruimte wilt krijgen om mee te werken kunt u de invoegtoepassing op een aparte pagina openen. Het is nog deel van Outlook, maar u hebt meer ruimte. Terwijl u in de pop-upweergave gegevens voor het document invoert, worden de wijzigingen automatisch opgeslagen. De volgende secties leiden u door enkele basistaken om u een algemeen begrip te geven van het gebruik ervan.

> [!TIP]
> In de taken wordt uitgelegd hoe u de invoegtoepassing vanuit een e-mailbericht kunt gebruiken. Maar u kunt hetzelfde doen vanuit een agenda-afspraak in Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Een zakelijk contact opzoeken bij het opstellen van een e-mail

1. Maak een nieuw e-mailbericht.
2. Ga op het lint naar **[!INCLUDE[prod_short](includes/prod_short.md)]** en kies **Contactinzichten**. Of als u Outlook op het web gebruikt, gaat u naar de onderkant van het bericht en kiest u ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) > **Contactinzichten**.
3. Zoek en kies in het deelvenster van de **[!INCLUDE[prod_short](includes/prod_short.md)]**-invoegtoepassing het gewenste contact.

    Een overzicht van het contact wordt weergegeven in het deelvenster en het contact wordt toegevoegd aan de **Aan**-regel van de e-mail.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>De contactgegevens bekijken of wijzigen of van bedrijf wisselen

De actiebalk boven aan het deelvenster van de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing bevat verschillende acties waarmee u dieper in details over de contactpersoon kunt graven en dingen kunt wijzigen.

![Actiebalk van Business Central-invoegtoepassing in Outlook.](media/outlook-addin-action-bar.png)

U kunt bijvoorbeeld de volledige contactgegevens openen zoals u ze zou zien in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u met meer dan één [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf werkt, kunt u gemakkelijk tussen bedrijven schakelen.

### <a name="track-incoming-documents"></a>Inkomende documenten traceren 

Misschien gebruikt u de lijst **Inkomende documenten** in [!INCLUDE[prod_short](includes/prod_short.md)] om documenten bij te houden voor verwerking die leveranciers naar u sturen, zoals een inkoopfactuur die moet worden betaald. Als u dat doet, kunt u eenvoudig records voor inkomende documenten maken vanuit de Outlook-invoegtoepassing en de e-mailbijlagen toevoegen.

1. Wanneer u een e-mail ontvangt van een leverancier met een bijlage, kiest u ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contactinzichten**. 

2. Kies in de actiebalk van de invoegtoepassing **Meer acties weergeven** en kies vervolgens **Verzenden naar inkomende documenten**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Nieuw document maken en verzenden naar een contact

1. Kies in het lint of onder aan het e-mailbericht ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nieuw** en kies vervolgens het type document dat u wilt maken, zoals **Verkoopofferte**.
2. Breng wijzigingen aan in het document in het deelvenster van de **[!INCLUDE[prod_short](includes/prod_short.md)]**-invoegtoepassing.
3. Wanneer het document klaar is om naar het contact te worden verzonden, kiest u in de actiebalk **Meer acties weergeven** en kiest u vervolgens de actie **Verzenden via e-mail**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Een document bekijken vanuit een e-mail met de invoegtoepassing Documentweergave

Of het nu een e-mail is die u hebt verzonden of ontvangen, u kunt elk [!INCLUDE[prod_short](includes/prod_short.md)]-document, zoals de verkoopofferte, rechtstreeks in Outlook bekijken. Van daaruit kunt u wijzigingen aanbrengen en naar gerelateerde informatie navigeren&mdash;net zoals u dat van binnen [!INCLUDE[prod_short](includes/prod_short.md)] zou doen.

Als u de Outlook-app gebruikt, kiest u gewoon **Documentkoppeling** boven aan het e-mailbericht. Zoek voor Outlook op het web naar de documentreferentielink in het e-mailbericht. De tekst van de referentielink bevat het documentnummer, dat is gebaseerd op de nummerreeks die wordt gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)]. De link voor een verkoopofferte zou bijvoorbeeld zoiets zijn als **Verkoopofferte S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Business Central op mijn mobiele apparaat krijgen](install-mobile-app.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Financiën](finance.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Minimale vereisten voor Outlook](product-requirements.md#outlook)  
[Invoegtoepassingen gebruiken in Outlook op het web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]