# Informeren aanvrager
![nl](https://img.shields.io/badge/lang-nl-g.svg)

![opvragen-informatie](opvragen-informatie.png)

## Inleiding
Het opvragen informatie bouwblok kan gebruikt worden om meer informatie bij een persoon (of bedrijf).
Het bouwblok biedt de mogelijkheid om:
- een portaaltaak open te zetten voor een persoon (of bedrijf) met de hulp van de portaaltaak plugin
- een doorloop tijd te berekenen en als nodig de afhandeltermijn aan the passen


## Installatie
We gaan uit van een bestaande Valtimo GZAC backend repository met daarin een bestaand proces.
Dit bouwblok is getest op Valtimo GZAC 10.7.0.RELEASE.

Kopiëer de bestanden van de `config` directory naar de config directory van Valtimo GZAC (`src/main/resources/config/`)
en behoud dezelfde directory structuur.


## Aanroepen bouwblok

Het proces van dit blouwblok kan aangeroepen worden via een call activity (Called element: opvragen-informatie) in een (hoofd)proces.
Het bouwblok maakt gebruik van (minimaal) twee input proces variabelen:
* `communicatievoorkeur` - voor bepaling van sequence flows en de informeren-aanvrager bouwblok.
* `informatieverzoek` - de daadwerkelijke verzoek object. bevat variabelen zoals `hersteltermijn`, `duedate`, `toelichting` en `opTeVragenInformatie`.
wordt gebruikt voor plugin acties, user tasks en service tasks van dit process.

## Gebruiken bouwblok

Dit bouwblok heeft twee flows: Portaal en Anders.  
Bij Portaal flow moet de behandelaar alleen de beoordeling taak afronden nadat en portaaltaak is verwerkt.  
Bij Anders flow is he van belang dat de twee hulp (ad-hoc) processen 
worden aan jouw Dossier definitie gekoppeld (via process-document-link of manuel) en dan vanuit het specifieke zaakdossier 
aangeroepen wanneer het nodig is voor dit process verder te gaan.