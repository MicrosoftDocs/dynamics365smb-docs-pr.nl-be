---
title: XMLports maken op basis van XML-schema's | Microsoft Docs
description: Gebruik XML-schema's om het kader voor gegevensuitwisseling in te stellen.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 5b10eaff0d412ee26ead2137a353054c41d05113
ms.contentlocale: nl-be
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a>Procedure: XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden
Om het importeren/exporteren van gegevens in XML-bestanden via het kader voor gegevensuitwisseling in [!INCLUDE[d365fin](includes/d365fin_md.md)] mogelijk te maken, kunt u XML-schema's gebruiken om te bepalen welke gegevenselementen u wilt uitwisselen met [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hiervoor opent u het venster **XML-schemaviewer** en laadt u het XML-schemabestand, selecteert u de relevante gegevenselementen en initialiseert u vervolgens een definitie voor gegevensuitwisseling of een XMLport.  

 Wanneer u hebt gedefinieerd welke gegevenselementen worden opgenomen op basis van het XML-schema, kunt u de actie **XMLport genereren** gebruiken om het XMLport-object te maken.  

 U kunt ook de actie **Gegevensuitwisselingsdefinitie aanmaken** gebruiken om een definitie voor gegevensuitwisseling te initialiseren die is gebaseerd op de geselecteerde gegevenselementen, die u vervolgens voltooit in het kader voor gegevensuitwisseling. Hiermee wordt een record gemaakt in het venster **Uitwisselingsdefinitie van boeking** waar u verdergaat door te bepalen welke elementen in het bestand worden gekoppeld aan welke velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Procedure: Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

 Dit onderwerp bevat de volgende procedures:  

-   Een XML-schemabestand laden  

-   Knooppunten in een XML-schema selecteren of wissen  

-   De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema  

-   Een XMLport genereren voor het bestand dat is gebaseerd op een XML-schema  

-   Een XMLport in Object Designer importeren  

### <a name="to-load-an-xml-schema-file"></a>Een XML-schemabestand laden  

1.  Zorg dat het relevante XML-schemabestand beschikbaar is. De bestandextensie is .xsd.  

2.  Voer in het vak **Zoeken** **XML-schema's** in en kies de gerelateerde koppeling.  

3.  Kies op het tabblad **Start** in de groep **Nieuw** de optie **Nieuw**.  

4.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geef een code op ter identificatie van het XML-schema.|  
    |**Beschrijving**|Geef een omschrijving op van het XML-schema.|  

     Het veld **Doelnaamspace** bevat elke naamruimte in het XML-schemabestand dat is geladen voor de regel.  

5.  Kies op het tabblad **Start** in de groep **Verwerken** de optie **Schema laden** en selecteer vervolgens het XML-schemabestand.  

     Wanneer het bestand is geladen, worden de overige velden op de regel gevuld met informatie uit het bestand en wordt het selectievakje **Schema is geladen** ingeschakeld.  

    > [!NOTE]  
    >  De structuur van het geladen XML-schema is standaard samengevouwen. U kunt een knooppunt uitvouwen door de knop **+** op het knooppunt te kiezen. Kies **Alles uitvouwen** op het lint om alle knooppunten uit te vouwen.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Knooppunten in een XML-schema selecteren of wissen  

1.  In het vak **Zoeken** voert u **XML-schemaviewer** in en vervolgens kiest u de gerelateerde koppeling.  

2.  Vul de velden in voor de kop, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Schemacode XML**|Geef het XML-schemabestand op dat u hebt geladen in stap 5 in het gedeelte "Een XML-schemabestand laden".|  
    |**Nieuw XMLport-nummer**|Geef het nummer op van de XMLport die is gemaakt op basis van dit XML-schema wanneer u de actie **XMLPort genereren** kiest.|  

     De regels worden nu gevuld met knooppunten die alle onderdelen in het XML-schema vertegenwoordigen. Knooppunten voor elementen die verplicht zijn volgens het XML-schema, worden standaard geselecteerd.  

3.  Vouw op de eerste regel in de kolom **Knooppuntnaam** het knooppunt **Document** uit en vouw vervolgens geleidelijk onderliggende knooppunten uit die u wilt controleren.  

     U kunt ook met de rechtermuisknop op een knooppunt klikken en **Alles uitvouwen** kiezen.  

