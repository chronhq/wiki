Here is a Google Sheet describing the database architecture: https://docs.google.com/spreadsheets/d/1jQ1Jm9ijuu2ZePYDQwe82kFxqiYLnrWi-t9-BbXs5EM/edit#gid=1000374390

### _Entities Tables_

#### _TerritorialEntity_

id |	wikidata_id |	color |	admin_level |	~predecessor~ |	_comments_
-- | -- | -- | -- | -- | --
1 |	https://www.wikidata.org/wiki/Q159	| #ccc |	2	| |	Russia
2	| https://www.wikidata.org/wiki/Q212	| #bbb	| 2	| |	Ukraine
3	| https://www.wikidata.org/wiki/Q7835		| | 2	|	| Crimea during Russian-Ukranian conflict 2014-today
4	| https://www.wikidata.org/wiki/Q29999	|	| 1	|	| Kingdom of Netherlands
5	| https://www.wikidata.org/wiki/Q458	|	| 2	|	| European Union
6	| https://www.wikidata.org/wiki/Q188161	|	| 2	| |	Dutch East Indies
7	| https://www.wikidata.org/wiki/Q55	|	| 2	|  | Netherlands

#### _PoliticalRelation_

id	| start_date |	end_date |	parent |	child	| control_type
-- | -- | -- | -- | -- | --
1 |	| |	Cyprus |	Northern Cyprus |	direct
2	|	| |	Turkey	| Northern Cyprus	| direct
3 |	| |	Germany	| Poland |	direct
4 |	| |	Germany	| Bavaria	 | direct
5 |	| |	French Empire	| Poland	| indirect
6 |	| |	Nato |	Germany |	group
7 | 1939 | 1945 |	[axis]	| japan |	group
8 |	| |	1935 |	1945 |	[axis]	| Germany	| group
9 |	| |	UK	| British HK |	inderect
10 |	| |	Japan	British HK |	direct
11 |	| |	UK	British HK	| inderect
12 |	| |	China	HK | China State |	inderect

### _Tables for MVT_

#### _CachedData_
id |	wikidata_id |	type |	location |	date |	rank
-- | -- | -- | -- | -- | --

#### _City_
id |	wikidata_id |	label |	location |	inception_date |	dissolution_date
-- | -- | -- | -- | -- | --

### _Geometry Tables_

#### _AtomicPolygon_

id |	geom
-- | --
1 |	Alsace-Lorraine
2 | Alsace
3	| Lorraine

#### _SpacetimeVolume_
id	| start_date |	end_date |	territory |	entity |	references |	related_events |	visual_center
-- | -- | -- | -- | -- | -- | -- | -- 
1	 | 1991 |	today | [array of APs] | 2 | [links to sources] | [events from cached data] | POINT(0, 0)
2 |	2018 |	today |	[1,2] |	Alsaice-Lorraine | [] | [] | POINT(1,1)

### _Narrative Tables_

#### _Narratives_

author |	title |	description |	tags |	_start_date_ |	_end_date_
-- | -- | -- | -- | -- | --
String | | | | 1700 |	1999

#### _Map Settings_

bbox	| zoom_min |	zoom_max
-- | -- | --
							
#### _Narration_
description	| title |	date_label |	map_datetime |	attached_events |	img |	video |	settings_id
-- | -- | -- | -- | -- | -- |-- | -- 
Interpretation of facts goes here	| Title |	Optional String |	Year  for borders |	{} |	url |	url |	FKEY to Map Settings
