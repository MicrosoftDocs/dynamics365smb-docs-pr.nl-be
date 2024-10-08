---
title: 'Hoe exportprotocollen instellen [BE]'
description: 'Voordat u elektronisch bankieren kunt gebruiken, moet u exportprotocollen instellen die de indeling definiëren van het bestand dat wordt gegenereerd wanneer de bank de export van de betalingsgeschiedenis verwerkt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 2000005
ms.date: 07/03/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-export-protocols-in-the-belgian-version"></a>Exportprotocollen instellen in de Belgische versie
Voordat u met elektronisch bankieren aan de slag kunt, moet u de exportprotocollen instellen. Exportprotocollen bepalen welke bestandsindeling wordt gegenereerd wanneer u de betaalrun exporteert die door de bank moet worden verwerkt. Elke regel bevat een exportprotocol dat door een code en een beschrijving wordt geïdentificeerd. U kunt zoveel exportprotocollen instellen als nodig is. U moet een exportprotocol voor binnenlandse betalingen, internationale betalingen en SEPA-betalingen binnen en buiten de eurozone instellen.  

 Met exportprotocollen kunt u de codeunit toewijzen waarmee de controle wordt gedefinieerd die moet worden uitgevoerd voordat de betalingsregels naar een bestand worden geëxporteerd. Daarnaast kunt u het rapport toewijzen waarmee de betalingsindeling wordt gedefinieerd. U kunt bijvoorbeeld een exportprotocol met de naam **DOM1** hebben. Dit exportprotocol bevat de codeunit voor de controle **Binnenlandse betalingen controleren** en het rapport **Binnenlandse betalingen indienen**. Elk exportprotocol omvat zowel een controlecodeunit als een bijbehorend rapport, zoals in de volgende tabel wordt weergegeven.  

|**Id controleobject**|**Id exportobject**|  
|-------------------------|--------------------------|  
|2000002 Binnenlandse betalingen controleren|Rapport 2000001 Binnenlandse betalingen indienen|  
|2000003 Internationale betalingen controleren|Rapport 2000002 Internationale betalingen indienen|  
|2000004 SEPA-betalingen controleren|Rapport 2000005 SEPA-betalingen indienen|  
|2000005 Controleer SEPA-betalingen die niet in euro's zijn|Rapport 2000006 Bestand Niet-euro SEPA-betalingen|  
|2000007 Controleer SEPA 001.001.09 Betalingen|Rapport 2000008 Bestand FCY SEPA 001.001.09 Betalingen|
|Als u deze optie niet wilt, stelt u deze in op nul. Anders selecteert u een andere optie.|XMLport 1000 (SEPA pain.001.001.03-betalingen)|  

 Als u exportprotocollen hebt ingesteld, kunt u deze gebruiken in uw betalingsdagboeken voor elektronisch bankieren.  

## <a name="to-set-up-an-export-protocol"></a>Een exportprotocol instellen

1.  Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Exportprotocollen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul op de pagina **Exportprotocollen** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geef een code op om het exportprotocol uniek mee aan te duiden.|  
    |**Beschrijving**|Geef een omschrijving op voor de exportprotocolpost. U kunt maximaal 50 tekens invoeren (cijfers en/of letters).|  
    |**Codeonkosten**|Geef de code op om het onkostentype voor de exportprotocolpost te omschrijven. Tot de onkostencodes behoren **leeg**, **DEL**, **BEG** en **ONS**. Voor internationale betalingen is **DEL** de standaard.|  
    |**Id controleobject**|Geef het identificatienummer op van de codeunit die u wilt gebruiken om een controle op het object uit te voeren voordat het betalingsbestand wordt geëxporteerd.|  
    |**Naam controleobject**|Geef de naam op van een verificatieproces dat wordt gebruikt om een controle op het object uit te voeren voordat het betalingsbestand wordt geëxporteerd. Wanneer u **Id controleobject** selecteert, wordt in dit veld de **naam van het controleobject** weergegeven.|  
    |**Exportobjecttype**|Geef het objecttype op waarmee de exportindeling van de export van het betalingsbestand wordt bepaald. Wanneer u **Id exportobject** selecteert, wordt in dit veld het **type van het exportobject** weergegeven.<br /><br /> **OPMERKING:** Om het exportprotocol voor SEPA pain.001.001.03 in te stellen, selecteert u **XMLPort**.|  
    |**Id exportobject**|Geef het identificatienummer op waarmee de exportindeling van de export van het betalingsbestand wordt bepaald. Als u **2000002** selecteert, is de exportindeling voor het betalingsbestand bijvoorbeeld **Internationale betalingen archiveren**.<br /><br /> **OPMERKING:** als u het exportprotocol wilt instellen voor SEPA pain.001.001.03, selecteert u XMLport **1000**.|  
    |**Exportnr. series**|Hiermee geeft u de nummerreekscode op die wordt gebruikt om id-nummers toe te wijzen aan de export van het betalingsbestand.|  
    |**Gegroepeerde betaling**|Hiermee wordt aangegeven of dit exportprotocol wordt gebruikt voor gegroepeerde betalingen.|  

4.  Kies de knop **Ok**.  

## <a name="see-also"></a>Zie ook
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)   
 [Elektronische betalingen testen](how-to-test-electronic-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
