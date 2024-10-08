---
title: Instelling van boekingsgroep
description: Leer hoe u boekingsgroepen gebruikt om tijd te besparen en fouten te voorkomen wanneer u transacties boekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 02/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-posting-groups"></a>Boekingsgroepen instellen

Boekingsgroepen wijzen entiteiten toe aan grootboekrekeningen. Voorbeelden van entiteiten zijn klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten. Boekingsgroepen besparen tijd en helpen fouten voorkomen bij het boeken van transacties. De transactiewaarden gaan naar de rekeningen die in de boekingsgroep zijn opgegeven voor die bepaalde entiteit. De enige voorwaarde is dat u een rekeningschema hebt. Zie [Het rekeningschema instellen](finance-setup-chart-accounts.md) voor meer informatie.  

Boekingsgroepen zijn verdeeld in drie categorieën:  

* Algemeen

  Definieer aan wie u verkoopt en van wie u koopt, en wat u verkoopt en wat u koopt. U kunt de boekingsgroepen ook combineren om zaken op te geven zoals de resultatenrekeningen waarnaar u wilt boeken, of groepen gebruiken om rapporten te filteren.  
* Specifiek

  Gebruik bijvoorbeeld verkoopdocumenten in plaats van rechtstreeks naar het grootboek te boeken. Wanneer u klantenposten maakt, worden bijbehorende posten in het grootboek gemaakt.  
* Btw

  Definieer de belastingpercentages en berekeningssoorten die moeten worden toegepast op degene aan wie u verkoopt en van wie u koopt, en op wat u verkoopt en wat u koopt.

In de volgende secties worden de boekingsgroepen van elke categorie beschreven.  

## <a name="general-posting-groups"></a>Algemene boekingsgroepen

De volgende tabel beschrijft de algemene boekingsgroepen.

| Soort | Omschrijving |
| --- | --- |
| Bedrijfsboekingsgroepen |Wijs deze groep aan klanten en leveranciers toe om op te geven aan wie u verkoopt en van wie u koopt. Stel deze boekingsgroepen in op de pagina **Algemene bedrijfsboekingsgroepen**. Als u dat doet, moet u bedenken hoeveel groepen u nodig hebt om verkopen en inkopen onder te verdelen. Groepeer bijvoorbeeld klanten en leveranciers per geografisch gebied of per bedrijfssoort. |
| Productboekingsgroepen |Wijs deze groep aan artikelen en resources toe om op te geven wat u verkoopt en wat u koopt. Stel deze boekingsgroepen in op de pagina **Algemene productboekingsgroepen**. Wanneer u dat doet, moet u bedenken hoeveel groepen u nodig hebt om verkoop onder te verdelen per product (artikelen en resources) en inkopen per artikel. Verdeel deze groepen bijvoorbeeld op basis van grondstoffen, detailhandel, resources, capaciteit, enzovoort. |
| Boekingsgroepinstellingen |Combineer bedrijfs- en productboekingsgroepen en kies de rekeningen waarnaar u wilt boeken. Voor elke combinatie van bedrijfs- en productboekingsgroepen kunt u een set grootboekrekeningen toewijzen. U kunt bijvoorbeeld de verkoop van hetzelfde artikel naar verschillende grootboekrekeningen boeken omdat klanten aan verschillende bedrijfsboekingsgroepen zijn toegewezen. Stel deze configuraties in op de pagina **Boekingsgroepinstellingen**. |

## <a name="specific-posting-groups"></a>Specifieke boekingsgroepen

In de volgende tabel worden de boekingsgroepen beschreven die specifiek zijn voor soorten gegevens.

