# TABLE OF CONTENTS

- [Overview](project/overview.md)
- [Onboarding](project/onboarding.md)
- [Features](project/features.md)
  - [Facts](project/facts.md)
  - Collaboration & Moderation
  - [Narratives](project/narratives.md)
  - Weight system
- [Contribute](./contribute/index.md)
  - [Input historical data](./contribute/input_historical_data.md)
  - [Draw historical maps](./contribute/draw_historical_maps.md)
    - [List of historic map resources](https://docs.google.com/document/d/16VRnTbky9e9FsBZ9H9JlnpvoaQQbquDte8APCQQ8cS8/edit)
- Roadmap & Open-Source Project Management
  - [v1 Roadmap](./project/v1_roadmap.md)
  - [Labeling](./project/labeling.md)
  - [License](./project/licenses.md)

We are always hanging out on Discord: [https://discord.gg/fUuNaDk](https://discord.gg/fUuNaDk).

# CURRENT ISSUES TBD

## TOP PRIORITY

- Create bugfixing issue - [#47 Demo stuck on loading screen](https://github.com/chronhq/frontend/issues/47) - done and closed
- [79 issue](https://github.com/chronhq/backend/issues/79) - connected to [16 issue](https://github.com/chronhq/microservices/issues/16) for @whirish to finish.
- [78 issue](https://github.com/chronhq/backend/issues/78)
- [77 issue](https://github.com/chronhq/backend/issues/77)
- [48 issue](https://github.com/chronhq/backend/issues/48) - decide with mappers how STV+TE (+PR) data should be stored in shapes - option to add everything to shapes while we don’t have admin interface instead of adding everything on site tbd

## NEXT TO DO

- Collect data for current political relations, add PR to database and we can’t automate that in any way, so someone should do it manually. We should figure out how to do that. We need to check all TEs and STVs and decide what we do in case more TEs for disputed territories (or colonies) are required. Also someone needs to map TEs with PRs. 
- PR+TE input interface - create an issue
- Authentication - needs further discussion if it’s critical issue for now as it requires lots of work on backend and frontend. So: do we need to store authors who change PR/TE or we take it all from Wikidata. As temporary measure we can start by providing proxy access. - create an issue
- Armies movement option (find maps, add functionality) - create an issue
