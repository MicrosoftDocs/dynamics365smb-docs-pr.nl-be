---
title: Een bedrijf configureren met de wizard RapidStart | Microsoft Docs
description: U kunt snel een nieuw bedrijf configureren dat u hebt gemaakt met behulp van de RapidStart Services-configuratiewizard.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9fb74bcf0b124dddc14d9441cdbfb4fc9116d3e2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378435"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Een bedrijf configureren met de wizard RapidStart
U kunt snel een nieuw bedrijf configureren dat u hebt gemaakt met behulp van de RapidStart Services-configuratiewizard.

In de volgende procedure hebt u het configuratiepakket aan de klant geleverd, dat vervolgens op een computer wordt geïnstalleerd. De klant opent het nieuwe bedrijf dat geen klantgegevens bevat. U of de klant volgt vervolgens de stappen in de RapidStart Services-wizard, die worden beschreven in deze procedure, om basisgegevens over het bedrijf te verstrekken. De wizard importeert het configuratiepakket en past het pakket vervolgens toe op het bedrijf.  

## <a name="to-configure-a-new-company"></a>Een nieuw bedrijf configureren  
1. Kies in het rolcentrum RapidStart Services-implementatie de actie **RapidStart-wizard**.  
2. Vouw het sneltabblad **Stap 1** uit. Dit bevat algemene informatie over het nieuwe bedrijf. Geef de juiste gegevens over het nieuwe bedrijf op in de velden. Er is één veld dat u verplicht bent om in te vullen, namelijk **Naam**. De overige velden zijn optioneel.  
3. Vouw het sneltabblad **Stap 2** uit. Dit bevat algemene communicatie- en contactgegevens voor het nieuwe bedrijf. Geef de juiste gegevens over het nieuwe bedrijf op in de velden.
4. Vouw het sneltabblad **Stap 3** uit. Dit bevat bankrekening- en betalingsgegevens voor het nieuwe bedrijf. Geef de juiste gegevens over het nieuwe bedrijf op in de velden.  
5. Vouw het sneltabblad **Stap 4** uit. Kies de knop **AssistEdit** om het configuratiepakket te selecteren dat u wilt toepassen. De naam van het configuratiepakket wordt weergegeven. U kunt vervolgens de volgende acties uitvoeren in de genoemde volgorde:  

    1. Pas de configuratie aan door **Pakket toepassen** te kiezen. Hiermee wordt het configuratiepakket geïmporteerd en worden de databasegegevens in het pakket allemaal tegelijk toegepast.  

    2. De configuratie controleren nadat deze is toegepast. Met deze optie kunt u de configuratiegegevens en vragenlijsten bekijken die door de partner zijn verstrekt en bepaalde hoofdgegevens die vereist zijn voor uw bedrijf importeren. Kies de actie **Configuratiewerkblad**. Zie voor meer informatie [De configuratievragenlijst voltooien](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Vouw het sneltabblad **Stap 5** uit. Opgeven welk Rolcentrum u standaard wilt gebruiken voor het nieuwe bedrijf.  

    > [!IMPORTANT]  
    >  Wijzig uw Rolcentrum pas nadat u de configuratie van het bedrijf hebt voltooid. Als u met meer instellingsgegevens rekening moet houden en meer wijzigingen moet doorvoeren, moet u eerst het configuratiewerkblad gebruiken om door te gaan met uw werk. Ga vervolgens terug naar de wizard voor het bijwerken van uw Rolcentrum-profiel of kies de actie **Volledige installatie**.

7. Kies de knop **OK**.  
8. U kunt controleren of de configuratiegegevens zijn toegepast op het nieuwe bedrijf. Kies het ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsgegevens** in en kies en vervolgens de gerelateerde koppeling.

De pagina **Bedrijfsgegevens** bevat gegevens die u hebt opgegeven.   

U hebt nu het bedrijf geconfigureerd en gegevens hierop toegepast.  

## <a name="see-also"></a>Zie ook  
[Configuraties toepassen op nieuwe bedrijven](admin-apply-configuration-to-new-companies.md)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]