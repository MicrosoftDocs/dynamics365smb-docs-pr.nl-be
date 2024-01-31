---
title: De Business Central-invoegtoepassing voor Outlook verkrijgen
description: Leer hoe u de Business Central-invoegtoepassing voor Outlook installeert voor uw organisatie of voor eigen gebruik.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 04/27/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# De Business Central-invoegtoepassing voor Outlook verkrijgen

Met [!INCLUDE[prod_short](includes/prod_short.md)] kunt u bedrijfsinteracties met uw klanten en leveranciers rechtstreeks in Microsoft Outlook beheren. Met de [!INCLUDE[prod_short](includes/prod_short.md)] Outlook-invoegtoepassing kunt u financiële gegevens bekijken met betrekking tot klanten en leveranciers. U kunt ook financiële documenten maken en verzenden, zoals offertes en facturen.  

Er zijn twee manieren om de Business Central-invoegtoepassing voor Outlook te installeren, afhankelijk van uw rol in de organisatie:

- Gebruik als Microsoft 365-beheerder *Gecentraliseerde implementatie* om de invoegtoepassing automatisch te installeren voor de hele organisatie, groepen of specifieke gebruikers.

- Installeer als gebruiker de invoegtoepassing voor eigen gebruik, als uw beheerder deze nog niet voor u heeft geïmplementeerd.

## Over de Business Central-invoegtoepassing voor Outlook

De Business Central-invoegtoepassing voor Outlook bestaat uit twee kleinere invoegtoepassingen:

