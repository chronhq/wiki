# Facts

Territorial entities, actors and events are presented on the map as facts; they are all interactive. All facts are backed by sources links that can be checked and voted upon. As for the first version all facts are taken from crowdsourced database [Wikidata](www.wikidata.org).<img src="https://s3.amazonaws.com/libapps/accounts/115194/images/Wikidata_stamp.png" height="50">

Facts are currently taken from wikidata by queries that can be found [here](https://github.com/chronhq/microservices). 
The absence of certain fact can be the result of:
* intentional absence in the request (which can be discussed in Discord or [Github issues](https://github.com/chronhq/microservices/issues))
* incomplete WIkidata info. To add facts please do it [through](https://www.wikidata.org/wiki/Wikidata:Tours) WIkidata engine.

In the near future we plan on adding more open data online resources and implementing the weighting system for it.

## Territorial Entities

Chron team uses the concept of Territorial Entities and SpaceTime Volumes. 

[TE](https://en.wikipedia.org/wiki/Territorial_entity) - A territorial entity that covers a part of the surface of the Earth with specified borders. TEs contain Wikidata id, political relations and color. TE also has [Admin level](/documentation/admin_level.md).

STV (SpaceTime Volume) is a territory with start-end dates. The start and end dates linked to the same territory cannot overlap. Therefore, put together, the Territories show the evolution in time of this Entity. For example a kingdom may see its borders changing with a series of Territories. 

### Political Relations

Political Relations represent political responsibilities between TE. For example Colorado State TE is in direct relation with USA TE. To see the full list of Political Relations, please refer to the database architecture at the end of the page or to [this WIki page](/documentation/political_relations.md).

### People

Request to WIkidata  
[https://github.com/chronhq/microservices/blob/master/fetch_actors.py](https://github.com/chronhq/microservices/blob/master/fetch_actors.py)

### Cities

[https://github.com/chronhq/microservices/blob/master/fetch_cities.py](https://github.com/chronhq/microservices/blob/master/fetch_cities.py)

### Battles and peace treaties

[https://github.com/chronhq/microservices/blob/master/fetch_battles.py](https://github.com/chronhq/microservices/blob/master/fetch_battles.py)
[https://github.com/chronhq/microservices/blob/master/fetch_treaties.py](https://github.com/chronhq/microservices/blob/master/fetch_treaties.py)

### Other ideas

Monuments, buildings etc, could all possibly be added in the future as entities. 

## Technical Implementation

Here is a Google Sheet describing the database architecture: [https://docs.google.com/spreadsheets/d/1jQ1Jm9ijuu2ZePYDQwe82kFxqiYLnrWi-t9-BbXs5EM/edit#gid=1000374390](https://docs.google.com/spreadsheets/d/1jQ1Jm9ijuu2ZePYDQwe82kFxqiYLnrWi-t9-BbXs5EM/edit#gid=1000374390)

