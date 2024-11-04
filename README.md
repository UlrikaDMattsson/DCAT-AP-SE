# DCAT-AP-SE

In this repository we maintain the Swedish adaption to DCAT-AP, referred to as DCAT-AP-SE. The specification is maintained by [Agency for digital government (DIGG)](https://www.digg.se/en), you will find the latest version of the documentation on [docs.dataportal.se/dcat](https://docs.dataportal.se/dcat/). Please note only the [formal specification document](https://docs.dataportal.se/dcat/en/) is available in english at this time.

I det här Github-arkivet hanterar vi den svenska anpassningen till DCAT-AP som benämns DCAT-AP-SE. Specifikationen förvaltas av [Myndigheten för digital förvaltning (DIGG)](https://www.digg.se) och aktuell dokumentation finner ni på [docs.dataportal.se/dcat](https://docs.dataportal.se/dcat/).

Under våren 2024 uppdaterades DCAT-AP-SE till version 3.0 av DCAT-AP. Se de olika versionerna och tillhörande arbetsprocesser:

* [Senaste stabila versionen](https://docs.dataportal.se/dcat/sv/) under våren togs DCAT-AP-SE version 3.0 fram. Se [arbetsprocess](process/3.0/index.md).
* [Version, 2.2.0](https://docs.dataportal.se/dcat/2.0.0/sv/) togs fram under hösten 2023 och början på våren 2024 då stöd för värdefulla datamängder las till.
* [Version 2.0.0](https://docs.dataportal.se/dcat/2.2.0/sv) togs fram hösten 2019 och våren 2020. Se [arbetsprocess](process/index.md).

## Hur man bidrar / ger återkoppling

- Skapa nya / kommentera på existerande [ärenden på GitHub](https://github.com/diggsweden/DCAT-AP-SE/issues)
- Skapa [pull-requests](https://github.com/diggsweden/DCAT-AP-SE/pulls) för konkreta ändringsförslag.
- Som en del av arbetsprocessen när sådan pågår:
   - Delta i en arbetsgrupp.
   - Ge återkoppling i form av en remiss.
- Mejla till [info@digg.se](mailto:info@digg.se).

## Förvaltning av specifikationens delar

Specifikationen kan delas upp i två delar.

1. En formell metadataspecifikationen som drivs av en [JSON konfiguration](bundle.json) via ramverket [RDForms-specs](https://bitbucket.org/metasolutions/rdforms-specs/src/main/).
2. Stödjande dokumentation uttryckt i markdown, se material i katalogen [docs](docs). Dokumentationssidor genereras av [MkDocs](https://www.mkdocs.org/).

Den formella metadataspecifikationen förvaltas på både engelska och svenska.

Observera att JSON konfigurationen är uppdelad i en mängd olika JSON filer (för ökad läsbarhet och förvaltning) som byggs ihop med ett node.js script till en stor JSON fil för att göra renderingen snabbare (minska mängden requests).
Så här bygger man:

    node buildBundle.js
    
Resultatet är att filen [`bundle.json`](bundle.json) uppdateras vilken sedemera laddas av metadata specifikationen vid rendering.
