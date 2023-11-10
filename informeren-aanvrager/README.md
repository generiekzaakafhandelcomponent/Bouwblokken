# Informeren aanvrager
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/generiekzaakafhandelcomponent/Basisprocessen/blob/feature/generieke-zaak/README.md)

## Inleiding
Het informeren aanvrager bouwblok kan gebruikt worden om op basis van meegegeven communicatievoorkeur een persoon te informeren. Het bouwblok biedt de mogelijkheid om: 
- een e-mail notificatie (bijvoorbeeld zonder inhoudelijke informatie) te versturen
- een e-mail (bijvoorbeeld met inhoudelijke informatie) te versturen
- een gebruikerstaak te presenteren die een gebruiker vraagt een brief af te drukken

## Installatie
We gaan uit van een bestaande Valtimo GZAC backend repository met daarin een bestaand proces. Dit bouwblok is getest op Valtimo GZAC 10.7.0.RELEASE.

Kopiëer de bestanden van de `config` directory naar de config directory van Valtimo GZAC (`src/main/resources/config/`)
en behoud dezelfde directory structuur.


## Aanroepen bouwblok

Het proces van dit blouwblok kan aangeroepen worden via een call activity (Called element: informeren-aanvrager) in een (hoofd)proces.
Het bouwblok maakt gebruik van (minimaal) één proces variabele: `communicatievoorkeur`. Zie de sequence flows in de bpmn.

