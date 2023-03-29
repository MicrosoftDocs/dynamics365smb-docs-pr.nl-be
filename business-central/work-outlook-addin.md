---
title: Business Central met Outlook gebruiken
description: Deze service is nauw geïntegreerd met Microsoft 365. U kunt al uw bedrijfs- en e-mailcommunicatie met klanten en leveranciers rechtstreeks in Outlook beheren.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365'
ms.date: 04/21/2022
ms.author: jswymer
---
# Business Central gebruiken als uw bedrijfsinbox in Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] biedt een invoegtoepassing waarmee u bedrijfsinteracties kunt beheren met uw klanten en leveranciers, rechtstreeks in Microsoft Outlook. Met de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing voor Outlook kunt u financiële gegevens bekijken met betrekking tot klanten en leveranciers, en financiële documenten maken en verzenden, zoals offertes en facturen.

De [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing bestaat uit twee afzonderlijke invoegtoepassingen die de volgende mogelijkheden bieden:

- Contactinzichten

   Met deze invoegtoepassing kunt u [!INCLUDE[prod_short](includes/prod_short.md)]-klant- of leveranciersinformatie opzoeken in Outlook-e-mails en agenda-afspraken. Het stelt u ook in staat om [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijfsdocumenten te maken en te verzenden, zoals een verkoopofferte of factuur aan een contact.

- Documentweergave

   Wanneer een bedrijfsdocument wordt verzonden in een e-mail, biedt de invoegtoepassing een directe, in-line koppeling van de hoofdtekst van de e-mail naar het eigenlijke bedrijfsdocument in [!INCLUDE[prod_short](includes/prod_short.md)].

## Aan de slag

1. Het eerste dat u moet doen, is de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing geïnstalleerd krijgen in Outlook. Uw beheerder heeft de invoegtoepassing mogelijk al voor u geïnstalleerd. Dus als u het niet zeker weet, neem dan contact op met uw beheerder of bekijk de volgende stap om te controleren of het is geïnstalleerd.

    Als de invoegtoepassing niet voor u is geïnstalleerd, zie [De invoegtoepassing installeren voor eigen gebruik](admin-outlook.md#install). 

2. Als de invoegtoepassing is geïnstalleerd, hebt u toegang tot de **[!INCLUDE[prod_short](includes/prod_short.md)]**-toepassing vanuit elk nieuw of bestaand e-mailbericht of agenda-afspraak in Outlook.

    Begin door in te loggen op Outlook en een e-mailbericht te openen. Als u de Outlook-app gebruikt, ga dan naar het lint en zoek naar **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Of als u Outlook op het web gebruikt, zoekt u boven of onder aan het e-mailbericht naar ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) of gaat u naar de Meer-acties ![Meer acties voor een e-mail weergeven in Outlook.](media/outlook-more-actions-button.png) -knop.

    ![Business Central-invoegtoepassingen in Outlook openen.](media/outlook-business-central-addin.png)

   Als u de invoegtoepassing zelf hebt geïnstalleerd en ervoor hebt gekozen om een voorbeeld-e-mail te ontvangen, controleer dan uw inbox voor de welkomst-e-mail. Deze e-mail bevat informatie om u op weg te helpen.

De eerste keer dat u de invoegtoepassing gebruikt, wordt u in het deelvenster van de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing, mogelijk gevraagd om in te loggen. Kies in dit geval **Nu aanmelden** en volg de instructies op het scherm om u aan te melden bij Business Central met uw account.

> [!TIP]
> Als u de nieuwe versie van Outlook op het web gebruikt, kunt u **[!INCLUDE[prod_short](includes/prod_short.md)]** vastzetten, zodat het altijd direct zichtbaar is, in plaats van dat u naar de knop Meer acties moet gaan, waardoor het handig is om contactinzichten te bekijken terwijl u door verschillende e-mails bladert.

Zie voor meer informatie [Invoegtoepassingen gebruiken in Outlook op het web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## Werken met contacten en documenten met behulp van de invoegtoepassing Contactinzichten

Stel u eens voor dat u een e-mailbericht ontvangt van een klant die een offerte voor enkele artikelen wil. U kunt rechtstreeks in Outlook de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing openen, die de afzender als een klant herkent en de klantenkaart voor dat bedrijf opent. Vanuit dit dashboard kunt u overzichtsinformatie voor de klant zien, evenals inzoomen voor meer details over specifieke documenten. U kunt ook de verkoophistorie van de klant bekijken. Als dit een nieuw contact is, kunt u het als nieuwe klant toevoegen in [!INCLUDE[prod_short](includes/prod_short.md)] zonder Outlook te verlaten.  

In de invoegtoepassing kunt u een verkoopofferte maken en deze naar de klant verzenden zonder Outlook te verlaten. Alle informatie die u in de verkoopofferte moet verzenden, is beschikbaar in uw bedrijfsinbox in Outlook. Nadat u de gegevens hebt ingevoerd, kunt u de offerte boeken en per e-mail verzenden. [!INCLUDE[prod_short](includes/prod_short.md)] genereert een .pdf-bestand met de verkoopofferte en koppelt dat aan het e-mailbericht dat u opstelt in de invoegtoepassing.  

En als u een e-mail van een leverancier ontvangt, kunt u net zo de invoegtoepassing gebruiken om met leveranciers en inkoopfacturen te werken.  

Soms wilt u meer velden bekijken dan u in de invoegtoepassing kunt weergeven, zoals wanneer u regels in een factuur wilt invullen. Als u wat meer ruimte wilt krijgen om mee te werken kunt u de invoegtoepassing op een aparte pagina openen. Het is nog deel van Outlook, maar u hebt meer ruimte. Terwijl u in de pop-upweergave gegevens voor het document invoert, worden de wijzigingen automatisch opgeslagen. De volgende secties leiden u door enkele basistaken om u een algemeen begrip te geven van het gebruik ervan.

> [!TIP]
> In de taken wordt uitgelegd hoe u de invoegtoepassing vanuit een e-mailbericht kunt gebruiken. Maar u kunt hetzelfde doen vanuit een agenda-afspraak in Outlook.

### Een zakelijk contact opzoeken bij het opstellen van een e-mail

1. Maak een nieuw e-mailbericht.
2. Ga op het lint naar **[!INCLUDE[prod_short](includes/prod_short.md)]** en kies **Contactinzichten**. Of als u Outlook op het web gebruikt, gaat u naar de onderkant van het bericht en kiest u ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) > **Contactinzichten**.
3. Zoek en kies in het deelvenster van de **[!INCLUDE[prod_short](includes/prod_short.md)]**-invoegtoepassing het gewenste contact.

    Een overzicht van het contact wordt weergegeven in het deelvenster en het contact wordt toegevoegd aan de **Aan**-regel van de e-mail.

### De contactgegevens bekijken of wijzigen of van bedrijf wisselen

De actiebalk boven aan het deelvenster van de [!INCLUDE[prod_short](includes/prod_short.md)]-invoegtoepassing bevat verschillende acties waarmee u dieper in details over de contactpersoon kunt graven en dingen kunt wijzigen.

![Actiebalk van Business Central-invoegtoepassing in Outlook.](media/outlook-addin-action-bar.png)

U kunt bijvoorbeeld de volledige contactgegevens openen zoals u ze zou zien in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u met meer dan één [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf werkt, kunt u gemakkelijk tussen bedrijven schakelen.

### Inkomende documenten traceren

Misschien gebruikt u de lijst **Inkomende documenten** in [!INCLUDE[prod_short](includes/prod_short.md)] om documenten bij te houden voor verwerking die leveranciers naar u sturen, zoals een inkoopfactuur die moet worden betaald. Als u dat doet, kunt u eenvoudig records voor inkomende documenten maken vanuit de Outlook-invoegtoepassing en de e-mailbijlagen toevoegen.

1. Wanneer u een e-mail ontvangt van een leverancier met een bijlage, kiest u ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contactinzichten**.  

2. Kies in de actiebalk van de invoegtoepassing **Meer acties weergeven** en kies vervolgens **Verzenden naar inkomende documenten**. .  

### Nieuw document maken en verzenden naar een contact

1. Kies in het lint of onder aan het e-mailbericht ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nieuw** en kies vervolgens het type document dat u wilt maken, zoals **Verkoopofferte**.
2. Breng wijzigingen aan in het document in het deelvenster van de **[!INCLUDE[prod_short](includes/prod_short.md)]**-invoegtoepassing.
3. Wanneer het document klaar is om naar het contact te worden verzonden, kiest u in de actiebalk **Meer acties weergeven** en kiest u vervolgens de actie **Verzenden via e-mail**.

### Bestanden bijvoegen bij records

Uw e-mailpostvak dient vaak als een bron van inkomende bestanden die werkstomen initiëren of deblokkeren. Bestanden kunnen zaken bevatten zoals betalingen van pdf-facturen, foto's van goederen of vereisten in een Word-document. Wanneer u in Outlook werkt met Business Central-records zoals leveranciers, klanten, inkoopfacturen of verkooporders, kunt u deze bestanden aan de records toevoegen.

Er zijn een aantal manieren waarop u bestanden kunt bijvoegen. Een daarvan is om bestanden vanaf uw apparaat te uploaden. De andere manier is het uploaden van bestanden die bij een e-mail zijn gevoegd. Stel dat u een e-mail ontvangt met bestanden van een contactpersoon. De invoegtoepassing geeft automatisch de contactrecord weer die overeenkomt met de afzender van de e-mail. Van daaruit kunt u naar een document voor de contactpersoon navigeren, zoals de laatste verkooporder. Zodra u de order hebt geïdentificeerd waarop de e-mail betrekking heeft, uploadt u snel de bestanden uit de e-mail naar die order.

![Laat zien hoe u bijlagen van een e-mail toevoegt aan records in Business Central.](media/outlook-attach-files.png)

Nadat een bestand is bijgevoegd, kunnen collega's het bestand direct downloaden en bekijken vanaf het Feitenblok **Bijlagen** in een van hun Business Central-clients. Of ze kunnen het bestand openen in OneDrive om het te delen met hun afdeling en samen te werken.

#### Een bestand bijvoegen

1. Open de e-mail, kies ![pictogram van Business Central-invoegtoepassing in Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Contactinzichten**.
2. Kies in de actiebalk van de invoegtoepassing **Meer acties weergeven** > **Bijlagen**.

    De pagina **Bijgevoegde documenten** wordt geopend om alle documenten weer te geven die al aan de record zijn gekoppeld.
3. Kies **Bijgevoegd(e) bestand(en)** en kies vervolgens een van de volgende opties:

   - Kies **Koppelen vanuit e-mail** om alle of geselecteerde bestanden te uploaden die aan de e-mail zijn toegevoegd.
   - Kies **Uploaden uit bestand** om een of meer bestanden vanaf uw apparaat te uploaden.

> [!NOTE]
> U kunt niet aan alle records bestanden bijvoegen. Deze functie is beschikbaar voor records die het Feitenblok **Bijlagen** gebruiken, zoals een leverancier, klant, inkoopfactuur of verkooporder.

## Een document bekijken vanuit een e-mail met de invoegtoepassing Documentweergave

Of het nu een e-mail is die u hebt verzonden of ontvangen, u kunt elk [!INCLUDE[prod_short](includes/prod_short.md)]-document, zoals de verkoopofferte, rechtstreeks in Outlook bekijken. Van daaruit kunt u wijzigingen aanbrengen en naar gerelateerde informatie navigeren&mdash;net zoals u dat van binnen [!INCLUDE[prod_short](includes/prod_short.md)] zou doen.

Als u de Outlook-app gebruikt, kiest u gewoon **Documentkoppeling** boven aan het e-mailbericht. Zoek voor Outlook op het web naar de documentreferentielink in het e-mailbericht. De tekst van de referentielink bevat het documentnummer, dat is gebaseerd op de nummerreeks die wordt gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)]. De link voor een verkoopofferte zou bijvoorbeeld zoiets zijn als **Verkoopofferte S-QUO1000**.  

> [!TIP]
> Vanaf releasewave 1 van 2022 openen documenten in een nieuw browservenster met alle mogelijkheden die u kent van [!INCLUDE [prod_short](includes/prod_short.md)]. U kunt van een document naar een lijst navigeren en weer terug, lijsten openen in Excel, documenten verzenden om af te drukken en gerelateerde rapporten uitvoeren of bekijken. U beschikt ook over alle bekende sneltoetsen wanneer u documenten vanuit Outlook opent.  


## Zie gerelateerde [Microsoft-training](/training/modules/alternative-interfaces-dynamics-365-business-central/index)

## Zie ook

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Business Central op mijn mobiele apparaat krijgen](install-mobile-app.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Financiën](finance.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Minimale vereisten voor Outlook](product-requirements.md#outlook)  
[Invoegtoepassingen gebruiken in Outlook op het web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