4.  Kies op het tabblad **Start** in de groep **Weergeven** een van de volgende acties om te wijzigen welke knooppunten worden weergegeven.  

    |**Actie**|Omschrijving|  
    |----------------|---------------------------------------|  
    |**Alles weergeven**|Alle knooppunten worden weergegeven.|  
    |**Niet-verplicht verbergen**|Alleen knooppunten die elementen vertegenwoordigen die vereist zijn volgens het XML-schema, worden weergegeven. Deze knooppunten worden doorgaans aangegeven met een **1** in het veld **MinOcurrs**.<br /><br /> Kies **Alles weergeven** om de weergave om te keren.|  
    |**Niet-geselecteerd verbergen**|Alleen knooppunten waarbij het selectievakje **Geselecteerd** is ingeschakeld, worden weergegeven.<br /><br /> Kies **Alles weergeven** om de weergave om te keren.|  

5.  Kies op het tabblad **Home** in de groep **Beheren** de optie **Bewerken**.  

6.  Geef met het selectievakje **Geselecteerd** voor elk knooppunt aan of u wilt dat het element wordt ondersteund in de definitie voor gegevensuitwisseling voor het gerelateerde SEPA-bankbestand.  

    > [!NOTE]  
    >  Wanneer u een verplicht onderliggend knooppunt selecteert, worden alle bovenliggende knooppunten ook geselecteerd.  

7.  Kies de actie **Alle verplichte elementen selecteren** om alle knooppunten opnieuw te selecteren die elementen voorstellen die verplicht zijn volgens het XML-schema.  

8.  Kies de actie **Alles deselecteren** om alle selecties te wissen.  

     Het veld **Keuze** geeft aan of het knooppunt twee of meer knooppunten op hetzelfde niveau heeft die functioneren als opties.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema  

1.  In het vak **Zoeken** voert u **XML-schema's** in en vervolgens kiest u de gerelateerde koppeling.  

2.  Selecteer het betreffende XML-schema en kies op het tabblad **Start** in de groep **Verwerken** de optie **XML-schema-viewer openen**.  

3.  Zorg dat de relevante knooppunten zijn geselecteerd. Zie voor meer informatie het gedeelte "Knooppunten selecteren of wissen in een XML-schema".  

4.  Kies in het venster **XML-schemaviewer** op het tabblad **Start** in de groep **Verwerken** de optie **Definities van gegevensuitwisseling genereren**.  

 In het venster **Uitwisselingsdefinitie van boeking** wordt een definitie voor gegevensuitwisseling gemaakt die u kunt invullen om op te geven welke elementen in het bestand moeten worden toegewezen aan welke velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Procedure: Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

> [!NOTE]  
>  U kunt ook de functie **Bestandstructuur ophalen** in het venster **Uitwisselingsdefinitie van boeking** gebruiken. Deze maakt gebruik van de functionaliteit van het venster **XML-schemaviewer** om het sneltabblad **Kolomdefinities** vooraf te vullen.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Een XMLport genereren dat is gebaseerd op een XML-schema  

1.  In het vak **Zoeken** voert u **XML-schema's** in en vervolgens kiest u de gerelateerde koppeling.  

2.  Selecteer het betreffende XML-schema en kies op het tabblad **Start** in de groep **Verwerken** de optie **XML-schemaviewer openen**.  

3.  Geef in het veld **Nieuw XMLport-nummer** het nummer op dat het nieuwe XMLport-object krijgt wanneer het wordt gegenereerd.  

4.  Zorg dat de relevante knooppunten zijn geselecteerd. Zie voor meer informatie het gedeelte "Knooppunten selecteren of wissen in een XML-schema".  

5.  Kies op het tabblad **Start** in de groep **Verwerken** de optie **XMLport genereren** en sla het object als een .txt-bestand op in een geschikte vestiging.  

6. Importeer de nieuwe XMLport in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-ontwikkelingsomgeving en compileer deze.

## <a name="see-also"></a>Zie ook  
[Procedure: Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)   
[Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md)   
[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[Over het kader voor gegevensuitwisseling](across-about-the-data-exchange-framework.md)

