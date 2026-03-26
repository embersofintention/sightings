---
tags:
tagline: test dataview gallery
created: 2026-03-07, 21:15
created_date: 2026, 03/07
created_time: 21:15
---

# Test Gallery made using Dataview

---


```dataview

TABLE WITHOUT ID 
EmbededCoverImg as "Preview", 
link(file.name) + " | " + tagline as "About"




FROM "Art" AND !"_templates" AND !"index"
SORT created

WHERE file.name != this.file.name
FLATTEN choice(typeof(img)="link",
    embed(link(meta(
        choice(
            typeof(img)="link",
                img, this.file.link
        )
    ).path, "250")), "![](" + img + ")") AS EmbededCoverImg

```













---
**Edit Basic Template:**
```button
name ➕ Edit Template
type link
action obsidian://open?vault=sightings&file=_templates%2F_ADD%20DATE%20AND%20TAGLINE%20STUFF
```
---
