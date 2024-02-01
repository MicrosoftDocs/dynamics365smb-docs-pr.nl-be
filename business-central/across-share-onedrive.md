---
title: Business Central-bestanden openen in OneDrive
description: Leer hoe u Business Central-gegevens kunt delen via OneDrive voor bedrijven.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Business Central-bestanden openen en delen in Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] maakt het gemakkelijk om bestanden op te slaan, te beheren en te delen met andere mensen via Microsoft OneDrive voor Bedrijven. Op de meeste pagina's met beschikbare bestanden, zoals de Rapportinbox, of als bestanden aan records zijn gekoppeld, vindt u de acties **Openen in OneDrive** en **Delen**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor rapporten":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="De acties Openen in OneDrive en Delen voor bijlagen":::


## <a name="open-in-onedrive"></a>Openen in OneDrive

Met de actie **Openen in OneDrive** wordt het bestand naar uw OneDrive gekopieerd en wordt het bestand vervolgens geopend in een toepassing, zoals Microsoft Excel online, Microsoft Word online of Microsoft PowerPoint online. 

<!--## Working with different types of files-->

Wanneer u **Openen in OneDrive** kiest, identificeert [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word- en PowerPoint-bestanden en opent deze in hun online toepassingen, dat wil zeggen Excel online, Word online en PowerPoint online. 

Met behulp van de online versies van deze toepassingen kunt u annotaties maken, bewerken en samenwerken met anderen zonder de browser te verlaten.

Voor andere populaire bestandstypen, zoals pdf's, tekstbestanden en afbeeldingen, biedt OneDrive bestandsviewers die functies bieden voor afdrukken, delen en meer. Als een bestand niet kan worden bekeken in OneDrive, wordt u mogelijk gevraagd om het te downloaden.

## <a name="share"></a>Deel

Met de actie **Delen** wordt het bestand naar uw OneDrive gekopieerd zodat u kunt zien met wie u het bestand al hebt gedeeld en het bestand met anderen kunt delen. Wanneer u de actie **Delen** selecteert, wordt de volgende pagina geopend.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Bestand delen in OneDrive":::

Als u bekend bent met OneDrive, herkent u misschien de bovengenoemde pagina. U ziet dat u twee opties hebt om het bestand te delen: **Koppeling verzenden** en **Koppeling kopiëren**.

- Met **Koppeling verzenden** kunt u de bestanden delen met specifieke personen. De personen met wie u het bestand deelt, krijgen een e-mail met een koppeling naar het bestand. Het bestand verschijnt ook in de sectie **Gedeeld** van hun OneDrive. Begin met het typen van de e-mailadressen of contactpersoonnamen in het veld **Naam, groep of e-mail**. Voeg desgewenst een bericht toe onder het veld **Naam, groep of e-mail**.

  > [!TIP]
  > Als u uw bericht in Outlook wilt opstellen, selecteert u de knop **Outlook**. De koppeling wordt ingevoegd in een concepte-mail en iedereen die u hebt ingevoerd voor delen, komt in de lijst **Aan**. Met deze optie kunt u e-mails schrijven met alle functies van Outlook, waaronder het opmaken van tekst, het toevoegen van andere bijlagen, het invoegen van afbeeldingen of tabellen en het toevoegen van CC- of BCC-ontvangers.

- Met **Koppeling kopiëren** wordt een bestandskoppeling gekopieerd die u kunt gebruiken om het bestand te delen via toepassingen zoals Facebook, Twitter of e-mail. 

Voordat u een bestandskoppeling verzendt of kopieert, stelt u het gewenste machtigingsniveau voor personen in. U kunt de huidige instelling zien onder **Koppeling verzenden** of **Koppeling kopiëren**. In de meeste gevallen is dit **Iedereen met de koppeling kan bewerken**, afhankelijk van de instellingen van uw beheerder. U kunt de machtigingen wijzigen door de koppeling te selecteren en wijzigingen aan te brengen op de pagina **Koppelingsinstellingen**.

De deelfunctie in Business Central is gebaseerd op OneDrive. Meer informatie over delen in OneDrive en machtigingen vindt u in [OneDrive-bestanden en -mappen delen](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> De actie **Delen** is niet beschikbaar in de Business Central-app voor mobiele apparaten.

## <a name="first-time-sign-in-from-business-central"></a>Eerste aanmelding vanuit Business Central

Wanneer u de actie **Openen in OneDrive** of **Delen** voor het eerst gebruikt, doet [!INCLUDE[prod_short](includes/prod_short.md)] het volgende:

1. De pagina **Lees de voorwaarden** wordt geopend. Lees de pagina, en als u akkoord gaat met de voorwaarden, selecteer **Akkoord** om door te gaan.
2. Er wordt een map gemaakt met de naam [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
3. In de map [!INCLUDE[prod_short](includes/prod_short.md)] wordt een map gemaakt met dezelfde naam als het bedrijf waarin u werkt. Als u in meer dan één bedrijf werkt, wordt met [!INCLUDE[prod_short](includes/prod_short.md)] een map gemaakt voor elk bedrijf waarin u werkt wanneer u de actie **Openen in OneDrive** of **Delen** gebruikt. 
4. Plaatst een kopie van het bestand dat u hebt geselecteerd in de bedrijfsnaammap en opent vervolgens het bestand. 

De volgende keer dat u de actie **Openen in OneDrive** of **Delen** gebruikt, wordt met [!INCLUDE[prod_short](includes/prod_short.md)] alleen het bestand gekopieerd en geopend. 

## <a name="managing-multiple-copies-of-a-file"></a>Meerdere exemplaren van een bestand beheren

Wanneer u **Openen in OneDrive** of **Delen** kiest, wordt het bestand gekopieerd van [!INCLUDE[prod_short](includes/prod_short.md)] naar uw map in OneDrive. Als u het bestand in OneDrive bewerkt, is dat bestand anders dan het [!INCLUDE[prod_short](includes/prod_short.md)]-bestand. Als u [!INCLUDE[prod_short](includes/prod_short.md)] wilt bijwerken met de laatste bestandsversie, verwijdert u het bestaande bestand uit [!INCLUDE[prod_short](includes/prod_short.md)] en uploadt u de laatste kopie.

Als er al een bestand met dezelfde naam bestaat in OneDrive, krijgt u de volgende keuzes:

- **Bestaande gebruiken**

  Met deze optie wordt het bestand geopend of gedeeld dat al is opgeslagen in OneDrive, in plaats van het bestand uit Business Central te kopiëren.
  
- **Vervangen**
  
  Met deze optie wordt het bestaande bestand in OneDrive vervangen met het bestand dat u hebt geselecteerd in Business Central. Het oorspronkelijke bestand is niet verloren&mdash;u kunt het zien en herstellen met behulp van de versiegeschiedenis in OneDrive. Meer informatie vindt u in [Een eerdere versie herstellen van een bestand dat is opgeslagen in OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive-159cad6d-d76e-4981-88ef-de6e96c93893).

- **Beide behouden**

  Met deze optie wordt het bestaande bestand ongewijzigd behouden en wordt het bestand opgeslagen dat u hebt geselecteerd in Business Central onder een andere naam. De nieuwe naam is vergelijkbaar met de bestaande naam, behalve met een achtervoegselnummer zoals "Items (2).xlsx".

## <a name="about-your-business-central-folder-on-onedrive"></a>Over uw Business Central-map op OneDrive

De map en de inhoud ervan zijn privé totdat u besluit ze met anderen te delen. U kunt dus besluiten om inhoud te delen met een of meer van uw collega's, of zelfs met mensen buiten uw organisatie. 

U heeft toegang tot uw OneDrive vanuit de pagina **Mijn instellingen** door de link in het veld **Cloudopslag** te kiezen. Meer informatie vindt u in [OneDrive-bestanden en -mappen delen](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Het veld Cloudopslag in Mijn instellingen":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Zie ook

[Integratie van Business Central en OneDrive](across-onedrive-overview.md)  
[OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)
