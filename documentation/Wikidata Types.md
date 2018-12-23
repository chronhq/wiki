
## Purpose

This arcticle describes the mapping between wikidata's [P31 (instance of)](https://www.wikidata.org/wiki/Property:P31) and our basic types

This document should be the source of truth for both, backend and frontend, projects.

## How we should treat different wikidata _instances_

###  battle:

- Q178561: 'battle'
- Q180684: 'conflict'
- Q124757: 'riot'
- Q1261499: 'navalBattle'

### document:

- Q49848: 'document'
- Q680655: 'constitutionalDocument'
- Q820655: 'statute'
- Q625298: 'peaceTreaty'
- Q131569: 'treaty'

### actor:

- Q5: 'human'
- Q215627: 'person' _// should not be used as `instance of`_
- Q20643955: 'humanBiblicalFigure'
- Q21070568: 'humanWhoMayBeFictional'

### cities:

- *TODO* subclasses of [Human Settlement](https://www.wikidata.org/wiki/Q486972)


### state

- *TODO* subclasses of [Political Territorial Entities](https://www.wikidata.org/wiki/Q1048835)

## Sub-types

Actor entity can be labeled by his [P106 occupation](https://www.wikidata.org/wiki/Property:P106)

## Code consistancy

- [Backend model](https://github.com/chronhq/backend/blob/master/project/api/models.py)
- [Frontend model](https://github.com/chronhq/frontend/blob/master/src/models/Wikidata/WikidataHelper.js)