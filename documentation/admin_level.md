# Admin Level

> STV stands for _Space Time Volume_  
> TE stands for _Territorial Entity_  
> _Political Relations_ can be direct (DPR), indirect (IDR), group (GDR) according to [#38](https://github.com/chronhq/backend/issues/38)

Using one _admin_level_ for all groups (coalitions, alliances, etc.) would be sufficient enough. Groups would not be shown automatically, they would appear on map in case they were selected by user in some menu or chosen by narrative author. Groups would be marked as first admin_level in database.
Groups will not have _STV's_ as they would be represented as _Group Political Relations_.

Second _admin_level_ would be default for countries. Next _admin_levels_ should be used for deeper administrative units. All of territories (TE + STV) with admin_level > 1 can be represented if a few different ways.

  For example we create _Territorial Entity_ of United Kingdom as _admin_level = 2_ and as for deeper administrative units we think of the UK's territories [`Scotland`, `Wales`, `Northern Ireland`, `England`]. We have two options to represent it then:
- STV with it's own territory in case it is deepest admin_level we've got. _Direct Political Relations_ are optional
  _Example_: we have to create a separate STV for United Kingdom in case we don't have `Scotland` ,`Wales`, `Northern Ireland` territories mapped. In this case we will create two STV's one for  _Territorial Entity_ called `England` with _DPR_ to UK, and the second one for UK with rest of the territories.
- only by _Political Relations_ without _STV_
  _Example_: we don't need an STV for United Kingdom if we have STV's of [`Scotland`, `Wales`, `Northern Ireland`, `England`] with `Direct Political Relations` to United Kingdom. 5 _Territorial Entities_ and 4 _STV's_

**[!]** As the result of using inheritance of territories based on admin_level deepness, each Atomic Polygon should be used only once among all of the STV's for selected time period.

Table of admin levels

| Admin Level | Usage |
| --- | --- |
| = 1 | coalitions, unions, alliances, supranational organizations |
| = 2 | nations, empires, kingdoms, countries |
| = 3 | regions as deeper administrative units |
| = 4 | (please fill here) |
| >= 5 | we won't use these for the MVP |

Why we should not create STV for territories that are already mapped on a deeper levels?

Main idea: it would be better to have one source of truth for maps. If borders were changed on deeper admin levels it would immediately affect countries and groups.

For displaying map properly while exploring it at the admin_level = 2 when we store a redundant STV's all foreign territories with _Direct Political Relations_ (like colonies) should be included as parents territory and parent should be updated each time colony has claimed new territory. This will result in creating a separate STV for parent each time.

Mapbox MVT layer used on frontend for visualization requires us to map AP only once per layer.