- Contactinzichten

    Deze invoegtoepassing biedt gebruikers met [!INCLUDE[prod_short](includes/prod_short.md)] klant- of leveranciersinformatie in Outlook-e-mails en agenda-afspraken. Het stelt u ook in staat om [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijfsdocumenten te maken en te verzenden, zoals verkoopoffertes en facturen aan een contact. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Documentweergave

    Wanneer een e-mail verwijst naar een bedrijfsdocumentnummer in de hoofdtekst van de e-mail, biedt deze invoegtoepassing een directe, in-line koppeling van de hoofdtekst van de e-mail naar het eigenlijke bedrijfsdocument in [!INCLUDE[prod_short](includes/prod_short.md)].

Zie [Business Central gebruiken als uw zakelijke inbox in Outlook](work-outlook-addin.md) voor meer informatie over wat u doet met de invoegtoepassingen.

Elke invoegtoepassing wordt geleverd als een XML-bestand, genaamd een *manifest*, dat in Outlook moet worden geïnstalleerd voor iedereen die deze functionaliteit wil. Deze bestanden beschrijven hoe u de invoegtoepassingen activeert en verbinding maakt met Business Central wanneer ze in Outlook worden gebruikt. Het werken met deze bestanden wordt meestal gedaan door een beheerder. Als normale gebruiker hoeft u in de meeste gevallen niet direct met deze bestanden om te gaan. Ofwel uw beheerder stelt de invoegtoepassing zo in dat deze automatisch voor u wordt geïnstalleerd of u gebruikt de ingebouwde begeleide instelling om de installatie af te handelen.

> [!IMPORTANT]
> Werken met meerdere omgevingen? De Business Central-invoegtoepassing voor Outlook is ontworpen om te werken met één Business Central-omgeving. Wanneer de invoegtoepassing is geïnstalleerd, wordt de naam van de omgeving opgenomen in het manifest van de invoegtoepassing. Deze configuratie betekent dat de invoegtoepassing alleen verbinding maakt met de omgeving van waaruit deze is geïnstalleerd. Om de invoegtoepassing met een andere omgeving te gebruiken, opent u de omgeving en installeert u de invoegtoepassing opnieuw.

## De invoegtoepassing implementeren met behulp van gecentraliseerde implementatie als beheerder

Gecentraliseerde implementatie is een functie in het Microsoft 365-beheercentrum die u gebruikt om automatisch invoegtoepassingen te installeren in Office-apps van gebruikers, zoals Outlook. Dit is de aanbevolen manier voor beheerders om Office-invoegtoepassingen te implementeren voor gebruikers en groepen binnen uw organisatie.

> [!NOTE]
> Voor Business Central on-premises zie [De invoegtoepassing voor Outlook-integratie instellen met Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) in de beheerinhoud (alleen Engels).

### Vereisten

- Een Microsoft 365-abonnement  
- Aan gebruikers wordt een Microsoft 365-licentie toegewezen  
- Uw Microsoft 365-account heeft de rol *Globale beheerder* of *Exchange-beheerder*

### De invoegtoepassing implementeren

1. Kies in Business Central het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Gecentraliseerde implementatie van Outlook-invoegtoepassing** om de begeleide instelling te starten.
3. Bekijk de eerste pagina en kies **Volgende** om de pagina te openen voor het downloaden van de invoegtoepassingen.
4. Selecteer in de kolom **Implementeren** het selectievakje voor de invoegtoepassingen die u wilt implementeren en kies vervolgens **Downloaden en doorgaan**.

    Een bestand met de naam *OutlookAddins.zip* wordt gedownload naar uw apparaat.

5. Op dit punt bent u klaar met het werk dat u moet doen in Business Central, dus u kunt **Gereed** kiezen.

   >[!TIP]
   > Selecteer voordat u **Volgende** kiest, de koppeling **Ga naar Microsoft 365 (wordt in een nieuw venster geopend)** om het Microsoft 365-beheercentrum te openen in een nieuw browservenster en u er bij aan te melden. U zult sowieso in een latere stap naar het Microsoft 365-beheercentrum moeten gaan.

6. Ga naar de map waar OutlookAddins.zip is gedownload en pak de bestanden **Contact Insights.xml** en **Document View.xml** uit de .zip uit in een map naar keuze.

    Voor meer informatie zie [Bestanden en mappen zippen en unzippen](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Meld u aan bij het Microsoft 365-beheercentrum en ga naar [Geïntegreerde apps](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Kies **Aangepaste apps uploaden**.
9. Kies op de pagina **Apps uploaden om te implementeren** **Manifestbestand (.xml) uploaden vanaf apparaat** > **Bestand kiezen**.
10. Selecteer een van de bestanden die u eerder hebt uitgepakt, bijvoorbeeld **Content Insights.xml**.
11. Volg de instructies om gebruikers toe te wijzen en de invoegtoepassing te implementeren.
12. Herhaal stap 9 tot en met 11 voor het andere bestand als u dat wilt.

> [!IMPORTANT]
> Er verschijnt een groen vinkje wanneer de invoegtoepassing is geïmplementeerd in het beheercentrum. Het kan echter tot 24 uur duren voordat gebruikers de invoegtoepassing zien in de Outlook-app. Gebruikers moeten mogelijk ook Outlook opnieuw starten.

Als u klaar bent, kunt u de implementatie altijd wijzigen in het Microsoft 365-beheercentrum, zoals het toewijzen van meer gebruikers. Zie [Invoegtoepassingen implementeren in het beheercentrum](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true) voor meer informatie over het implementeren van invoegtoepassingen in het beheercentrum.

## <a name="install"></a>De invoegtoepassing installeren voor eigen gebruik

Als uw organisatie dit toestaat, kunt u de Business Central-invoegtoepassing alleen voor uzelf installeren. Vraag het uw beheerder als u het niet zeker weet.

1. Ga in Business Central naar het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **De Outlook-invoegtoepassing ophalen** in en kies vervolgens de gerelateerde koppeling.
2. Lees de pagina en kies **Volgende** wanneer u klaar bent.
3. Als u een welkomstbericht van Business Central wilt ontvangen met een overzicht van het gebruik van de invoegtoepassing, schakelt u **Voorbeeld-e-mailbericht verzenden** in.
4. Kies **Voltooien** om de installatie te voltooien.

Business Central maakt verbinding met uw e-mailserver en installeert de invoegtoepassing in uw Outlook. Dit duurt niet lang. U bent nu klaar om de invoegtoepassing in Outlook te gaan gebruiken.

### <a name="onprem"></a>Voor Business Central on-premises

Als u Business Central on-premises gebruikt, kan het installeren van de invoegtoepassing iets anders zijn.

1. Ga in Business Central naar het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **De Outlook-invoegtoepassing ophalen** in en kies vervolgens de gerelateerde koppeling.
2. Lees de pagina en kies **Volgende** wanneer u klaar bent.
3. Voer een van de volgende stappen uit, afhankelijk van de pagina die u ziet:

    - Als u de knop **Installeren in mijn Outlook** ziet, kiest u deze en bent u klaar.
    - Als u de knop **Volgende** ziet, kiest u deze. Als u op de volgende pagina een welkomstbericht van Business Central wilt ontvangen met een overzicht van het gebruik van de invoegtoepassing, schakelt u **Voorbeeld-e-mailbericht verzenden** in. Kies dan **Voltooien** en u bent helemaal klaar.
    - Als u de knop **Invoegtoepassing downloaden** ziet, kiest u deze en gaat u naar de volgende stap.
4. Wanneer u **Invoegtoepassing downloaden** kiest, wordt een bestand met de naam *OutlookAddins.zip* gedownload naar uw apparaat. U zou het bestand boven aan de browser moeten zien.

   Ga naar de map waar OutlookAddins.zip is gedownload en pak de bestanden **Contact Insights.xml** en **Document View.xml** uit de .zip uit in een map naar keuze. Voor meer informatie over het uitpakken van bestanden zie [Bestanden en mappen zippen en unzippen](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Open Outlook en kies **Invoegtoepassingen ophalen** op het lint. Of, als u Outlook op het web gebruikt, selecteert u het vervolgkeuzemenu in een nieuw of bestaand e-mailbericht en selecteert u vervolgens **Invoegtoepassingen ophalen**.
6. Kies **Mijn invoegtoepassingen** > **Een aangepaste invoegtoepassing toevoegen** > **Toevoegen vanuit een bestand**.
7. Kies een van de .xml-bestanden die u hebt uitgepakt, zoals **Contact Insights.xml** en kies dan **Openen** > **Installeren**.
8. Herhaal stap 6 en 7 voor het andere .xml-bestand, als u er een hebt gedownload.

U bent nu klaar om de invoegtoepassing in Outlook te gaan gebruiken.

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
