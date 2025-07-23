# Documentation
### CatalogName : tutorial_for_writeback_with_fact_InlineTable
### Schema tutorial_for_writeback_with_fact_InlineTable : 
---
### Cubes :

    C

### Cube "C" diagram:

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
c0["C"]{
M Measure1 ""
M Measure2 ""
M Fact_Count ""
D Measures ""
D D1 ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["D1"] {
H HierarchyWithHasAll ""
}
h010["HierarchyWithHasAll"] {
L _All_ ""
L L1 ""
L L2 ""
}
"c0" ||--|| "d01" : "L2-L2"
"d01" ||--|| "h010" : "L2-"
"d01" ||--|| "h010" : "L2-L1"
"d01" ||--|| "h010" : "L2-L2"
```
---
### Cube Matrix for tutorial_for_writeback_with_fact_InlineTable:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube C: [0.1000, 0.0005]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"FACT❌"{
Integer VAL "is null ✔"
Integer VAL1 "is null ✔"
Varchar L2 "is null (100) ✔"
Integer VAL "is null ❌"
Integer VAL1 "is null ❌"
Varchar L2 "is null (100) ❌"
}
"L1✔"{
Varchar L1 "is null (100) ✔"
Varchar L2 "is null (100) ✔"
}
"L2✔"{
Varchar L2 "is null (100) ✔"
}
"FACTWB✔"{
Integer VAL "is null ✔"
Integer VAL1 "is null ✔"
Varchar L2 "is null (100) ✔"
Varchar ID "is null (100) ✔"
Varchar USER "is null (100) ✔"
}
"FACT❌"{
Integer VAL "is null ❌"
Integer VAL1 "is null ❌"
Varchar L2 "is null (100) ❌"
}

"FACT❌" ||--o{ "L1✔" : "L2-L2"
"L1✔" ||--o{ "L2✔" : "L2-L2"
```
---
## Validation result for catalog tutorial_for_writeback_with_fact_InlineTable
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|SCHEMA|Dimension with name D1 absent in cube with name C for write back|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
