---
title: Periodieke btw-rapporten afdrukken
description: Met de btw-rapportagefunctie kunt u btw-transactiedetails afdrukken. U moet de volgende btw-rapporten aan de Belgische belastingdienst versturen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8f42d02f1d1e394dbac0c71975cd16cc8f803de6
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="print-periodic-vat-reports"></a>Periodieke btw-rapporten afdrukken
Met de btw-rapportagefunctie kunt u btw-transactiedetails afdrukken. U moet de volgende btw-rapporten aan de Belgische belastingdienst versturen:  

- Aangifte per maand/kwartaal  
- Jaarlijkse btw-lijst (op papier/diskette)  
- Btw-VIES-lijst (op papier/diskette)  

## <a name="to-print-the-monthlyquarterly-declaration"></a>De aangifte per maand/kwartaal afdrukken  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Formulier/Intervat-aangifte** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de velden in het venster **Btw - Formulier** in.  

    |Veld|Description|  
    |------------------------------------|---------------------------------------|  
    |**Verkeerd ondernemingsnr.**|Hiermee wordt opgegeven of u het rapport wilt afdrukken dat de verkeerde ondernemingsnummers bevat.|  
    |**Jaarlijkse btw-lijst**|Hiermee wordt opgegeven of u het rapport **Jaarlijkse btw-lijst** wilt afdrukken.|  
    |**Jaar**|Voer het jaar in van de periode waarvoor u het rapport wilt afdrukken. U moet het jaar als 4-cijferige code invoeren. Als u bijvoorbeeld een aangifte voor 2013 wilt afdrukken, moet u '2013' invoeren (en niet '13').|  
    |**Minimumbedrag**|Voer het minimale jaarsaldo van de klant in dat u in het rapport wilt opnemen. Als het jaarlijkse saldo van de klant minder is dan het minimumbedrag, wordt de klant niet opgenomen in de aangifte.|  
    |**Klanten opnemen uit**|Selecteer deze optie om alle klanten uit EU-landen/regio's of een bepaald land of bepaalde regio in het rapport op te nemen.|  
    |**Land/regio**|Selecteer het land of regio die in het rapport moet worden opgenomen.|  

3.  Kies de knop **Afdrukken** om het rapport af te drukken of kies de knop **Voorbeeld** om het rapport op het scherm weer te geven. Kies de knop **Annuleren** om de gegevens op te slaan zonder het rapport af te drukken.  

## <a name="to-print-the-vat-annual-listing-on-disk"></a>De jaarlijkse btw-lijst op diskette afdrukken  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zeken naar pagina of rapport"), voer **Jaarlijkse lijst - Schijf** in en voer vervolgens de gerelateerde koppeling in.  
2.  Vul in het venster **Jaarlijkse btw-lijst - Schijf** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Jaar**|Voer het jaar van de btw-aangifte in. U moet het jaar als 4-cijferige code invoeren. Als u bijvoorbeeld een aangifte voor 2013 wilt afdrukken, moet u '2013' invoeren (en niet '13').|  
    |**Minimum**|Voer het minimale jaarsaldo van de klant in dat u in het rapport wilt opnemen.<br /><br /> Als het jaarlijkse saldo van de klant minder is dan het minimumbedrag, wordt de klant niet opgenomen in de aangifte.|  
    |**Testaangifte**|Hiermee wordt opgegeven of u een testaangifte wilt maken.<br /><br /> Als dit is ingeschakeld, wordt een kenmerktest naar het bestand geschreven dat de waarde 1 gebruikt, wat aangeeft dat dit een testbestand is. Als u het XML-bestand wilt testen voordat het wordt verzonden, kunt u het bestand naar de Intervat-site uploaden. Het bestand wordt dan gevalideerd zonder te worden opgeslagen op de server en u ontvangt een bericht als het bestand geldig is. Ook wordt het unieke volgnummer in het XML-bestand niet verhoogd wanneer een testaangifte wordt gemaakt, wat betekent dat u zoveel interne testaangiftes kunt maken als u wilt.|  
    |**Vertegenwoordiger toevoegen**|Hiermee wordt opgegeven of u de vertegenwoordiger van de btw-aangifte wilt opnemen.<br /><br /> Een vertegenwoordiger is een persoon of een bureau dat geautoriseerd is om een btw-aangifte voor uw bedrijf te maken.|  
    |**Id**|Voer de id in van de vertegenwoordiger die voor het maken van de btw-aangifte verantwoordelijk is.|  
    |**Bestandsnaam**|Voer het pad en de naam van het bestand in waarnaar u de aangifte wilt maken.|  

3.  Kies de knop **Afdrukken** om het rapport af te drukken of kies de knop **Voorbeeld** om het rapport op het scherm weer te geven. Kies de knop **Annuleren** om de gegevens op te slaan zonder het rapport af te drukken.  

## <a name="to-print-the-vat-vies-declaration-report-to-disk"></a>Btw-VIES-aangifterapport op schijf afdrukken  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Btw - Intracommunautaire opgave - Schijf** in en kies vervolgens de gerelateerde koppeling.  
2.  Voer de gewenste informatie in en kies de knop **OK** om de batchverwerking te starten, waarmee een XML-bestand wordt gemaakt. Zie voor meer informatie Btw-VIES-opgaveschijf.  
3.  Als u een correctie moet aanbrengen, kiest u het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Btw-VIES-correctie** in en klikt u vervolgens op de gerelateerde koppeling.  
4.  Kies de actie **Lijst bewerken** en voer vervolgens de informatie in die moet worden aangepast. Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [Belgische btw](belgian-vat.md)   
 [Niet-aftrekbare btw instellen](how-to-set-up-non-deductible-vat.md)

