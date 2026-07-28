# The Data Landscape: Federal vs. Local Politics Research

**How to read this table.** Each row is a general question researchers might ask about politics regardless of the level of government representation. The federal column cites a canonical source at the federal level, the local status is a code (see below) on the opportunity for data collection at local level, and the local sources describes any existing data (and its coverage).

For local status, we apply the following codes (in hopes of encouraging future work):

- **Fragmented** rows present an opportunity for research that requires aggregating existing sources with the help of LLMs: most of the records necessary for this work are public, but require diverse means of discovering, scraping, etc. (campaign finance, public comment, municipal codes, local news).
- **Absent** rows are opportunities for more innovative data collection. These represent the highest-effort, highest-reward projects (candidate identity, roll calls / voting).
- **Partial** rows are access and licensing restricted. This doesn't mean the data can't be obtained but likely requires significant effort and low likelihood of institutional collaboration because of potential for commercialization (e.g. budgets, institutional surveys, procurement history).
- **Emerging** rows are places for building upon or reusing existing data sources — many of these are research projects and therefore require some validation or updating in order to be immediately useful (e.g. LocalView, the Local Elections Database, MRP estimates).

## A. People

| Question | Federal standard | Local status | Local sources & coverage |
|---|---|---|---|
| Who holds office? | [Biographical Directory of Congress](https://bioguide.congress.gov/) (1774–); [Voteview](https://voteview.com/) member files (1789–) | **Absent** | [Ballotpedia](https://ballotpedia.org/) (systematic only for the largest ~100 cities and their school districts); Power Almanac (commercial directory); ICMA Municipal Year Book (paywalled). The Census Bureau last enumerated individual local elected officials in the **1992** Census of Governments (~493,000 officials). |
| Who runs for office? | [FEC candidate master files](https://www.fec.gov/data/browse-data/?tab=bulk-data) (1980–) | **Absent** | [CEDA — California Elections Data Archive](https://www.csus.edu/center/institute-social-research/ceda.html) (all CA local contests, 1995–); Local Elections in America Project (LEAP, Rice; larger cities); Our Campaigns (crowdsourced). |

## B. Elections & Money

| Question | Federal standard | Local status | Local sources & coverage |
|---|---|---|---|
| Who wins, by how much? | [MIT Election Data + Science Lab](https://electionlab.mit.edu/data) (federal returns, 1976–) | **Emerging** | [American Local Government Elections Database](https://www.nature.com/articles/s41597-023-02792-x) (de Benedictis-Kessner, Lee, Velez & Warshaw 2023): ~78,000 candidates in ~57,000 contests, 1989–2021, seven offices (mayor, council, county exec & legislature, sheriff, prosecutor, school board), jurisdictions over 50k population.<br><br>CEDA covers the full California universe. |
| Who funds campaigns? | [FEC bulk data](https://www.fec.gov/data/browse-data/?tab=bulk-data) (1979–) | **Fragmented** | [FollowTheMoney](https://www.followthemoney.org/) (now part of [OpenSecrets](https://www.opensecrets.org/states)) aggregates state-level filings; large cities run their own portals (NYC CFB, LA Ethics). |

## C. Governing

| Question | Federal standard | Local status | Local sources & coverage |
|---|---|---|---|
| How do officials vote? | [Voteview](https://voteview.com/) (every roll call, 1789–) | **Absent** | No structured corpus, but large vendor systems (Legistar/Granicus) offer voting data by API; [Council Data Project](https://councildataproject.org/) has a data model, but only data from a handful of cities. |
| What do politicians say? | [Congressional Record](https://www.govinfo.gov/app/collection/CREC) (1873–; speaker-attributed corpora available) | **Emerging** | [LocalView](https://www.nature.com/articles/s41597-023-02044-y) (Barari & Simko 2023): 139,616 meeting videos + transcripts, 2006–2022, 1,012 places, 2,861 governments, 49 states, collected from YouTube. |
| What does the public say / How do they provide input on lawmaking? | [Regulations.gov](https://www.regulations.gov/) notice-and-comment corpus | **Emerging** | PublicSpeak — algorithms and datasets of extracted public comments during city council meetings. |
| What laws do they pass? | [Congress.gov](https://www.congress.gov/) / U.S. Code | **Fragmented** | [Municode](https://library.municode.com/), American Legal Publishing, and General Code host most municipal codes (note there are other secondary products that have scraped and normalized these for NLP research). [National Zoning Atlas](https://www.zoningatlas.org/) — zoning codes state by state. **Note:** because codes change rapidly there are temporal validity issues with some of these local sources. |
| How do they spend? | [USAspending](https://www.usaspending.gov/) (2006–); OMB | **Partial** | [Government Finance Database](https://willamette.edu/mba/research-impact/public-datasets/index.html) (harmonized Census of Governments finance data, 1967–2023, every local government); also on [ICPSR](https://www.icpsr.umich.edu/web/ICPSR/studies/37641). **Caveat:** government-level aggregates with multi-year lag; line-item detail lives in ACFR PDFs — another LLM extraction target. |

## D. Context

| Question | Federal standard | Local status | Local sources & coverage |
|---|---|---|---|
| What are the rules? | Constitution and [Federal Rules of Civil Procedure](https://www.law.cornell.edu/rules/frcp) | **Partial** | [Census of Governments](https://www.census.gov/programs-surveys/cog.html) (this includes the existence, type, boundaries, etc. This data is collected every 5 years); ICMA Form of Government surveys (paywalled). |
| Who covers politicians and their performance? | ProQuest / LexisNexis archives; GDELT (varying quality) | **Fragmented** | [NewsBank / America's News](https://www.newsbank.com/); [Medill State of Local News](https://localnewsinitiative.northwestern.edu/projects/state-of-local-news/) tracks the growth of news deserts. |
| What does the public think (polls)? | [ANES](https://electionstudies.org/) (1948–); ubiquitous polling | **Emerging** | MRP-based city ideology estimates ([Tausanovitch & Warshaw](https://www.americanideologyproject.com/)); CES samples support inference for large cities. **Note:** these estimate general ideology, not opinion on local issues (in other words, these are not stand-ins for local issue polling). |