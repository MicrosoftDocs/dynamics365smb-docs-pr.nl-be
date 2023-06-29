---
title: XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden
description: Gebruik XML-schema's om het raamwerk voor gegevensuitwisseling in te stellen om te definiëren met welke gegevenselementen u wilt uitwisselen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden

Om het importeren/exporteren van gegevens in XML-bestanden via het kader voor gegevensuitwisseling in [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk te maken, kunt u XML-schema's gebruiken om te bepalen welke gegevenselementen u wilt uitwisselen met [!INCLUDE[prod_short](includes/prod_short.md)]. Hiertoe opent u de pagina **XML-schemaviewer** en laadt u het XML-schemabestand, selecteert u de relevante gegevenselementen en initialiseert u vervolgens een definitie van gegevensuitwisseling.  

 Wanneer u hebt gedefinieerd welke gegevenselementen moeten worden opgenomen op basis van het XML-schema, kunt u de actie **Definities van gegevensuitwisseling genereren** gebruiken om een definitie van gegevensuitwisseling te initialiseren die is gebaseerd op de geselecteerde gegevenselementen, die u vervolgens voltooit in het kader voor gegevensuitwisseling. Hiermee wordt een record gemaakt op de pagina **Uitwisselingsdefinitie van boeking** waar u verdergaat door te bepalen welke elementen in het bestand worden gekoppeld aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

 Dit onderwerp bevat de volgende procedures:  

- Een XML-schemabestand laden  

- Knooppunten in een XML-schema selecteren of wissen  

- De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema  

## <a name="to-load-an-xml-schema-file"></a><a name="to-load-an-xml-schema-file"></a>Een XML-schemabestand laden

1. Zorg dat het relevante XML-schemabestand beschikbaar is. De bestandextensie is .xsd.  

2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **XML-schema's** in en kies vervolgens de gerelateerde koppeling  

3. Kies de actie **Nieuw**.  

4. Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geef een code op ter identificatie van het XML-schema.|  
    |**Beschrijving**|Geef een omschrijving op van het XML-schema.|  

     Het veld **Doelnaamspace** bevat elke naamruimte in het XML-schemabestand dat is geladen voor de regel.  

5. Kies de actie **Schema laden** en selecteer het XML-schemabestand.  

     Wanneer het bestand is geladen, worden de overige velden op de regel gevuld met informatie uit het bestand en wordt het selectievakje **Schema is geladen** ingeschakeld.  

    > [!NOTE]  
    >  De structuur van het geladen XML-schema is standaard samengevouwen. U kunt een knooppunt uitvouwen door de knop **+** op het knooppunt te kiezen. Kies **Alles uitvouwen** op het lint om alle knooppunten uit te vouwen.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Knooppunten in een XML-schema selecteren of wissen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **XML-schemaviewer** in en kies vervolgens de gerelateerde koppeling  

2. Vul de velden in voor de kop, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Schemacode XML**|Geef het XML-schemabestand op dat u hebt geladen in stap 5 in het gedeelte 'Een XML-schemabestand laden'.|  
    |**Nieuw XMLport-nr.**|Geef het nummer op van de XMLport die wordt gemaakt op basis van dit XML-schema wanneer u de actie **XMLport genereren** kiest.|  

     De regels worden nu gevuld met knooppunten die alle onderdelen in het XML-schema vertegenwoordigen. Knooppunten voor elementen die verplicht zijn volgens het XML-schema, worden standaard geselecteerd.  

3. Vouw op de eerste regel in de kolom **Knooppuntnaam** het knooppunt **Document** uit en vouw vervolgens geleidelijk onderliggende knooppunten uit die u wilt controleren.  

     U kunt ook met de rechtermuisknop op een knooppunt klikken en **Alles uitvouwen** kiezen.  

4. Kies een van de volgende acties om te wijzigen welke knooppunten moeten worden weergegeven.  

    |**Actie**|Omschrijving|  
    |----------------|---------------------------------------|  
    |**Alles weergeven**|Alle knooppunten worden weergegeven.|  
    |**Niet-verplicht verbergen**|Alleen knooppunten die elementen vertegenwoordigen die vereist zijn volgens het XML-schema, worden weergegeven. Deze knooppunten worden doorgaans aangegeven met een **1** in het veld **MinOccurs**.<br /><br /> Kies **Alles weergeven** om de weergave om te keren.|  
    |**Niet-geselecteerd verbergen**|Alleen knooppunten waarbij het selectievakje **Geselecteerd** is ingeschakeld, worden weergegeven.<br /><br /> Kies **Alles weergeven** om de weergave om te keren.|  

5. Kies de actie **Bewerken**.  

6. Geef met het selectievakje **Geselecteerd** voor elk knooppunt aan of u wilt dat het element wordt ondersteund in de definitie voor gegevensuitwisseling voor het gerelateerde SEPA-bankbestand.  

    > [!NOTE]  
    >  Wanneer u een verplicht onderliggend knooppunt selecteert, worden alle bovenliggende knooppunten ook geselecteerd.  

7. Kies de actie **Alle verplichte elementen selecteren** om alle knooppunten opnieuw te selecteren die elementen voorstellen die verplicht zijn volgens het XML-schema.  

8. Kies de actie **Alles deselecteren** om alle selecties te wissen.  

     Het veld **Keuze** geeft aan of het knooppunt twee of meer knooppunten op hetzelfde niveau heeft die functioneren als opties.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XML-schema's** in en kies vervolgens de gerelateerde koppeling  

2. Selecteer het desbetreffende XML-schema en kies de actie **XML-schemaviewer openen**.  

3. Zorg dat de relevante knooppunten zijn geselecteerd. Zie het gedeelte 'Knooppunten selecteren of wissen in een XML-schema' voor meer informatie.  

4. Kies op de pagina **XML-schemaviewer** de actie **Definitie voor gegevensuitwisseling genereren**.  

 Op de pagina **Uitwisselingsdefinitie van boeking** wordt een definitie voor gegevensuitwisseling gemaakt die u kunt invullen om op te geven welke elementen in het bestand moeten worden toegewezen aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

> [!NOTE]  
> U kunt ook de functie **Bestandstructuur ophalen** op de pagina **Uitwisselingsdefinitie van boeking** gebruiken. Deze maakt gebruik van de functionaliteit van de pagina **XML-schemaviewer** om het sneltabblad **Kolomdefinities** vooraf te vullen.  

> [!NOTE]
> In releasewave 1 van 2019 en eerdere versies kon u een XMLport genereren die was gebaseerd op het schema en die vervolgens importeren in uw oplossing. Dit wordt niet langer ondersteund.

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)  
[Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Over het kader voor gegevensuitwisseling](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
