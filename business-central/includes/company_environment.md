---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
[!INCLUDE[prod_short](prod_short.md)]-gebruikers ondersteunen soms meer dan één afdeling of suborganisatie binnen een business unit. Een bedrijf kan bijvoorbeeld verkoopkantoren hebben in verschillende steden en meerdere landen/regio's, dus heeft het voor elk kantoor een afzonderlijke bedrijfseenheid gemaakt. De kantoren in hetzelfde land/regio zijn opgezet als aparte *bedrijven* in een gedeelde *omgeving*. Andere kantoren zijn gemaakt als bedrijven in afzonderlijke omgevingen omdat ze geografisch gevestigd zijn in andere landen/regio's.

- Wat is een bedrijf?

  Denk aan een *bedrijf* als een container die informatie over een rechtspersoon bevat. Met behulp van het bovenstaande voorbeeld heeft het bedrijf een verkoopkantoor in Seattle en een ander in New York, dus maakt het een bedrijf in [!INCLUDE[prod_short](prod_short.md)] voor elk kantoor, zodat het de bewerkingen voor elk kantoor afzonderlijk kan beheren.

- Wat is een omgeving?

  Bedrijven in [!INCLUDE[prod_short](prod_short.md)] online bestaan in wat wordt aangeduid als *omgevingen*. Er zijn twee soorten omgevingen, **productie** en **sandbox**. Kortom, productieomgevingen bevatten live bedrijfsgegevens en sandboxomgevingen worden gebruikt als een veilige plek om zaken als nieuwe bedrijfsprocessen of functies te testen. Zie [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (uitsluitend in het Engels) voor meer informatie. Als u toegang hebt tot een bedrijf, hebt u toegang tot de omgeving waarin het zich bevindt. Als u toegang hebt tot meer dan één bedrijf en die bedrijven zich in verschillende omgevingen bevinden, specificeert u wanneer u zich aanmeldt bij [!INCLUDE[prod_short](prod_short.md)] de omgeving waarin u wilt werken. Omgevingen zijn specifiek voor een bepaald land/regio, dus als uw organisatie in meerdere landen/regio's werkt, heeft u voor elk land/regio afzonderlijke omgevingen nodig. Zie [Environments and companies](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (uitsluitend in het Engels) voor meer informatie.
