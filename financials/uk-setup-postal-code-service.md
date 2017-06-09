---
title: De extensie GetAddress.io UK Postcodes instellen | Microsoft Docs
description: Beschrijft hoe u de postcodeservice installeert en configureert waarmee u adressen in het VK kunt importeren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>De extensie GetAddress.io UK Postcodes instellen
De extensie maakt het eenvoudig om adressen in het VK in te voeren voor entiteiten zoals klanten, contactpersonen, medewerkers, leveranciers, bankrekeningen e.d. 

De extensie GetAddress.io UK Postcodes gebruikt de getAddress-API om adressen te vinden in postcodes in het VK. Als u de extensie wilt gebruiken, moet u een abonnement en een API-sleutel voor de getAddress-API hebben. Dat is heel eenvoudig. Wij helpen u deze te krijgen wanneer u de extensie GetAddress.io UK Postcodes configureert. Het abonnement is gebaseerd op gebruik, of wat wordt aangeduid als ´calls´. Een call (of aanroep) is in dit geval wanneer [!INCLUDE[d365fin](includes/d365fin_md.md)] een lijst met adressen in een postcode weergeeft. U kiest het meest geschikte abonnement op basis van hoe vaak u adressen moet toevoegen. Als u op de pagina alleen **Get API Key** kiest, krijgt u een **Free** abonnement. Daarmee kunt u 20 adressen per dag toevoegen en het is geldig voor 30 dagen. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>De extensie GetAddress.io UK Postcodes instellen 
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Serviceverbindingen** in en klik op de gerelateerde koppeling.  
2. Kies in het venster **Serviceverbindingen** de waarde **UK Postcode Service**.
3. Kies op de pagina **Postcode provider configuration** de optie **Disabled** (uitgeschakeld).
4. Kies in het venster **Postal code service selection** de optie **GetAddress.io**.
5. Kies in het venster **GetAddress.io Config** de optie **Get API Key**. De pagina **Plans** op de website van getAddress API wordt geopend.  

    **Opmerking:** U moet mogelijk pop-ups in uw browser toestaan.
6. Schaf een abonnement aan of kies **Get API Key** en geef uw e-mailadres op.
7. Open de e-mail die u van getAddress.io krijgt en kopieer de API-code. De code vindt u onder de koptekst **Your API Key**.
8. Plak in het venster **GetAddress.io Config** de API-code in het veld **API key** en kies **OK**.
9. Controleer of op de pagina **Serviceverbindingen** in het veld **Address Provider** de waarde **GetAddress.io** wordt weergegeven. Als dit zo is, is de service ingeschakeld.

## <a name="see-also"></a>Zie ook
[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md) [[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
