# PCC - Codebook V4.0.0

**The PCC Project Team**

---

## Table of Contents

1. [Project Description](#project-description)
   - [Aim of this Document](#aim-of-this-document)
   - [Short Project Summary](#short-project-summary)
   - [Mid-term Road-map of the Project](#mid-term-road-map-of-the-project)
2. [Data Structure, Sources & Sampling](#data-structure-sources--sampling)
   - [Data Structure](#data-structure)
   - [Data Sources](#data-sources)
   - [Sample](#sample)
3. [How to Read this Codebook](#how-to-read-this-codebook)
   - [Labels, Abbreviations, Etc.](#labels-abbreviations-etc)
   - [Collection Effort Per Variable](#collection-effort-per-variable)
4. [POLI - Politician Level Data Frame](#poli---politician-level-data-frame)
5. [PARE - Parliamentary Episode Data Frame](#pare---parliamentary-episode-data-frame)
6. [RESE - Resume Entries Data Frame](#rese---resume-entries-data-frame)
7. [Political Functions Coding](#political-functions-coding)
8. [Policy Area Codes](#policy-area-codes)
9. [PARL - Parliament Data Frame](#parl---parliament-data-frame)
10. [MEME - Membership Episode Data Frame](#meme---membership-episode-data-frame)
11. [PART - Party Data Frame](#part---party-data-frame)
12. [FACT - Faction Data Frame](#fact---faction-data-frame)
13. [COMM - Committee Data Frame](#comm---committee-data-frame)
14. [ELEC - Election Data Frame](#elec---election-data-frame)
15. [ELLI - Electoral List Data Frame](#elli---electoral-list-data-frame)
16. [ELEN - Electoral List Entry Data Frame](#elen---electoral-list-entry-data-frame)
17. [ELDI - Electoral District Data Frame](#eldi---electoral-district-data-frame)
18. [ORGS - Organisations Data Frame](#orgs---organisations-data-frame)
19. [QUOT - Quota Module](#quot---quota-module)
20. [Appendices](#appendices)

---

## Project Description

### Aim of this Document

The primary purpose of this codebook is to provide detailed information on the data structure and variables of the parliamentary careers in comparison data. This codebook's secondary - much more ambitious, long-term and as such necessarily more controversial - purpose is to establish a new data-standard (see Turner-Zwinkels 2016 for a specification of the requirements of such a new standard). As such, we aimed to design a data-structure and coding-standard that can be used to study political careers in any context (country, level, system...). Any input that informs our success in this regard is very welcome!

### Short Project Summary

The research project "Parliamentary Careers in Comparison" (PCC) aims to investigate political careers and activities of parliamentary candidates and parliamentarians in Switzerland, Germany and the Netherlands (most of the Dutch data has already been collected as part of the PhD thesis of PCC project member Tomas Turner-Zwinkels) since the Second World War. Based on an extensive collection of detailed individual-level data, we investigate biographical and behavioural dynamics to obtain a full and dynamic picture of parliamentary careers.

The research interests covered by the project cover three broad areas:
1. The first set of questions revolves around career paths on different levels, how they typically develop, and how these patterns can be explained.
2. With the second set of questions we focus on the impact of political institutions on political careers.
3. A third strand highlights the consequences of the different career paths on parliamentary behaviour and future post-parliamentary careers.

The PCC data-set contains detailed information on the political careers of parliamentarians and parliamentary candidates. Examples of variables include socio-demographic information of national candidates and parliamentarians of the three countries since the second world war, the candidate list positions, political functions (if elected) of national parliamentarians. Future versions of this data will also include data on regional parliamentarians and expand the range of included variables. See [parliamentarycareersincomparison.org](http://parliamentarycareersincomparison.org) for more information.

### Mid-term Road-map of the Project

Data will be collected in several waves over a three year period (2016-2019). The codebook below summarizes the data-collections efforts in the first wave. Future waves will likely include the collection of both *similar data on other politicians* (e.g. candidates for the national parliament, regional parliamentarians) and *different data for the same politicians* (e.g. additional variables in parliamentary behavior). Please drop us an email if you would like to see specific variables included. We can't promise anything but are always happy to consider!

---

## Data Structure, Sources & Sampling

### Data Structure

The PCC data-structure is organized into five levels and eleven data-frames. Example data can be found [here (.xlsx download)](http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx). The logic behind this data-structure is to collect static and time-varying variables as much is possible in an 'intuitive' way, sticking close to the structures that researchers are used to and the format that different kinds of data (e.g. biographical profiles, electoral lists) are typically stored in. In practice this implies that each data frame only contains information varying on the same level (e.g. the individual or the electoral list). We use a system of identifiers to allow data-points to be connected up together.

**Data Frames Overview:**

- **Politician level data**
  - **POLI** - Stable characteristics (see [POLI section](#poli---politicians-data-frame))
  - **PARE** - Parliamentary episodes (see [PARE section](#pare---parliamentary-episode-data-frame))
  - **RESE** - Resume entries
  - **MEME** - Membership episodes (see [MEME section](#meme---membership-episode-data-frame))

- **PART** - Parties (see [PART section](#part---party-data-frame))

- **PARL** - Parliaments (see [PARL section](#parl---parliament-data-frame))

- **FACT** - Factions (see [FACT section](#fact---faction-data-frame))

- **COMM** - Committees (see [COMM section](#comm---committee-data-frame))

- **Electoral list data**
  - **ELDI** - Electoral districts (see [ELDI section](#eldi---electoral-district-data-frame))
  - **ELLI** - Electoral lists (see [ELLI section](#elli---electoral-list-data-frame))
  - **ELEN** - Electoral list entries (see [ELEN section](#elen---electoral-list-entry-data-frame))

### Data Sources

Data was collected by a combination of different sources. A main source for the CH and DE parliamentary career data are yearbooks. A main source in the Netherlands was the website of the Dutch parliamentary documentation centre. Other data stem from different statistical offices or are based on newspaper articles or personal websites.

### Sample

Data can be regarded a **complete (population) sample of national parliamentarians since 1946 of all three countries (CH, DE, NL)** (wave one data collection). Note: Up until 1990 only data on West-Germany is included.

Both parliamentarians in the lower-house (i.e. Bundestag, Nationalrat, Tweede Kamer) and the upper-house (i.e. Ständerat, Eerste Kamer) are included. Future waves will likely include candidates for national elections in Germany and Switzerland (and maybe the Netherlands) since 1946, and of regional parliamentarians of all three countries (wave two). The data will likely also include data on the candidates for elections to regional parliaments (e.g. German Bundesländer or Swiss Cantons).

---

## How to Read this Codebook

### Labels, Abbreviations, Etc.

- Brackets (`[` and `]`) in variable names signify variable names. `[country]_` for example means that there will be as many of this variable (set) in the data-frame as there are countries in the data.
- `DNC` means: Do Not Collect, these are specifications that are kept in codebook for reference purposes whose values we do not intend to collect (to this level of detail).
- If a variable name contains an (by underscores) indexed element on the lists which is not used, `NA` will be used as a filler.

### Collection Effort Per Variable

Not all variables are collected with the same effort. Our effort to collect different variables varies from the highest level ('Collect and follow-up until Complete') to the lowest level ('Collect When Easy'). These are the matching abbreviations:

| Abbreviation | Meaning |
|-------------|---------|
| COMP | Collect and follow-up until complete |
| CWA | Collect when available |
| CWE | Collect when easy |
| DNC | Do not collect |

---

## Glossary of Abbreviations

| Abbreviation | Meaning |
|-------------|---------|
| PCC | Parliamentary Careers in Comparison |
| POLI | Politician Level Data Frame |
| PARE | Parliamentary Episode Data Frame |
| PARL | Parliament Data Frame |
| MEME | Membership Episode Data Frame |
| PART | Party Data Frame |
| FACT | Faction Data Frame |
| COMM | Committee Data Frame |
| ELLI | Electoral List Data Frame |
| ELEN | Electoral List Entry Data Frame |
| ELDI | Electoral District Data Frame |
| RESE | Resume Entries Data Frame |
| ORGS | Organisations Data Frame |
| QUOT | Quota Module (extension of FACT) |
| CH | Switzerland |
| DE | Germany |
| NL | Netherlands |
| L | List |
| D | District |
| LD | List and District |
| ST | Static |
| TV | Time-Varying |

---

## POLI - Politician Level Data Frame

Politician level variables are all static variables on the level of individual politicians. Example data can be found [here (.xlsx download)](http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/DF.xlsx).

### Summary of POLI Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `pers_id` | PriID | [country]\_[last\_name]\_[first\_name]\_[year\_of\_birth] e.g. CH\_Abate\_Fabio\_1966, DE\_Mueller\_Johann\_1956dec, NL\_Mark\_Rutte\_1956dec-1 | **parliamentarians individual identification code**: a combination of `country_abb`, `last_name`, `first_name` and `birth_date` | COMP |
| `id_[country]_parl` | ID | 2739 = Gobbi, Norman | **e.g. parlamentsdienst CH identification number**: identification number, as used by the CH Parlamentsdienst | CWA |
| `last_name` | String | Mueller, deCourten, Mutlu-Blum | **parliamentarian's last name**: contains the last name with 'von' etc. connected, double last names hyphenated and special characters replaced | COMP |
| `first_name` | String | "Jules-Henri", "Elisabeth", "Johann-Ulrich-Werner", "Heinrich-E." | **parliamentarian's first name**: contains the first name with double first names hyphenated and special characters replaced | COMP |
| `other_name` | String | Hans, Muller | **parliamentarian's alternative name or alias**: contains an (array of) first or last name(s) or alias(es) for matching purposes | CWA |
| `gender` | Factor | m = male, f = female, nb = non-binary, tm = trans male, tf = trans female | **parliamentarian's gender** | COMP |
| `birth_date` | Date | 16apr1897, 29may1930 | **parliamentarian's birth date** | COMP |
| `death_date` | Date | 16apr1897, 29may1930 | **date of death**: empty if still alive and NA when unknown | CWA |
| `birth_place_raw` | String | "Berlin", "Zuerich", "Baden-Wuerttemberg" | **place of birth**: place of birth of the parliamentarian | CWA |
| `citizenship` | String | DE, DE; SK, CH | **parliamentarian's citizenship(s)**: array of citizenship(s) as country abbreviation(s) | CWA |
| `citizenship_canton` | String | "ZH" | **Swiss canton of citizenship**: Switzerland-specific variable. Array of citizenship(s) as canton abbreviation(s). Contains all citizenships over the entire lifetime | CWA |
| `hometown_raw` | String | "Fehraltorf" | **hometown**: Switzerland-specific string variable. Name of place/city/municipality that is the candidate's/parliamentarian's hometown | CWA |
| `educ_age` | Integer | 0-100 | **age at completion of education**: ratio variable indicating how old a politician was when finishing their last degree | CWA |
| `educ_raw` | String | School 'The Bear' 1932 | **education**: raw text string field with all available educational information | COMP |
| `title_raw` | String | Prof. Dr. | **academic title**: academic title(s), if any. Set to "none" if known that MP has no academic title | COMP |
| `military_raw` | String | Major, Appointé | **military rank**: raw string information about the military career | CWA |
| `twitter_screen_name` | String | Petra_Sitte_MdB, KathyR111 | **twitter screen name**: raw string information about the twitter screen name (can be changed) | CWA |
| `twitter_id` | Integer | 17535941, 2179010672 | **twitter id**: refers to the specific account and cannot be changed | CWA |
| `facebook_username` | String | john.doe, janedoe123, 100009711991629 | **facebook username**: unique identifier for users on Facebook (sometimes numerical, sometimes changed by user) | CWA |

### Variable Descriptions

#### pers_id
**Parliamentarians individual primary identification code**: Identification code, individual to each parliamentarian across levels. The code consists of:
- Country abbreviation (as specified in variable `country_abb`)
- Last name (as specified in variable `last_name`) — but see the hyphenated-surname rule below
- First name (as specified in `first_name`) — only the first part of a double first name (see below)
- Year of birth (as specified by the last four digits of variable `birth_date`)

All connected by underscores.

**Hyphenated (double) names — pers_id uses only the first part:**
The `pers_id` must **not** contain hyphenated surnames. For a double surname
(Doppelname), only the **first** part is used in the `pers_id`, while the full
hyphenated form is retained in the `last_name` variable, and the dropped surname
part(s) are additionally recorded in `other_name` (see below) so the alternative
single-surname form is available for matching. The same holds for double first
names: only the first part enters the `pers_id`. For example, the person whose
`last_name` is `Mackensen-Geis` and `first_name` is `Isabel` has `pers_id`
`DE_Mackensen_Isabel_1986`; `Goering-Eckardt` / `Katrin-Dagmar` gives
`DE_Goering_Katrin_1966`. (This keeps `pers_id`s stable when a second surname is
added by marriage, and reserves the hyphen for the disambiguation index `-x`.)

**Special cases:**
- If the ID is not unique to one person, the month of birth is appended by underscore
- If the month of birth is not known or still does not uniquely identify the person, an additional index `-x` is appended by hyphen
- If a birth-year is unknown, that part of the identification string will be written as `9999`
- If first name or last name are unknown, that part will be written as `XXX`
- As soon as the information becomes known, the placeholder is replaced with the actual value

Alternative IDs and how they correspond to the main ID can be found in the appendix.

#### last_name & first_name

**For the cleaning of names** the following rules apply:

- Names always start with a capital letter
- An umlaut (ö, ä, ü) is written as "oe", "ae", "ue"
- A "ß" will be written as "ss"
- All accents or similar (é, ã, ê, š, ğ, ç, ÿ) are left out, instead just the basic letter is written (e, a, e, s, g, c, y)
- If names contain prepositions like 'Von' or 'Van der' then the space between these prepositions (name-particle) and the actual lastname are removed and capitals are replaced. So, 'Von Liebig' is spelled as 'vonLiebig' and 'Van Der Maden' is spelled as 'vanderMaden'
- If the names contain multiple parts (e.g. first_name Jean Luc) then the spaces are replaced with hyphens (e.g. Jean-Luc)
- Additional non-name particles such as junior are included after underscores (Carl_jun)

#### last_name
**Parliamentarian's last name**: The last name(s) of the parliamentarian, following the cleanup rules specified above.

#### first_name
**Parliamentarian's first name**: The first name(s) of the parliamentarian, following the cleanup rules specified above.

#### other_name
**Parliamentarian's alternative names or alias**: Contains an (array of) first or last name(s) or alias(es) in case there is or was another first or last name used than mentioned in `first_name` or `last_name`. This might be due to name change, a maiden name, or a commonly used shortage or alias. **For a hyphenated / double surname (Doppelname), record here the surname part(s) DROPPED from the `pers_id` by the first-part-only rule** (the second and later components) so the alternative name stays available for matching when another source holds the person under that part. Example: `last_name` `Michaud-Gigon`, `pers_id` `CH_Michaud_Sophie_1975`, `other_name` `Gigon`. (The full hyphenated form is still in `last_name`, and the first part is already in the `pers_id`, so it is the dropped part that is worth recording here.)

#### gender
**Parliamentarian's gender**: Gives the gender of the parliamentarian in string format:
- m = male
- f = female
- nb = non-binary
- tm = trans male
- tf = trans female

#### birth_date
**Parliamentarian's birth date**: Mentions the date of birth of a parliamentarian consisting of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year of birth. If only the month is known the days are dropped and if only the years are known the day and month letters are dropped.

#### death_date
**Parliamentarian's death date**: Mentions the date of death of a parliamentarian consisting of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year of death. Is empty if still alive at the moment of data-collection and NA when unknown.

*Effort: collect for those who died 'in office' and limit to MPs.*

#### citizenship
**Parliamentarian's citizenship(s)**: Mentions the parliamentarian's array of citizenship(s) by mentioning the abbreviation of country(s) he/she is citizen of. The used abbreviations follow the ISO "ALPHA-2" code. (See: http://www.nationsonline.org/oneworld/country_code_list.htm)

---

## PARE - Parliamentary Episode Data Frame

The parliamentary episode data-frame contains information that varies across parliamentary episodes. This data-frame connects the parliament (PARL) data-frame with the politician (POLI) data-frame. It contains the crucial information of what politician was in what parliament and stores additional information that is typically available with this resolution.

The data-frame does not only contain elected politicians and the parliament they were member of, but also candidates. Candidates are associated to the parliament they ran for. Several time-varying variables are collected for which we know they vary across episodes but on which we do not have more detailed time-stamped information (e.g., the number of children). This would also be the data-level where parliamentary behavior variables end up.

### Summary of PARE Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `parl_episode_id` | PriID | CH\_Abate\_Fabio\_1966\_\_CH\_NT-NR\_1946 | **parliamentary episode ID**: combination of pers\_id and parliament\_id | COMP |
| `pers_id` | String | CH\_Abate\_Fabio\_1966 | See POLI. A politician is considered a part of a specific parliament as soon as he/she has spent at least one day in the parliament | COMP |
| `parliament_id` | String | [country]\_[level]-[abbr]\_firstyear e.g. NL\_NT\_1946 | **parliament identifier**: see specification below | COMP |
| `member_ofthisparliament_atsomepoint` | String | "yes", "no" | **member of this parliament at some point**: dummy indicating whether someone was in the current parliament or not | COMP |
| `residence_place_raw` | String | "Mecklenburg", "Zuerich", "Essen" | **place of residence raw**: all available information on the place a parliamentarian lives in | CWA |
| `residence_address` | String | "Bismarkstrasse 57, 10627 Berlin" | **residence address**: complete residential address of the parliamentarian, only full address otherwise residence\_place\_raw is used | CWE |
| `residence_address_longi` | String | longitude | **longitude of the residence address** | CWE |
| `residence_address_lati` | String | latitude | **latitude of the residence address** | CWE |
| `family_status_raw` | String | 'Widowed' | **any (other) family information**, in a raw-text format | CWA |
| `married` | Binary | 1 = 'married', 0 = 'not married' | **parliamentarian's marital status**, including registered partnerships | CWA |
| `nr_children` | Integer | 0-15 | **number of children** | CWA |

### Variable Descriptions

#### parl_episode_id
**Unique identifier of the parliament episode**: Combination of the pers\_id and parliament\_id.

#### birth_place_raw
**Place of birth**: Mentions the place of birth of the parliamentarian. The "place" that is mentioned may be very specific (e.g. street, city) to very broad (e.g. district or state). Which one is mentioned depends on the information available. In case more than one information/level of detail is available, the information is appended to the existing information by a semicolon. In case the place has different names in different languages and these are available, the name in the local language is chosen.

#### residence_place_raw
**Place of residence**: Mentions the place a parliamentarian lives in. The "place" that is mentioned may be very specific (e.g. city) to very broad (e.g. district or state). Which one is mentioned depends on the information available. In case more than one information/level of detail is available, the information is appended to the existing information by semicolon. In case we have the full address of residence, the information is recorded in variable `residence_address`. In case different place names exist in different languages and are available, the name in the local language is chosen.

#### residence_address
**Residence address**: Complete residential address of the parliamentarian. Only full addresses are mentioned (otherwise use the variable `residence_place_raw`). The house number is separated from the street name by a blank space, the city name and code are separated from the street name and house number by a comma.

#### married
**Parliamentarian was married at entry**: Dummy variable capturing whether a parliamentarian was married (or in a registered partnership). Time-varying. If the status is not known, then the status during the last parliamentary term is used.

#### family_status_raw
**Family status raw**: The raw description of one's relationship status. If the status is known, but not when, then the last parliamentary term is used.

#### nr_children
**Number of children**: Numeric variable that captures the number of children a parliamentarian has. Time-varying. If the status is not known, then the status during last parliamentary term is used.

---

## RESE - Resume Entries Data Frame

### What are resume entries?

In a nutshell, resume entries refer to the multitude of experiences, activities, and positions that individuals have held throughout their careers. It answers the question: *who held what political job when*.

This data-frame contains a long list of all functions (political- and non-political jobs and side-functions) that MPs held throughout their (political) career. Functions are defined as *all positions politicians can hold*. This entails paid and unpaid functions as well as full-time and part-time ones. It can be as big as being a prime-minister and as small as a short voluntary activity for a local sport-club. Everything that entails an activity that a politician considers worth reporting on their resume is included.

Each politician occurs multiple times in this data. A politician that held a total of 20 different (political) functions throughout her career will occupy 20 lines in this data-frame.

A complete resume entry contains:
- Reference to the role somebody played in an organization
- The name of the organization
- Where in the organization this individual played this role
- A start and end-date

A typical resume entry as used in biographies and CVs contains a description of the activity as well as a start and an end date. The RESE therefore collects all resume entry variables and variables directly based on or related to these entries.

### Summary of RESE Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `res_entry_id` | PriID | CH\_Abate\_Fabio\_1966\_\_01, DE\_Mueller\_Johann\_1956\_dec\_\_06 | **resume entry ID**: combination of pers\_id and an index number | COMP |
| `pers_id` | String | CH\_Abate\_Fabio\_1966 | **politician identifier**: reference to POLI | COMP |
| `country_abb` | String | CH, DE, NL | **country abbreviation**: ISO Alpha-2 code | COMP |
| `res_entry_type` | String | pol, prof, educ, iden, oth | **resume entry type**: categorizes entry as political, professional, educational, occupational identity, or other | COMP |
| `res_entry_index` | Integer | 01, 02, ... | **entry index**: position of the entry in the source (1=first mentioned) | COMP |
| `res_entry_start` | Date | 29apr1976, aug1953, 2012 | **resume entry start date**: when this entry started | COMP |
| `res_entry_end` | Date | 29apr1976, aug1953, 2012 | **resume entry end date**: when this entry ended | COMP |
| `res_entry_at` | Date | 29apr1976;aug1953 | **at date(s)**: array of dates indicating position was held at this point in time | COMP |
| `res_entry_raw` | String | Ständerat von 05.12.2011 bis | **raw entry**: the resume entry as taken from the source | COMP |
| `political_function` | String | NT\_LE-UH\_T3\_NA\_01, NT\_LE\_T2-CO\_1500\_03 | **political function code**: multi-level code for political functions | COMP |
| `pf_geolevel` | String | NT, RE, MU, DI, EU, IN | **geographic level**: position in multi-level hierarchy (national, regional, etc.) | COMP |
| `pf_instdomain` | String | LE, EX, PA, IG, AD, JU, SI, OT | **institutional domain**: type of organization (legislative, executive, party, etc.) | COMP |
| `pf_orglevel` | String | T1, T2-CO, T2-DL, T3 | **organizational tier**: level in organizational hierarchy | COMP |
| `pf_policy_area` | String | 0100, 1500, NA | **policy area**: CAP-based policy area code | COMP |
| `pf_position` | String | 01, 02, 03, 09, 10, 11 | **position type**: type of position (e.g., member, chair, substitute, reserve deputy, non-voting member) | COMP |
| `parliament_id` | String | CH\_NT-NR\_2007;CH\_NT-SR\_2007 | **parliament identifier(s)**: parliament(s) associated with this entry | COMP |
| `faction_id` | ID | - | **faction identifier**: faction associated with this entry | CWA |
| `comm_id` | ID | CH\_NT-NR\_2007\_\_CO\|FK | **committee identifier**: committee associated with this entry | CWA |
| `prof_field` | Integer | 100:2300 | **professional field**: CAP-based field code for professional entries | DNC |
| `isco08` | Integer | 1:9999 | **ISCO-08 code**: International Standard Classification of Occupations | CWA |
| `tomas_code` | String | - | **Tomas code**: project-specific coding | CWA |
| `educ_level_isced2011` | Integer | 0:8 | **education level**: ISCED 2011 level code | COMP |
| `educ_field_isced2013` | Integer | 00:10 | **education field**: ISCED 2013 field code | COMP |
| `org_id` | ID | - | **organization identifier**: reference to ORGS data frame | CWA |
| `res_entry_source` | String | parlament.ch, CH Yearbooks | **data source**: source of this entry | COMP |
| `length` | Integer | 9 | **length**: duration of the entry | CWA |

### Variable Descriptions

#### res_entry_id
**Resume entry identification code**: Individual to each parliamentarian and entry. The code consists of `pers_id` and a number per entry. Numbers below 10 are written with an additional zero (e.g., 05) and connected to `pers_id` by two underscores. The order of numbers is arbitrary but roughly corresponds to the order of appearance in the source.

#### pers_id
**Politician identifier**: Unique identification code for different politicians. See POLI for details.

#### res_entry_type
**Resume entry type**: Categorization of resume entries:
- **pol** = Political functions (directly or indirectly aimed at creating and shaping policy)
- **prof** = Professional (non-political work experience)
- **educ** = Educational (periods of education/training)
- **iden** = Occupational Identity (the job an MP mentions to the election council)
- **oth** = Other biographical episodes

#### res_entry_start
**Resume entry start date**: The first calendar day on which the person holds the position described by this resume entry.

For parliamentary membership episodes specifically, this is the first day on which the member holds a **legal mandate** to serve in parliament — i.e., the date from which they would be entitled to participate and vote if parliament were convened. This is distinct from the date the member was sworn in (a procedural step that may occur later) or the date parliament first sat in session (which may be later still).

The exact legal basis for the mandate start date varies by country and depends on constitutional provisions, electoral law, or parliamentary rules of procedure. For example:
- In some systems, the mandate begins on a constitutionally fixed date (e.g., January 3 in the US post-20th Amendment, or March 4 pre-20th Amendment).
- In others, the mandate begins on the day after the election, or on the day election results are officially certified.
- The country-specific interpretation must be documented in the data extraction pipeline for that country.

**Date format**: Date entries consist of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year (e.g., `04jan1966`). In case of missing information on days or month, shortened versions are used (e.g., `jan1966` or `1966`).

#### res_entry_end
**Resume entry end date**: The last calendar day on which the person holds the position described by this resume entry. Same format as start date.

For parliamentary membership episodes specifically, this is the last day on which the member holds a legal mandate to serve (see `res_entry_start` for the definition of "legal mandate"). The end date convention must be consistent with the start date convention within each country — both should reflect the boundaries of the legal mandate, not session calendars or procedural events.

**Midnight rule (no same-day overlap)**: PCC dates operate at day granularity. A calendar day "belongs to" a person if they held the position at midnight going into that day (i.e., they went to bed the night before as a holder of the position). This means that when one person's term ends and another's begins on the same constitutional moment (e.g., noon on January 3 in the US), the **outgoing** member's `res_entry_end` must be set to the **day before** the incoming member's `res_entry_start`. Two consecutive episodes for different persons in the same seat must never share the same date. For example, if the new term starts on January 3, the outgoing member's end date is January 2. This rule ensures that counting unique members on any given calendar day produces the correct parliament size without double-counting.

**Death during term**: When a parliamentarian dies during their term, the `res_entry_end` is set to the actual date of death (as recorded in `death_date` in POLI). This represents the last day the person held the position.

**Censoring notation**: Dates may include `[[lcen]]` (left-censored, meaning "at least since") or `[[rcen]]` (right-censored, meaning "at least until").

#### res_entry_at
**At date(s)**: (Array of) dates indicating that this position was held at this point in time, when exact start/end dates are not known.

#### res_entry_raw
**Raw entry**: The resume entry text as taken from the original source. May be edited for completeness.

#### res_entry_source
**Data source**: The source from which this entry was extracted (e.g., parlament.ch, CH Yearbooks).

#### res_entry_index
**Entry index**: The position of the entry in the source (1=first mentioned, 2=second, etc.).

#### political_function
**Political function code**: Multi-level code capturing various facets of political resume entries. Format: `[pf_geolevel]_[pf_instdomain]_[pf_orglevel]_[pf_policy_area]_[pf_position]`. See the Political Functions Coding section below for the complete coding scheme.

#### pf_geolevel
**Geographic level**: Position in the multi-level political system hierarchy. See Political Functions Coding section.

#### pf_instdomain
**Institutional domain**: Type of organization. See Political Functions Coding section.

#### pf_orglevel
**Organizational tier**: Level in the organizational hierarchy. See Political Functions Coding section.

#### pf_policy_area
**Policy area**: CAP-based policy area code. See Political Functions Coding section.

#### pf_position
**Position type**: Type of position within the organization. See Political Functions Coding section.

#### parliament_id
**Parliament identifier(s)**: Unique identification code for parliaments. Added whenever `political_function` refers to a function connected to national and regional parliaments. Is an array separated by ';' when there are multiple parliaments.

#### faction_id
**Faction identifier**: Reference to FACT data frame when the entry relates to a parliamentary faction.

#### comm_id
**Committee identifier**: Reference to COMM data frame when the entry relates to a parliamentary committee.

#### prof_field
**Professional field**: Professional field codes based on the CAP / U.S. Standard Industrial Classification, assigned to entries of type "prof".

#### isco08
**ISCO-08 code**: International Standard Classification of Occupations (4-digit). Assigned to entries of type "prof" or "iden". Main categories:
- 1: Managers
- 2: Professionals
- 3: Technicians and associate professionals
- 4: Clerical support workers
- 5: Service and sales workers
- 6: Skilled agricultural, forestry and fishery workers
- 7: Craft and related trades workers
- 8: Plant and machine operators, and assemblers
- 9: Elementary occupations
- 10: Armed forces occupations

See [ILO ISCO-08](https://www.ilo.org/public/english/bureau/stat/isco/isco08/) for details.

#### educ_level_isced2011
**Education level**: ISCED 2011 level code for educational entries:
- 0: Early childhood education
- 1: Primary education
- 2: Lower secondary education
- 3: Upper secondary education
- 4: Post-secondary non-tertiary education
- 5: Short-cycle tertiary education
- 6: Bachelor's or equivalent level
- 7: Master's or equivalent level
- 8: Doctoral or equivalent level

See [UNESCO ISCED 2011](http://www.uis.unesco.org/Education/Documents/isced-2011-en.pdf).

#### educ_field_isced2013
**Education field**: ISCED 2013 field code for educational entries:
- 00: Generic programmes and qualifications
- 01: Education
- 02: Arts and humanities
- 03: Social sciences, journalism and information
- 04: Business, administration and law
- 05: Natural sciences, mathematics and statistics
- 06: Information and Communication Technologies
- 07: Engineering, manufacturing and construction
- 08: Agriculture, forestry, fisheries and veterinary
- 09: Health and welfare
- 10: Services

See [UNESCO ISCED-F 2013](http://www.uis.unesco.org/Education/Documents/isced-fields-of-education-training-2013.pdf).

#### org_id
**Organization identifier**: Reference to ORGS data frame when the entry relates to an organization.

#### length
**Length**: Duration of the entry (typically in years).

*Note: See the Political Functions Coding section below for the complete coding scheme for political functions.*

---

## Political Functions Coding

Political functions in the PCC database are coded using a five-level hierarchical system:

### Level 1: Domain (L1DOM)

The domain distinguishes between different spheres of political activity:

| Code | Domain |
|------|--------|
| LE | Legislative |
| EX | Executive |
| PA | Party |
| IG | Interest Group |
| AD | Administration |
| JU | Judiciary |

### Level 2: Institutional Domain (L2ID)

Further specification of the institutional context:

| Code | Description |
|------|-------------|
| LE_NT | Legislative - National |
| LE_RE | Legislative - Regional |
| LE_LO | Legislative - Local |
| EX_NT | Executive - National |
| EX_RE | Executive - Regional |
| EX_LO | Executive - Local |
| PA_NT | Party - National |
| PA_RE | Party - Regional |
| PA_LO | Party - Local |
| IG_NT | Interest Group - National |
| IG_RE | Interest Group - Regional |
| IG_LO | Interest Group - Local |
| AD_NT | Administration - National |
| AD_RE | Administration - Regional |
| AD_LO | Administration - Local |
| JU_NT | Judiciary - National |
| JU_RE | Judiciary - Regional |
| JU_LO | Judiciary - Local |

### Level 3: Tier (L3TIER)

The tier level distinguishes between leadership positions and regular membership:

| Code | Description |
|------|-------------|
| T1 | Top leadership (e.g., President, Speaker, Party Leader) |
| T2 | Upper leadership (e.g., Vice-President, Committee Chair) |
| T3 | Lower leadership (e.g., Secretary, Deputy Chair) |
| T4 | Regular member |
| T5 | Substitute/Deputy member |

### Level 4: Policy Area (L4POL)

Policy areas are coded according to the Comparative Agenda Project (CAP) scheme. See the [Policy Area Codes](#policy-area-codes) section for the complete list.

### Level 5: Position (L5POS)

The specific position held within the institutional context.

| Code | Description |
|------|-------------|
| 01 | Regular member / office-holder |
| 02 | Deputy / vice / second-in-command |
| 03 | Chair / president / leader |
| 09 | Seated deputy / serving substitute |
| 10 | Reserve deputy: elected or designated substitute/deputy member eligible to take a seat; this reserve status can coexist with separate seated-deputy episodes |
| 11 | Seated non-voting / observer member: occupies a seat and may vote in committees and internal parliamentary elections, but not on legislation (e.g. the West Berlin Bundestag deputies, "Berliner Abgeordnete", 1949–1990). Counted as a seated member for `parliament_size`, but distinguishable from a full voting member |

---

## Policy Area Codes

Policy areas are coded using a modified version of the Comparative Agenda Project (CAP) coding scheme. The main categories are:

| Code | Policy Area |
|------|-------------|
| 1 | Macroeconomics |
| 2 | Civil Rights, Minority Issues, Immigration, and Civil Liberties |
| 3 | Health |
| 4 | Agriculture |
| 5 | Labor |
| 6 | Education |
| 7 | Environment |
| 8 | Energy |
| 9 | Immigration |
| 10 | Transportation |
| 12 | Law and Crime |
| 13 | Social Welfare |
| 14 | Housing |
| 15 | Domestic Commerce |
| 16 | Defense |
| 17 | Technology |
| 18 | Foreign Trade |
| 19 | International Affairs |
| 20 | Government Operations |
| 21 | Public Lands |
| 23 | Culture |
| 99 | Other/Unclassified |

### Subcategories

Each main category has subcategories for more detailed coding. For example:

**1 - Macroeconomics:**
- 100: General
- 101: Inflation, Prices, and Interest Rates
- 103: Unemployment
- 104: Monetary Policy, Central Bank
- 105: National Budget and Debt
- 107: Taxation, Tax Policy, and Tax Reform
- 108: Industrial Policy
- 110: Price Control and Stabilization
- 199: Other Macroeconomic Issues

**2 - Civil Rights:**
- 200: General
- 201: Ethnic Minority and Racial Group Discrimination
- 202: Gender and Sexual Orientation Discrimination
- 204: Age Discrimination
- 205: Disability Discrimination
- 206: Voting Rights, Political Participation, Suffrage
- 207: Freedom of Speech, Press, Religion
- 208: Right to Privacy
- 209: Anti-Government Activities
- 210: Migrant and Seasonal Workers
- 211: Indigenous Affairs
- 299: Other Civil Rights

**3 - Health:**
- 300: General
- 301: Health Care Reform
- 302: Health Insurance
- 321: Regulation of Drug Industry and Medical Devices
- 322: Facilities Construction and Regulation
- 323: Provider and Insurer Payment and Regulation
- 324: Medical Liability
- 325: Health Manpower
- 331: Disease Prevention and Health Promotion
- 332: Infants and Children
- 333: Mental Health
- 334: Long-Term Care, Home Health, Terminally Ill
- 335: Prescription Drug Coverage and Costs
- 336: Other Health Topics
- 341: Tobacco Abuse
- 342: Alcohol Abuse
- 343: Illegal Drug Abuse
- 344: Controlled Substance Regulation
- 398: Research and Development
- 399: Other Health Issues

**4 - Agriculture:**
- 400: General
- 401: Trade
- 402: Government Subsidies, Agricultural Prices
- 403: Food Inspection and Safety
- 404: Marketing, Promotion
- 405: Animal and Crop Disease
- 406: Fisheries and Fishing
- 407: Research and Development
- 408: Migrant and Seasonal Workers
- 498: Research and Development
- 499: Other Agriculture Issues

**5 - Labor:**
- 500: General
- 501: Worker Safety, OSHA
- 502: Employment Training
- 503: Employee Benefits
- 504: Labor Unions
- 505: Fair Labor Standards
- 506: Youth Employment
- 508: Parental Leave
- 509: Collective Bargaining
- 529: Migrant and Seasonal Workers
- 599: Other Labor Issues

**6 - Education:**
- 600: General
- 601: Higher Education
- 602: Primary and Secondary Education
- 603: Underprivileged Students
- 604: Vocational Education
- 606: Special Education
- 607: Excellence, Educational Quality
- 609: Arts and Humanities
- 698: Research and Development
- 699: Other Education Issues

**7 - Environment:**
- 700: General
- 701: Drinking Water
- 703: Waste Disposal
- 704: Hazardous Waste
- 705: Air Pollution
- 707: Recycling
- 708: Indoor Environmental Hazards
- 709: Species and Forest Protection
- 710: Land and Water Conservation
- 711: Climate Change
- 798: Research and Development
- 799: Other Environment Issues

**8 - Energy:**
- 800: General
- 801: Nuclear Energy
- 802: Electricity
- 803: Natural Gas and Oil
- 805: Coal
- 806: Alternative and Renewable Energy
- 807: Energy Conservation
- 898: Research and Development
- 899: Other Energy Issues

**10 - Transportation:**
- 1000: General
- 1001: Mass Transportation and Public Transit
- 1002: Highway Construction and Maintenance
- 1003: Airports and Air Traffic Control
- 1005: Railroad Transportation
- 1006: Truck and Automobile Transportation
- 1007: Maritime
- 1008: Infrastructure
- 1010: Motor Vehicle Safety
- 1098: Research and Development
- 1099: Other Transportation Issues

**12 - Law and Crime:**
- 1200: General
- 1201: Law Enforcement Agencies
- 1202: White Collar Crime
- 1203: Illegal Drug Production and Trafficking
- 1204: Court Administration
- 1205: Prisons
- 1206: Juvenile Crime
- 1207: Child Abuse
- 1208: Family Issues
- 1209: Criminal and Civil Code
- 1210: Riots and Demonstrations
- 1211: War Crimes
- 1227: Police
- 1299: Other Law and Crime Issues

**13 - Social Welfare:**
- 1300: General
- 1301: Food Stamps, Assistance
- 1302: Elderly Assistance
- 1303: Assistance to the Disabled
- 1304: Volunteer Associations
- 1305: Child Care
- 1308: Parental Leave
- 1399: Other Social Welfare Issues

**14 - Housing:**
- 1400: General
- 1401: Community Development
- 1403: Urban Development
- 1404: Rural Development
- 1405: Rural Housing
- 1406: Low-Income Housing
- 1407: Veterans Housing
- 1408: Homeless
- 1409: Elderly and Disabled Housing
- 1498: Research and Development
- 1499: Other Housing Issues

**15 - Domestic Commerce:**
- 1500: General (Banking, Finance, Commerce)
- 1501: Bank Regulation
- 1502: Securities and Commodities
- 1504: Consumer Protection
- 1505: Sports Regulation
- 1507: Bankruptcy
- 1520: Corporate Management
- 1521: Small Business Issues
- 1522: Copyrights and Patents
- 1523: Domestic Disaster Relief
- 1524: Tourism
- 1525: Consumer Finance
- 1526: Stock and Bond Markets
- 1598: Research and Development
- 1599: Other Commerce Issues

**16 - Defense:**
- 1600: General
- 1602: Security Alliances
- 1603: Intelligence
- 1604: Readiness
- 1605: Nuclear Weapons
- 1606: Arms Control
- 1608: Arms Industry
- 1610: Military Personnel
- 1611: Dependents
- 1612: Contractors
- 1614: Military Aid
- 1615: Civil Defense and Homeland Security
- 1616: National Guard
- 1617: Direct War
- 1619: Relief Effort
- 1620: Reserve Forces
- 1698: Research and Development
- 1699: Other Defense Issues

**17 - Technology:**
- 1700: General
- 1701: Space
- 1704: Commercial Uses
- 1705: Science Transfer
- 1706: Telecom Regulation
- 1707: Broadband Regulation
- 1708: Internet Regulation
- 1798: Research and Development
- 1799: Other Technology Issues

**18 - Foreign Trade:**
- 1800: General
- 1802: Trade Agreements
- 1803: Export Promotion
- 1806: Tariff and Import Restrictions
- 1807: Exchange Rates
- 1899: Other Foreign Trade Issues

**19 - International Affairs:**
- 1900: General
- 1901: Foreign Aid
- 1902: Resources and Exploitation
- 1905: Developing Countries
- 1906: International Finance
- 1910: West Europe
- 1921: Other Specific Countries
- 1925: Human Rights
- 1926: International Organizations
- 1927: Terrorism
- 1929: Diplomats
- 1999: Other International Issues

**20 - Government Operations:**
- 2000: General
- 2001: Intergovernmental Relations
- 2002: Government Efficiency
- 2003: Postal Service
- 2004: Government Employees
- 2005: Appointments
- 2006: Currency and Central Bank
- 2007: Government Procurement
- 2008: Government Property
- 2009: Tax Administration
- 2010: Public Corruption
- 2011: Branch Relations
- 2012: Regulation
- 2013: Political Campaigns
- 2014: Census
- 2015: District of Columbia
- 2030: National Capital
- 2099: Other Government Operations

**21 - Public Lands:**
- 2100: General
- 2101: National Parks
- 2102: Indigenous Affairs
- 2103: Public Lands
- 2104: Water Resources
- 2105: Dependencies and Territories
- 2199: Other Public Lands Issues

**23 - Culture:**
- 2300: General
- 2301: Sports and Recreation
- 2302: Arts and Humanities
- 2399: Other Culture Issues

---

## PARL - Parliament Data Frame

The parliament data frame (PARL) includes variables that contain relevant information related to the parliament primarily as an institution. It aims to cover both stable and time-variant characteristics of national and regional parliaments. The characteristics of parliaments change over time, differ between countries and differ between levels within countries.

A "parliament" thus always entails a combination of a legislative term (e.g. `leg_period`) and either a country (`country_abb`) or a within country region (`region_abb`).

### Summary of PARL Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `parliament_id` | String | [country_abb]\_[level]-[type/reg_abb]\_[year] e.g. NL\_NT-TK\_1946, DE\_NT-BT\_2009, CH\_NT-NR\_1971, CH\_RE-BS\_1997, DE\_RE-BW\_1956 | **parliament identifier**: Unique code for different parliaments, both across countries/levels and over time | COMP |
| `leg_period_start` | Date | 29apr1976, aug1953, 2012 | **legislative period start date**: Variable that captures when a specific legislative period started | COMP |
| `leg_period_end` | Date | 29apr1976, aug1953, 2012 | **legislative period end date**: Variable that captures when a specific legislative period ended | COMP |
| `level` | String | NT, RE | **Location in the multi-level structure**: The organisational level at which the parliament is situated | COMP |
| `country_abb` | String | CH = Switzerland, DE = Germany, NL = Netherlands | **country abbreviation of the parliament** | COMP |
| `region_abb` | String | BB = Brandenburg, ZH = Zürich | **abbreviation of the region**: abbreviation of the name of the region (NL), federal state (DE) or canton (CH) of the parliament | COMP |
| `leg_period` | Integer | 43, 13 | **number of the legislative period** | CWA |
| `assembly_name` | String | Kantonsrat, Grosser Rat, Buergerversammlung, Landesparlament | **name of assembly**: as locally used | COMP |
| `assembly_abb` | String | Bundestag(BT), Tweede Kamer(TK), Kantonsrat(KR), Grosser Rat(GR), Landesparlament(LP) | **two letter abbreviation of the assembly** | COMP |
| `coalition_parties` | String | NL\_VVD\_NT; NL\_PvdA\_NT | Array of party\_id's indicating which part(ie/y) was/were a part of the governing coalition during this parliamentary term | CWA |
| `previous_parliament` | ID | NL\_NT-TK\_1946 | Parliament\_id of the previous parliament | CWA |
| `parliament_size` | Integer | 150, 519, `519;663` | **parliament size**: the number of members seated in the parliament. If the size fluctuates within a term, the successive values are separated by `;` in chronological order | CWA |
| `comment` | String | "size step from 410 to 421 on 01feb1952, when the West Berlin non-voting delegation grew…" | **free-text note**: optional human-readable annotation about the parliament row; typically empty. Used to document the reason and changeover date(s) behind a `;`-separated `parliament_size` | CWA |

### Variable Descriptions

#### parliament_id
**Unique identification code for different parliaments**, both across countries/level and over time. The id consists of:
- Country abbreviation (variable `country_abb`)
- The organizational level of the parliament (see `level`)
- The type (DE: BundesTag(BT) & BundesRat(BR); NL: Tweede Kamer(TK) & Eerste Kamer(EK); CH: NationalRat(NR) & StändeRat(SR))
- The abbreviated region (variable `reg_abb`)
- The start year of the legislative period (see variable `leg_period_start`)

All appended by underscore.

#### leg_period_start
**Legislative period start date**: The first calendar day on which members of this parliament hold a legal mandate to serve. This follows the same mandate-based principle as `res_entry_start` in RESE: the date is determined by constitutional or statutory law, not by when parliament first convened or when members were sworn in. The exact legal basis varies by country and must be documented in the data extraction pipeline (see RESE section for details). Date format: two-digit day, month (first three letters), and four-digit year (e.g., `03jan2025`). Shortened versions are used when day or month are unknown.

#### leg_period_end
**Legislative period end date**: The last calendar day on which members of this parliament hold a legal mandate to serve. Same mandate-based principle and format as `leg_period_start`. The midnight rule applies: `leg_period_end` must be the day before `leg_period_start` of the next parliament, so that consecutive parliaments never share the same date (see the midnight rule under `res_entry_end` in the RESE section).

#### country_abb
**Country abbreviation**: Abbreviated name of the country the parliament (parliamentarian) belongs to (works for). The used abbreviations follow the ISO "ALPHA-2" code. (See: http://www.nationsonline.org/oneworld/country_code_list.htm)

#### region_abb
**Region abbreviation**: Abbreviation of the name of the region (NL), federal state (DE), or canton (CH) of the parliament using two capital letters.

#### assembly_name
**Name of assembly**: String variable that captures the assembly name as commonly used.

#### parliament_size
**Parliament size**: The number of members seated in the parliament — i.e. the count of unique members holding a mandate on a given calendar day (the same population produced by counting seated members under the midnight rule, see `res_entry_end` in the RESE section). This is a *seated-member* count, so it includes members who sit without a full legislative vote where those members occupy seats (e.g. the 22 West Berlin deputies in the German Bundestag, 1953–1990). Such non-voting seat-holders are recorded in RESE with `pf_position = 11` (`political_function` ending `_11`), so they are counted here yet remain distinguishable from full voting members.

**Fluctuating sizes**: when the number of seats changes *within* a single term, the successive values are written as integers separated by `;` in chronological order — the same convention used for committee `seats` (see the COMM section). Each value is the size in force until the next changeover. For example, the 11th German Bundestag (`DE_NT-BT_1987`, 18feb1987–19dec1990) is recorded as `519;663`: 519 seated members until German reunification, then 663 from 03oct1990 when 144 former GDR *Volkskammer* delegates joined the sitting Bundestag. The intra-term changeover date itself is not stored in the `parliament_size` cell; consumers that need a daily size series supply it separately, and the `comment` field (see below) is where that changeover date and its reason are recorded in prose. A single-value size (the common case) is just one integer.

#### comment
**Free-text note**: An optional human-readable annotation about the parliament row. Empty for the vast majority of rows. Its main use so far is to document the reason and the changeover date(s) behind a `;`-separated `parliament_size`, since those dates are not stored in the `parliament_size` cell itself. For example, `DE_NT-BT_1949` carries "size step from 410 to 421 on 01feb1952, when the West Berlin non-voting delegation grew from 8 to 19 members" and `DE_NT-BT_1953` notes "Saarland joined West Germany mid-term with 10 members." The field is descriptive only and is not parsed by any pipeline.

---

## MEME - Membership Episode Data Frame

The membership episode data frame (MEME) includes variables that relate to instances of membership in parties (both national and regional) of an individual. The characteristics of member episodes change over time and differ between individuals. A "member episode" entails a combination of the party in question (i.e. `party_id`), an id specific to the individual politician (`pers_id`), and the id of the party (`part_id`).

### Summary of MEME Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `memep_id` | String | CH\_Abate\_Fabio\_1966\_\_CH\_RL\_NA\_\_2 | **membership episode identification code**: a combination of `pers_id`, `party_id` and an integer to count episodes | COMP |
| `pers_id` | String | CH\_Abate\_Fabio\_1966, DE\_Mueller\_Johann\_1956\_dec | **parliamentarians' individual identification code**: a combination of `country_abb`, `last_name`, `first_name` and `birth_date` | COMP |
| `party_id` | String | DE\_CSU\_RE-BY | **unique party identifier**: a combination of `country_abb`, `party_abb`, level, `reg_abb` | COMP |
| `memep_startdate` | Date | 29apr1976, aug1953, 2012 | **membership episode start date**: Variable that captures when a specific membership episode started | COMP |
| `memep_enddate` | Date | 29apr1976, aug1953, 2012 | **membership episode end date**: Variable that captures when a specific membership episode ended | COMP |
| `memep_type_raw` | String | honorary member | **membership episode type (raw)**: a string variable that describes the kind of party membership the individual in question has. Defaults to "NA" if no information | CWA |
| `meme_entry_raw` | String | ARP (Anti-Revolutionaire Partij), tot juli 1970 | **membership episode entry (raw)**: a string variable that describes the membership in a party. Defaults to "NA" if no information | CWA |
| `meme_entry_source` | String | Dutch PDC data May 2019 extraction | **membership episode entry source**: a string variable that indicates the source of the membership episode. Defaults to "NA" if no information | CWA |
| `meme_date_altered` | Number | 0, 1 | **indicator if altered**: a number variable that indicates if the date in the meme\_entry was altered manually (= 1) or not (= 0) | CWA |

### Variable Descriptions

#### memep_id
**Membership episode identification code**: Identification code that is specific to this data frame. It combines an individual's (`pers_id`) with a specific party (`party_id`). When an MP has multiple episodes in the same party (e.g. she breaks with party 'X' but later becomes a member again) then an index (\_01, \_02 etc.) is used to signify subsequent episodes.

#### pers_id
**Personal identifier**: Unique identification code for different politicians. See POLI for details.

#### party_id
**Unique party identifier**: Party identifier consisting of the country abbreviation (see PARL, variable `country_abb`), the party abbreviation (see `party_abb`), the organizational level and the abbreviated region (see PARL, variables `level`, and `reg_abb`) appended by underscore.

#### memep_startdate
**Membership episode start date**: Contains the start date of the membership episode, in the same format as described in variable `birth_date` (two-digit day, month (first three letters), and four-digit year). The chosen date is either:
- i) the date on which the MP in question became a member of the party;
- ii) the official date mentioned by the parliament as the first day of the respective legislative term on basis of which a party membership episode could be constructed because an MP occurred on this party's election list (see the ELLI data-frame for more details).

#### memep_enddate
**Membership episode end date**: Contains the end date of the membership episode, in the same format as described in variable `birth_date` (two digit day, month (first three letters), and four digit year). The chosen date is either:
- i) the date on which the MP left the party or the party membership of the MP was revoked
- ii) the day the MP joined another party or faction
- iii) the official date mentioned by the parliament as the last day of the respective legislative term following the same logic as for the start date

#### meme_entry_raw
**Membership episode entry (raw)**: Contains all raw information about party membership episodes, e.g. party name, faction name, start and end date of the episode if this information was taken from a qualitative source.

#### meme_entry_source
**Membership episode entry source**: Indicates the source from where the information about the party membership episode comes from.

#### meme_date_altered
**Indicator if altered**: Indicates if the memep\_startdate and/or memep\_enddate were manually changed (and thus do not correspond to the content of meme\_entry\_raw). The number 1 indicates a manual change, while the number 0 indicates no change in the date.

---

## PART - Party Data Frame

The party data frame (PART) includes variables that relate to the parties included in the dataset. The characteristics of parties change over time, between countries, and across regions. A "party" entails a combination of the country (`country_abb`), the party (`party_abb`), the level at which the party operates (`level`), and the region (`reg_abb`).

### Summary of PART Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `party_id` | String | [country\_abb]\_[party\_abb]\_[level]-[reg\_abb] e.g. DE\_CSU\_RE-BY | **unique party identifier**: A variable that uniquely identifies each party. Combination of `country_abb`, `party_abb`, `level`, and `reg_abb`, separated by underscores, with regional abbreviation by hyphen | COMP |
| `party_level` | String | see level coding | **organizational/federal level a party operates on** | COMP |
| `region_abb` | String | BB = Brandenburg, ZH = Zürich | **abbreviation of the region**: abbreviation of the name of the region (NL), federal state (DE) or canton (CH) of the parliament/district | COMP |
| `ancestor_party_id` | String | NL\_ARP\_NA | **ancestor party id**: shows the party id of other party(s) if a party has come about from a merger or after a split from another party | CWA |
| `mother_party_id` | String | NL\_CDA\_NA | **mother party id**: gives the id of (the) mother party (if applicable) | CWA |
| `party_abb` | String | CDA = Dutch Christian Democrats, CDU = German Christian Democrats | **abbreviated party names**: abbreviated party names as used by ParlGov | COMP |
| `party_name` | String | Buendnis 90/ Die Gruenen | **party names**: Full party name in original language | CWA |
| `party_parlgov_id` | Integer | 1591, 1277 | **ParlGov party id**: party id as used by ParlGov | CWA |
| `old_party_abb` | String | KK-CC;CCPS;K-CPS | **Old party id**: a list of party abbreviations that the party has had in the past, separated by semi-colons (only collected for CH) | CWA |
| `old_party_name` | String | Catholic Conservatives;Katholische Konservative;... | **Old party name**: a list of party names that the party has had in the past, separated by semi-colons (only collected for CH) | CWA |

### Variable Descriptions

#### party_id
**Unique party identifier**: Party identifier consisting of the country abbreviation (see PARL, variable `country_abb`), the party abbreviation (see `party_abb`), the organizational level and the abbreviated region (PARL, variables `level`, and `reg_abb`) appended by underscore.

#### party_level
**Organizational/federal level a party operates on**.

#### region_abb
**Region abbreviation**: Abbreviation of the name of the region (NL), federal state (DE), or canton (CH) of the parliament using two capital letters.

#### ancestor_party_id
**Ancestor party id**: Shows the party id of other party(s) if a party has come about from a merger or after a split from another party (if applicable). Can be empty.

#### mother_party_id
**Mother party id**: Gives the id of (the) mother party (if applicable). Signifies relations between parties in the multilevel structure (e.g. but not limited to lower level membership implying higher level membership). Can be empty.

#### party_abb
**Abbreviated party names**: Party names as used by ParlGov, consisting of a party abbreviation appended to a three digit country abbreviation by underscore.

#### party_name
**Party names**: Full party name in original language. The same spelling rules as set out for the variable "last name" apply. Furthermore the rules set out by ParlGov apply. See: http://www.parlgov.org/documentation/codebook

#### party_parlgov_id
**Party id**: Party id as used by ParlGov (see http://www.parlgov.org/documentation/codebook).

#### old_party_abb
**Old party abbreviation**: A(n array of) potential party abbreviation(s) that the party has had in the past, separated by semi-colons.

#### old_party_name
**Old party name**: A(n array of) potential party name(s) that the party has had in the past, separated by semi-colons.

---

## FACT - Faction Data Frame

The faction data frame (FACT) includes variables that relate to groups of parties in assemblies (i.e. 'factions', or 'parliamentary party groups'). The characteristics of factions change over time, across parliaments, and within parliaments.

We define a 'faction' as a collection of individuals in parliament that collectively represent either a party or a collection of parties. Note that this entails both groups made up entirely by members of the same party (like in the Netherlands) as well as party groups (typical in Germany and Switzerland). If factions lose a seat (e.g., one politician breaks with them and joins another party or starts her own faction), then a new line is added to the faction data-frame with the new faction layout and the date of the break as the respective start and end dates of the two episodes.

### Summary of FACT Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `faction_id` | String | DE\_NT\_2009\_\_ DE\_CDU\_NT--DE\_CSU\_NT, CH\_NT-NR\_2009\_\_CH\_BDP\_\_1 | **faction identifier**: combination of the parliament\_id, and the party ids in alphabetical order separated by double hyphens '--'. Changes in the same faction within the same year are denoted by a count after a double underscore '\_\_' | COMP |
| `faction_name` | String | gruene\_fraktion, union | **faction name**: the name of the faction | COMP |
| `party_id('s)` | String | DE\_CDU\_NT; DE\_CSU\_NT | **party identifiers for faction members**: (array of) party identifiers for all factions included in the faction, separated by a semicolon | COMP |
| `parliament_id` | String | [country\_abb]\_[level]-[type/reg\_abb]\_[year] e.g. NL\_NT-TK\_1946 | **parliament identifier**: Unique code for different parliaments | COMP |
| `seats` | Integer | 45, 27 | **Faction seats**: the number of seats that all parties included in the faction have combined in the parliament in question | COMP |
| `faction_composition` | Integer | 29-16, 20-7 | **Faction composition**: the number of seats per party in the faction, separated by hyphen. Order follows the order of abbreviations in `faction_id` | COMP |
| `faction_start` | Date | 29apr1976, aug1953, 2012 | **faction start date**: when a specific faction came into being or changed with regard to any other collected faction variable | COMP |
| `faction_end` | Date | 29apr1976, aug1953, 2012 | **faction end date**: when a specific faction ended or changed with regard to any other collected faction variable | COMP |

### Variable Descriptions

#### faction_id
**Faction identifier**: Combination of the name of the faction (`faction_name`) and `parliament_id`.

#### faction_name
**Name of the faction**: Mentions the full name of the faction (as given by the relevant parliament/in the original language). As for spelling of the names, see rules at `last_name_raw`.

#### party_id('s)
**Unique identifiers for faction parties**: Party identifiers for all parties included in the faction; each party identifier consists of the country abbreviation, the party abbreviation, the organizational level and the abbreviated region, appended by underscore.

#### parliament_id
**Unique identification code for different parliaments**: See PARL for details.

#### seats
**Seats**: The number of seats that the faction has in the respective episode in parliament.

#### faction_composition
**Composition of the faction**: The seats held by parties that constitute the faction, in the same order as the parties contained in `faction_id`.

#### faction_start
**Faction start date**: This variable gives the start date of a faction. These date entries consist of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. In case of missing information on days or month, shortened versions of the date are used. In cases when the sources do not provide episode data, periods are inferred based on snapshots of faction compositions in conjunction with parliamentary episodes.

#### faction_end
**Faction end date**: This variable gives the end date of a faction. These date entries consist of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. In case of missing information on days or month, shortened versions of the date are used. In cases when the sources do not provide episode data, periods are inferred based on snapshots of faction compositions in conjunction with parliamentary episodes.

---

## COMM - Committee Data Frame

The committee data frame (COMM) includes variables that relate to non-partisan specific groups in legislative assemblies (i.e. 'parliamentary committees', 'parliamentary delegations', 'all-party parliamentary groups', and their respective subbodies). These bodies can either have official standing in parliament such as committees and delegations or constitute informal cross-party groups such as all-party parliamentary groups. In either case, the characteristics of these legislative bodies change over time, across parliaments, and within parliaments.

### Summary of COMM Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `comm_id` | PriID | CH\_NT-NR\_1999\_\_CO\|FK--SC\|EDA/WBF | **committee identifier**: combination of parliament\_id(s), committee maintype, abbreviated maintype name, subtype and abbreviated subtype name if applicable | COMP |
| `parliament_id` | ID | NL\_NT-TK\_1946, DE\_NT-BT\_2009 | **parliament identifier**: Unique code for different parliaments | COMP |
| `comm_name` | String | Delegation bei der parlamentarischen Versammlung der OSZE, Geschäftsprüfungskommission | **committee name**: name of the committee, delegation, all-party parliamentary group, or subcommittee | COMP |
| `comm_maintype` | String | CO, DL, FA, AG | **type of committee**: Body maintype is either parliamentary committee (CO), parliamentary delegation (DL), faction (FA) or all-party parliamentary group (AG) | COMP |
| `comm_subtype` | String | SC, SD, SA | **subtype of committee**: Body subtype refers to either parliamentary subcommittee (SC), parliamentary subdelegation (SD), or all-party parliamentary subgroup (SA) | CWA |
| `comm_maintype_abb` | String | FK, FinDel, Drogenpolitik | **main committee abbreviation**: Abbreviation of main body as used by officials. If none available, a shortened version of comm\_name is used | COMP |
| `comm_subtype_abb` | String | EDA/WBF, AgrRisikorep, D | **subcommittee abbreviation**: Abbreviation of subbody as used by officials | CWA |
| `seats` | Integer | 45, 27;28;29 | **committee seats**: the number of seats that all MPs included in the respective body have combined during the respective parliament | CWA |
| `comm_start` | Date | 29apr1976, aug1953, 2012 | **committee start date**: when a specific committee, delegation, or all-party parliamentary group came into being or changed with regard to any other collected COMM variable | COMP |
| `comm_end` | Date | 29apr1976, aug1953, 2012 | **committee end date**: when a specific committee, delegation, or all-party parliamentary group ended or changed with regard to any other collected COMM variable | COMP |

### Variable Descriptions

#### comm_id
**Committee identifier**: Combination of the parliament\_id(s), the committee maintype, the abbreviated maintype name, as well as the subtype and the abbreviated subtype name if applicable.

Format: `[parliament_id(s)]__[comm_maintype]|[comm_maintype_abb]--[comm_subtype]|[comm_subtype_abb]`

Multiple parliament\_id as well as the last parliament\_id and the maintype are separated by double underscores '\_\_'. Maintype/subtype and abbreviated maintype/subtype name are separated by a vertical bar '|'. In case a subtype is specified, it is separated from the abbreviated maintype name by double hyphens '--'.

#### parliament_id
**Parliament identifier**: Unique identification code for different parliaments. See PARL for details.

#### comm_name
**Committee name**: Official long version of the name of the committee, delegation, all-party parliamentary group, or subcommittee. Exception: In case of faction, "Leadership body" or "Working Groups".

#### comm_maintype
**Type of committee**: Main type refers to either parliamentary committee (CO), parliamentary delegation (DL), faction (FA) or all-party parliamentary group (AG). Main type uses two-letter abbreviations.

#### comm_subtype
**Subtype of committee**: Subtype refers to either parliamentary subcommittee (SC), parliamentary subdelegation (SD), or all-party parliamentary subgroup (SA). Subtype uses two-letter abbreviations.

#### comm_maintype_abb
**Main committee abbreviation**: Abbreviation of main type as used by officials. If none is available, a shortened version of comm\_name is used instead.

#### comm_subtype_abb
**Subcommittee abbreviation**: Abbreviation of subtype as used by officials. If none is available, a shortened version of comm\_name is used instead.

#### seats
**Committee seats**: The number of seats that all MPs included in the respective body have combined during the respective parliament. If the number of seats fluctuates during the same term, the different seat numbers are separated by ';'.

#### comm_start
**Committee start date**: Variable that captures when a specific committee, delegation, or all-party parliamentary group came into being or changed with regard to any other collected COMM variable. These date entries consist of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. In case of missing information on days or month, shortened versions of the date are used. In cases when the sources do not provide episode data, periods are inferred based on snapshots of faction compositions in conjunction with parliamentary episodes.

#### comm_end
**Committee end date**: Variable that captures when a specific committee, delegation, or all-party parliamentary group ended or changed with regard to any other collected COMM variable. These date entries consist of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. In case of missing information on days or month, shortened versions of the date are used. In cases when the sources do not provide episode data, periods are inferred based on snapshots of faction compositions in conjunction with parliamentary episodes.

---

## ELEC - Election Data Frame

The election data frame (ELEC) includes information on elections: for example when did the election take place? Which parliament was elected? The data frame captures each election (i.e. also the second round of an election, by-elections and replacement-elections) on the level of the district it is executed on (i.e. on the level of the election lists).

### Summary of ELEC Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `election_id` | PriID | [district\_id]\_[election\_date], e.g. DE\_NT-BT\_2017\_\_Hessen\_\_24sep2017 | **unique election identifier**: Unique code used to identify an election, consisting of the district\_id and the election\_date | COMP |
| `parliament_id` | String | NL\_NT-TK\_1946, DE\_NT-BT\_2009, CH\_NT-NR\_1971 | **parliament identifier**: Unique code for the parliament the election relates to/elects | COMP |
| `district_id` | ID | [parliament\_id]\_\_[constituency\_name], e.g. CH\_NT\_1971\_\_Zuerich | **unique district identifier**: identification code of the district, as used in the other data frames, identifying the district the electoral list belongs to | COMP |
| `election_date` | Date | 18oct1987 | **date of election** | COMP |
| `election_type` | String | regular, early | **election type**: Variable indicating if the election was a normal or an early/snap election due to special circumstance (like a crisis and constitutional change) | CWA |
| `election_mode` | String | popular, by\_other\_parliament, town\_square | **election mode**: Mode of election | CWA |
| `parliament_id_of_electing_parliament` | ID | DE\_RE-BW\_1956 | **electing parliament**: Parliament ID if election is by another parliament | COMP |
| `district_votes_total_source` | Numeric | 1250 | **total number of valid votes**: cast within a given district and period | CWA |

### Variable Descriptions

#### election_id
**Unique election identifier**: Unique identification code for different elections. The id consists of the district\_id and the election\_date.

#### parliament_id
**Parliament identifier**: Unique code for the parliament the election relates to/elects. See PARL for details.

#### district_id
**Unique district identifier**: Identification code of the district, as used in the other data frames, identifying the district the electoral list belongs to.

#### election_date
**Date of election**: Contains the official date(s) the respective parliament was elected. Uses the PCC date format: two-digit day, three-letter lowercase month abbreviation, and four-digit year (e.g. `18oct1987`). If only the month and year are known, the day may be omitted (e.g. `sep2021`). If only the year is known, use the year alone (e.g. `2021`).

#### election_type
**Election type**: Variable indicating if the election was a normal or an early/snap election due to special circumstance (like a crisis and constitutional change).

#### election_mode
**Election mode**: Mode of election:
- popular = Direct popular election
- by\_other\_parliament = Elected by another parliament
- town\_square = Town square assembly election

#### parliament_id_of_electing_parliament
**Electing parliament identifier**: Parliament ID of the parliament that conducted the election (relevant when election\_mode is by\_other\_parliament).

#### district_votes_total_source
**Total number of valid votes**: A list got within a given district and period according to a given data source (which is mentioned in the end of the variable name).

---

## ELLI - Electoral List Data Frame

The electoral list data frame (ELLI) includes information on the individual electoral lists, which might originate from one or several parties. All variables in this data frame are on the level of the electoral lists and vary per parliamentary term: TV\_P (start/end `parliament_id`). Each list is identified by a combination of the parliament id (`parliament_id`), the district id (`district_id`), and the name of the list (`list_name`). An example of this data-frame can be downloaded at: [http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx](http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx)

### Summary of ELLI Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `list_id` | PriID | [parliament\_id]\_\_[district\_id]\_\_[list\_name], e.g. DE\_NT\_2009\_\_CH\_NT\_1971\_\_Zuerich\_\_Landesliste-Sozialdemokratische-Partei-Deutschlands | **unique list identifier**: consisting of the parliament id, the list name and the district id | COMP |
| `list_name` | String | Sozialdemokratische-und-Gewerkschaftliche-Liste, NA\_ZH\_1 | **name of the electoral list**: mentions the full name of the electoral list (as given by the relevant electoral office) | COMP |
| `parliament_id` | ID | [country\_abb]\_[level]-[type/reg\_abb]\_[year] | **parliament identifier**: Unique code for different parliaments | COMP |
| `party_id` | ID | [country\_abb]\_[party\_abb]\_[level]-[reg\_abb], e.g. DE\_CSU\_RE-BY | **unique party identifier** | COMP |
| `district_id` | ID | [parliament\_id]\_\_[constituency\_name], e.g. CH\_NT\_1971\_\_Zuerich | **unique district identifier**: identification code of the district | COMP |
| `list_level` | String | DE\_BY, CH\_GR | **level a list is on**: the variable specifies the level (national or subnational) a list is on and gives the identity of the level | COMP |
| `list_number` | Numeric | 1, 13 | **number of electoral list**: identifying number of consecutive number of the list as mentioned in the original data source | CWA |
| `list_party_id` | String (of IDs) | DE\_CSU\_RE-BY | **list party id(s)**: id of the party(s) that constructed the list. Can be identical with `party_id`. Several party ids can exist if the list is a collaboration of several parties | COMP |
| `list_length` | Numeric | 1:99 | **total number of spots on the electoral list** | CWA |
| `list_connections` | String (of IDs) | CH\_NA\_Sozialdemokratische-und-Gewerkschaftliche-Liste\_36 | **list connections**: Id(s) of list(s) an electoral list is connected with | CWA |
| `list_votes_total_source` | Numeric | 1250 | **total number of valid votes a list got** | CWA |
| `list_type` | String | party, youth, party\_female, other\_female | **type of list**: the variable characterizes the electoral list | CWA |

### Variable Descriptions

#### list_id
**Unique list identifier**: Electoral list identifier consisting of the parliament id (see variable `parliament_id`), the list name (see `list_name`), and the identity of the list level (see `list_level`) connected by underscores.

#### list_name
**Name of the electoral list**: Mentions the full name of the electoral list (as given by the relevant electoral office). As for spelling of the names, see rules at `last_name`. Blank spaces between the words are exchanged by hyphens. When a list\_name is unknown NA\_[reg\_abb]\_[integer] is used. For CH only: In case the MP did not run on a list, we use the format `NA_[kanton_abb]_index`, where index starts at 1 and increments by 1 with every unnamed list for the Kanton in the order in which they are listed in the *Bundesblatt*.

#### parliament_id
**Parliament identifier**: Unique identification code for different parliaments. See PARL for details.

#### party_id
**Unique party identifier**: Party identifier. See PART for details.

#### district_id
**Unique district identifier**: Identification code of the district, as used in the other data frames, identifying the district the electoral list belongs to.

#### list_level
**Level the list is on**: The variable consists of the country abbreviation (two letters) and an abbreviation of the sub-national unit (region/state/or sub- and inter-regional units in the case of the NL, again two letter abbreviations) appended to each other by underscore. The variable specifies the level (national or subnational) a list is on (a national party list would have a country abbreviation but no sub-national/regional abbreviation) and gives the identity of the level (e.g. DE\_XX = German federal level list, or DE\_BY = state based list in the German state of Bavaria).

#### list_number
**Number of electoral list**: Identifying number of consecutive number of the list as mentioned in the original data source (usually the national bureau for elections). Can be an array (e.g. 1;2;3) if the same election lists (same politicians in same order) was used across different electoral districts (this for example often happens in the Netherlands).

#### list_party_id
**List party id(s)**: Id of the party(s) that constructed the list. Can be identical with the variable `party_id`. Several party ids can exist in this variable, if the list is a collaboration of several parties.

#### list_length
**Total number of spots on the electoral list**.

#### list_connections
**List connections**: This variable is NL-specific and mentions the list\_id(s) of other lists that the respective list is connected with, which means that these lists will get the votes that the respective list can not use (e.g. because it did not make the quorum).

#### list_votes_total_source
**Total number of valid votes a list got** according to a specific source.

#### list_type
**Type of list**: The variable mentions the list-type. The values of this variable provide information about who composed the list (a political party or some other group) and who is typically on the list (e.g. only females). In case the information is not known, the variable takes the value "NA".

Possible codes:
- party = list of political party
- youth = youth party list
- party\_female / other\_female = female-only party/other list
- party\_male / other\_male = male-only party/other list
- multi\_party / multi\_other = multi party/other groups list
- other = list of non-party groupings
- NA

---

## ELEN - Electoral List Entry Data Frame

The electoral list entry data frame (ELEN) includes information on the candidacy of individual politicians (on lists). All variables in this data frame are on the level of the individual politician (see `pers_id`) and vary per election (see `parliament_id`) and election district (see `list_id`). Each election list entry is identified by a combination of the electoral list id (`list_id`), and the ID identifying the person (`pers_id`). An example of this data-frame can be downloaded at: [http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx](http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx)

### Summary of ELEN Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `elec_entry_id` | PriID | [list\_id]\_\_[pers\_id], e.g. DE\_NT\_2009\_\_DE\_NT\_2009\_\_Saarland\_\_Landesliste-Sozialdemokratische-Partei-Deutschlands\_\_DE\_Funk\_Alexander\_1974 | **unique electoral list entry identifier**: consisting of the electoral list id and the personal id | COMP |
| `list_id` | ID | [parliament\_id]\_\_[district\_id]\_\_[list\_name] | **unique list identifier**: consisting of the parliament id, the list name and the list level | COMP |
| `pers_id` | ID | CH\_Abate\_Fabio\_1966, DE\_Mueller\_Johann\_1956\_dec | **parliamentarians individual identification code**: a combination of `country_abb`, `last_name`, `first_name` and `birth_date` | COMP |
| `listplace` | Numeric | 1:99 | **listplace the person ran on** | COMP |
| `elected_[source]` | Binary | 0=not elected, 1=elected | **elected**: binary variable that specifies if a list position or other type of candidature of a candidate was successful (elected) according to a specific source | CWA |
| `candidature_type` | String | L=list, D=district, LD=list and district | **type of candidature of a person**: only relevant for DE | CWA |
| `seat_type` | Numeric | 1=direct mandate, 2=list without succession, 3=succession via list, 11=byelection, 12=Volkskammer GDR, 13=list | **type of seat/mandate in detail**: only relevant for DE | CWA |
| `district_id` | ID | see ELDI | **district identifier**: Primary ID in ELDI, also included here because candidates might run from subdistricts but be part of a larger primary district | CWA |
| `candidate_votes` | Numeric | 1250 | **total number of votes a candidate got in the first (possibly the only) round of elections** | CWA |
| `candidate_votes2` | Numeric | 1250 | **total number of votes a candidate got in the second round of elections** (if applicable) | CWA |

### Variable Descriptions

#### elec_entry_id
**Unique electoral list entry identifier**: Consisting of the electoral list id (`list_id`), consisting of [parliament\_id]\_[district\_id]\_[list\_name], and the personal id (`pers_id`), which is a combination of `country_abb`, the `last_name`, the `first_name` and the `birth_date`, connected by underscores. In case the same person appears more than once on the same electoral list, a consecutive number is appended by underscore.

#### list_id
**Unique list identifier**: Electoral list identifier consisting of the parliament id, the list name, and the identity of the list level connected by underscores.

#### pers_id
**Personal identifier**: Unique identification code for different politicians. See POLI for details.

#### listplace
**Listplace**: Variable is a positive number that indicates the position on the electoral list a person ran on and/or was elected on.

#### elected_[source]
**Elected**: Binary variable that specifies whether, according to a specific source (mentioned in [external data source]), the federal statistical bureau for example, a list position or other type of candidature of a candidate was successful (elected) or not.

#### candidature_type
**Candidature type**: Variable is mainly important for German candidate selection and mentions the type of candidature (list, district, or both) of a candidate.
- L = list
- D = district
- LD = list and district

#### seat_type
**Seat type**: Variable is mainly important for (elected) parliamentarians from mixed systems like Germany. It specifies the seat type or mandate of a parliamentarian:
- 1 = direct mandate (based on a district mandate)
- 2 = part of the parliament due to a successful list candidacy without succession
- 3 = succeeded another parliamentarian via the list
- 11 = entered the parliament due to a byelection
- 12 = part of the GDR Volkskammer
- 13 = part of the parliament due to a successful list candidacy

#### district_id
**District identifier**: Primary ID in ELDI, also included here because candidates might run from subdistricts but be part of a larger primary district. Also included to make DE data easier to understand.

#### candidate_votes
**Candidate votes**: Numeric variable mentioning the total number of (valid) votes a candidate/list position got in the first round (which may be the only round) of (national parliament) elections.

#### candidate_votes2
**Candidate votes (second round)**: Numeric variable mentioning the total number of (valid) votes a candidate/list position got in the second round of (national parliament) elections.

---

## ELDI - Electoral District Data Frame

The electoral district data frame (ELDI) includes information on the organizational units (districts) the elections are executed in. For example, the name of a given district or size of it. Variables in this data frame are on the level of the districts and (are allowed to) vary per election (see `parliament_id`). Each electoral district (constituency) is identified by a combination of the parliament (`parliament_id`) and the constituency name (`constituency_name`). An example of this data-frame can be downloaded at: [http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx](http://parliamentarycareersincomparison.org/wp-content/uploads/2017/03/PCC-example-data_v311.xlsx)

### Summary of ELDI Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `district_id` | PriID | [parliament\_id]\_\_[constituency\_name], e.g. CH\_NT-NR\_1971\_\_Zuerich | **unique district identifier**: identification code as used in the other data frames | COMP |
| `parliament_id` | ID | NL\_NT\_1946, DE\_NT\_2009, CH\_NT\_1971, CH\_RE-BS\_1997, DE\_RE-BW\_1956 | **parliament identifier**: Unique code for different parliaments, both across countries/levels and over time | COMP |
| `country_abb` | String | CH=Switzerland, DE=Germany, NL=Netherlands | **country abbreviation of the parliament** | COMP |
| `region_abb` | String | BB=Brandenburg, ZH=Zürich | **abbreviation of the region**: abbreviation of the name of the region (NL), federal state (DE) or canton (CH) of the parliament/district | COMP |
| `constituency_name` | String | Zuerich, Stuttgart | **name of the constituency** | COMP |
| `constituency_code_CLEA` | Numeric | 001-900, 901-999 | **identifying code of the constituency**: as assigned by CLEA | CWA |
| `constituency_name_CLEA` | Numeric | 001-900, 901-999 | **name of the constituency**: as assigned by CLEA | CWA |
| `dist_magnitude` | Numeric | positive number, -992=Uncontested election, -994=Suspended election | **district magnitude**: measured by the number of seats allocated in a given district | CWA |

### Variable Descriptions

#### district_id
**Unique district identifier**: Unique identification code for electoral districts consisting of the parliament id (variable `parliament_id`), and the name of the constituency (variable `constituency_name`) appended by underscore.

#### parliament_id
**Parliament identifier**: Unique identification code for different parliaments. See PARL for details.

#### country_abb
**Country abbreviation of the parliament**: Abbreviated name of the country the parliament/district belongs to. The used abbreviations follow the ISO "ALPHA-2" code. (See: http://www.nationsonline.org/oneworld/country_code_list.htm)

#### region_abb
**Abbreviation region**: Abbreviation of the name of the region (NL), federal state (DE), or canton (CH) of the parliament using two capital letters. For CH based on: http://swiss-government-politics.all-about-switzerland.info/swiss-federal-states-cantons.html

#### district_aliases
**District aliases**: (Array of) potential aliases the district is also known under. E.g. 'kies kring numbers' for NL.

#### constituency_name
**Name of the constituency**: Mentions the full name of the electoral constituency (as given by the relevant electoral office/in the original language). As for spelling of the names, see rules at `last_name`. Called 'CST' in CLEA. Dots are removed. Remaining spaces are replaced by hyphens ('-').

#### constituency_code_CLEA
**Identifying code of the constituency**: As assigned by the Constituency Elections Archive (CLEA) (see http://www.electiondataarchive.org/about.html). Note: this code is unique only to constituency and election (hence, the same district can have different codes at different elections). CLEA codes exist only for some national elections.

#### dist_magnitude
**District magnitude**: Measured by the number of seats allocated in a given district. The number of seats is expressed in a positive number, the following other codes are possible:
- -992 = Uncontested election (i.e. a single candidate contested the election)
- -994 = Suspended election

(See also http://www.electiondataarchive.org/about.html)

---

## ORGS - Organisations Data Frame

The organisations data frame (ORGS) captures information on the level of organisations that parliamentarians are members of at some stage of their career. In most instances, these organisations are interest groups as data on parties (PART), factions (FACT), and parliaments (PARL) are collected in other data frames. Responsible for the module and the data contained is: OH.

Some of the data presented here are drawn from secondary sources. For more extensive discussions of these sources, readers are therefore referred to the codebooks and studies for which these data have been collected and coded for in the first place.

### Summary of ORGS Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `org_id` | ID | [country\_abb]\_[12 digit code], e.g. CH\_H8KkcewN6fGv | **unique organisation identifier**: identification code to link organisations mentioned in RESE | COMP |
| `org_name` | String | Cranex AG, Opfikon; Crédit Suisse / Schweizerische Kreditanstalt (SKA) | **name of organisation**: Name and synonyms (previously used names, names in other languages) used for an organisation | COMP |
| `country_abb` | String | CH=Switzerland, DE=Germany, NL=Netherlands | **country abbreviation of the organisation's headquarters location** | COMP |
| `legal_form` | String | AG, AG; Gen., KollG; EG | **legal form**: Legal form of the organisation as given in the source. Multiple legal forms are separated by semicolons | CWA |
| `polactive_start_date` | Date | 29apr1976, aug1953, 2012 | **political activity start date**: when an organisation was known to be politically active for the first time | CWA |
| `polactive_end_date` | Date | 29apr1976, aug1953, 2012 | **political activity end date**: when an organisation was known to be politically active for the last time | CWA |
| `address_raw` | String | Musterstr. 3, Basel; Postfach, Beispielstadt | **raw address**: Address of the organisation | CWA |
| `GAVA_assoc_id` | Numeric | 1, 329, 4605 | **Gava association id**: Id assigned to organisations by Gava et al. in the DATABASE ON INTEREST GROUPS IN THE SWISS PARLIAMENT | CWA |
| `GAVA_assoc_name` | String | Pro Natura Basel, Sportstiftung Thurgau | **Gava association name**: Name of organisations as used by Gava et al. | CWA |
| `GAVA_assoc_aggregate_name` | String | Pro Natura, Swiss Life | **Gava aggregate association name**: Umbrella names of organisations as used by Gava et al. | CWA |
| `GAVA_assoc_legal_form` | Numeric | 11, 30, 50 | **Gava legal form**: Legal form of organisations as used by Gava et al. | CWA |
| `GAVA_assoc_general` | String | Association, Commission, Societe | **Gava general form of association**: Form of organisations as used by Gava et al. | CWA |
| `GAVA_assoc_ig_type_name` | String | Business groups, Identity groups, Unions | **Gava interest group category**: Categories of interest groups adapted from the INTERARENA project | CWA |
| `GAVA_assoc_ig_code` | Numeric | 26, 63, 89 | **Gava interest group category code**: Category codes adapted from the INTERARENA project | CWA |
| `GAVA_level` | Numeric | 1, 2, 4 | **Gava level of organisation**: Level codes ranging from local to international | CWA |
| `GAVA_category` | String | Local, Regional/Cantonal, International | **Gava category of level**: Level categories ranging from local to international | CWA |
| `GAVA_topic` | Numeric | 6, 10, 12 | **Gava topic**: Policy area in which an organisation is active in, based on the CAP coding scheme | CWA |
| `GAVA_topic_business` | Numeric | 1500, 1505, 1564 | **Gava topic business**: For organisations in category General Business (1500), more detailed information on the area of business | CWA |
| `NCCR_nqid` | Numeric | 46, 827, 2608 | **NCCR interest group id**: Id of interest groups from the project NCCR IP 8: MEDIATIZATION OF POLITICAL INTEREST GROUPS by Jarren et al. | CWA |
| `NCCR_A4Organisation` | String | Alpen-Initiative, Castagna Zürich, FachFrauen Umwelt | **NCCR interest group name**: Name of interest groups from the NCCR project | CWA |
| `GK_interest_group` | String | Verein Al Forno, Semaine du Gout, Swissgas AG | **Giger & Klüver IG name**: Name of interest group from Giger and Klüver's project on SWISS MPS AND THEIR INTEREST GROUP AFFILIATION | CWA |
| `GK_canton_ig_raw` | String | LU, Halle (BRD), ZH | **Giger & Klüver canton of IG location**: Raw (uncleaned) string of the canton in which an interest group is headquartered | CWA |
| `GK_type` | String | culture, ngo, prof | **Giger & Klüver IG type**: Type of interest group | CWA |
| `GK_policy_code` | String | 7, 13, 28 | **Giger & Klüver IG policy code**: Policy area of interest group based on the CAP coding scheme | CWA |

### Variable Descriptions

**Note on variables**: The detailed description of variables, their ranges or categories are only provided for original variables presented in this codebook. For variables from secondary sources that are mentioned in the above table, readers are referred to the original codebooks and studies. The variables in question all start with a capitalised indicator: GAVA, NCCR, and GK.

#### org_id
**Unique organisation identifier**: Unique identification code for organisations consisting of the country abbreviation (variable `country_abb`), and a 12 digit combination of letters, numbers, and special characters. The 12 digits code is created in Excel with the VBA hash function BASE64SHA1.

#### org_name
**Organisation name**: Name(s) of the organisation as used over time in different languages. The string captures exclusively names that refer to exactly the same organisation (Organisations that split or merged are not added to the same organisation). Alternative names are separated by slashes. If available, the place where an organisation is headquartered is given at the end separated by a comma: [name\_1]/[name\_2]/[name\_n], [place of headquarters].

#### country_abb
**Country abbreviation of the parliament**: Abbreviated name of the country the parliament/district belongs to. The used abbreviations follow the ISO "ALPHA-2" code. (See: http://www.nationsonline.org/oneworld/country_code_list.htm)

#### legal_form
**Legal form**: The legal form of organisations as indicated in the data source. The Register of Interest Ties prepared by the Swiss Parliamentary Services for instance distinguishes between 15 different types of legal forms. The current list of abbreviations and their meaning can be looked up online: https://www.parlament.ch/centers/documents/de/interessen-nr.pdf

#### polactive_start_date
**First known political activity**: Captures the time when an organisation was first politically active e.g. had first ties to a parliamentarian. The date consists of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. If only the month is known the days are dropped and if only the years are known the day and month letters are dropped.

#### polactive_end_date
**Last known political activity**: Captures the time when an organisation was last politically active e.g. had last ties to a parliamentarian. The date consists of the two-digit day, the month (first three letters, small, of the English name of the month) and the four-digit year. If only the month is known the days are dropped and if only the years are known the day and month letters are dropped.

#### address_raw
**Raw address**: Contains the raw address of the organisation's headquarters. If multiple addresses are known for the organisation, the time period for which the address is valid is added in brackets after the address e.g. [[2015-2017]]. Multiple addresses are separated by the pipe symbol "|".

### Secondary Source Variables

#### GAVA Variables
Variables prefixed with `GAVA_` come from Gava et al.'s DATABASE ON INTEREST GROUPS IN THE SWISS PARLIAMENT. Categories are adapted from the INTERARENA project.

#### NCCR Variables
Variables prefixed with `NCCR_` come from the project NCCR IP 8: MEDIATIZATION OF POLITICAL INTEREST GROUPS by Jarren et al.

#### GK Variables
Variables prefixed with `GK_` come from Giger and Klüver's project on SWISS MPS AND THEIR INTEREST GROUP AFFILIATION.

---

## QUOT - Quota Module

This is a PCC data module on (gender) quota information (at the level of the national parties, QUOT). The quota data is appended to and compatible with the FACT data frame, however the data is strictly speaking not part of the PCC data. Responsible for the module and the data contained are: EF and TTZ.

### Summary of Quota Variables

| NAME | TYPE | VALUES/EXAMPLE | SHORT DESCRIPTION | EFFORT |
|------|------|----------------|-------------------|--------|
| `faction_id` | String | DE\_NT\_2009--DE\_CDU\_NT | **faction identifier**: combination of the parliament\_id and the party id | COMP |
| `quota_bin` | Binary | 0=no gender quota, 1=gender quota | **quota dummy**: indicates whether the party has any ('soft' or 'hard') gender quota or not | CWA |
| `quota_percentage` | Numeric | 0:100 | **quota value**: mentions the percentage (of candidates or posts) that the quota specifies to be female at least | CWA |
| `quota_zipper` | Binary | 0=no zipper quota, 1=zipper quota | **zipper quota dummy**: indicates whether the party reserves alternating seats to different sexes | CWA |
| `quota_soft` | Binary | 0='hard' quota, 1='soft' quota | **soft gender quota**: shows if a gender quota is 'soft'/informal/non-binding in wording or not | CWA |
| `quota_execution` | Binary | 0=quota not implemented, 1=quota implemented | **quota implementation**: indicates whether the party actually implemented the quota or not | CWA |

### Variable Descriptions

#### faction_id
**Faction identifier**: Combination of the `parliament_id` and the name of the party (`faction_id`). Identifies the party-parliament dyad for which the quota of the national party applies. In case the quota was introduced during a parliamentary term, the quota information is recorded for the next parliamentary term/election.

#### quota_bin
**Quota dummy**: Indicates if a party/fraction in or for a certain parliament has any gender quota ('soft' or 'hard'):
- 0 = No gender quota
- 1 = Has gender quota

Gender quotas are defined as any ratio/share of females to males (greater than zero) with regard to electoral candidates, list positions, or elected MPs (party offices and delegates for party conventions are not considered) mentioned in an official party document (party statute, party convention decision, minutes of party convention) as officially decided by the party.

#### quota_percentage
**Quota value**: Numeric variable mentioning the highest percentage of females (candidates or positions) that the quota prescribes explicitly. When the quota text prescribes "at least X percent", X is the recorded value. The variable is zero if the party has no gender quota. When the wording 'equal' is used, this is coded as a 50% quota.

#### quota_zipper
**Zipper quota dummy**: Indicates if the respective party has a gender quota that reserves alternating positions on electoral lists for male and female candidates (zipper system):
- 0 = No zipper quota
- 1 = Has zipper quota

A zipper system can also leave certain positions open to both sexes (e.g., SPD in Germany prescribes alternating sexes but leaves every fifth position open for either sex).

#### quota_soft
**Soft gender quota**: Shows if a gender quota is 'soft'/informal/non-binding in wording:
- 0 = 'Hard' quota (binding)
- 1 = 'Soft' quota (non-binding)

For 'soft' quotas, the party statutes say "ideally there should be..." or "there should be..." a certain share of females (or similar expression).

#### quota_execution
**Quota implementation**: Indicates whether the gender quota was actually implemented by the party in the respective legislative election/period:
- 0 = Quota not implemented
- 1 = Quota implemented

---

## Appendices

### Alternative IDs (ALID)

Different data sources offer different challenges and possibilities for ID creation. When the standard PCC ID cannot be created directly, alternative IDs may be used. For all alternative IDs, a correspondence table is created to map them to PCC IDs.

| Alternative Value(s) | ID Structure | Examples |
|---------------------|--------------|----------|
| Region | Country_LastName_FirstName_Region | CH_Allenspach_Heinz_ZH, DE_Doerflinger_Thomas_BW |
| Party | Country_LastName_FirstName_Party | CH_Allenspach_Heinz_FDP\|PRD, DE_Doerflinger_Thomas_CDU, NL_Elias_Ton_VVD |
| Year of Parliament Entry | Country_LastName_FirstName_EntryYear | CH_Allenspach_Heinz_E1979, DE_Doerflinger_Thomas_E1998, NL_Elias_Ton_E2008 |

### Regional Abbreviations

#### Switzerland (CH)

| Abbreviation | Canton |
|-------------|--------|
| AG | Aargau |
| AI | Appenzell Innerrhoden |
| AR | Appenzell Ausserrhoden |
| BS | Basel-Stadt |
| BL | Basel-Landschaft |
| BE | Bern |
| FR | Fribourg |
| GE | Geneva |
| GL | Glarus |
| GR | Graubünden |
| JU | Jura |
| LU | Lucerne |
| NE | Neuchâtel |
| NW | Nidwalden |
| OW | Obwalden |
| SH | Schaffhausen |
| SZ | Schwyz |
| SO | Solothurn |
| SG | St. Gallen |
| TG | Thurgau |
| TI | Ticino |
| UR | Uri |
| VS | Valais |
| VD | Vaud |
| ZG | Zug |
| ZH | Zürich |

#### Germany (DE)

| Abbreviation | State (Bundesland) |
|-------------|-------------------|
| BW | Baden-Württemberg |
| BY | Bavaria |
| BE | Berlin |
| BB | Brandenburg |
| HB | Bremen |
| HH | Hamburg |
| HE | Hesse |
| NI | Lower Saxony |
| MV | Mecklenburg-Vorpommern |
| NW | North Rhine-Westphalia |
| RP | Rhineland-Palatinate |
| SL | Saarland |
| SN | Saxony |
| ST | Saxony-Anhalt |
| SH | Schleswig-Holstein |
| TH | Thuringia |

#### Netherlands (NL)

| Abbreviation | Province |
|-------------|----------|
| DR | Drenthe |
| FL | Flevoland |
| FR | Friesland |
| GD | Gelderland |
| GR | Groningen |
| LB | Limburg |
| NB | Noord-Brabant |
| NH | Noord-Holland |
| OV | Overijssel |
| UT | Utrecht |
| ZH | Zuid-Holland |
| ZL | Zeeland |
| BO | Openbare lichamen Bonaire, Sint Eustatius en Saba |

---

*This codebook documents the PCC (Parliamentary Careers in Comparison) database structure and coding conventions.*
