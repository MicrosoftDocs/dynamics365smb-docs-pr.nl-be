---
title: E-documenten toewijzen aan inkooporderregels met Copilot
description: Meer informatie over hoe u Copilot kunt gebruiken om e-documenten aan inkooporderregels toe te wijzen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/10/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>E-documenten toewijzen aan inkooporderregels met Copilot (preview)

Naarmate inkoopprocessen digitaler worden, speelt de functie voor e-documenten in Business Central een sleutelrol bij het automatiseren van de ontvangst en verwerking van leveranciersfacturen. Copilot kan bij dit proces helpen door de toewijzing en afstemming van leveranciersfacturen met inkooporders te verbeteren. Deze hulp vermindert de tijd die wordt besteed aan taken die normaal gesproken uitgebreid zoeken, opzoeken en gegevensinvoer omvatten. Een ander voordeel is wanneer leveranciersfacturen niet precies verband houden met inkooporders. In dat geval is Copilot goed gepositioneerd om de bijbehorende inkooporders te identificeren. Verbeterde afstemmingsmogelijkheden komen vooral ten goede aan kleine en middelgrote organisaties die behoefte hebben aan efficiënte documenttracering voor inkooporderregels. Copilot is de door AI aangestuurde assistent voor werk waarmee creativiteit wordt gestimuleerd en productiviteit wordt verbeterd voor Business Central-gebruikers.

> [!IMPORTANT]
> - Dit is een preview-functie die gereed is voor productie voor productie- en sandbox-omgevingen in elke landlokalisatie<!-- with the exception of Canada -->.
> - Op productieklare previews zijn aanvullende gebruiksvoorwaarden van toepassing. Meer informatie: [Aanvullende gebruiksvoorwaarden voor Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274)
> - Door AI gegenereerde inhoud is mogelijk onjuist.

In de eerste release van de app voor **e-documenten** introduceerden we fundamentele scenario’s voor e-documenten voor het gehele verkoopproces. Er is echter behoefte aan uitbreidingen en automatisering bij het verwerken van de ontvangen documenten, vooral in de context van aankoopprocessen. Copilot verfijnt de manier waarop u e-documenten beheert in het aankoopproces, vooral met betrekking tot inkooporders. Met het raamwerk voor e-documenten kunt u opgeven welk type inkoopdocument u voor elke leverancier wilt maken wanneer u e-facturen van hen ontvangt. Voorheen was de enige optie het maken van een inkoopfactuur, als document of als grootboekdagboek.

U kunt nu een bestaande inkooporder in Business Central bijwerken met de informatie die u op de e-factuur hebt ontvangen.

## <a name="available-languages"></a>Beschikbare talen

[!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## <a name="activate-copilot"></a>Copilot activeren

Als u de Copilot **Hulp bij afstemming van e-document** niet hebt geactiveerd, moet u dit handmatig doen. Als u de copilot **Hulp bij afstemming van e-document** wilt inschakelen, volgt u deze stappen: 

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Copilot en AI-mogelijkheden** in en selecteer vervolgens de gerelateerde koppeling. 
2. Kies in de lijst met mogelijkheden **Hulp bij afstemming van e-document** en wijzig de status in **Actief**.  

U kunt Copilot gaan gebruiken zodra het is geactiveerd. 

## <a name="identify-purchase-orders"></a>Inkooporders identificeren

Ten eerste kunt u de inkooporders identificeren die u automatisch kunt afstemmen. Als uw **leverancier** het veld **E-document ontvangen om** heeft geconfigureerd om te werken met **Inkooporders**, doet [!INCLUDE[prod_short](includes/prod_short.md)] het volgende wanneer het elektronische document wordt gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] (handmatig of vanaf een extern eindpunt):

