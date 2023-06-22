---
title: De extensie QuickBooks Online-gegevensmigratie
description: 'Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Online naar Business Central te migreren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, QuickBooks, import'
ms.search.form: '1830,'
ms.date: 06/24/2021
ms.author: bholtorf
---

# <a name="the-quickbooks-online-data-migration-extension" />De extensie QuickBooks Online-gegevensmigratie

Deze extensie wordt opgenomen in de begeleide instelling **Gegevensmigratie**, om u te helpen belangrijke bedrijfsgegevens te migreren van QuickBooks Online naar [!INCLUDE[prod_short](includes/prod_short.md)]. Dat is bijvoorbeeld handig als uw bedrijf groeit en u hebt besloten uw app voor bedrijfsmanagement te upgraden door [!INCLUDE[prod_short](includes/prod_short.md)] te gaan gebruiken.

## <a name="what-data-can-i-import-from-quickbooks-online" />Welke gegevens kan ik importeren uit QuickBooks Online?

U kunt de volgende gegevens uit QuickBooks Online importeren naar [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Klanten
* Leveranc.
* Artikelen
* Rekeningschema
* Beginsaldotransactie in het grootboek
* In voorraad aantallen voor voorraadartikelen
* Open documenten voor klanten en leveranciers, zoals facturen, creditnota's en betalingen

Wij migreren alleen hele bedragen op verkoop- en inkoopdocumenten. We werken geen gedeeltelijk betaalde bedragen bij. Als een klant bijvoorbeeld 300 van een totaal van 500 euro op een verkoopfactuur heeft voldaan, migreren we de hele 500. Wanneer u gedeeltelijke betalingen hebt ontvangen, moet u deze handmatig bijwerken, voordat of nadat u gegevens migreert. Het is raadzaam openstaande transacties te vereffenen voordat u migreert, om zaken achteraf gemakkelijker te maken.

> [!NOTE]  
> Wij migreren geen inkooporders of verkooporders.

## <a name="before-you-start" />Voordat u begint

Een belangrijk deel van het migratieproces is de rekeningen opgeven waarnaar transacties moeten worden gemigreerd. Het is aan te raden deze koppeling te plannen voordat u gegevens migreert. Bijvoorbeeld, de rekeningen waarnaar u transacties boekt voor:  

* De verkoop van artikelen of services aan klanten.
* De aankoop van artikelen of services van leveranciers.  
* Herwaarderingen in het grootboek.  

[!INCLUDE[prod_short](includes/prod_short.md)] vereist dat aan grootboekrekeningen rekeningnummers zijn toegewezen. Zorg ervoor dat rekeningnummers zijn toegewezen aan uw rekeningen in QuickBooks Online.

Als transacties in QuickBooks Online belastingbedragen hebben, moet u eerst een belastingrekening instellen voor uw belastingjurisdictie in [!INCLUDE[prod_short](includes/prod_short.md)], voordat u transacties kunt boeken.

## <a name="how-do-i-start-using-the-extension" />Hoe kan ik beginnen de extensie te gebruiken?

Aan de slag gaan is eenvoudig. Het enige wat u moet doen is de begeleide instelling **Gegevensmigratie** uitvoeren. U doet dat als volgt:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Begeleide instelling** in en kies vervolgens **Bedrijfsgegevens migreren**.
2. Volg de instructies in elke stap in de begeleide instelling.

## <a name="what-do-i-do-after-i-migrate-data" />Wat doe ik nadat ik gegevens heb gemigreerd?

Nadat u gegevens migreert, hebben transacties de status **Niet geboekt**, zodat u deze kunt controleren en correcties kunt aanbrengen. Als u de transacties wilt controleren, gaat u naar de pagina waar u deze normaal zou vinden. Als u bijvoorbeeld ongeboekte verkoopfacturen wilt controleren, gaat u naar de pagina **Verkoopfacturen**. Als u betalingsdagboeken wilt controleren, gaat u naar de pagina **Betalingsdagboeken**.  

Er zijn enkele dingen die u met name moet doen:

* Als de transacties in QuickBooks Online opslag- of kortingsbedragen bevatten, moet u de bedragen handmatig toevoegen aan de gerelateerde transacties in [!INCLUDE[prod_short](includes/prod_short.md)] voordat u deze boekt.
* Als u btw gebruikt, hebt u mogelijk een bedrijfsboekingsgroep en een productboekingsgroep in de boekingsinstellingen nodig, zodat u btw-bedragen kunt boeken.
* Controleer de beginsaldi voor de rekeningen in het grootboek. QuickBooks Online slaat het huidige saldo van alle rekeningen niet op, dus u moet mogelijk beginsaldi corrigeren.

## <a name="see-related-microsoft-trainingtrainingmodulesmigrate-data-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/modules/migrate-data-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
