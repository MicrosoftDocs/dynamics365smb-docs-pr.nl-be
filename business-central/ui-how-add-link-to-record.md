---
title: 'Bijlagen, koppelingen en notities aan records toevoegen'
description: 'Koppel een hyperlink naar een document of een website aan een bepaalde record, zoals een klant of document.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms-service: dynamics-365-business-central
ms.service: dynamics-365-business-central
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Bijlagen, koppelingen en notities op kaarten en in documenten beheren

Op de meeste lijstpagina's, kaarten en documenten kunt u bestanden bijvoegen, koppelingen toevoegen en notities schrijven op het tabblad **Bijlagen** van het venster **Feitenblok**. Het getal in de titel van het tabblad geeft aan hoeveel bijgevoegde bestanden, koppelingen of notities er zijn voor de kaart of het document.

Op het sneltabblad **Regels** kunt u ook de actie **Bijlagen** gebruiken om documenten aan een specifieke regel toe te voegen. U wilt bijvoorbeeld ontwerpspecificaties toevoegen aan een artikel op een inkoopfactuur.

Bijlagen, koppelingen en notities blijven aan kaarten of het documenten gekoppeld terwijl deze worden verwerkt in andere statussen. Bijvoorbeeld van een lopende verkooporder naar een geboekte verkoopfactuur. Geen van de bijlagetypen wordt echter door het systeem uitgevoerd, bijvoorbeeld bij het afdrukken of bij het opslaan in een bestand.

U kunt ook bijlagen toevoegen aan de e-mails die u verzendt vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. Wanneer u een e-mail rechtstreeks vanuit een document verzendt, zoals een verkoopofferte, kunt u met de actie **Bestand toevoegen vanuit brondocument** bestanden kiezen die eraan zijn toegevoegd. U kunt alleen bestanden kiezen die aan het document zijn toegevoegd. U kunt geen bestanden kiezen die aan regels zijn toegevoegd.

> [!NOTE]
> Wanneer u een verkooporder of inkooporder gedeeltelijk verzendt en factureert, wordt de bijlage alleen aan de definitieve factuur van de order toegevoegd. Wanneer u uitstel factureert, wordt de bijlage ook alleen gekoppeld aan de grootboekposten voor het document, maar niet voor de uitstelposten.
>
> Als u een bestelling verwijdert voordat deze wordt gefactureerd, wordt de bijlage ook verwijderd.
>
> Wanneer u de actie **Ontvangstregels ophalen** in een inkoopfactuur gebruikt, wordt de bijlage bij de gerelateerde inkooporder aan de inkoopfactuur toegevoegd.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Een bestand bijvoegen bij een inkoopfactuur

U kunt elk type bestand, zoals tekst, afbeelding of video, aan een kaart of document of aan een regel in een document toevoegen. Dit is bijvoorbeeld handig als u de factuur van een leverancier wilt opslaan als PDF-bestand op de bijbehorende inkoopfactuur in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Bestanden die zijn gekoppeld met de functie Inkomende documenten, worden niet opgenomen op het tabblad **Bijlagen**. Zie voor meer informatie [Inkomende documenten](across-income-documents.md). Hetzelfde geldt voor bestanden die zijn gekoppeld aan regels in documenten.

De volgende procedure is gebaseerd op een inkoopfactuur. De stappen lijken op alle andere ondersteunde documenten en kaarten.

> [!TIP]
> Als uw bijlage specifiek is voor een regel in een document, kunt u deze aan de regel toevoegen. Kies de regel en kies vervolgens de actie **Bijlagen**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Open de inkoopfactuur waaraan u een bestand wilt koppelen.
3. Kies in het venster **Feitenblok** het tabblad **Bijlagen**.
4. Kies de waarde achter het veld **Documenten**, zoals '0'.
5. Op de pagina **Gekoppelde documenten**, in het **Bijlage**.
6. Voer in het dialoogvenster **Een document Koppelen** een van de volgende stappen uit om een bestand te koppelen:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Het bestand wordt nu gekoppeld aan de inkoopfactuur.

## <a name="to-view-an-attached-file"></a>Een gekoppeld bestand weergeven

1. Open op het feitenblok het tabblad **Bijlagen**.
2. Kies de waarde achter het veld **Documenten**, zoals '1'.
3. Kies op de pagina **Gekoppelde documenten** de actie **Voorbeeld**.
4. Open het gedownloade bestand.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Een document als PDF-bijlage opslaan

Wanneer u een document als bestand moet opslaan, kunt u de actie **Bijvoegen als PDF** gebruiken om de huidige documentinhoud vast te leggen als een PDF-bestand als bijlage bij het feitenblok van het document. Dit is bijvoorbeeld handig wanneer documenten meerdere stappen in een proces volgen, zoals een verkoopproces of een goedkeuringswerkstroom, en u wilt verwijzen naar een afdruk van de vorige stap.

De volgende procedure is gebaseerd op een verkooporder. De stappen zijn vergelijkbaar voor alle ondersteunde documenten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een verkooporder en kies de actie **Bijvoegen als PDF**.

Een PDF-bestand met de huidige inhoud van de verkooporder wordt toegevoegd aan het tabblad **Bijlagen** in het feitenblok.

## <a name="to-add-a-link-from-an-item-card"></a>Een koppeling toevoegen vanuit een artikelkaart

U kunt een koppeling vanuit een kaart of document toevoegen aan een URL. Dit is bijvoorbeeld handig als u een artikelkaart wilt koppelen aan de artikelcatalogus van de leverancier.

De volgende procedure is gebaseerd op een artikelkaart. De stappen lijken op alle andere ondersteunde documenten en kaarten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het item waaruit u een koppeling wilt toevoegen en kies vervolgens het tabblad **Bijlagen** in het feitenblok.
3. Kies in de **Koppelingen** het pictogram **+**.
4. Voer in het veld **Koppelingsadres** de koppeling in.

    De koppeling moet een geldige internet- of intranet-URL zijn.

5. Voer in het veld **Beschrijving** informatie over de koppeling in.  
6. Kies de knop **Ok**.

De koppeling is nu gekoppeld aan de artikelkaart.  

## <a name="to-write-a-note-on-a-sales-order"></a>Een notitie over een klantorder schrijven

U kunt bijvoorbeeld een notitie op een document of kaart schrijven om speciale instructies aan andere gebruikers van het document of de kaart te communiceren. U kunt bestandskoppelingen en URL's opnemen in notities.

> [!NOTE]
> Opmerkingen over het tabblad **Bijlagen** zijn niet gerelateerd aan interne notitiefunctionaliteit, die voornamelijk wordt gebruikt om te communiceren tussen werkstroomgebruikers. Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).

De volgende procedure is gebaseerd op een verkooporder. De stappen lijken op alle andere ondersteunde documenten en kaarten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de verkooporder waarin u een notitie wilt schrijven en kies vervolgens het tabblad **Bijlagen** in het feitenblok.
3. Kies in de sectie **Notities** het pictogram **+**.
4. Schrijf in het veld **Notitie** tekst, zoals "Dit is een dringende bestelling."
5. Kies de knop **Ok**.

De notitie is nu aan de verkooporder toegevoegd.

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Inkomende documenten](across-income-documents.md)  
[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