1. Als de **inkooporder** voor deze specifieke leverancier *bestaat en er een inkoopordernummer* in het ontvangen **E-document**-bestand staat, koppelt [!INCLUDE[prod_short](includes/prod_short.md)] dit **E-document** automatisch aan de opgegeven **Inkooporder**. De **documentstatus** van dit **E-document** is **Wordt uitgevoerd** en de **E-documentstatus** op de subpagina **Servicestatus** is **Order gekoppeld**.  
Deze koppeling is zichtbaar in het veld **Document** veld van dit specifieke **e-document**. Als u de automatisch gekoppelde **inkooporder** moet wijzigen, kunt u dit doen met behulp van de actie **Koppeling van inkooporder bijwerken** en kiest u handmatig een van de bestaande inkooporders voor deze leverancier. U kunt dit alleen doen voordat u de regels tussen **E-document** en **Inkooporder** afstemt.  
2. Als de **inkooporder** voor deze specifieke leverancier *bestaat, maar er geen inkoopordernummer* in het bestand van het ontvangen **e-document** staat, biedt [!INCLUDE[prod_short](includes/prod_short.md)] u, als u dit document handmatig hebt geüpload, de mogelijkheid een van de bestaande inkooporders te kiezen, waardoor de lijst **Inkooporders** wordt geopend met orders die u hebt gekregen van leveranciers en die alleen **E-document** bevatten. U moet daar dan de gewenste **Inkooporder** selecteren en **OK** selecteren. Als u niet de juiste **Inkooporder** selecteert of als u het **E-document** automatisch van een extern eindpunt hebt ontvangen met behulp van de **taakwachtrij**, wordt het nieuwe **E-document** niet gekoppeld aan enig inkoopdocument, wordt de **documentstatus** weergegeven als **Fout** en is de **E-documentstatus** op de subpagina **Servicestatus** **Verwerkingsfout met geïmporteerd document**. Als u de koppeling met de **Inkooporder** wilt voltooien, kiest u de actie **Koppeling van inkooporder bijwerken** en kiest u vervolgens een van de bestaande inkooporders voor deze leverancier.  

## <a name="map-lines"></a>Regels toewijzen

Copilot helpt u bij het automatisch afstemmen van e-factuurregels met inkooporderregels en biedt extra afstemmingsinformatie om de overeenkomsten te verbeteren.

Nadat inkooporders zijn afgestemd en toegewezen, werkt [!INCLUDE [prod_short](includes/prod_short.md)] de afgestemde inkooporder bij met de relevante ontvangstinformatie om ervoor te zorgen dat de juiste hoeveelheden op de orderregels worden ontvangen.

U kunt uw ontvangen elektronische documenten afstemmen met de regels van inkooporders van twee verschillende plaatsen, vanaf de pagina **E-documenten** of vanaf de pagina **Inkooporder**. De eenvoudigste manier om de reeds gekoppelde **Inkooporders** te vinden is het gebruik van de tegel **Gekoppelde inkooporders** als onderdeel van **E-documentactiviteiten**. Alle niet-gekoppelde documenten zijn te vinden via de tegel **Wachtende e-inkoopfacturen**, waar u een lijst hebt met **E-documenten** die u moet beoordelen.  

> [!NOTE]
> De **E-documentactiviteiten** met deze twee tegels vindt u in de volgende rolcentra: **Evaluatie van bedrijfsmanager**, **Bedrijfsmanager**, **Accountant**, **Voorraadbeheerder** en **Verzending en ontvangst**.

Als u een afstemming wilt uitvoeren vanaf de inkooporder, kiest u de actie **E-documentregels toewijzen**, die zowel op de inkooporder- als op de inkooporderlijstpagina's aanwezig is. Maar als u afstemming wilt uitvoeren vanaf de pagina **E-documenten**, kiest u de actie **Inkooporder afstemmen** vanaf deze pagina. Als u de afstemming wilt uitvoeren, volgt u deze stappen:

