# PCC — Parliaments Day-by-Day

**Who was in what parliament, party, and party-group, and when.**

PCC (*Parliamentary Careers in Comparison*) is an open dataset of the full political careers of (almost) every national and regional parliamentarian in several countries, reconstructed **day by day** rather than election by election. It tracks people across parliamentary mandates, party memberships, factions, committees, electoral candidacies, and every other resume entry that makes up a political career — from a first city-council seat to a term as prime minister.

- Website: [parliamentarycareersincomparison.org](http://parliamentarycareersincomparison.org)
- Full data dictionary: [`pcc_codebook/PCC_codebook.md`](pcc_codebook/PCC_codebook.md) — this README only summarizes it
- Found a data issue? [Open a GitHub issue](issues) — country-labelled reports are how this dataset gets better

## Data at a glance

| | |
|---|---|
| Countries | Switzerland, Germany, Netherlands, Norway, Canada, Ireland, United Kingdom (Scotland) |
| Parliaments covered | 980 legislative terms — both national assemblies and regional ones (Swiss cantonal parliaments, German Länder) |
| Time span | 1867 – 2025 |
| Politicians | 88,130 |
| Resume entries | 250,525 career-spell records |

Coverage depth varies by country and is still growing — see the per-country notes inside the codebook and the repository's issue tracker for known gaps. Exact current numbers can shift between exports; check [`dataversion.txt`](dataversion.txt) for the export timestamp this copy was built from.

## Getting the data

Each `.csv` file at the repository root is one data frame (table). A few things that trip people up on first load:

- **Delimiter is `;`**, not `,` (values themselves may contain commas).
- **Encoding is Windows-1252 / Latin-1**, not UTF-8.
- **Dates** are written as `03jan2025` (or truncated to `jan2025` / `2025` when only that much is known), never as `YYYY-MM-DD`.
- Every free-text field is restricted to plain printable ASCII (accents and umlauts are transliterated, e.g. `ü` → `ue`) — the one exception is the `id_[country]_*` source-identifier columns, which are kept byte-for-byte as issued by the original source and may contain accents.

In R:

```r
poli <- read.csv("POLI.csv", sep = ";", fileEncoding = "Windows-1252")
```

## Data structure

The data is organized into linked data frames rather than one flat table, so that variables are only ever stored at the level they actually vary on (a politician's birth date doesn't need to be repeated once per parliamentary term; a party's founding date doesn't need to be repeated once per member). IDs cross-reference the frames to each other.

![PCC entity-relationship diagram](pcc_codebook/ERdiagram.png)

| File | Data frame | One line in this table is... |
|---|---|---|
| `POLI.csv` | Politician | one politician's static, non-time-varying characteristics (name, birth date, gender, ...) |
| `PARE.csv` | Parliamentary episode | one spell of one politician being a member of, or candidate for, one parliament |
| `RESE.csv` | Resume entries | one job or position (political or not) a politician held at some point in their career |
| `MEME.csv` | Membership episode | one spell of party membership for one politician |
| `PART.csv` | Party | one political party |
| `FACT.csv` | Faction | one parliamentary party group ('faction'), which may span multiple parties |
| `COMM.csv` | Committee | one parliamentary committee, delegation, or cross-party group |
| `PARL.csv` | Parliament | one legislative term of one national or regional assembly |
| `ELEC.csv` | Election | one election (including by-elections and second rounds), at district level |
| `ELLI.csv` | Electoral list | one candidate list put forward in one district for one election |
| `ELEN.csv` | Electoral list entry | one candidacy of one politician on one list |
| `ELDI.csv` | Electoral district | one constituency, for one parliamentary term |
| `ORGS.csv` | Organisations | one interest group / outside organisation a politician was affiliated with |
| `QUOT.csv` | Quota module | one gender-quota rule for one party, at the faction level |
| `MINE.csv` | Ministerial episode | one spell of a politician holding cabinet/ministerial office — newest frame, not yet fully documented in the codebook |

Every definition, coding rule, and edge case (what counts as "the same" faction after a split, how mandate start dates are determined, the political-function and policy-area code lists, etc.) lives in the codebook — treat this table as a map, not a substitute.

## Data sources

PCC combines official parliamentary records, national statistical/biographical registers, and secondary academic sources, country by country:

- **Switzerland** — the Swiss Parliamentary Services' official OData web service ([ws.parlament.ch](https://ws.parlament.ch)), plus Swiss yearbooks for historical coverage.
- **Germany** — German Bundestag open data (official *Stammdaten* biographical register, [bundestag.de/services/opendata](https://www.bundestag.de/services/opendata)) for current terms; German yearbooks for historical coverage; cross-referenced against Philip Manow's Bundestag biographical dataset.
- **Netherlands** — [parlement.com](https://www.parlement.com), the website of the Dutch Parliamentary Documentation Centre (PDC), cross-checked against the Tweede Kamer's own open-data portal.
- **Norway** — the Storting's official [Open Data API](https://data.stortinget.no/).
- **Canada** — ParlInfo, the Library of Parliament's public parliamentarian database ([lop.parl.ca](https://lop.parl.ca)).
- **Ireland** — official records of the Houses of the Oireachtas.
- **United Kingdom** — official membership records of the Scottish Parliament.

Additional country pipelines are under active development. Some fields are enriched from Wikidata (e.g. birth dates, external identifiers). See the codebook's *Data Sources* section and the `id_[country]_*` columns in `POLI.csv` for the exact source system behind each row.

## License

This dataset is released under the **[Creative Commons Attribution-NonCommercial 4.0 International license (CC BY-NC 4.0)](LICENSE)**.

In short: you are free to use, share, and adapt this data for **any non-commercial purpose** (research, teaching, journalism, personal projects), as long as you give appropriate credit. Commercial use requires separate permission from the PCC project team.

### How to cite

If you use this data in published or public-facing work, please cite:

> Turner-Zwinkels, T., Huwyler, O., Frech, E., Manow, P., Bailer, S., Goet, N. D., & Hug, S. (2022). Parliaments day-by-day: A new Open Source database to answer the question of who was in what parliament, party, and party-group, and when. *Legislative Studies Quarterly*, 47(3), 761–784. https://doi.org/10.1111/lsq.12359

```bibtex
@article{turnerzwinkels2022pcc,
  title   = {Parliaments day-by-day: A new Open Source database to answer the question of who was in what parliament, party, and party-group, and when},
  author  = {Turner-Zwinkels, Tomas and Huwyler, Oliver and Frech, Elena and Manow, Philip and Bailer, Stefanie and Goet, Niels D. and Hug, Simon},
  journal = {Legislative Studies Quarterly},
  volume  = {47},
  number  = {3},
  pages   = {761--784},
  year    = {2022},
  doi     = {10.1111/lsq.12359}
}
```

Publication page: https://research.tilburguniversity.edu/en/publications/parliaments-daybyday-a-new-open-source-database-to-answer-the-que/
