---
title: Betalingsbestanden exporteren in de Belgische versie
description: 'Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken in de Belgische versie van Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 2000001
ms.date: 01/10/2022
ms.author: bholtorf
---
# Betalingsbestanden exporteren in de Belgische versie

Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand exporteren.  

Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta). Het bestand kan elektronisch naar een bank worden verzonden. U kunt slechts één bestand per boekingsdatum en valutacode maken. Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.  

In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.  

## Een betalingsbestand afdrukken  

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer *Betalingsdagboek* in en kies de koppeling om de pagina **EB-betalingsdagboek** te openen.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer in het veld **Exportprotocol** het exportprotocol.  

    Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd. U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen. Wanneer u de betalingsregels naar een bestand exporteert, kunt u slechts één exportindeling, of exportprotocol, gebruiken.  

    > [!NOTE]
    > Door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.
4. Voer de betalingsdagboekregelinformatie in.

    1. Kies de actie **Leveranciersbetalingen voorstellen**.
    2. Stel de desbetreffende filters en opties in op de pagina **Leveranciersbetalingen voorstellen**.

        Met deze batchtaak worden openstaande leveranciersposten verwerkt en wordt een betalingsvoorstel in de vorm van regels in een betalingsdagboek gemaakt. Openstaande leveranciersposten zijn het resultaat van het boeken van facturen en rentefacturen.

        In de batchtaak worden alleen posten opgenomen van leveranciers waarvoor het veld **Betalingen voorstellen** is geselecteerd op de kaart **Leverancier**. De voorstellen worden geregistreerd in een betalingsdagboek. U moet de uiterste betaaldatum opgeven die u tijdens de batchverwerking wordt gebruikt.

        Ook worden in de batchtaak worden alleen leveranciersposten opgenomen die niet zijn gemarkeerd als **Afwachten** op de pagina **Leveranciersposten**. U kunt de batchverwerking ook zo uitvoeren dat betalingen worden opgenomen waarvoor u een korting kunt verkrijgen.

        Wanneer u een beschikbaar bedrag invoert, worden de leveranciers geordend op **Prioriteit**.

        Met filters kunt u precies bepalen welke gegevens in de lijst moeten worden opgenomen. Stel extra velden in op het tabblad door het veld te kiezen. [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]
    3. Verwijder of wijzig zo nodig de regels.
    4. Als er geen bankrekening is aangegeven in de betalingsdagboeksjabloon, geeft op elke regel een bankrekening voor betalen aan.
5. Kies de actie **Betalingsregels controleren**.

    De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten. Als er fouten zijn, moet u deze oplossen voordat u kunt doorgaan.

6. Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.  

    Het rapport dat u in het betreffende exportprotocol hebt opgegeven, verwerkt de betalingregels en genereert het bestand.  

## Zie ook

[Elektronisch bankieren voor België](belgian-electronic-banking.md)  
[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[Leveranciersbetalingen voorstellen](../../payables-how-suggest-vendor-payments.md)  
[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)  
[Elektronische betalingen testen](how-to-test-electronic-payments.md)  