1. Kies de actie **E-documentregels toewijzen** of **Inkooporder afstemmen** voor reeds gekoppelde documenten.  
2. U kunt merken dat de prompt **Afstemmingsorderregels van e-document met Copilot** werkt en u hebt de pagina **Afstemming inkooporders** op de achtergrond. Dat betekent dat hetzelfde proces plaatsvindt, maar dan met de automatische ondersteuning van **Copilot**, die het afstemmingsproces uitvoert in plaats van u. 
3. Na een paar seconden stelt **Afstemmingsorderregels van e-document met Copilot** regels voor afstemming voor met meer details: 

    1. In de promptkop vindt u de volgende informatie:   

    |Veldnaam |Omschrijving |
    |--------|-----------------|
    |Automatisch afgestemd | Hiermee wordt het aantal automatisch voorgestelde overeenkomsten opgegeven. Dit nummer is gebaseerd op een tekenreeksvergelijking en als de beschrijvingen 80% of meer overlappen, stemt het systeem deze beschrijvingen automatisch af zonder Copilot-mogelijkheden te gebruiken. |
    |Copilot afgestemd | Specificeert het aantal door Copilot voorgestelde overeenkomsten met behulp van zowel tekenreeks- als semantische vergelijking. |
    |E-documentnr. | Hiermee wordt het gekoppelde e-documentnummer opgegeven. |
    |Totaalbedrag van factuur exclusief btw | Hiermee wordt het totale factuurbedrag exclusief btw opgegeven. |
    |Afgestemd totaalbedrag inclusief btw | Hiermee wordt het afgestemde bedrag exclusief btw opgegeven. |
    
    2. Als alle regels overeenkomen, ziet u de groene tekst in de rechterbovenhoek: **Alle regels (100%) zijn afgestemd. Controleer afstemmingsvoorstellen**.  
    3. Op de **Afgestemd voorstel**-regels vindt u de volgende informatie:  

    |Veldnaam |Omschrijving |
    |--------|-----------------|
    |E-documentregelnr. | Specificeert het regelnummer van het e-document (afkomstig uit het originele e-documentbestand). |
    |Omschrijving van e-documentregel | Specificeert de regelbeschrijving van het e-document (afkomstig uit het originele e-documentbestand). |
    |Afgestemde hoeveelheid | Hiermee wordt de hoeveelheid opgegeven die wordt vereffend met de inkooporderregel. |
    |Voorstel | Specificeert de door AI voorgestelde actie, en deze voorgestelde acties hebben betrekking op het afstemmen van de inkooporderregels. |

    4. Alle volledig voorgestelde en afgestemde lijnen zijn gemarkeerd met een groene kleur. Als er een probleem is, bijvoorbeeld een andere prijs maar binnen de toegestane prijsklasse, wordt deze regel gemarkeerd met een gele kleur. Als er enige gelijkenis is tussen de beschrijvingsvelden, maar het prijsverschil groter is dan toegestaan, wordt deze regel gemarkeerd met een rode kleur.
    5. Als u niet tevreden bent met sommige suggesties, kunt u deze verwijderen met behulp van de actie **Regel verwijderen**.  
    6. Als u voorstelafstemmingen wilt zien, kunt u de koppeling in de kolom **Voorstel** selecteren om de pagina **Afstemmingsdetails e-document** te openen. 
    7. Op de pagina **Afstemmingsdetails e-document** kunt u details van de **E-documenten** en de **Inkooporder** vergelijken om zeker te zijn van de voorgestelde afstemming voordat u deze bevestigt. 
    8. Sluit na het controleren de pagina.   

4. Als u niet tevreden bent met de meeste suggesties, of als u de functie **Afstemmingsorderregels van e-document met Copilot** niet wilt gebruiken, selecteert u **Verwijderen** en u kunt doorgaan met de [handmatige afstemming](finance-how-use-edocuments-purchase.md).  
5. Als u suggesties wilt bewaren, kiest u de knop **Behouden**. Het systeem slaat alle suggesties van de **Copilot** op.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] sluit de Copilot-prompt en regels op de pagina **Afstemming inkooporders** worden groen gemarkeerd, omdat ze al zijn afgestemd.  
7. Vanaf dit moment kunt u doorgaan met handmatige afstemming en dat betekent dat u afstemmingen en handmatige afstemmingen kunt verwijderen, het afstemmen opnieuw kunt instellen of, als u geen wijzigingen wilt aanbrengen, gewoon de actie **Toepassen op inkooporder** kunt kiezen en kunt doorwerken met de **Inkooporder**. 

> [!NOTE]
> U kunt ook de actie **Afstemmen met Copilot** op de pagina **Afstemming inkooporders** kiezen, maar in dit geval wordt u gevraagd of u de bestaande afstemmingen wilt overschrijven, omdat alle regels al zijn afgestemd.  

> [!NOTE]
> Prijs-/kostenanalyse en de controle van de beschikbare hoeveelheid maken deel uit van de voorverwerkingsactiviteit. 

## <a name="see-also"></a>Zie ook

[Overzicht van e-documenten](finance-edocuments-overview.md)    
[E-documenten gebruiken bij verkoop](finance-how-use-edocuments.md)    
[E-documenten gebruiken bij inkoop](finance-how-use-edocuments-purchase.md)   
[Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)    
[Veelgestelde vragen over verantwoordelijke AI voor hulp bij bankreconciliatie](faqs-bank-reconciliation.md)    
