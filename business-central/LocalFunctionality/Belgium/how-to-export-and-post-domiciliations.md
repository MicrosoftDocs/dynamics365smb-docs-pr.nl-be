---
title: Domiciliëringen exporteren en boeken
description: U kunt domiciliëringen naar uw bank verzenden door de gegevens naar een bestand te exporteren. Wanneer u naar een bestand exporteert, kunt u ervoor kiezen de regels automatisch naar het grootboek te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 935e7d2c7a244703e3aa75ac789bd3ec5ab661b6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914002"
---
# <a name="export-and-post-domiciliations"></a>Domiciliëringen exporteren en boeken
U kunt domiciliëringen naar uw bank verzenden door de gegevens naar een bestand te exporteren. Wanneer u naar een bestand exporteert, kunt u ervoor kiezen de regels automatisch naar het grootboek te boeken.  

Afhankelijk van de instelling van het veld **Exportindeling van incasso van SEPA** op de pagina **Bankrekeningkaart**, wordt met de actie **Bestandsdomiciliëringen** een van deze aanvraagpagina's geopend:  

- De pagina **Dagboekregels maken**, voor de indeling SEPA Incasso.  
- De pagina **Bestandsdomiciliëringen**, voor binnenlandse indelingen.  

## <a name="to-export-and-post-domiciliations-in-sepa-format"></a>Domiciliëringen exporteren en boeken in SEPA-indeling  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Bestandsdomiciliëringen**.  
3.  Vul op de pagina **Dagboekregels maken** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Selecteer de dagboeksjabloon waaruit de domiciliëringen worden geboekt.|  
    |**Dagboekbatch**|Selecteer de algemene dagboekbatch waaruit de dagboekregels worden overgebracht.|  
    |**Dagboekregels boeken**|Selecteer deze optie om naar het grootboek te boeken.|  

4.  Klik op **OK** om het bestand te exporteren.  
5.  Kies de locatie van waar u het bestand naar uw bank wilt uploaden en kies **Opslaan**.  
6.  Kies de knop **Ja** om de domiciliëringsdagboekregels automatisch te boeken.  

    Als u het selectievakje **Dagboekregels boeken** niet hebt ingeschakeld, moet u de domiciliëringen handmatig in het dagboek boeken.  

    > [!NOTE]  
    >  Nadat u domiciliëringen in het dagboek hebt geboekt, verwijdert u de geboekte domiciliëringen op de pagina **Domiciliëringsdagboek**. Hiervoor selecteert u alle regels met de status **Geboekt** en kiest u de knop **Verwijderen**.  

## <a name="to-export-and-post-domiciliations-in-isabel-format"></a>Domiciliëringen exporteren en boeken in Isabel-indeling  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Bestandsdomiciliëringen**.  
3.  Vul op de pagina **Bestandsdomiciliëringen** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Selecteer de dagboeksjabloon waaruit de domiciliëringen worden geboekt.|  
    |**Dagboekbatch**|Selecteer de algemene dagboekbatch waaruit de dagboekregels worden overgebracht.|  
    |**Dagboekregels boeken**|Selecteer deze optie om naar het grootboek te boeken.|  
    |**Spildatum**|Voer een spildatum in als u op de domiciliëringsregels een datum wilt hebben die afwijkt van de boekingsdatum. De ingevoerde datum overschrijft de boekingsdatum op de geselecteerde dagboekregels.|  
    |**Inschrijvingsnr.**|Voer het inschrijvingsnummer in dat zich op de schijf voor intracommunautaire aangiften bevindt. Dit nummer is opgenomen in het bestand en de begeleidende notitie.|  
    |**Bestandsnaam**|Geef de naam op van het exportbestand dat u maakt.|  

4.  Kies de knop **Afdrukken** om de domiciliëringen te exporteren en de begeleidende notitie af te drukken. Kies de knop **Voorbeeld** om deze op het scherm weer te geven. Als u het bestand nu niet wilt exporteren, kiest u de knop **Annuleren** om het venster te sluiten.  
5.  Kies de knop **OK** om het rapport naar de printer te verzenden.  
6.  Kies de knop **Ja** om de domiciliëringsdagboekregels automatisch te boeken.  

    Als u het selectievakje **Dagboekregels boeken** niet hebt ingeschakeld, moet u de domiciliëringen handmatig in het dagboek boeken.  

    > [!NOTE]  
    >  Nadat u domiciliëringen in het dagboek hebt geboekt, verwijdert u de geboekte domiciliëringen op de pagina **Domiciliëringsdagboek**. Hiervoor selecteert u alle regels met de status **Geboekt** en kiest u de knop **Verwijderen**.  

## <a name="see-also"></a>Zie ook  
 [Incasso via domiciliëring](direct-debit-using-domiciliation.md)   
 [Domiciliëringen instellen](how-to-set-up-domiciliations.md)   
 [Domiciliëringsvoorstellen genereren](how-to-generate-domiciliation-suggestions.md)   
 [Domiciliëringen testen](how-to-test-domiciliations.md)   
 [Domiciliëringsregels bewerken en verwijderen](how-to-edit-and-delete-domiciliation-lines.md)
