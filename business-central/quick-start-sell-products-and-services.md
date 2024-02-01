---
title: Snelstartgids Verkoop (bevat video)
description: 'Leer hoe u de eerste kritieke velden over producten en klanten in Business Central invult, zodat u uw verkoopprocessen kunt starten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="sales-quick-start"></a>Snelstartgids Verkoop

Om producten en services te kunnen verkopen moet u eerst artikelen en klanten instellen. Zodra dat is gebeurd, kunt u beginnen met het registreren van verkooporders en het verzenden van facturen.

## <a name="set-up-items-to-sell"></a>Te verkopen artikelen instellen

Deze video laat zien hoe u een artikel instelt om te verkopen in [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Een nieuw artikel instellen

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Voor meer informatie en aanvullende dingen die u kunt doen wanneer u artikelen instelt, zie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Klanten instellen

Deze video laat zien hoe u een nieuwe klant maakt in [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Een nieuwe klant instellen

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Voor meer informatie en aanvullende dingen die u kunt doen wanneer u klanten instelt, zie [Nieuwe klanten registreren](sales-how-register-new-customers.md)

## <a name="create-a-sales-order"></a>Een verkooporder maken

Wanneer u iets aan een klant verkoopt, hebt u twee opties. De eerste en eenvoudigste is om gewoon een verkoopfactuur te maken. Als uw verkoopproces echter complexer is, bijvoorbeeld als u situaties heeft waarin u slechts delen van een orderhoeveelheid verzendt, gebruikt u een verkooporder.

### <a name="to-create-a-sales-order"></a>Een verkooporder maken

1. Kies het pictogram ![Lampje dat de functie Vertel me 10 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer **Nieuw** om een nieuwe post te maken.
3. Voer in het veld **Klant** de naam in van een bestaande klant.

    Overige velden op de pagina **Verkooporder** worden nu ingevuld met de standaardinformatie over de geselecteerde klant.  

4. Vul desgewenst de overige velden op de pagina **Verkooporder** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.

6. Kies in het veld **Nr.** het nummer in van een voorraadartikel of service.

7. Geef in het veld **Aantal** op hoeveel artikelen u wilt verkopen.

8. In het veld **Regelkorting %** voert u een percentage in als u de klant een korting op het product wilt verlenen.

9. Als u een opmerking over de orderregel wilt toevoegen die de klant op de afgedrukte verkooporder kan zien, schrijft u een opmerking in het veld **Omschrijving** op een lege regel.

10. Herhaal stap 5 t/m 9 voor elk artikel dat u aan de klant wilt verkopen.

11. Als u slechts een deel van het orderaantal wilt verzenden, voert u dat aantal in het veld **Te verzenden aantal** in. De waarde wordt gekopieerd naar **Te factureren aantal**.

12. Als u slechts een deel van het verzonden aantal wilt factureren, voert u dat aantal in het veld **Te factureren aantal** in. Het aantal moet lager zijn dan de waarde in het veld **Te verzenden aantal**.

13. Wanneer de verkooporderregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.

Voor meer informatie en aanvullende dingen die u kunt doen bij het maken van klantenverkooporders zie [Producten verkopen met een klantenverkooporder](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Een verkoopfactuur maken

Wanneer u een verkoopfactuur maakt en boekt, maakt u niet alleen het factuurdocument dat u naar de klant verzendt, maar maakt u ook de gerelateerde hoeveelheid- en waardeposten in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="to-create-and-post-a-sales-invoice"></a>Een verkoopfactuur maken en boeken

1. Kies het pictogram ![Lampje dat de functie Vertel me 20 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  

2. Selecteer **Nieuw** om een nieuwe post te maken.

3. Voer in het veld **Klant** de naam in van een bestaande klant.

4. Vul desgewenst de overige velden op de pagina **Verkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.

6. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

7. Voer in het veld **Aantal** in hoeveel eenheden van het product, de kosten of de transactie met de regel voor de klant worden geregistreerd.  

8. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

9. Herhaal stap 5 t/m 8 voor elk product of kosteneenheid waarvoor u de klant wilt factureren.  

10. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

11. Wanneer de verkoopfactuurregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.  

Voor meer informatie en aanvullende dingen die u kunt doen bij het maken van klantenverkoopfacturen zie [Verkopen factureren](sales-how-invoice-sales.md)

## <a name="see-also"></a>Zie ook

[Snelstartgidsen voor Business Central](quick-start-business-central.md)  
[Verkoopoverzicht](sales-manage-sales.md)  
[Producten verkopen met een klantverkooporder](sales-how-sell-products.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
