---
title: OCR gebruiken om van PDF e-facturen te maken
description: Beschrijft hoe u een OCR-service kunt gebruiken voor het converteren van inkomende PDF- of afbeeldingsbestanden naar elektronische documenten.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten

Vanuit PDF- of afbeeldingsbestanden die u ontvangt van uw handelspartners, kunt u elektronische documenten laten genereren door een externe OCR-service (Optical Character Recognition - optische tekenherkenning), die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)]. Bijvoorbeeld, wanneer u facturen in PDF-indeling van uw leverancier ontvangt, kunt u deze [naar de OCR-service verzenden vanaf de pagina **Inkomende documenten**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Als alternatief voor het verzenden van het bestand vanaf de pagina **Inkomende documenten**, kan de OCR-service de optie bieden om [bestanden te verwerken die zijn doorgestuurd naar een speciaal e-mailadres](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Wanneer u het elektronische document terug ontvangt, wordt automatisch een gerelateerde inkomende documentrecord gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)].

Na enkele seconden zal de OCR-service het verwerkte bestand naar de pagina **Inkomende documenten** sturen als een elektronische documentrecord die kan worden [omgezet naar een inkoopfactuur voor de leverancier](#to-receive-the-resulting-electronic-document-from-the-ocr-service), een verkoopfactuur, een creditnota of een journaalboeking.

Omdat OCR is gebaseerd op optische herkenning, is het waarschijnlijk dat de OCR-service tekens in uw PDF- of afbeeldingsbestanden verkeerd interpreteert wanneer bijvoorbeeld de documenten van een bepaalde leverancier voor het eerst worden verwerkt. De service interpreteert het bedrijfslogo mogelijk niet als de naam van de leverancier of interpreteert het totaalbedrag op een ontvangstbewijs verkeerd vanwege de lay-out ervan. Als u deze fouten voortaan wilt voorkomen, kunt u ze corrigeren in een aparte versie van de pagina **Inkomende documenten**. Vervolgens stuurt u de correcties terug naar de OCR-service om deze te trainen in het interpreteren van de specifieke tekens en velden wanneer de volgende keer een PDF- of afbeeldingsbestand voor dezelfde leverancier wordt ontvangen. Zie voor meer informatie [De OCR-service trainen om fouten te voorkomen](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Het verkeer van bestanden van en naar de OCR-service wordt verwerkt door een speciale taakwachtrij. Deze taakwachtrij wordt automatisch gemaakt wanneer u de externe OCR-serviceverbinding inschakelt. Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).

> [!NOTE]
> De OCR-functie wordt geleverd door externe providers. Kies een servicepakket dat past bij uw organisatie en/of land/regio. U vindt services die compatibel zijn met [!INCLUDE[prod_short](includes/prod_short.md)] en details over beschikbare functies op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## Een PDF- of afbeeldingsbestand verzenden naar de OCR-service vanaf de pagina Inkomende documenten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Maak een nieuwe inkomende documentrecord en koppel het bestand eraan. Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.  
3. Selecteer op de pagina **Inkomende documenten** een of meer regels en kies vervolgens de actie **Verzenden naar taakwachtrij**.

   De waarde in het veld **OCR-status** verandert in **Gereed**. Het bijgevoegde PDF- of afbeeldingsbestand wordt naar de OCR-service verzonden door de taakwachtrij, volgens de planning, als er geen fouten zijn.
4. Of selecteer op de pagina **Inkomende documenten** een of meer regels en kies de actie **Verzenden naar OCR-service** om de bestanden direct te verzenden voor verwerking.

   De waarde in het veld **OCR-status** verandert in **Verzonden** als er geen fouten zijn.

## Een PDF- of afbeeldingsbestand naar de OCR-service verzenden per e-mail

Vanuit uw e-mailtoepassing kunt u een e-mailbericht doorsturen naar de aanbieder van de OCR-service met het PDF- of afbeeldingsbestand als bijlage. Zie de website van de provider van de OCR-service voor meer informatie over het e-mailadres waarnaar het bericht moet worden verzonden.

Aangezien er geen inkomende documentrecord bestaat voor het bestand, wordt automatisch een nieuwe record gemaakt op de pagina **Inkomende documenten** wanneer de OCR-service het resulterende elektronische document verzendt. Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.

> [!NOTE]  
> Als u op een tablet of telefoon werkt, kunt u het bestand naar de OCR-service verzenden zodra u een foto van het document hebt gemaakt, of u kunt rechtstreeks een inkomend document maken. Zie [Een inkomende documentrecord maken door een foto te maken](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo) voor meer informatie.

## Het resulterende elektronische document ontvangen van de OCR-service

Het elektronische document dat door de OCR-service van het PDF- of het afbeeldingsbestand wordt gemaakt, wordt automatisch ontvangen op de pagina **Inkomende documenten** door de verwerkingswachtrijpost die wordt ingesteld wanneer u de OCR-service inschakelt.

Als u geen verwerkingswachtrij gebruikt of een voltooid OCR-document eerder wilt ontvangen dan volgens het verwerkingswachtrijschema wordt verwacht, kunt u de actie **Ontvangen van OCR-service** kiezen. Met deze optie worden alle documenten opgehaald die door de OCR-service zijn voltooid.

> [!NOTE]  
> Als de OCR-service zo is ingesteld dat handmatige verificatie van verwerkte documenten is vereist, bevat het veld **OCR-status** de waarde **In afwachting van verificatie**. In dat geval voert u de volgende stappen uit om u aan te melden bij de website van de OCR-service om een OCR-document handmatig te verifiëren.

1. Kies in het veld **OCR-status** de hyperlink **In afwachting van verificatie**.
2. Meld u op de website van de OCR-service aan met de aanmeldgegevens van uw OCR-serviceaccount. Zie voor meer informatie [Een OCR-service instellen](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   De gegevens voor het OCR-document worden weergegeven met zowel de broninhoud van het PDF- of afbeeldingsbestand als de resulterende OCR-veldwaarden.
3. Controleer handmatig de veldwaarden en bewerk of typ handmatig waarden in de velden die de OCR-service heeft gemarkeerd als onbepaald.
4. Kies de knop **Ok**. Het OCR-proces is voltooid en het resulterende elektronische document wordt verzonden naar de pagina **Inkomende documenten** in [!INCLUDE[prod_short](includes/prod_short.md)] in overeenstemming met het verwerkingswachtrijschema.
5. Herhaal stap 2 tot en met 4 voor elk ander OCR-document dat moet worden geverifieerd.

U kunt nu doorgaan met het, handmatig of automatisch, maken van documentrecords voor de ontvangen elektronische documenten in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie de volgende procedure voor meer informatie. U kunt ook [de nieuwe inkomende documentrecord aan bestaande geboekte of niet-geboekte documenten koppelen](across-how-connect-disconnect-income-document-records.md) zodat het bronbestand gemakkelijk toegankelijk is vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

## Een inkoopfactuur op basis van een elektronisch document ontvangen van de OCR-service maken

Met de volgende procedure wordt beschreven hoe u een inkoopfactuurrecord maakt op basis van een leveranciersfactuur die is ontvangen als een elektronisch document van de OCR-service. De procedure is hetzelfde wanneer u bijvoorbeeld een dagboekregel van een kostenontvangst maakt of een verkoopretourorder van een klant.

> [!NOTE]  
> De velden **Omschrijving** en **Nr.** op de gemaakte documentregels worden alleen ingevuld als u eerst tekst die is gevonden in het OCR-document, hebt toegewezen aan de twee velden in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt deze toewijzing als artikelverwijzingen uitvoeren, voor documentregels van het type Artikel. Zie voor meer informatie [Artikelverwijzingen gebruiken](inventory-how-use-item-cross-refs.md). U kunt ook de functie **Toewijzing tekst aan rekening** gebruiken. Zie [Tekst in een inkomend document toewijzen aan een bepaalde leveranciers-, grootboek- of bankrekening](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account) voor meer informatie.

1. Selecteer de regel voor het inkomende document en kies de actie **Document maken**.

In [!INCLUDE[prod_short](includes/prod_short.md)] wordt een inkoopfactuur gemaakt gebaseerd op de gegevens in het elektronische leveranciersdocument dat u van de OCR-service hebt ontvangen. Gegevens worden in de nieuwe inkoopfactuur ingevoegd op basis van de toewijzing die u als verwijzing of als toewijzing van tekst aan rekening hebt opgegeven.

Eventuele validatiefouten, die meestal worden veroorzaakt door onjuiste of ontbrekende mastergegevens in [!INCLUDE[prod_short](includes/prod_short.md)], worden weergegeven op het sneltabblad **Fouten en waarschuwingen**. Zie [Fouten afhandelen bij de ontvangst van elektronische documenten](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents) voor meer informatie.

### Tekst in een inkomend document aan een bepaalde leveranciersrekening toewijzen

Voor inkomende documenten gebruikt u meestal de actie **Tekst toewijzen aan rekening**om te definiëren daten bepaalde tekst op een leveranciersfactuurontvangen van OCR-service, is toegewezen aan een bepaalde leveranciersrekening. In de toekomst betekent elk deel van de inkomende documentbeschrijving dat bestaat als een toewijzingstekst, dat het veld **Leveranciersnr.** op resulterende document- of journaalregels van het type *Grootboekrekening* wordt gevuld met de betreffende leverancier.

U kunt tekst niet alleen aan een leveranciersrekening of aan grootboekrekeningen toewijzen, maar ook aan een bankrekening. Deze optie is nuttig voor elektronische documenten voor kosten die al zijn betaald en waarvoor u een dagboekregel wilt maken die kan worden geboekt naar een bankrekening.

1. Selecteer de betreffende inkomende documentregel en kies de actie **Tekst afstemmen op rekening**. De pagina **Toewijzing tekst aan rekening** wordt geopend.
2. In het veld **Toewijzing tekst** voert u de tekst in die moet worden opgenomen in leveranciersfacturen waarvoor u inkoopdocumenten of dagboekregels wilt maken. U kunt maximaal 50 tekens invoeren.
3. In het veld **Leveranciersnr.** voert u de leverancier in waarvoor het resulterende inkoopdocument of de dagboekregel wordt gemaakt.
4. In het veld **Debetrekeningnr.** voert u de debetgrootboekrekening in die wordt ingevoegd in het resulterende inkoopdocument of op de dagboekregel van het type Grootboekrekening.
5. In het veld **Creditrekeningnr.** voert u de creditgrootboekrekening in die wordt ingevoegd in het resulterende inkoopdocument of op de dagboekregel van het type Grootboekrekening.

   > [!NOTE]
   > Gebruik de velden **Bronsoort saldo** en **Bronnr. saldo** niet in combinatie met inkomende documenten. Deze worden alleen gebruikt voor automatische betalingsreconciliatie. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.
6. Herhaal stap 2 tot en met 5 voor alle tekst in inkomende documenten waarvoor u automatisch documenten wilt maken.

## Fouten afhandelen bij de ontvangst van elektronische documenten

1. Selecteer op de pagina **Inkomende documenten** de regel voor een elektronisch document dat is ontvangen van de OCR-service met fouten, aangegeven door de waarde *Fout* in het veld **OCR-status**.
2. Kies de actie **Bewerken**om de pagina **Inkomende documenten** te openen.
3. Selecteer op het sneltabblad **Fouten en waarschuwingen** het bericht en kies vervolgens de actie **Gerelateerde record openen**.
4. De pagina die de verkeerde of ontbrekende gegevens bevat, zoals een leverancierskaart waarop een veldwaarde ontbreekt, wordt geopend.
5. Corrigeer de fout of fouten zoals in elke foutmelding wordt beschreven.
6. Ga door met de verwerking van het inkomende elektronische document door nogmaals de actie **Handmatig maken** te kiezen.
7. Herhaal stap 5 en 6 voor eventuele andere fouten tot het elektronische document probleemloos kan worden ontvangen.

## De OCR-service trainen om fouten te voorkomen

Omdat OCR is gebaseerd op optische herkenning, kan de OCR-service tekens in uw PDF- of afbeeldingsbestanden verkeerd interpreteren wanneer bijvoorbeeld de documenten van een bepaalde leverancier voor het eerst worden verwerkt. De service interpreteert het bedrijfslogo mogelijk niet als de naam van de leverancier of interpreteert het totaalbedrag op een onkostenbewijs verkeerd vanwege de lay-out ervan. Als u dergelijke fouten voortaan wilt voorkomen, kunt u gegevens die van de OCR-service worden ontvangen, corrigeren en de feedback vervolgens terugsturen naar de service.

De pagina **Correctie OCR-gegevens**, die u opent vanuit de pagina **Inkomend document**, bevat de velden van het sneltabblad **Financiële informatie** in twee kolommen. Een kolom met de bewerkbare OCR-gegevens en een kolom met de alleen-lezen OCR-gegevens. Wanneer u de knop **OCR-feedback verzenden** kiest, wordt de inhoud van de pagina **Correctie OCR-gegevens** naar de OCR-service verzonden. De volgende keer dat de service PDF- of afbeeldingsbestanden verwerkt die de betreffende gegevens bevatten, worden uw correcties meegenomen om de documentherkenning te verbeteren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Open een inkomende documentrecord die gegevens bevat die van de OCR-service zijn ontvangen en die u wilt corrigeren.
3. Kies op de pagina **Inkomend document** de actie **Correctie OCR-gegevens**.
4. Overschrijf op de pagina **Correctie OCR-gegevens** de gegevens in de bewerkbare kolom voor elk veld dat een onjuiste waarde heeft.
5. Als u correcties ongedaan wilt maken die u hebt aangebracht sinds u de pagina **Correctie OCR-gegevens** hebt geopend, kiest u de actie **OCR-gegevens opnieuw instellen**.
6. Als u de correcties naar de OCR-service wilt sturen, kiest u de actie **OCR-feedback verzenden**.
7. Als u de correcties wilt opslaan, sluit u de pagina **Correctie OCR-gegevens**.

De velden op het sneltabblad **Financiële informatie** op de pagina **Inkomende documenten** worden bijgewerkt met nieuwe waarden die u in stap 4 hebt ingevoerd.

## Zie ook

[Inkomende documentrecords maken](across-how-create-income-document-records.md)
[Inkomende documentrecords maken direct van documenten en posten](across-how-connect-disconnect-income-document-records.md)
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
