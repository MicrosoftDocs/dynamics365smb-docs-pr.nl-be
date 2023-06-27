---
title: VA-afschrijving instellen
description: U hebt de beschikking over verschillende afschrijvingsmethoden. In Business Central definieert u de afschrijvingsmethode van een activum op de pagina **Vast activum**.
author: edupont04
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: edupont
---

# <a name="set-up-fixed-asset-depreciation"></a>Afschrijving van vaste activa instellen

U kunt diverse afschrijvingsmethoden gebruiken ter voorbereiding van financiële stukken en de aangifte van inkomstenbelasting. Veel grote ondernemingen gebruiken lineaire afschrijving voor hun jaarverslag omdat deze methode in het algemeen tot hogere netto-inkomsten leidt. Voor inkomstenbelastingdoeleinden gebruiken veel bedrijven echter een versnelde afschrijvingsmethode, zoals boekwaarde-afschrijving. U definieert de afschrijvingsmethode van een activum met het veld **Afschrijvingsmethode** op de pagina **Vast activum**. Zie voor meer informatie over wat de verschillende methoden doen [Afschrijvingsmethoden](fa-depreciation-methods.md).

U stelt afschrijvingsboeken in waarin u de verschillende manieren definieert waarop afschrijvingen moeten worden berekend voor verschillende typen vaste activa. In elk afschrijvingsboek kunt u afzonderlijke afschrijvingsvoorwaarden opgeven. U kunt bijvoorbeeld opgeven dat een vast activum binnen een periode van drie jaar moet worden afgeschreven in het ene boek, en binnen een periode van vijf jaar in een ander boek.

Wanneer u de betreffende afschrijvingsboeken hebt ingesteld, moet u aan elk vast activum een of meer afschrijvingsboeken toewijzen. Naar een afschrijvingsboek dat aan een vast activum wordt toegewezen, wordt als een afschrijvingsboek voor vaste activa verwezen. Het aantal afschrijvingsboeken dat u kunt instellen, is oneindig voor een vast activum.  

## <a name="to-create-a-depreciation-book"></a>Een afschrijvingsboek maken

In een afschrijvingsboek voor vaste activa geeft u op hoe vaste activa worden afgeschreven. Het is mogelijk om meerdere afschrijvingsboeken in te stellen om diverse afschrijvingsmethoden toe te passen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Lijst met afschrijvingsboeken** de actie **Nieuw**.
3. Vul op de pagina **Afschrijvingsboek** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > U kunt transacties voor vaste activa registreren op de pagina **VA fin. dagboek** of op de pagina **VA-dagboek**, afhankelijk van de vraag of de transacties zijn bedoeld voor financiële rapportage of intern beheer. Voer de volgende stap uit om te definiëren welk soort dagboek standaard wordt gebruikt voor de verschillende activiteiten voor vaste activa.
4. Schakel op het sneltabblad **Integratie** het selectievakje in voor elke activiteit voor vaste activa waarvan u transacties wilt boeken met de pagina **Financieel dagboek voor vaste activa**.
5. Herhaal stap 2 t/m 4 voor elke afschrijvingsmethode of boekingsmethode die u aan vaste activa als afschrijvingsboek wilt toewijzen.

> [!IMPORTANT]
> Kies het veld **Period. afschr. afronden** veld om de berekende periodieke afschrijving op hele getallen af te ronden. Als uw bedrijf bijvoorbeeld ook factuurafronding op hele getallen gebruikt op de pagina **Grootboekinstellingen**, kan afschrijvingsbedragen op hele getallen ook afronden transparantie verschaffen.

Als u bijvoorbeeld een vast activum uit gebruik neemt waarbij in het afschrijvingsboek geen afronding is gespecificeerd, maar het grootboek van uw bedrijf afronding vereist, ziet u bij het uit gebruik nemen van het vaste activum een foutmelding dat een bedrag moet worden afgerond in een post.  

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Een afschrijvingsboek aan een vast activum toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum waarvoor u een afschrijvingsboek voor vaste activa wilt instellen.
3. Vul op het sneltabblad **Afschrijvingsboek** indien nodig de velden in.
4. Als u meer dan één afschrijvingsboek aan het vaste activum moet toewijzen, kiest u de actie **Meer afschrijvingsboeken toevoegen**.
5. U kunt ook de actie **Afschrijvingsboeken** kiezen om een of meer afschrijvingsboeken voor vaste activa op te geven.

    > [!NOTE]  
    >   Als u de handmatige afschrijvingsmethode gebruikt, moet u de afschrijving handmatig invoeren in het financieel dagboek voor vaste activa. Uit de functie **Afschrijving berekenen** worden de vaste activa weggelaten die handmatig worden afgeschreven. U kunt deze methode gebruiken voor activa waarop niet wordt afgeschreven, zoals grond.

    > [!NOTE]  
    > Wanneer u de door de gebruiker gedefinieerde afschrijvingsmethode gebruikt, moet u het afschrijvingsboek op een andere manier toewijzen. Zie voor meer informatie [Door de gebruiker gedefinieerde afschrijvingsmethode instellen](fa-how-setup-user-defined-depreciation-method.md).

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Een afschrijvingsboek aan meerdere vaste activa toewijzen met een batchverwerking