|Soort | Omschrijving |
| --- | --- |
| Klantboekingsgroepen |Definieer de rekeningen die moeten worden gebruikt als u klanttransacties boekt. Als u voorraad gebruikt bij klanten, worden de rekeningen waarnaar de verkooporderregels worden geboekt bepaald door de algemene bedrijfsboekingsgroep die is toegewezen aan uw klant en de algemene productboekingsgroep die is toegewezen aan het voorraadartikel. Zie *Bedrijfsboekingsgroepen* en *Productboekingsgroepen* in de sectie [Algemene boekingsgroepen](#general-posting-groups). Stel deze boekingsgroepen in op de pagina **Klantboekingsgroepen**. |
| Leveranciersboekingsgroepen |Definieer waar transacties voor tegoeden, servicekostenrekeningen en contantkortingsrekeningen moeten worden geboekt. Dit is vergelijkbaar met klantboekingsgroepen. Stel deze boekingsgroepen in op de pagina **Leveranciersboekingsgroepen**. |
| Voorraadboekingsgroepen |Definieer voorraadboekingsgroepen die u vervolgens toewijst aan de relevante artikelrekeningen op de pagina **Voorraadboekingsgroepinstellingen**. Wanneer u dan posten voor een artikel boekt, word er geboekt naar de grootboekrekening die is ingesteld voor deze aan het artikel gekoppelde combinatie van artikelboekingsgroep en vestiging. Voorraadboekingsgroepen vormen tevens een ideale manier om uw voorraad te organiseren. Wanneer u rapporten genereert, kunt u artikelen dan scheiden op boekingsgroepen. Stel deze boekingsgroepen in op de pagina **Voorraadboekingsgroepen**. |
| Bankboekingsgroepen |Definieer de grootboekposten waarnaar bankrekeningsposten worden geboekt. Hiermee kunnen bijvoorbeeld de processen om transacties te traceren en bankrekeningen te reconciliëren worden vereenvoudigd. Stel deze boekingsgroepen in op de pagina **Bankboekingsgroepen**. We raden aan dat deze grootboekrekeningen het veld **Direct boeken** hebben ingesteld op *Nee*. |
| VA-boekingsgroep |Definieer rekeningen voor verschillende soorten onkosten en kosten, zoals aanschafkosten, gecumuleerde afschrijvingsbedragen, aanschafkosten bij BGS, gecumuleerde afschrijving bij BGS, winst bij BGS, verlies bij BGS, onderhoudskosten en afschrijvingskosten. Stel deze boekingsgroepen in op de pagina **VA-boekingsgroepen**. |

### <a name="allow-substitute-customer-or-vendor-posting-groups-on-documents"></a>Boekingsgroepen voor vervangende klanten of leveranciers op documenten toestaan

U kunt mensen andere boekingsgroepen voor klanten en leveranciers laten kiezen dan de standaardgroepen wanneer ze met verkoop- of inkoopdocumenten en journaals werken.

Als u wijzigingen in klantenboekingsgroep wilt toestaan, kiest u **Meerdere boekingsgroepen toestaan** op de pagina's **Verkoopinstellingen** en **Servicebeheerinstellingen**, terwijl u de pagina **Instellingen Inkoop en betalingen** kiest voor wijzigingen in leveranciersboekingsgroepen.

Op de pagina's **Klantenboekingsgroepen** of **Leveranciersboekingsgroepen** kunt u de boekingsgroepen specificeren die u als vervangers wilt toestaan door **Vervangingen** te kiezen. Vervangende boekingsgroepen kunnen de standaardboekingsgroepen voor klanten of leveranciers vervangen die zijn opgegeven voor een klant of leverancier.

Nadat u dit hebt ingesteld, kunt u kiezen uit de toegestane vervangende boekingsgroepen en de klant- of leveranciersboekingsgroep wijzigen bij het boeken van verkoop- of inkoopdocumenten en dagboeken. De boekingsgroepen voor vervangende klanten of leveranciers worden gekopieerd naar geboekte documenten en dagboeken, terwijl te betalen of te ontvangen grootboekposten worden geboekt naar de grootboekrekeningen die zijn opgegeven voor de vervangingen.

Bij het vereffenen van bijvoorbeeld een factuur en betaling die zijn geboekt met verschillende boekingsgroepen voor klanten of leveranciers (verschillende grootboekrekeningen), boekt [!INCLUDE[prod_short](includes/prod_short.md)] de bedragen tussen de grootboekrekeningen om ze in evenwicht te brengen.

## <a name="tax-posting-groups"></a>Btw-boekingsgroepen

De volgende tabel beschrijft de algemene btw-gerelateerde boekingsgroepen.

| Soort | Omschrijving |
| --- | --- |
| Btw-bedrijfsboekingsgroepen |Bepaal hoe u btw voor klanten en leveranciers kunt berekenen en boeken. Stel deze boekingsgroepen in op de pagina **Btw-bedrijfsboekingsgroepen**. Als u dit doet, moet u bedenken hoeveel groepen u nodig hebt. Dit kan bijvoorbeeld afhangen van factoren, zoals lokale wetgeving en of u zowel nationaal/regionaal als internationaal wilt handelen. |
| Btw-productboekingsgroepen |Geef de belastingberekeningen aan die nodig zijn voor de soorten artikelen of resources die u koopt of verkoopt. |
| Btw-boekingsinstellingen |Combineer btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Wanneer u een algemene dagboekregel, inkoopregel of verkoopregel invult, wordt gekeken naar de combinatie om te bepalen welke rekeningen moeten worden gebruikt. |

Zie [Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md) als in uw land/regio belasting over de toegevoegde waarde (btw) wordt gehanteerd.  

## <a name="example-of-linking-posting-groups"></a>Voorbeeld van het koppelen van boekingsgroepen

Hier volgt een scenario.  

Deze boekingsgroepen worden gekozen op de klantenkaart:  

* Algemene bedrijfsboekingsgroep
* Klantboekingsgroep  

Deze boekingsgroepen worden gekozen op de artikelkaart:  

* Algemene productboekingsgroep  
* Voorraadboekingsgroep  

Wanneer u een verkoopdocument maakt, wordt in de verkoopkoptekst de klantenkaartinformatie gebruikt en wordt op de verkoopregels de artikelkaartinformatie gebruikt.  

* De inkomstenboeking (resultatenrekening) wordt bepaald door de combinatie van de algemene bedrijfsboekingsgroep en de algemene productboekingsgroep.  
* De klantboeking (balans) wordt bepaald door de klantboekingsgroep.  
* De voorraadboeking (balans) wordt bepaald door de voorraadboekingsgroep.  
* De boeking van kosten van verkochte goederen (resultatenrekening) wordt bepaald door de combinatie van algemene bedrijfsboekingsgroep en algemene productboekingsgroep.  

Uw instelling bepaalt wanneer de boeking plaatsvindt. Wanneer de boeking plaatsvindt, hangt bijvoorbeeld af van het tijdstip waarop u periodiek activiteiten uitvoert, zoals het boeken van voorraadkosten of het aanpassen van kostenposten.

## <a name="copy-posting-setup-lines"></a>Boekingsinstellingsregels kopiëren

Hoe meer product- en bedrijfsboekingsgroepen u hebt, des te meer regels u op de pagina **Boekingsgroepinstellingen** ziet. Hoewel er veel verschillende combinaties van bedrijfs- en productboekingsgroepen kunnen zijn, wordt door verschillende combinaties mogelijk toch naar dezelfde grootboekrekeningen geboekt. Om de hoeveelheid handmatige invoer te beperken, kopieert u de grootboekrekeningen van een bestaande regel op de pagina **Boekingsgroepinstellingen**.

## <a name="set-up-posting-groups-on-the-go"></a>Boekingsgroepen onderweg instellen

Om gebruikers sneller aan de slag te krijgen, kunnen in [!INCLUDE[prod_short](includes/prod_short.md)] meldingen over ontbrekende grootboekrekeningen worden weergegeven in verschillende boekingsgroepinstellingen. Om deze meldingen te ontvangen, moet u ervoor zorgen dat de melding **Grootboekrekening ontbreekt in boekingsgroep of instelling** is geselecteerd op de pagina **Mijn berichten** die u kunt openen via het veld **Wijzigen wanneer ik berichten ontvang** op de pagina **Mijn instellingen**.  

Op deze manier krijgt u een bericht wanneer u aan een document werkt dat gebruikmaakt van een boekingsgroep of een instelling waarvoor een vereiste grootboekrekening ontbreekt. Kies de koppeling in het bericht om een pagina te openen waar u de relevante wijzigingen kunt aanbrengen, mits u hiervoor toestemming hebt.  

> [!NOTE]
> Om u rechtstreeks naar de boekingsgroep of instelling te brengen waarvoor een grootboekrekening ontbreekt, wordt in [!INCLUDE[prod_short](includes/prod_short.md)] een tijdelijke plaatsingsgroep of instelling gemaakt. Boekingsgroepen en -instellingen zijn een manier voor de accountant om te bepalen hoe boekingen naar het grootboek worden geboekt, dus het net op tijd maken van boekingsgroepen en -instellingen is mogelijk niet toegestaan in uw organisatie.  
>
> Schakel in dat geval het bericht *Grootboekrekening ontbreekt in boekingsgroep of instelling* uit en werk vervolgens samen met uw accountant om de relevante wijzigingen aan te brengen in de boekingsgroep, de instellingen of uw document. Dit is een belangrijke stap, want nadat documenten zijn geboekt, kunt u onjuist gebruikte boekingsgroepen of instellingen niet meer verwijderen omdat er grootboekposten voor worden gemaakt.

Gebruik het veld **Geblokkeerd** op de pagina **Boekingsgroepinstellingen** om te voorkomen dat gebruikers per ongeluk een instelling gebruiken die niet langer relevant is voor nieuwe boekingen. 

## <a name="access-all-fields-and-accounts-when-you-set-up-a-posting-group"></a>Krijg toegang tot alle velden en rekeningen wanneer u een boekingsgroep instelt

Het kan ingewikkeld zijn om boekingsgroepen in te stellen. Omdat sommige typen rekeningen niet vaak worden gebruikt, worden deze in [!INCLUDE [prod_short](includes/prod_short.md)] niet weergegeven als kolommen op de regels. Om het kiezen van de juiste rekeningen iets eenvoudiger te maken, filtert [!INCLUDE [prod_short](includes/prod_short.md)] de rekeningen die u kunt kiezen bij het opzoeken van velden. 

Als u toegang wilt krijgen tot alle rekeningen op de regels en in de veldzoekopdrachten, is er een aantal instellingen dat u kan helpen:

* Als u alle rekeningen als kolommen op de regels wilt weergeven, zet u de schakelaar **Alle rekeningen weergeven** aan.
* Als u op afzonderlijke regels toegang wilt krijgen tot alle rekeningen in de veldzoekopdrachten, kiest u het selectievakje **Alle rekeningen van opzoekactie weergeven**.

> [!NOTE]
> Het lijkt erop dat de schakelaar **Alle rekeningen weergeven** niet werkt op de pagina **Boekingsgroepinstellingen** . Dat komt doordat [!INCLUDE [prod_short](includes/prod_short.md)] alle rekeningen altijd als kolommen op de regels op die pagina weergeeft.

## <a name="troubleshooting-posting-group-errors"></a>Problemen met boekingsgroepfouten

Boekingsgroepen zijn een van de meer geavanceerde concepten om in te stellen in [!INCLUDE[prod_short](includes/prod_short.md)]. Als ze niet correct zijn ingesteld, kunnen er fouten optreden bij het boeken van documenten of journaalregels. Deze fouten worden bijvoorbeeld meestal veroorzaakt door een fout in de manier waarop grootboekrekeningen worden toegewezen of hoe boekingsgroepen worden gecombineerd.

Wanneer er iets mis is, geeft [!INCLUDE[prod_short](includes/prod_short.md)] de pagina **Foutmeldingen** weer. De pagina **Foutmeldingen** kan het gemakkelijker maken om het probleem te identificeren en op te lossen. De pagina biedt een beschrijving van de fout die verwijst naar de boekingsgroepinstelling die aandacht behoeft. Het bericht kan bijvoorbeeld luiden "Vooruitbetalingsrekening heeft geen boekingsgroepinstellingen." Er is ook een link om de pagina te openen die de oorzaak van het probleem is, zodat u het snel kunt oplossen.  

> [!NOTE]
> De hierboven beschreven foutafhandeling is niet beschikbaar voor artikel-, resource-, werknemers- en vaste-activajournalen, of voor grootboekrekeningen die zijn toegevoegd in lokale versies van boekingsgroepen.

## <a name="see-also"></a>Zie ook

[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
