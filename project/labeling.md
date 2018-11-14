# Labeling

This page is to explain the conventions over Chron's labeling system.

Labels are split into several groups.

- 'A' group is used for code-review status and are applicable only to Pull Requests.
- 'F' group is used to encode the type (and accordingly the severity) of issues; they are applicable only within the Issue Tracker.
- 'M' group is to encode the affected feature in the product.
- 'P' group is to denote priority. They are generally relevant only to issues, though may in principle be used on pull-requests.
- 'Q' group is to denote difficulty, only used in issues.
- 'Z' group are reasons for why something is a non-issue. They are applicable only within the Issue Tracker.

As such, a pull request must have a single label from the 'A' group and may additionally have a single label from the 'P' group (though typically will not).

An valid issue must have a single label from the 'F' group and may additionally have a single label from the 'P' group. An invalid issue should be closed with a single label from the 'Z' group.

### 'A' group

All pull requests should start labeled with either 'A0-pleasereview', 'A3-inprogress', or 'A2-insubstantial' (should it be an alteration which requires no code review). After review it should be relabeled with another 'A' group label.

- `A0-pleasereview` Pull request needs code review.
- `A1-onice` Pull request is reviewed well, but should not yet be merged.
- `A2-insubstantial` Pull request requires no code review (e.g. a sub-repository hash update).
- `A3-inprogress` Pull request is in progress. No review needed at this stage.
- `A4-gotissues` Pull request is reviewed and has significant issues which must be addressed. Once addressed, author should relabel as `A0-pleasereview`.
- `A8-looksgood` Pull request is reviewed well.
- `A9-buythatmanabeer` Pull request is reviewed well and worth buying the author a beer.

### 'F' group

Issues should have only one of these. Do not combine; if multiple labels are equally applicable to an issue, use the one with the lowest number.

- `F1-panic` The client panics and exits without proper error handling.
- `F1-security` The client fails to follow expected, security-sensitive, behaviour.
- `F2-bug` The client fails to follow expected behavior.
- `F3-annoyance` The client behaves within expectations, however this "expected behaviour" itself is at issue. Annoyances are small enhancements which dramatically improve the usability of the client.
- `F4-tests` Tests need fixing, improving or augmenting.
- `F5-documentation` Documentation needs fixing, improving or augmenting.
- `F6-refactor` Code needs refactoring.
- `F7-footprint` An enhancement to provide a smaller (system load, memory, network or disk) footprint.
- `F7-optimisation` An enhancement to provide better overall performance in terms of time-to-completion for a task.
- `F8-enhancement` An additional feature.
- `F9-proposal` A proposal of a feature or user story.

### 'M' group

Used to denote the affected component or sub-project. Each issue and pull request should have (at least) one.

- `M0-interactivemap` The 4d interactive map.
- `M1-factoids` Factoids and facts, from Wikidata and from our own database.
- `M2-narratives` Narratives.
- `M3-voting` Voting system on factoids to find their truth score.
- `M4-weighing` Weighing system in the context of a user search or a narrative.
- `M5-autonomylevel` Toggle to see administrative sub-units or groupments of political entities.
- `M9-admininterface` A backend interface to create factoirs, narratives and other data.

### 'P' group

Typically used only to annotate issues, however P0 and P2 may reasonably be used on PRs in exceptional circumstances.

- `P0-dropeverything` Everyone should address the issue/PR now.
- `P2-asap` No need to stop dead in your tracks, however issue/PR should be addressed as soon as possible.
- `P5-sometimesoon` Issue is worth doing soon.
- `P7-nicetohave` Issue is worth doing eventually.
- `P9-backlog` Issue is put in the product backlog, might be worth doing eventually.

### 'Q' group

Is used to annotate difficulty of issues.

- `Q0-trivial` Can be fixed by anyone with access to a computer.
- `Q1-mentor` An easy task were a mentor is available. Please indicate in the issue who the mentor could be.
- `Q2-easy` Can be fixed by copy and pasting from StackOverflow.
- `Q5-substantial` Can be fixed by a developer with decent experience.
- `Q7-involved` Can be fixed by a team of developers and probably takes some time.
- `Q9-epic` Can only be fixed by John Skeet.

### 'Z' group

Used only on issues which will (or _may_, in the case of Z5) be closed immediately.

- `Z0-duplicate` Issue is a duplicate. Closer should comment with a link to the duplicate.
- `Z0-intended` Issue describes a behavior which turns out to work as intended. Closer should explain why.
- `Z0-invalid` Issue is invalid. Closer should comment why.
- `Z0-question` Issue is a question. Closer should answer.
- `Z0-stale` Issue is in principle valid, but it is not relevant anymore or can not reproduced.
- `Z0-wontfix` Issue is in principle valid, but this project will not address it. Closer should explain why.
- `Z5-unconfirmed` Issue might be valid, but it's not yet known.
