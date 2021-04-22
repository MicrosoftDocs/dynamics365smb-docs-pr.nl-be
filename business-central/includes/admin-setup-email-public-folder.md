---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2867dbccab19226c16f761bb974528bbdcf0a21f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777660"
---
Voordat u e-mailregistratie kunt instellen, moet u uw Exchange Online voorbereiden met [openbare mappen](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). U kunt dit doen in het [Exchange-beheercentrum](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) of u kunt de [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) gebruiken.  

> [!TIP]
> Als u de [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) wilt gebruiken, vindt u inspiratie voor het opzetten van uw script in een voorbeeldscript dat we hebben gepubliceerd [de BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

De volgende lijst beschrijft de belangrijkste stappen met koppelingen voor meer informatie.  

- Maak een beheerdersrol voor openbare mappen op basis van de informatie in de volgende tabel:

  |Eigenschap        |Waarde                     |
  |----------------|--------------------------|
  |Name            |Beheer van openbare mappen |
  |Geselecteerde rollen  |Openbare mappen            |
  |Geselecteerde leden|Het e-mailadres van het gebruikersaccount dat Business Central zal gebruiken om de e-mailregistratietaak uit te voeren|

  Zie [Rolgroepen beheren](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true) voor meer informatie.

- Maak een nieuwe openbare mappostbus op basis van de informatie in de volgende tabel:

  |Eigenschap        |Waarde                     |
  |----------------|--------------------------|
  |Name            |Openbare postbus            |

  Zie voor meer informatie [Een openbare mappostbus maken in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Nieuwe openbare mappen maken

  - Maak een nieuwe openbare map met de naam *E-mailregistratie* in de root zodat het volledige pad naar de map ```\Email Logging\``` wordt
  - Maak twee submappen zodat het resultaat de volgende volledige paden naar de mappen is:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Raadpleeg [Een openbare map maken](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true) voor meer informatie.

- De openbare map *Wachtrij* inschakelen voor post

  Zie voor meer informatie [Een openbare map in- of uitschakelen voor post](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Het verzenden van e-mails naar de openbare map *Wachtrij* inschakelen met behulp van Outlook of de Exchange Management Shell

  Zie voor meer informatie [Anonieme gebruikers toestaan om e-mail te verzenden naar een voor e-mail geschikte openbare map](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Stel de gebruiker van e-mailregistratie in als eigenaar van beide openbare mappen, *Wachtrij* en *Opslag*, die Outlook of de Exchange Management Shell gebruiken op basis van de informatie in de volgende tabel:

  |Eigenschap        |Waarde                     |
  |----------------|--------------------------|
  |Gebruiker            |Het e-mailadres van het gebruikersaccount dat Business Central zal gebruiken om de e-mailregistratietaak uit te voeren|
  |Machtigingsniveau|Eigenaar                     |

  Zie voor meer informatie [Machtigingen voor openbare mappen toewijzen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Maak twee mapstroomregels op basis van de informatie in de volgende tabel

  |Doel  |Name |Voorwaarden                        |Actie                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Een regel voor inkomende e-mail |Naar deze organisatie verzonden e-mail registreren|*De afzender* bevindt zich *buiten de organisatie* en *de ontvanger* bevindt zich *binnen de organisatie*|BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*|
  |Een regel voor uitgaande e-mail | Uit deze organisatie verzonden e-mail registreren |*De afzender* bevindt zich *binnen de organisatie* en *de ontvanger* bevindt zich *buiten de organisatie*|BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*|
  
  Zie voor meer informatie [Poststroomregels beheren in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) en [Poststroomregelacties in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Als u wijzigingen aanbrengt in de Exchange Management Shell, worden de wijzigingen met vertraging zichtbaar in het Exchange-beheercentrum. De wijzigingen die in Exchange zijn aangebracht, zijn ook beschikbaar in [!INCLUDE[prod_short](prod_short.md)] na een vertraging. De vertraging kan enkele uren duren.
