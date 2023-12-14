---
title: E-documenten instellen
description: Leer hoe u de e-documentfunctionaliteit instelt.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# E-documenten instellen

> [!IMPORTANT]
> De kernmodule E-documenten is een raamwerk. Standaard is er geen veld **Service-integratie**. Als u de **Documentindeling**-optie standaard vindt, moet u er rekening mee houden dat deze als voorbeeld worden aangeboden en dat de lokalisatie een gedetailleerde indeling moet bieden. Deze details maken deel uit van lokalisatie-apps, omdat ze beide specifiek zijn voor lokale vereisten.

> [!NOTE]
> Vanaf versie 23.2 is een standaard PEPPOL-documentindeling toegevoegd als globale indeling in het veld **Documentindeling**. Houd er rekening mee dat u dit formaat waarschijnlijk niet in de huidige vorm kunt gebruiken. Het is een W1-indeling die wordt geleverd om te laten zien hoe u deze functie kunt gebruiken. We raden u aan het bestaande PEPPOL-formaat te testen voordat u dit formaat gaat gebruiken.

De eerste stap bij de configuratie van elektronische documenten (e-documenten) is het opzetten van de E-documentenservice, waarin u het volledige gedrag van uw systeem configureert met betrekking tot de communicatie met e-documenten.

## De e-documentservice instellen

Volg deze stappen om de E-documentservice in te stellen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-documentservices** in en selecteer vervolgens de gerelateerde koppeling
2. Selecteer **Nieuw** en configureer dan op de pagina **E-documentservice** op het tabblad **Algemeen** de velden zoals beschreven in de volgende tabel.

    | Veld | Omschrijving |
    |-------|-------------|
    | Code | Selecteer de instelcode voor elektronische export. |
    | Omschrijving | Voer een korte omschrijving in van de instelling van elektronische export. |
    | Documentindeling | <p>De exportindeling van de instelling van elektronische export.</p><p>Standaard zijn er twee opties in dit veld. U kunt **PEPPOL BIS 3** selecteren als een generiek, op code gebaseerde indeling of **Gegevensuitwisseling** wanneer u vooraf documenten met specifieke indelingen moet instellen op het sneltabblad **Definitie van gegevensuitwisseling**.</p> |
    | Service-integratie | Selecteer de integratiecode voor de instelling van elektronische export. In wave 1 is de enige optie **Geen integratie**. |
    | Batchverwerking gebruiken | Geef op of de service batchverwerking gebruikt voor export. |

3. Configureer op het sneltabblad **Geïmporteerde parameters** de velden zoals beschreven in de volgende tabel.

    | Veld | Omschrijving |
    |-------|-------------|
    | Ontvangend bedrijf valideren | Geef op of de gegevens van het ontvangende bedrijf tijdens de import moeten worden gevalideerd. |
    | Maateenheid oplossen | Geef op of de maateenheid tijdens de import moet worden opgelost. |
    | Artikelreferentie opzoeken | Geef op of een artikel tijdens de import op de artikelreferentie moet worden gezocht. |
    | GTIN van artikel opzoeken | Geef op of een artikel tijdens de import op Global Trade Item Number (GTIN) moet worden gezocht. |
    | Rekeningtoewijzing opzoeken | Geef op of een rekening in **Rekeningtoewijzing** tijdens de import moet worden doorzocht op de inkomende tekst. |
    | Regelkorting valideren | Geef op of een regelkorting moet worden gevalideerd tijdens de import. |
    | Factuurkorting toepassen | Geef op of een factuurkorting moet worden toegepast tijdens de import. |
    | Totalen controleren | Geef op of een factuurtotaal moet worden geverifieerd tijdens de import. |
    | Order bijwerken | Geef op of de corresponderende inkooporder moet worden bijgewerkt. |
    | Dagboekregels maken | Geef op of een dagboekregel moet worden gemaakt in plaats van een inkoopdocument. Selecteer deze optie als u dagboeken wilt gebruiken als bestemming voor uw facturen. |
    | Naam van fin. dagboeksjabloon | Geef de naam op van de dagboeksjabloon die wordt gebruikt voor het maken van dagboekregels. Dit veld is van toepassing wanneer u dagboeken wilt gebruiken als bestemming voor uw facturen. |
    | Naam van fin. dagboekbatch | Geef de naam op van de dagboekbatch die wordt gebruikt voor het maken van dagboekregels. Dit veld is van toepassing wanneer u dagboeken wilt gebruiken als bestemming voor uw facturen. |
    | Automatisch importeren | Geef op of documenten automatisch moeten worden geïmporteerd vanuit de service. |
    | Begintijd van batch | Geef de starttijd voor importtaken op. |
    | Minuten tussen uitvoeringen | Geef het aantal minuten op tussen importtaakuitvoeringen. |

