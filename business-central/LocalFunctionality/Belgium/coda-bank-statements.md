---
title: 'Belgische CODA-bankafschriften [BE]'
description: 'CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, om elektronische bankafschriften automatisch te verwerken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '2000040, 2000041, 2000042, 2000043, 2000045'
ms.date: 02/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="belgian-coda-bank-statements-in-the-belgian-version"></a>Belgische CODA-bankafschriften in de Belgische versie

CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, waarmee elektronische bankafschriften automatisch kunnen worden verwerkt.  

Aan elke soort transactie in een CODA-afschrift wordt een unieke code toegewezen. [!INCLUDE[prod_short](../../includes/prod_short.md)] gebruikt deze code om transacties te interpreteren en deze te vereffenen met de betreffende posten.  

## <a name="applying-statement-lines"></a>Afschriftregels vereffenen

Wanneer u een CODA-afschrift hebt geïmporteerd, kunt u de afschriftregels vereffenen met bestaande posten, op basis van de gegevens in de tabel **Transactiecodering**.  

Als de transactiecodering van de afschriftregel niet wordt gevonden, stopt [!INCLUDE[prod_short](../../includes/prod_short.md)] met de verwerking en wordt doorgegaan naar de volgende afschriftregel. Als u het veld **Standaardboeking** selecteert, wordt de afschriftregel als standaardboeking gebruikt.  

Als de transactiecodering van de afschriftregel wordt gevonden, worden de afschriftregels vergeleken met de volgende rekeningsoorten en bijbehorende rekeningnummers:  

- Grootboek: als de rekeningsoort een grootboekrekening is, wordt de afschriftregel geboekt op de bijhorende grootboekrekening.  

- Klant of leverancier: als de rekeningsoort een klant- of leveranciersrekening is, wordt een overeenkomende klant- of leverancierspost gevonden op basis van de volgende criteria:  

  - Als een post met de standaardindeling wordt gevonden, wordt de post vergeleken met de afschriftregel en wordt de vereffeningsstatus ingesteld op **Vereffend**. Als de post niet de standaardindeling gebruikt, wordt het bankrekeningnummer van de klant of leverancier gebruikt om de klant of leverancier te vinden.  

  - Als er geen post met een corresponderend restbedrag wordt gevonden, wordt de klant- of leveranciersrekening gebruikt en wordt de vereffeningsstatus ingesteld op **Gedeeltelijk vereffend**.  

  - Als het bankrekeningnummer wordt gebruikt om de klant of leverancier te zoeken, wordt een bijbehorende post gevonden op basis van het bedrag van de afschriftregel. Als het bedrag wordt gevonden, wordt de afschriftregel vergeleken met de bijbehorende post en wordt de vereffeningsstatus ingesteld op **Vereffend**.  

  - Als het bankrekeningnummer niet kan worden gebruikt om de klant of leverancier te zoeken, wordt in [!INCLUDE[prod_short](../../includes/prod_short.md)] gestopt met de verwerking of wordt de huidige regel als standaardboeking gebruikt, voordat wordt doorgegaan met de volgende afschriftregel.  

U kunt het proces zo vaak uitvoeren als u wilt. Alleen afschriftregels met een lege vereffeningsstatus worden vereffend.  

Wanneer u alle afschriftregels hebt vereffend met een grootboekrekening of een bijbehorende klanten- of leverancierspost, kunt u de CODA-afschriftregels boeken. Zie voor meer informatie [CODA-afschriften automatisch overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md).  

## <a name="extending-the-coda-integration"></a>De CODA-integratie uitbreiden

De huidige ondersteuning voor CODA-bankafschriften kan in [!INCLUDE [prod_short](../../includes/prod_short.md)] online en on-premises worden gebruikt. Partners kunnen echter de functies niet uitbreiden in een app voor [!INCLUDE [prod_short](../../includes/prod_short.md)] online. De code is niet afgeschaft maar kan alleen worden uitgebreid of aangepast voor on-premises implementaties.  

## <a name="see-also"></a>Zie ook

[Elektronisch bankieren voor België](belgian-electronic-banking.md)   
[Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md)   
[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
[CODA-afschriften importeren](how-to-import-coda-statements.md)   
[CODA-afschriften vereffenen](how-to-apply-coda-statements.md)   
[Financiële dagboeken maken](how-to-create-financial-journals.md)   
[CODA-afschriften automatisch overbrengen en boeken](how-to-automatically-transfer-and-post-coda-statements.md)   
[CODA-afschriften handmatig overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
