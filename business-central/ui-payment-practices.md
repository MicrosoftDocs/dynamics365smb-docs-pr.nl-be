---
title: Rapport over betalingspraktijken
description: Ontdek hoe u eenvoudig het rapport Betalingspraktijken voor leveranciers en klanten kunt maken.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
--- 

# Rapport over betalingspraktijken  

Sommige landen/regio's vereisen dat bedrijven betalingstijden voor hun leveranciers rapporteren, zoals gedefinieerd door de lokale autoriteiten. Deze rapportage kan gebaseerd zijn op verschillende bronnen en kan leveranciers sorteren op basis van hun omvang of gedefinieerde betalingsvoorwaarden, waardoor leveranciers rapportage kunnen krijgen over het volgende, zoals vereist door de lokale autoriteiten:  

- De gemiddelde overeengekomen betalingsperiode.  
- De gemiddelde werkelijke betalingsconditie.   
- Het deel van facturen dat na het einde van de overeengekomen betalingstermijn wordt betaald. 

Gebruikers kunnen de periode selecteren waarvoor ze een berekening willen uitvoeren en details vinden op basis van een groepering die u kiest. Voor elk van deze groeperingen kunt u bronposten vinden. 

> [!NOTE]
> Deze rapportage is tot nu toe in sommige landen/regio's vereist, maar dit is een wereldwijde functie en kan overal worden gebruikt. Momenteel moeten Zweedse bedrijven met 250 of meer werknemers elk jaar aan het Zweedse bedrijvenregistratiebureau rapporteren welke betalingstermijnen zij hebben voor aankopen bij bedrijven die kleiner zijn dan zijzelf. Soortgelijke handelingen bestaan ​​in het Verenigd Koninkrijk, Australië en Nieuw-Zeeland.  

## Het rapport genereren 

Voer de volgende stappen uit om het rapport **Betalingspraktijken** uit te voeren:

1. Selecteer het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingspraktijken** in en selecteer vervolgens de gerelateerde koppeling. 
2. Selecteer **Nieuw**.
3. Vul op het sneltabblad **Algemeen** waarden in de volgende velden in:

   | Veld | Omschrijving |
   |---------|-----------------------------------|
   | Nr. | Geef het nummer van de post of record voor het rapport op. |
   | Samenvoegingstype | Geef op hoe gegevens worden geaggregeerd. Als u de optie **Periode** kiest, wordt het rapport gebaseerd op verschillende perioden, maar als u de optie **Bedrijfsgrootte** kiest, wordt het rapport gemaakt op basis van de bedrijfsgroottes die zijn geconfigureerd in het veld **Code bedrijfsgrootte** op de **Leverancier**skaart. |
   | Type koptekst | Specificeert de bron voor posten in de betalingspraktijk en u kunt Leveranciers, Klanten of beide kiezen. |
   | Begindatum | Hiermee geeft u de begindatum van de betalingsmethode. |
   | Einddatum | Hiermee geeft u de einddatum van de betalingsmethode op. |

> [!NOTE]
> Als u besluit de optie **Bedrijfsgrootte** te gebruiken, moet u eerst posten maken op de pagina **Bedrijfsgroottes** en voeg ze toe aan alle leveranciers die u via deze methode wilt volgen.

4. Wanneer u alle velden in de koptekst heeft ingevuld, moet u de actie **Genereren** uitvoeren om gegevens in de regels en statistieken te genereren voor het geselecteerde type rapportage.
5. Op basis van het **Aggregatietype** krijgt u verschillende regels. U kunt sommige waarden handmatig wijzigen, maar in dit geval wordt elke gewijzigde regel en het hele rapport gemarkeerd als **Handmatig gewijzigd**.
6. Vanuit alle berekende velden kunt u dieper ingaan om te zien hoe dit resultaat is berekend. Hiervoor opent u de pagina **Lijst met gegevens over betalingsmethoden**.
7. Als u het document wilt afdrukken, kunt u dit doen door de actie **Afdrukken** uit te voeren.

## Zie ook

[Financiële rapporten](finance-reports.md)  
[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Debiteurenrapporten en -analyses](receivables-reports.md)  
[Crediteurenrapporten en -analyses](payables-reports.md)  
[Financiën instellen](finance-setup-finance.md)  
[Financiën](finance.md)  
[Overzicht van lokale functionaliteit](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
