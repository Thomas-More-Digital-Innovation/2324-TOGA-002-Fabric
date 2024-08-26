# Demo Microsoft Fabric voor ToGaether

## doel van het project

In opdracht van ToGaether, een dochterbedrijf van de Algorythm group binnen Cronos, maakten Bryan Deckers en Nathan Neve een demonstratie van Microsoft Fabric. Het doel van de demo is de capaciteiten van Fabric te gaan ontdekken, alsook kinderziekten te vinden en rapporteren. Tijdens het maken van de opdracht was Fabric nog maar net uit beta.

## verloop

Na onze eerste kennismaking met de managing partners en onze begeleider gingen we van start met onze opdracht. We kregen als data source de fictieve dataset: [Adventure Works](https://www.kaggle.com/datasets/algorismus/adventure-works-in-excel-tables).
We maakten een data model en deden een studie naar alle Paas-tools die geïntegreerd zijn in de Saas-offering "Microsoft Fabric", zodat we wisten welke tools we konden gebruiken.

Vervolgens werden we geïnformeerd over de werkwijze in ToGaether:

### 1. Bronze Layer (Ruwe Data)

**Doel:** Opslag van ruwe, onbewerkte data.

**Wat gebeurt er:**

- De data wordt rechtstreeks ingeladen vanuit de bron.
- Dit is de eerste plaats waar de gegevens terechtkomen in het data lakehouse.
- De data wordt vaak in zijn oorspronkelijke vorm opgeslagen zonder enige significante transformatie of cleaning.
- Dit dient als archief, zodat er altijd terug kan worden gegaan naar de originele gegevens in geval van fouten in de verdere lagen.

### 2. Silver Layer (Gecleande en Verrijkte Data)

**Doel:** Schoonmaken en verrijken van de data.

**Wat gebeurt er:**

- In deze laag worden de ruwe gegevens uit de Bronze Layer opgeschoond en verrijkt.
- Data wordt schoongemaakt (bijvoorbeeld ontbrekende waarden opvullen, outliers verwijderen).
- Transformaties zoals het samenvoegen van datasets of het standaardiseren van formaten worden gedaan.
- De Silver Layer bevat gegevens die klaar zijn voor analytische verwerking, maar nog steeds gedetailleerd en uitgebreid genoeg zijn om flexibel te blijven.

### 3. Gold Layer (Geaggregeerde en Geoptimaliseerde Data)

**Doel:** Data voorbereiden voor eindgebruik en business intelligence.

**Wat gebeurt er:**

- In de Gold Layer worden de gegevens verder getransformeerd naar een model dat geschikt is voor specifieke analytische toepassingen of rapportages.
- Dit kan bestaan uit geaggregeerde tabellen, kant-en-klare datasets, of gestroomlijnde weergaven die zijn geoptimaliseerd voor prestaties.
- Vaak worden hier specifieke KPI's of rapportagedata voorbereid, zodat eindgebruikers gemakkelijk toegang hebben tot relevante informatie zonder extra verwerking.
- Deze laag is ontworpen voor gebruik door BI-tools en dashboards, en bevat dus alleen data die direct nuttig is voor de business.

#

### Belangrijkste documenten in deze repo:

```
├───documentatie
|   |
│   │   Algorhythm Referentiearchitectuur.pptx
│   │   Best Practices.pdf
            Analyse naar best practises in Microsoft Fabric
│   │   Data Analysis.pdf
            Gedetailleerde analyse van alle datatypes van onze source
│   │   Data Architecture.pdf
            Analyse van paas platformen in Fabric in relatie met hun functie
│   │   Data Modelling.pdf
            Het datamodel
│   │   Detailed design.xlsx
            Evolutie van alle data doorheen alle zone's beschreven in excel, cleaning, staging,...
│   │   SCD Type 2.pdf
            Beschrijving van slowly changing dimensions
│   │
│   └───notebooks
|           Hier zijn alle Spark notebooks terug te vinden
│
└───documents
    ├───files
    │       Alle source files voor ons project (= Adventure works source files)
    │
    └───star_schema
            AdventureWorks_StarSchema_v1.mdj, het datamodel
```
