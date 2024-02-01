---
title: Klantenprijsgroepen instellen
description: Leer hoe u klantenprijsgroepen instelt en verkoopprijzen voor die groepen maakt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Klantenprijsgroepen instellen
  
U kunt de verkoopprijzen laten afhangen van de klantengroepen waarmee u zaken doet. Dit worden klantenprijsgroepen genoemd.

Voordat u klantenprijsgroepen instelt, moet u eerst bepalen hoeveel groepen u wilt maken en welke klanten aan elke groep worden toegewezen.  

## Verkoopprijzen voor een groep klanten maken  

Als u overeenstemming hebt bereikt over de prijs die de groep klanten betaalt voor bepaalde artikelen, kunt u de overeenkomst per artikel registreren op de regels van de pagina **Verkoopprijzen**.

### Verkoopprijzen voor een groep klanten maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantenprijsgroepen** in en kies vervolgens de gerelateerde koppeling.  

2. De regel voor de klantenprijsgroep selecteren. Als er nog geen regel bestaat, kunt u een nieuwe regel maken. Selecteer **Nieuw** om een nieuwe entiteit te maken en deze een naam te geven.  
    
    Controleer voor de geselecteerde regel de inhoud van de velden **Regelkorting toestaan**, **Factuurkorting toestaan**, **Prijs inclusief btw** en **Btw-bedr.-boekingsgr. (Prijs)**. 
  
3. Selecteer de actie **Navigeren** en kies **Verkoopprijzen**. De pagina **Verkoopprijzen** wordt geopend. Het veld **Verkoopsoort** wordt ingevuld met **Klantenprijsgroep**.  
  
4. Vul de **Verkoopcode** in met de verkoopcode die u op de vorige pagina hebt geselecteerd.  
  
5. Vul de velden op de regels in met het **Artikelnummer**, de **Code van maateenheid** en de overeengekomen **Eenheidsprijs**. U kunt ook de kolom **Variant** weergeven en opgeven welke **variant** geldig is als er sprake is van verschillende artikelvarianten.  
  
6. Als de klantengroep een minimumaantal moet inkopen om in aanmerking te komen voor de overeengekomen prijs, vult u het veld **Minimumaantal** in.  

7. Geef indien vereist de **begindatum** en **einddatum** van de prijsovereenkomst op.  
  
8. Geef indien relevant ook de **Valutacode** op.

Herhaal stap 4 tot en met 8 voor elk artikel waarvoor u een verkoopprijs wilt invoeren.

## Klantenprijsgroepcodes invoeren op klantenkaarten  

Nadat u de klantenprijsgroepen hebt ingesteld, kunt u klantenprijsgroepcodes invoeren op de klantenkaarten.

### Klantenprijsgroepcodes invoeren op een klantenkaart  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  

2. Open de **klantenkaart** voor een klant die u in een klantenprijsgroep wilt plaatsen.  

3. Selecteer op het sneltabblad **Facturering** in het veld **Klantenprijsgroep** de code van de **Klantenprijsgroep**.  


## Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Speciale verkoopprijzen en kortingen registreren](sales-how-record-sales-price-discount-payment-agreements.md)  
[Klantenkortingsgroepen instellen](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
