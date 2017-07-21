---
title: BTW-aangifte aan belastingdienst beheren| Microsoft Docs
description: Leren om een rapport voor te bereiden met btw van verkopen in een bepaalde periode, en het rapport verzenden aan de belastingdienst.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Procedure: Btw rapporteren aan de belastingdienst
De lijst Verkoopoverzicht EU bevat de btw-bedragen die u hebt geïnd voor verkopen binnen de EU, zodat u de btw-bedragen kunt verzenden naar de webservice van de belastingdienst.

> [!NOTE]  
>   In het VK moeten alle bedrijven die elk jaar meer dan een bepaalde waarde verkopen aan klanten in EU-lidstaten, een elektronische versie indienen van hun verkoopoverzicht EU in XML-indeling, door middel van de website van Her Majesty's Revenue and Customs (HMRC).

De lijst Verkoopoverzicht EU werkt alleen voor landen in de EU. Deze bevat bijvoorbeeld geen btw van verkopen aan andere landen zoals China of de Verenigde Staten.

Als u elektronisch btw wilt aangeven bij een belastingdienst, moet u [!INCLUDE[d365fin](includes/d365fin_md.md)] verbinden met de webservice van de belastingdienst. Hiertoe moet u een account instellen bij uw belastingdienst. Wanneer u een account hebt ingesteld, kunt u een serviceverbinding inschakelen die we aanbieden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In het VK kunt u bijvoorbeeld de serviceverbinding **GovTalk** gebruiken.

De lijst bevat slechts één regel voor elke soort transactie met de klant en toont het totale bedrag voor elk soort transactie. Er zijn drie soorten transacties die de lijst kan bevatten:  
  
* B2B-goederen  
* B2B-services  
* B2B getrianguleerde goederen  
  
B2B-goederen en -services geven aan of u een artikel of een service hebt verkocht en worden bepaald door de instelling **EU-service** in de btw-boekingsinstellingen. B2B getrianguleerde goederen geven aan of u hebt gehandeld met een derde en worden bepaald door de instelling **ABC-/Driehoekstransacties** op verkoopdocumenten, zoals verkooporders, facturen, creditnota's, enzovoort.  
  
Als u de lijst hebt verzonden, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] de service en wordt een record van uw communicatie bijgehouden. Het veld **Status** geeft aan waar in het proces de lijst zich bevindt. Als de belastingdienst uw rapport bijvoorbeeld verwerkt, verandert de status van het rapport in **Succesvol**. Als de belastingdienst fouten in de lijst heeft gevonden die u hebt verzonden, wordt de status van de lijst **Mislukt**. U kunt de fouten bekijken onder **Fouten en waarschuwingen**, deze corrigeren en vervolgens de lijst opnieuw verzenden. Als u een overzicht wilt van al uw verkoopoverzichten EU, gaat naar de pagina **Rapporten verkoopoverzicht EU**.  
  
> [!NOTE]  
>   Als u een andere methode gebruikt om de lijst te verzenden, bijvoorbeeld door de XML te exporteren en deze te uploaden naar een website, kunt u daarna **Markeren als verzonden** kiezen om de rapportageperiode te sluiten. Wanneer u het btw-rapport markeert als vrijgegeven, wordt het niet-bewerkbaar. Als u het rapport moet wijzigen nadat het is gemarkeerd als vrijgegeven, moet u het opnieuw openen. 
  
Nadat de belastingdienst uw lijst heeft gecontroleerd, wordt er een e-mail naar de contactpersoon voor uw bedrijf verzonden. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt de contactpersoon opgegeven op de pagina **Bedrijfsgegevens**. Voordat u de lijst verzendt, moet u ervoor zorgen dat een contact is geselecteerd.

<!--> [!NOTE]  
>   De lijst Verkoopoverzicht EU kan maximaal 1000 regels bevatten. Als u meer regels hebt, moet u nog een lijst verzenden. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Verbinding maken met de webservice van uw belastingdienst
[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt serviceverbindingen die verbinding maken met belastingdienstwebsites. In het VK moet u bijvoorbeeld de serviceverbinding **GovTalk** inschakelen.  

1. In het veld **Zoeken naar pagina's of rapporten** voert u **Serviceverbindingen** in en kiest u de juiste koppeling. <!-- remember to get the updated text for this-->  
2. Vul de vereiste velden in.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Het Verkoopoverzicht EU instellen
1. Voer in het veld **Zoeken naar pagina's of rapporten** **Btw-rapportinstellingen** in en kies de juiste koppeling.  
2. Als u gebruikers deze lijst wilt laten wijzigen en verzenden, kiest u het selectievakje **Verzonden rapporten aanpassen**.  
3. Geef de nummerreeks op voor Verkoopoverzichten EU.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>De lijst Verkoopoverzicht EU voorbereiden en verzenden
1. Voer in het veld **Zoeken naar pagina's of rapporten** **Verkoopoverzicht EU** in en kies de juiste koppeling.  
2. Kies **Nieuw** en vul vervolgens de vereiste velden in.  
3. Als u de inhoud van de lijst wilt genereren, kiest u de actie **Regels voorstellen**.  

    > [!NOTE]  
>   U kunt transacties controleren die op de regel zijn opgenomen, voordat u de lijst verzendt. Kies hiervoor de regel en kies vervolgens de actie **Btw-posten weergeven**.  
4. Als u de lijst voor verzending wilt voorbereiden, kiest u de actie **Vrijgeven**.  
5. Als u de lijst wilt verzenden, kiest u de actie **Verzenden**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] controleert of het rapport correct is ingesteld. Als de validatie mislukt, worden de fouten weergegeven onder **Fouten en waarschuwingen**, zodat u de juiste wijzigingen kunt aanbrengen.

## <a name="viewing-communications-with-your-tax-authority"></a>Communicatie met uw belastingdienst weergeven
In sommige landen kunt u berichten met de belastingdienst uitwisselen wanneer u rapporten verzendt. U kunt het eerste en laatste bericht dat u hebt ontvangen of verzonden, bekijken door de acties **Indieningsbericht downloaden** en **Responsbericht downloaden** te kiezen.  

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
[Btw instellen](finance-setup-vat.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Procedure: Verkopen factureren](sales-setup-sales.md)  

