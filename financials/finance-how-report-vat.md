---
title: BTW-rapporten indienen bij de belastingdienst| Microsoft Docs
description: Leren om rapporten voor te bereiden met btw van verkopen in een bepaalde periode, of van verkopen en inkopen, en het rapport verzenden aan de belastingdienst.
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 07/17/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2f1e4016df9932b0441d664e203be947e1fa643e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-report-vat-to-a-tax-authority"></a>Procedure: Btw rapporteren aan een belastingdienst
Dit onderwerp beschrijft de rapporten in [!INCLUDE[d365fin](includes/d365fin_md.md)] die u kunt gebruiken om gegevens over btw-bedragen voor verkopen en inkopen in te dienen bij de belastingdienst in uw regio.

U kunt de volgende rapporten gebruiken:

* Het **Verkoopoverzicht EU** bevat de btw-bedragen die u hebt geïnd voor verkopen aan btw-plichtige klanten in EU-landen.  
* Het rapport **BTW-aangifte** bevat btw voor verkopen en inkopen aan klanten in alle landen die btw gebruiken.

Als u een volledige historie van btw-posten wilt weergeven, maakt elke boeking waarop btw van toepassing is, een post op de pagina **Btw-posten**. Met deze posten wordt het btw-vereffeningsbedrag, dat uit een betaling of vergoeding kan bestaan, berekend voor een bepaalde periode. Als u btw-posten wilt weergeven, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Btw-posten** in en kiest u vervolgens de gerelateerde koppeling.

