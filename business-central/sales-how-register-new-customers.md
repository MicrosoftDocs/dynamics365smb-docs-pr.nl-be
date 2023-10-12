---
title: Nieuwe klanten registreren door een klantenkaart te maken (bevat video)
description: Beschrijft hoe u een klantenkaart maakt om informatie te registreren over elke nieuwe klant of cliënt aan wie u verkoopt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: bholtorf
---
# Nieuwe klanten registreren

Klanten zijn uw bron van uw inkomsten. U moet elke klant aan wie u verkoopt registreren als een klantenkaart. Klantenkaarten bevatten de informatie die is vereist om producten aan de klant te verkopen. Zie voor meer informatie [Verkopen factureren](sales-how-invoice-sales.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

Voordat u nieuwe klanten kunt vastleggen, moet u verschillende verkoopcodes instellen waaruit u kunt kiezen bij het invullen van klantenkaarten. Zie voor meer informatie [Verkopen instellen](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## Nieuwe klanten toevoegen

U kunt nieuwe klanten handmatig toevoegen door de pagina **Klantenkaart** in te vullen of u kunt sjablonen gebruiken die vooraf gedefinieerde informatie bevatten. U kunt bijvoorbeeld een sjabloon maken voor verschillende typen klantprofielen. Het gebruik van sjablonen bespaart tijd bij het toevoegen van nieuwe klanten en helpt ervoor te zorgen dat de informatie elke keer correct is. 

Als u maakt:
* Als u meerdere sjablonen voor gebruik met meer dan één type klant maakt, kunt u de geschikte sjabloon kiezen die u wilt gebruiken wanneer u een klant toevoegt.
* Als u slechts één sjabloon maakt, wordt deze voor alle nieuwe klanten gebruikt. 

Nadat u een sjabloon heeft gemaakt, kunt u de actie **Sjabloon toepassen** gebruiken om deze toe te passen op een of meer geselecteerde klanten. Om een sjabloon te maken vult u de informatie in die opnieuw moet worden gebruikt op de pagina **Klantenkaart** en slaat u deze vervolgens op als sjabloon. Zie voor meer informatie [De klantenkaart als sjabloon opslaan](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Het kan handig zijn om de pagina **Klantensjabloon** te personaliseren wanneer u een sjabloon maakt. U kunt bijvoorbeeld het veld **Kredietlimiet** aan een sjabloon toevoegen. Zie de sectie [Uw werkruimte personaliseren](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode) voor meer informatie.

U kunt ook een klant maken op basis van een contact. Zie voor meer informatie de sectie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### Een nieuwe klantenkaart maken

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

De actie **Prijzen en kortingen** biedt opties voor het beheren van speciale prijzen of kortingen voor de klant wanneer een order aan bepaalde criteria voldoet. Voorbeelden van dergelijke criteria zijn wanneer ze een bepaald artikel kopen, een minimale hoeveelheid bestellen of vóór een bepaalde datum kopen, zoals wanneer een campagne eindigt. Zie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) voor meer informatie.

De klant is nu geregistreerd en de klantenkaart is klaar om voor verkoopdocumenten te worden gebruikt.  

### De klantenkaart als sjabloon opslaan

U kunt een klantenkaart als sjabloon gebruiken wanneer u nieuwe klantenkaarten maakt.

1. Kies op de pagina **Klantenkaart** de actie **Opslaan als sjabloon**. De pagina **Klantensjabloon** opent de weergave van de klantenkaart als sjabloon.
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de klant zijn ingesteld.
4. Bewerk of typ dimensiecodes die u wilt toepassen op nieuwe klantenkaarten die worden gemaakt met deze sjabloon.  
5. Wanneer u de nieuwe klantensjabloon hebt voltooid, kiest u **OK**.

De klantensjabloon wordt toegevoegd aan de lijst met klantensjabloon en u kunt deze gebruiken om nieuwe klantenkaarten te maken.

## Klantenkaarten verwijderen

Als u een transactie voor een klant hebt geboekt, kunt u de klantenkaart niet verwijderen omdat de grootboekposten mogelijk nodig zijn voor controle. Als u klantenkaarten met grootboekposten wilt verwijderen, neemt u contact op met uw Microsoft-partner om dat via code te doen.  

## Kredietlimieten beheren

Op basis van kredietlimieten, saldobedragen en betalingscondities kan [!INCLUDE [prod_short](includes/prod_short.md)] een kredietwaarschuwing of een waarschuwing voor openstaande saldo's genereren zodra u een verkooporder invoert. Bovendien kunt u met aanmaningscondities en rentefactuurcondities rente en/of extra kosten factureren.  

Het veld **Kredietlimiet** op een klantenkaart specificeert het maximale bedrag dat u de klant toestaat om het betalingssaldo mee te overschrijden voordat waarschuwingen worden afgegeven. Wanneer u vervolgens informatie invoert in dagboeken, offertes, bestellingen en facturen, test [!INCLUDE [prod_short](includes/prod_short.md)] de verkoopkop en individuele verkoopregels om te zien of de kredietlimiet is overschreden.

U kunt zelfs boeken als de kredietlimiet is overschreden. Als het veld leeg is, geldt er geen kredietlimiet voor de klant.  

U kunt ervoor kiezen om geen waarschuwingen te ontvangen die u vertellen dat de kredietlimiet van de klant is overschreden, en u kunt aangeven welke soorten waarschuwingen u wilt zien.

### Waarschuwingen voor kredietlimieten opgeven

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.

2. Kies op het sneltabblad **Algemeen** in het veld **Waarschuwingen** de relevante optie zoals beschreven in de volgende tabel:

    |Optie| Omschrijving|
    |------|------------|
    |**Beide**| Zowel het veld **Kredietlimiet** als het veld **Openstaand saldo** op de klantenkaart wordt ingeschakeld en er wordt een waarschuwing weergegeven als de klant de kredietlimiet overschrijdt of als de klant een openstaand saldo heeft.|
    |**Kredietlimiet**|De waarde in het veld **Kredietlimiet** op de klantenkaart wordt vergeleken met het klantsaldo en er wordt een waarschuwing weergegeven als het klantsaldo dit bedrag overschrijdt.|
    |**Openstaand saldo**|Het veld **Openstaand bedrag** op de klantenkaart wordt ingeschakeld en er wordt een waarschuwing weergegeven als de klant een openstaand saldo heeft.|
    |**Geen**|Er worden geen kredietwaarschuwingen weergegeven over de status van de klant.|

## Zie ook

[Betalingsmethoden definiëren](finance-payment-methods.md)  
[Dubbele records samenvoegen](sales-how-merge-duplicate-records.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Gedeeltelijke verzendingen inschakelen met verzendadvies](sales-how-send-partial-shipments.md)  
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Online kaarten gebruiken om locaties en routebeschrijvingen te vinden](across-online-maps.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
