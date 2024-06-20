---
title: QuickBooks-extensie gegevensmigratie
description: 'Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Desktop naar Business Central te importeren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.search.form: '1911, 1912, 1913, 1914, 1915, 1916, 1918, 1919'
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-quickbooks-data-migration-extension"></a>De QuickBooks-extensie gegevensmigratie

Met deze extensie kunt u gemakkelijk klanten, leveranciers, artikelen en accounts vanuit QuickBooks naar [!INCLUDE[prod_short](includes/prod_short.md)] migreren. Als uw bedrijf momenteel QuickBooks gebruikt, kunt u de relevante gegevens exporteren en vervolgens een begeleide instelling openen om de gegevens naar [!INCLUDE[prod_short](includes/prod_short.md)] te uploaden.  
Zie [Gegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md) voor meer informatie.

## <a name="data-from-quickbooks-desktop"></a>Gegevens vanuit QuickBooks Desktop

U kunt de volgende gegevens uit QuickBooks Online importeren naar Business Central:

- Klanten  
- Leveranc.  
- Artikelen  
- Rekeningschema  
- Beginsaldotransacties in het grootboek  
- In voorraad aantallen voor voorraadartikelen  
- Open documenten voor klanten en leveranciers, zoals facturen, creditnota's en betalingen  

Wij migreren alleen hele bedragen op verkoop- en inkoopdocumenten. We werken geen gedeeltelijk betaalde bedragen bij. Als een klant bijvoorbeeld 300 van een totaal van 500 euro op een verkoopfactuur heeft voldaan, migreren we de hele 500. Wanneer u gedeeltelijke betalingen hebt ontvangen, moet u deze handmatig bijwerken, voordat of nadat u gegevens migreert. Het is raadzaam openstaande transacties te vereffenen voordat u migreert, om zaken achteraf gemakkelijker te maken.

> [!NOTE]
> Wij migreren geen inkooporders of verkooporders.

## <a name="before-you-start"></a>Voordat u begint

Een belangrijk deel van het migratieproces is de rekeningen opgeven waarnaar transacties moeten worden gemigreerd. Het is aan te raden deze koppeling te plannen voordat u gegevens migreert. Bijvoorbeeld, de rekeningen waarnaar u transacties boekt voor:

- De verkoop van artikelen of services aan klanten  
- De aankoop van artikelen of services van leveranciers  
- Herwaarderingen in het grootboek  

Business Central vereist dat aan grootboekrekeningen rekeningnummers zijn toegewezen. Zorg ervoor dat rekeningnummers zijn toegewezen aan uw rekeningen in QuickBooks.
Als transacties in QuickBooks belastingbedragen hebben, moet u eerst een belastingrekening instellen voor uw belastingjurisdictie in Business Central, voordat u transacties kunt boeken.

Als u de gegevens uit de QuickBooks Desktop-toepassing wilt ophalen, moet u de Microsoft-tool Data Exporter downloaden.  De instructies voor de tool bevinden zich in de wizard Gegevensmigratie in [!INCLUDE[prod_short](includes/prod_short.md)]. Het hulpprogramma maakt verbinding met uw QuickBooks-toepassing en exporteert de toepasselijke gegevens naar een .zip-bestand.  

> [!NOTE]
> Momenteel werkt de tool Data Exporter alleen met QuickBooks 2017 en 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>De extensie QuickBooks-gegevensmigratie vinden

De extensie QuickBooks-gegevensmigratie is geïnstalleerd en kan worden gebruikt als geïntegreerd onderdeel van de begeleide instelling Gegevensmigratie. Als u klaar bent om nu aan de slag te gaan en uw gegevens uit QuickBooks hebt geëxporteerd, kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies vervolgens de gerelateerde koppeling. Kies **Bedrijfsgegevens migreren** en voer de stappen in de handleiding uit.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Wat doe ik nadat ik gegevens heb gemigreerd?

Nadat u gegevens migreert, hebben transacties de status Niet geboekt, zodat u deze kunt controleren en correcties kunt aanbrengen. Als u de transacties wilt controleren, gaat u naar de pagina waar u deze normaal zou vinden. Als u bijvoorbeeld ongeboekte verkoopfacturen wilt controleren, gaat u naar de pagina Verkoopfacturen. Als u betalingsdagboeken wilt controleren, gaat u naar de pagina Betalingsdagboeken.
Er is met name een aantal dingen die u moet doen: als de transacties in QuickBooks opslag of kortingen bevatten, moet u de bedragen handmatig optellen bij de gerelateerde transacties in Business Central voordat u deze boekt.
Als u btw gebruikt, hebt u mogelijk een bedrijfsboekingsgroep en een productboekingsgroep in de boekingsinstellingen nodig, zodat u btw-bedragen kunt boeken.
Controleer de beginsaldi voor de rekeningen in het grootboek. QuickBooks slaat het huidige saldo van alle rekeningen niet op, dus u moet mogelijk beginsaldi corrigeren.

## <a name="see-also"></a>Zie ook

[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
