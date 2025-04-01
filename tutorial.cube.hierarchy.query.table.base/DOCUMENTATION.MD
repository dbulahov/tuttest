# Documentation
### CatalogName : Hierarchy - Query based on seperate Tables for Fact and Dimension
### Schema Hierarchy - Query based on seperate Tables for Fact and Dimension : 
---
### Cubes :

    Cube Query linked Tables

### Cube "Cube Query linked Tables" diagram:

---

```mermaid
%%{init: {
"theme": "default",
"themeCSS": [
    ".er.entityBox {stroke: black;}",
    ".er.attributeBoxEven {stroke: black;}",
    ".er.attributeBoxOdd {stroke: black;}",
    "[id^=entity-c] .er.entityBox { fill: lightgreen;} ",
    "[id^=entity-d] .er.entityBox { fill: powderblue;} ",
    "[id^=entity-h] .er.entityBox { fill: pink;} "
]
}}%%
erDiagram
c0["Cube Query linked Tables"]{
M theMeasure ""
M Fact_Count ""
D Measures ""
D Town ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Town"] {
H TownHierarchy ""
}
h010["TownHierarchy"] {
L Town ""
}
"c0" ||--|| "d01" : "TOWN_ID-ID"
"d01" ||--|| "h010" : "ID-ID"
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"Fact✔"{
Integer TOWN_ID "is null ✔"
Integer VALUE "is null ✔"
}
"Town✔"{
Integer ID "is null ✔"
Varchar NAME "is null ✔"
}

"Fact✔" ||--o{ "Town✔" : "TOWN_ID-ID"
```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
int TOWN_ID "is null (32.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Hierarchy - Query based on seperate Tables for Fact and Dimension:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube_Query_linked_Tables: [0.0500, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"Fact✔"{
Integer TOWN_ID "is null ✔"
Integer VALUE "is null ✔"
}
"Town✔"{
Integer ID "is null ✔"
Varchar NAME "is null ✔"
}

"Fact✔" ||--o{ "Town✔" : "TOWN_ID-ID"
```
---
## Validation result for catalog Hierarchy - Query based on seperate Tables for Fact and Dimension
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