Als u een afschrijvingsboek wilt toewijzen aan meerdere vaste activa, kunt u de batchverwerking **VA-afschr.-boeken maken** gebruiken om VA-afschrijvingsboeken te maken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum waaraan u een afschrijvingsboek wilt toewijzen en kies vervolgens de actie **Bewerken**.
3. Op de pagina **Afschrijvingsboek** kiest u de actie **VA-afschrijvingsboeken maken**.
4. Op de pagina **VA-afschrijvingsboeken maken** vult u het veld **Afschrijvingsboek** in.
5. Kies het veld **Kopiëren van VA-nr.** en selecteer het nummer van het vaste activum dat u als basis wilt gebruiken voor het maken van nieuwe VA-afschrijvingsboeken.

    Als u dit veld invult, bevatten de afschrijvingsvelden in de nieuwe afschrijvingsboeken voor vaste activa dezelfde gegevens als de overeenkomstige velden in het afschrijvingsboek voor vaste activa waaruit u kopieert. Laat het veld leeg als u nieuwe VA-afschrijvingsboeken met lege afschrijvingsvelden wilt maken.  
6. Op het sneltabblad **Vast activum** kunt u met behulp van een filter aangeven voor welke activa u de afschrijvingsboeken voor vaste activa wilt maken.
7. Kies de knop **Ok**.

## <a name="to-set-up-depreciation-posting-types"></a>Boekingssoorten voor afschrijving instellen

Voor elk afschrijvingsboek moet u instellen hoe [!INCLUDE[prod_short](includes/prod_short.md)] diverse boekingssoorten moet verwerken. Bijvoorbeeld, of de boeking debet of credit moet zijn, en of het boekingssoort moet worden opgenomen in de afschrijvingsbasis.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het afschrijvingsboek dat u wilt instellen en kies vervolgens de actie **VA-boekingssoortinstellingen**.
3. Vul indien nodig de velden op de pagina **Instellingen van VA-boekingstype** in.

    > [!NOTE]  
    >   Op de pagina **VA-boekingssoortinstellingen** kunt u geen regels wissen of invoegen. U kunt alleen de bestaande regels wijzigen.

Het wordt aangeraden om de instellingen van afschrijvingsboeken waarvoor al posten zijn geboekt niet te wijzigen. De wijzigingen gelden namelijk niet voor reeds geboekte posten, waardoor de statistische gegevens van het afschrijvingsboek onjuist worden.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Standaardsjablonen en batches instellen voor afschrijvingsboeken voor vaste activa

Voor elk afschrijvingsboek definieert u een standaardinstelling van sjablonen en batches. U gebruikt deze standaardwaarden om regels van het ene dagboek naar het andere dagboek te dupliceren, dagboekregels te maken met de batchverwerkingen **Afschrijving berekenen** of **Vaste activa indexeren** of aanschafkosten in het verzekeringsdagboek te dupliceren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Afschrijvingsboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het afschrijvingsboek waarvoor u standaarddagboeken posten wilt definiëren en kies vervolgens de actie **VA-dagboekinstellingen**.  
3. Als u voor elke gebruiker een standaardinstelling wilt gebruiken, kiest u het veld **Gebruikers-id** om een selectie te maken op de pagina **Gebruikers**.  
4. In de andere velden selecteert u de dagboeksjabloon of dagboekbatch die standaard moet worden gebruikt.  

## <a name="fiscal-year-365-days-field-depreciation"></a>Afschrijving met Veld Boekjaar (365 dagen)

Bij het berekenen van de afschrijvingen wordt in de batchverwerking Afschrijving berekenen gewoonlijk een standaardjaar van 360 gebruikt waarbij elk van de 12 maanden 30 dagen telt.

Als u dit veld selecteert, wordt in de batchverwerking Afschrijving berekenen het agendajaar van 365 dagen gebruikt, waarbij elke maand hetzelfde aantal dagen heeft als op de agenda. De enige uitzondering is februari in schrikkeljaren, die door de batchtaak worden beschouwd als 28 dagen en niet 29. Daarom worden alle jaren, ook schrikkeljaren, geacht 365 dagen te hebben.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/configure-depreciation-books/)

## <a name="see-also"></a>Zie ook

[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