## <a name="about-the-ec-sales-list-report"></a>Informatie over het Verkoopoverzicht EU
In het VK moeten alle bedrijven die goederen en diensten verkopen aan btw-plichtige klanten, inclusief klanten in andere EU-landen, een elektronische versie indienen van het Verkoopoverzicht EU in XML-indeling door middel van de website van de HMRC (Her Majesty's Revenue and Customs). De lijst Verkoopoverzicht EU werkt alleen voor landen in de EU.

De lijst bevat slechts één regel voor elke soort transactie met de klant en toont het totale bedrag voor elk soort transactie. Er zijn drie soorten transacties die de lijst kan bevatten:  

* B2B-goederen  
* B2B-services  
* B2B getrianguleerde goederen  

B2B-goederen en -services geven aan of u een artikel of een service hebt verkocht en worden bepaald door de instelling **EU-service** in de btw-boekingsinstellingen. B2B getrianguleerde goederen geven aan of u hebt gehandeld met een derde en worden bepaald door de instelling **ABC-/Driehoekstransacties** op verkoopdocumenten, zoals verkooporders, facturen, creditnota's, enzovoort.  

Nadat de belastingdienst uw lijst heeft gecontroleerd, wordt er een e-mail naar de contactpersoon voor uw bedrijf verzonden. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt de contactpersoon opgegeven op de pagina **Bedrijfsgegevens**. Voordat u de lijst verzendt, moet u ervoor zorgen dat een contact is geselecteerd.

## <a name="about-the-vat-return-report"></a>Over het rapport BTW-aangifte
Gebruik deze lijst om btw voor verkoop- en inkoopdocumenten in te dienen, zoals inkoop- en verkooporders, facturen en creditnota's. De informatie in de lijst heeft dezelfde indeling als op het declaratieformulier van de douane en de belastingdienst.  

De btw wordt gebaseerd op de btw-boekingsinstelling en de btw-boekingsgroepen die u hebt ingesteld.

Voor de btw-aangifte kunt u de posten opgeven die u wilt opnemen:

* Alleen openstaande transacties of open en afgesloten transacties. Dit is bijvoorbeeld handig wanneer u de definitieve jaarlijkse btw-aangifte voorbereidt.
* Alleen posten uit de opgegeven perioden indienen of ook posten uit eerdere perioden opnemen. Dit is handig om een btw-retour bij te werken die u al hebt ingediend, bijvoorbeeld als u leverancier u een late factuur stuurt.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Verbinding maken met de webservice van uw belastingdienst
[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt serviceverbindingen met belastingdienstwebsites. Als u zich bijvoorbeeld in het VK bevindt, kunt u de **GovTalk**-serviceverbinding inschakelen om het Verkoopoverzicht EU en de btw-aangifte elektronisch in te dienen. Als u de lijst handmatig wilt verzenden, bijvoorbeeld door uw gegevens op de website van de belastingdienst in te voeren, is dit niet vereist.   

Als u elektronisch btw wilt aangeven bij een belastingdienst, moet u [!INCLUDE[d365fin](includes/d365fin_md.md)] verbinden met de webservice van de belastingdienst. Hiertoe moet u een account instellen bij uw belastingdienst. Wanneer u een account hebt ingesteld, kunt u een serviceverbinding inschakelen die we aanbieden in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceverbindingen** in en kies vervolgens de juiste koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
>   Het is aan te raden de verbinding te testen. Kies hiervoor het selectievakje **Testmodus** en bereid uw btw-aangifte voor en verzend deze zoals beschreven in de sectie _Een btw-aangifte voorbereiden en indienen_. In de testmodus test de service of de belastingdienst uw aangifte kan ontvangen en de status van de aangifte geeft aan of de testindiening succesvol was. Vergeet niet dat dit geen werkelijke indiening is. Als u de aangifte echt wilt indienen, moet u het selectievakje **Testmodus** uitzetten en de indiening herhalen.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>Btw-rapporten instellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-rapportinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Als u gebruikers deze lijst wilt laten wijzigen en opnieuw verzenden, kiest u het selectievakje **Verzonden rapporten aanpassen**.  
3. Kies de nummerreeks die voor elke aangifte moet worden gebruikt.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Een btw-aangifte voorbereiden en indienen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Btw-rapportinstellingen** of **BTW-aangifte** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies **Nieuw** en vul vervolgens de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u de inhoud van de lijst wilt genereren, kiest u de actie **Regels voorstellen**.  

    > [!NOTE]  
>   In het Verkoopoverzicht EU kunt u de transacties bekijken die in de aangifteregels zijn opgenomen, voordat u de aangifte indient. Kies hiervoor de regel en kies vervolgens de actie **Btw-posten weergeven**.  
4. Als u de lijst voor verzending wilt valideren en voorbereiden, kiest u de actie **Vrijgeven**.  

    >  [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)] controleert of het rapport correct is ingesteld. Als de validatie mislukt, worden de fouten weergegeven onder **Fouten en waarschuwingen**, zodat u weet wat u moet corrigeren. Als het bericht gaat over een ontbrekende instelling in [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u op het bericht kunt klikken om de pagina te openen met de te verbeteren informatie.  
5. Als u de lijst wilt verzenden, kiest u de actie **Verzenden**.  

Als u de lijst hebt verzonden, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] de service en wordt een record van uw communicatie bijgehouden. Het veld **Status** geeft aan waar in het proces de lijst zich bevindt. Als de belastingdienst uw rapport bijvoorbeeld verwerkt, verandert de status van het rapport in **Succesvol**. Als de belastingdienst fouten in de lijst heeft gevonden die u hebt verzonden, wordt de status van de lijst **Mislukt**. U kunt de fouten bekijken onder **Fouten en waarschuwingen**, deze corrigeren en vervolgens de lijst opnieuw verzenden. Als u een overzicht wilt van al uw verkoopoverzichten EU, gaat naar de pagina **Rapporten verkoopoverzicht EU**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Communicatie met uw belastingdienst weergeven
In sommige landen kunt u berichten met de belastingdienst uitwisselen wanneer u rapporten verzendt. U kunt het eerste en laatste bericht dat u hebt ontvangen of verzonden, bekijken door de acties **Indieningsbericht downloaden** en **Responsbericht downloaden** te kiezen.  

## <a name="submitting-vat-reports-manually"></a>Handmatig btw-aangiftes verzenden
Als u een andere methode gebruikt om de lijst te verzenden, bijvoorbeeld door de XML te exporteren en deze te uploaden naar een website, kunt u daarna **Markeren als verzonden** kiezen om de rapportageperiode te sluiten. Wanneer u het btw-rapport markeert als vrijgegeven, wordt het niet-bewerkbaar. Als u het rapport moet wijzigen nadat het is gemarkeerd als vrijgegeven, moet u het opnieuw openen.

## <a name="vat-settlement"></a>Btw-vereffening
U moet periodiek de netto-btw afdragen aan de belastingdienst. Als u vaak btw moet vereffenen, kunt u de batchverwerking **Btw-vereffening berekenen en boeken** uitvoeren om de open btw-posten te sluiten en inkoop- en verkoop-btw-bedragen over te boeken naar de btw-vereffeningsrekening.

Wanneer u btw-bedragen overmaakt naar de vereffeningsrekening, worden de bedragen die voor de opgegeven periode zijn berekend, opgeteld bij de rekening voor inkoop-btw en afgetrokken van de rekening voor verkoop-btw. Het nettobedrag wordt opgeteld of afgetrokken als het inkoop-btw-bedrag groter is, bij de btw-vereffeningsrekening. U kunt de vereffening meteen boeken of eerst een controlelijst afdrukken.

>    [!NOTE]  
>    Wanneer u de batchverwerking **Btw-vereffening berekenen en boeken** gebruikt en u geen **Btw-bedrijfsboekingsgroep** en **Btw-productboekingsgroep** opgeeft, worden posten met alle bedrijfsboekingsgroepen en productboekingsgroepscodes opgenomen.

## <a name="configuring-your-own-vat-reports"></a>Uw eigen btw-rapporten configureren
U kunt het verkoopoverzicht EU kant-en-klaar gebruiken, maar u kunt ook uw eigen lijsten maken. Hiertoe moet u enkele codeunits maken. Als u hierbij hulp nodig hebt, neemt u contact op met een Microsoft-partner.  

De volgende tabel beschrijft codeunits die u voor uw lijst moet maken.

| Codeunit | Wat het moet doen |
|----|-----|
|Regels voorstellen| Gegevens ophalen uit de tabel met btw-posten en deze weergeven op regels in het btw-rapport.|
|Inhoud | De indeling van het rapport bepalen. Bijvoorbeeld of het XML of JSON is. De te gebruiken indeling is afhankelijk van de webservice van uw belastingdienst. |
|Verzending | Bepaal hoe en wanneer u de lijst verzendt, op basis van de behoeften van uw belastingdienst. |
|Antwoordmanager | Behandel de retournering van de belastingdienst. Bijvoorbeeld, er kan een e-mailbericht naar de contactpersoon van uw bedrijf zijn verzonden. |
|Annuleren | Verzend een annulering of btw-rapport dat eerder is ingediend naar de belastingdienst. |

> [!NOTE]  
>   Wanneer u codeunits maakt voor het rapport, besteed dan aandacht aan de waarde in het veld **Btw-rapportversie**. Dit veld moet de versie reflecteren van het rapport dat is of werd vereist door de belastingdienst. U kunt bijvoorbeeld **2017** in het veld invoeren om aan te geven dat de lijst voldoet aan de vereisten die dat jaar golden. Als u de huidige versie wilt bepalen, neemt u contact op met de belastingdienst.  

## <a name="see-also"></a>Zie ook 
[Berekeningen en voor boekingsmethoden voor btw instellen](finance-setup-vat.md)  
[Procedure: Met btw werken bij verkoop en inkoop](finance-work-with-vat.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Procedure: Verkopen factureren](sales-setup-sales.md)  

