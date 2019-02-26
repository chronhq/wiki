# Political Relations

Chron currently has 3 types of political relations:  
* direct - has property [located in the administrative territorial entity](https://www.wikidata.org/wiki/Property:P131)
* indirect - instance of any subclass of [dependent territory](http://tinyurl.com/ycjpqy3b) or [client state](http://tinyurl.com/ybkh7gus)
* group - has property [member of](https://www.wikidata.org/wiki/Property:P463)  

General rule is:

* has 2 direct PR -> it means disputed
* has 1 direct PR, and wikidata says `occupied territory` -> it's occupied
* has 1 direct PR, and wikidata says nothing else -> it's a normal sub-region