4. Als u **Gegevensuitwisseling** hebt geselecteerd in het veld **Documentindeling** op het sneltabblad **Algemeen**, gebruikt u de **Definitie van gegevensuitwisseling** om de volgende velden in te stellen.

    | Veld | Omschrijving |
    |-------|-------------|
    | Documenttype | Geef het documenttype op dat gegevensuitwisseling gebruikt voor het importeren/exporteren van de gegevens. Voorbeelden hiervan zijn **Verkoopfactuur**, **Verkoopcreditnota** en **Aankoopfactuur**. |
    | Importcode van definitie van gegevensuitwisseling | Geef de code voor gegevensuitwisseling op die wordt gebruikt voor het importeren van de gegevens. Gebruik dit veld alleen om een document te ontvangen tijdens het aankoopproces. |
    | Exportcode van definitie van gegevensuitwisseling | Geef de code voor gegevensuitwisseling op die wordt gebruikt voor het exporteren van de gegevens. Gebruik dit veld alleen om documenten aan te leveren in het verkoopproces. |

> [!NOTE]
> Er zijn definities voor gegevensuitwisseling opgesteld voor het PEPPOL-formaat die gerelateerd zijn aan het standaard verkoop- en inkoopdocument. U kunt deze definities echter waarschijnlijk niet in de huidige vorm gebruiken. Het zij allemaal W1-indelingen die worden geleverd om te laten zien hoe u deze functie kunt gebruiken. We raden u aan het bestaande PEPPOL-formaat te testen voordat u dit formaat gaat gebruiken.

Als u de indeling **Definitie van gegevensuitwisseling** in uw lokalisatie hebt geconfigureerd, kunt u een regel toevoegen voor elk documenttype dat u nodig heeft. Voeg regels toe die overeenkomen met het standaardvoorbeeld van gegevensuitwisseling voor het W1 PEPPOL-formaat. Selecteer echter eerst de optie **Type document** voor elke regel die u nodig heeft. Selecteer voor elk gegevenstype de waarde **Definitiecode van gegevensuitwisseling importeren** of **Definitiecode van gegevensuitwisseling exporteren** die u wilt gebruiken.

