---
title: Conversie van bankgegevens instellen| Microsoft Docs
description: U kunt bankrekeningen instellen om transacties bij te houden en bankfeeds, zoals Yodlee, te importeren of exporteren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 04c9a867e43a1228839eaf95b3b31e5ab3421fe6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304072"
---
# <a name="set-up-the-bank-data-conversion-service"></a>Conversieservice voor bankgegevens instellen
Een algemene provider van services om betalingsgegevens naar elke willekeurige gegevensindeling te converteren die uw bank vereist, is verbonden en gereed om te worden ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hiernaar wordt verwezen in [!INCLUDE[d365fin](includes/d365fin_md.md)] als conversieservice bankgegevens.

U kunt betalingsregels uit de pagina **Betalingsdagboek** exporteren naar een bestand of een gegevensstroom die u vervolgens uploadt naar uw bank voor automatische verwerking, zodat u geen afzonderlijke elektronische betalingen hoeft te doen. Zie voor meer informatie [Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md).

U kunt bankafschriftbestanden op de pagina **Betalingsreconciliatiedagboek** importeren door de conversieservice voor bankgegevens te gebruiken om een bestand te converteren dat u van de bank ontvangt, naar een gegevensstroom die [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importeren. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Als alternatief voor het importeren van bankafschriften met de conversieservice bankgegevens, kunt u de service Envestnet Yodlee Bank Feeds gebruiken. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).

Als u bankbestanden wilt importeren of exporteren, moet u uw eigen bankrekening en de bankrekeningen van uw leveranciers instellen. Zie voor meer informatie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> De conversieservice voor bankgegevens kan een limiet aan het aantal regels opleggen dat in een bestand mag worden geëxporteerd. Er wordt een foutbericht gestuurd als de limiet wordt overschreden. Het wordt aangeraden dat bankafschriftbestanden de 1000 regels niet overschrijden omdat de verwerkingstijd in de conversieservice van de bankgegevens anders beduidend kan toenemen.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Uw bedrijf aanmelden voor de conversieservice van bankgegevens
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling gegevensconv.service bank** in en kies vervolgens de gerelateerde koppeling.  
2. De pagina **Instelling gegevensconv.service bank** wordt geopend met drie vooraf ingevulde velden met relevante URL's van de provider van de conversieservice voor bankgegevens.

    > [!NOTE]  
    >   In de demonstratiedatabase CRONUS International Ltd. worden de velden Gebruikersnaam en Wachtwoord vooraf ingevuld met demoaanmeldgegevens, die u vervangt door de werkelijke gegevens van uw bedrijf wanneer u zich aanmeldt bij de conversieservice voor bankgegevens.
3. Kies in het veld **Inschrijvings-URL** de browserknop om de aanmeldingspagina van de serviceprovider te openen.  
4. Voer op de inschrijvingspagina van de serviceprovider van bankgegevens de gebruikersnaam en het wachtwoord in van het abonnement van uw bedrijf op de service en voltooi vervolgens het aanmeldingsproces volgens de instructies van de serviceprovider.

    Uw bedrijf is nu aangemeld voor de conversieservice van bankgegevens. Ga door met het invoeren van de gebruikersnaam en het wachtwoord, die u voor de service hebt opgegeven in de gerelateerde instellingsvelden in [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. Voer op de pagina **Instelling gegevensconv.service bank** in het veld **Naam** dezelfde waarde in die u in stap 4 als aanmeldnaam op de pagina van de serviceprovider hebt ingevoerd.
6. Voer in het veld **Wachtwoord** dezelfde waarde in die u in stap 4 in het veld **Wachtwoord** op de pagina van de serviceprovider hebt ingevoerd.

> [!NOTE]  
> Uw aanmeldgegevens worden automatisch versleuteld.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>De lijst met momenteel ondersteunde bankgegevensindelingen weergeven of bijwerken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling gegevensconv.service bank** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Instelling gegevensconv.service bank** de actie **Banknaam - Gegevensconversielijst** om de lijst met banknamen te openen die bankgegevensindelingen vertegenwoordigen die door de conversieservice worden ondersteund.
3. Kies op de pagina **Banknaam - Gegevensconversielijst** de actie **Banknaamlijst bijwerken**.

De lijst met bankgegevensindelingen die door de conversieservice voor bankgegevens worden ondersteund, wordt nu bijgewerkt. Dit is de lijst met banknamen, gefilterd op land/regio, die u kunt selecteren vanuit het veld **Banknaam - Gegevensconversie** op de pagina **Bankrekeningkaart**.

> [!NOTE]  
>   De bijwerking van ondersteunde bankgegevensindelingen treedt ook op wanneer u een waarde selecteert of invoert in het veld **Banknaam - Gegevensconversie** voor de bankrekening.

U bent nu aangemeld voor de conversieservice van bankgegevens. Ga verder om de inschrijvingsinformatie door te voeren voor elke bankrekening die de service zal gebruiken.

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen beheren](bank-manage-bank-accounts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
