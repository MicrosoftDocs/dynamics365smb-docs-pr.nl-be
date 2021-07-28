---
title: Nieuwe klanten registreren door een klantenkaart te maken
description: Beschrijft hoe u een klantenkaart maakt om informatie te registreren over elke nieuwe klant of cliënt aan wie u verkoopt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bb323a5cceb4988035d442d6bc8347125f927bf4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436763"
---
# <a name="register-new-customers"></a>Nieuwe klanten registreren

Klanten zijn de bron van uw inkomsten. U moet elke klant aan wie u verkoopt registreren als een klantenkaart. Klantenkaarten bevatten de informatie die is vereist om producten aan de klant te verkopen. Zie voor meer informatie [Verkopen factureren](sales-how-invoice-sales.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

Voordat u nieuwe klanten kunt vastleggen, moet u verschillende verkoopcodes instellen waaruit u kunt selecteren bij het invullen van klantenkaarten. Zie [Verkopen instellen](sales-setup-sales.md) voor meer informatie.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Nieuwe klanten toevoegen

Als u een nieuwe klant wilt registreren, moet u een klantenkaart invullen. U kunt sjablonen maken voor verschillende klantprofielen of u kunt klanten zonder sjablonen toevoegen. U kunt ook een klant maken op basis van een contact. Zie voor meer informatie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Als er klantsjablonen voor verschillende klantsoorten bestaan, wordt een pagina weergegeven wanneer u een nieuwe klantenkaart maakt waar u een geschikte sjabloon kunt selecteren. Als er slechts één klantensjabloon bestaat, gebruiken nieuwe klantenkaarten altijd deze sjabloon.  

### <a name="to-create-a-new-customer-card"></a>Een nieuwe klantenkaart maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Klanten** de actie **Nieuw**.

    Als er slechts één klantensjabloon bestaat, wordt vervolgens een nieuwe klantenkaart geopend waarin sommige velden zijn ingevuld met informatie van de sjabloon.

    Als er meer dan één klantensjabloon bestaat, wordt er een pagina geopend waarin u een klantensjabloon kunt selecteren. In dat geval volgt u de volgende twee stappen.
3. Kies op de pagina **Selecteer een sjabloon voor een nieuwe klant** de sjabloon die u wilt gebruiken voor de nieuwe klantenkaart.
4. Kies de knop **Ok**. Een nieuwe klantenkaart wordt geopend waarin in sommige velden informatie uit de sjabloon is ingevuld.  
5. Ga indien nodig door met het invullen of wijzigen van velden op de klantenkaart. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Op het sneltabblad **Verkoopprijzen** kunt u speciale prijzen of kortingen weergeven die u voor de klant verleent als aan bepaalde criteria, zoals artikel, minimaal orderaantal of einddatum, wordt voldaan. Elke rij vertegenwoordigt een speciale prijs of regelkorting. Elke kolom vertegenwoordigt een criterium dat moet worden toegepast om de speciale prijs te garanderen die u invoert in het veld **Eenheidsprijs** of de regelkorting die u invoert in het veld **Regelkorting %**. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).

De klant is nu geregistreerd en de klantenkaart is klaar om voor verkoopdocumenten te worden gebruikt.

Als u deze klantenkaart als sjabloon wilt gebruiken wanneer u nieuwe klantenkaarten maakt, kunt u deze opslaan als een sjabloon. Zie de volgende onderwerpen voor meer informatie.  

### <a name="to-save-the-customer-card-as-a-template"></a>De klantenkaart als sjabloon opslaan

1. Kies op de pagina **Klantenkaart** de actie **Opslaan als sjabloon**. De pagina **Klantensjabloon** opent de weergave van de klantenkaart als sjabloon.
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de klant zijn ingesteld.
4. Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe klantenkaarten die worden gemaakt met de sjabloon.  
5. Wanneer u de nieuwe klantensjabloon hebt voltooid, kiest u de knop **OK**.

De klantensjabloon wordt toegevoegd aan de lijst met klantensjabloon, zodat u deze kunt gebruiken om nieuwe klantenkaarten te maken.

## <a name="deleting-customer-cards"></a>Klantenkaarten verwijderen

Als u een transactie voor een klant hebt geboekt, kunt u de kaart niet verwijderen omdat de grootboekposten mogelijk nodig zijn voor controle. Als u klantenkaarten met grootboekposten wilt verwijderen, neemt u contact op met uw Microsoft-partner om dat via code te doen.  

## <a name="managing-credit-limits"></a>Kredietlimieten beheren

Op basis van kredietlimieten, saldobedragen en betalingscondities kan [!INCLUDE [prod_short](includes/prod_short.md)] een kredietwaarschuwing of een waarschuwing voor openstaande saldo's genereren zodra u een verkooporder invoert.  Bovendien kunt u met aanmaningscondities en rentefactuurcondities rente en/of aanvullende kosten factureren.  

Het veld **Kredietlimiet** op een klantenkaart specificeert het maximale bedrag dat u de klant toestaat om het betalingssaldo te overschrijden voordat waarschuwingen worden afgegeven. Wanneer u vervolgens informatie invoert in dagboeken, offertes, bestellingen en facturen, test [!INCLUDE [prod_short](includes/prod_short.md)] de verkoopkop en individuele verkoopregels om te zien of de kredietlimiet is overschreden.

Ook als de kredietlimiet is overschreden, kunt u boeken. Als het veld leeg is, geldt er geen kredietlimiet voor de klant.  

U kunt ervoor kiezen om geen waarschuwingen te ontvangen die u vertellen dat de kredietlimiet van de klant is overschreden, en u kunt aangeven welke soorten waarschuwingen u wilt zien.

### <a name="to-specify-credit-limit-warnings"></a>Waarschuwingen voor kredietlimieten opgeven

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.

2. Kies op het sneltabblad **Algemeen** in het veld **Waarschuwingen** de relevante optie zoals beschreven in de volgende tabel:

    |Optie| Omschrijving|
    |------|------------|
    |**Beide**| Zowel het veld **Kredietlimiet** als het veld **Openstaand saldo** op de klantenkaart wordt ingeschakeld en er wordt een waarschuwing weergegeven als de klant de kredietlimiet heeft overschreden of als de klant een openstaand saldo heeft.|
    |**Kredietlimiet**|De waarde in het veld **Kredietlimiet** op de klantenkaart wordt vergeleken met het klantsaldo en er wordt een waarschuwing weergegeven als het klantsaldo dit bedrag overschrijdt.|
    |**Openstaand saldo**|Het veld **Openstaand bedrag** op de klantenkaart wordt ingeschakeld en er wordt een waarschuwing weergegeven als de klant een openstaand saldo heeft.|
    |**Geen**|Er worden geen waarschuwingen weergegeven over de status van de klant.|

## <a name="see-also"></a>Zie ook

[Betalingsmethoden definiëren](finance-payment-methods.md)  
[Dubbele records samenvoegen](sales-how-merge-duplicate-records.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