Als u de indeling **Definitie van gegevensuitwisseling** niet gebruikt, kunt u formaten maken en configureren met behulp van de [interface](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Pas de informatie aan op de regels **Toewijzing exporteren** en **Toewijzing importeren** , waar u de tabellen en velden kunt vinden voor het configureren van transformatieregels. In dit geval moet u een nieuwe optie toevoegen in het veld **Documentindeling** die betrekking heeft op uw indeling.

## Een verzendprofiel voor documenten instellen

U kunt voor elk van uw klanten een voorkeursmethode voor het verzenden van verkoopdocumenten instellen. Op deze manier hoeft u niet telkens een verzendoptie te selecteren wanneer u de actie **Boeken en verzenden** selecteert. Op de pagina **Documentverzendprofielen** kunt u verschillende verzendprofielen instellen en daar vervolgens uit kiezen in het veld **Verzendprofiel van document** op een klantenkaart. U kunt het selectievakje **Standaard** selecteren om aan te geven dat een documentverzendprofiel het standaardprofiel is voor alle klanten, behalve voor klanten waarvoor het veld **Verzendprofiel van document** is ingesteld op een ander profiel.

Deze functionaliteit wordt gebruikt om automatisering van elektronische facturering in te stellen. Wanneer u **Boeken en verzenden** in een verkoopdocument kiest, wordt in het dialoogvenster **Boeken en verzenden bevestigen** het gebruikte verzendprofiel getoond. Dit is het voor de klant ingestelde profiel of het standaardprofiel voor alle klanten.

Volg deze stappen om een documentverzendprofiel in te stellen,

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendprofiel van document** in en selecteer de gerelateerde koppeling.
2. Selecteer op de pagina **Documentverzendprofielen** **Nieuw**.
3. Voer op het sneltabblad **Algemeen** de vereiste veldgegevens in.
4. Configureer op het sneltabblad **Verzendopties** de velden, zoals in de volgende tabel is beschreven.

    | Veld | Omschrijving |
    |-------|-------------|
    | Elektronisch document | Geef op of het document als e-document wordt verzonden dat de klant in het systeem kan importeren, wanneer u de knop **Boeken en verzenden** selecteert. Om deze optie te gebruiken moet u ook het veld **Indeling** of **Code van servicestroom voor elektronische documenten** instellen. U kunt het bestand ook naar schijf opslaan. |
    | Formaat | Geef de indeling op die moet worden gebruikt om een e-document te verzenden. Dit veld is vereist als u **Via documentuitwisseling** in het veld **Elektronisch document** selecteert. |
    | Code van servicestroom voor elektronische documenten | Geef de elektronische servicestroom op die wordt gebruikt voor het verzenden van documenten. Dit veld is vereist als u **Uitgebreide servicestroom voor e-document** in het veld **Elektronisch document** selecteert. |

    > [!NOTE]
    > Als u **Uitgebreide servicestroom voor e-document** in het veld **Elektronisch document** selecteert, moet de werkstroom al zijn geconfigureerd voor uw e-documenten.

## De werkstroom instellen

Volg deze stappen om de werkstroom in te stellen die wordt gebruikt in de e-documentfunctionaliteit.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstroomsjablonen** in en selecteer vervolgens de gerelateerde koppeling.
2. Als u **Werkstroomsjablonen van e-document** niet kunt vinden op de pagina **Werkstroomsjablonen**, selecteert u **Microsoft-sjablonen opnieuw instellen**. **Werkstroomsjablonen van e-document** zouden dan moeten verschijnen. De pagina sluiten.
3. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en selecteer vervolgens de gerelateerde koppeling.
4. Voer de actie **Nieuwe werkstroom uit sjabloon** uit om een sjabloon voor het e-documentproces te selecteren. De beschikbare sjablonen zijn **Verzenden naar één service** en **Verzenden naar meerdere services**.
5. Selecteer **OK** om het instellen van de werkstroom te voltooien.
6. Selecteer in het veld **Dan reactie** **E-document verzenden met instelling** om de werkstroomreacties te configureren.
7. Selecteer de e-documentservice die u als optie hebt gemaakt, selecteer **OK** en schakel vervolgens de werkstroom in.

> [!NOTE]
> U kunt uw eigen werkstroom voor e-documenten maken zonder vooraf gedefinieerde werkstroomsjablonen te gebruiken. Als u meer services heeft, kunt u verschillende werkstromen gebruiken.

Als u meer werkstromen wilt gebruiken, configureert u deze via de documentverzendprofielen voor verschillende klanten. Wanneer u de werkstroom instelt, geeft u het profiel voor het verzenden van documenten op in de kolom **Op voorwaarde** op het sneltabblad **Werkstroomstappen**, omdat u niet twee services kunt hebben die hetzelfde documentverzendprofiel gebruiken in werkstromen.

Wanneer u uw werkstroom configureert op de pagina **Werkstroom**, wijst u naar het veld **Op voorwaarde** op het sneltabblad **Werkstroomstappen**. Selecteer op de pagina **Gebeurtenisvoorwaarden** in het veld **Filter** het documentverzendprofiel dat u wilt gebruiken.

## Een bewaarbeleid instellen voor e-documenten

E-documenten kunnen onderwerp zijn van verschillende lokale wetgevingen die verband houden met de periode dat de e-documenten worden bewaard. Daarom hebben we een bewaarbeleid toegevoegd voor alle belangrijke informatie die verband houdt met e-documenten. Beheerders kunnen een bewaarbeleid definiëren dat specificeert hoe vaak Dynamics 365 Business Central verouderde records die verband houden met e-documenten, worden verwijderd. Zie voor meer informatie over bewaarbeleid [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Volg deze stappen om een bewaarbeleid voor e-documenten in te stellen.

1. Voer op de pagina **E-documentservices** de actie **Bewaarbeleid** uit.
2. Wanneer de actie is voltooid, selecteert u een van de volgende bewaarbeleidsregels om in te stellen:

    - Logbestand van e-document
    - Logbestand van e-documentintegratie
    - Logbestand van toewijzing van e-document
    - Opslag van e-documentgegevens

## Zie ook

[Hoe u e-documenten gebruikt in Business Central](finance-how-use-edocuments.md)  
[Hoe u e-documenten uitbreidt in Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Financieel beheer](finance.md)  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Aankopen registreren met inkoopfacturen en orders](purchasing-how-record-purchases.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
