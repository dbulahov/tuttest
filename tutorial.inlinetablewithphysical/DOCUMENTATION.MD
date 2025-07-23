# Documentation
### CatalogName : CubeOneMeasureInlineTableLevelPhysicalAndInlineTables
### Schema CubeOneMeasureInlineTableLevelPhysicalAndInlineTables : 
---
### Cubes :

    CubeTwoLevelsInlineAndPhysicalTable

### Cube "CubeTwoLevelsInlineAndPhysicalTable" diagram:

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
c0["CubeTwoLevelsInlineAndPhysicalTable"]{
M Measure-Sum ""
M Fact_Count ""
D Measures ""
D Dimension ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dimension"] {
H Hierarchy ""
}
h010["Hierarchy"] {
L Country ""
L Town ""
}
"c0" ||--|| "d01" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-KEY"
```
---
### Cube Matrix for CubeOneMeasureInlineTableLevelPhysicalAndInlineTables:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeTwoLevelsInlineAndPhysicalTable: [0.1000, 0.0003]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"TOWN✔"{
Integer KEY "is null ✔"
Integer KEY_COUNTRY "is null ✔"
Varchar NAME "is null ✔"
}
"COUNTRY❌"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer KEY "is null ❌"
Varchar NAME "is null ❌"
}
"Fact❌"{
Integer KEY "is null ✔"
Double VALUE "is null ✔"
Integer KEY "is null ❌"
Double VALUE "is null ❌"
}
"COUNTRY❌"{
Integer KEY "is null ❌"
Varchar NAME "is null ❌"
}
"Fact❌"{
Integer KEY "is null ❌"
Double VALUE "is null ❌"
}

"Fact❌" ||--o{ "TOWN✔" : "KEY-KEY"
"TOWN✔" ||--o{ "null✔" : "KEY_COUNTRY-KEY"
```
---
## Validation result for catalog CubeOneMeasureInlineTableLevelPhysicalAndInlineTables
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|SCHEMA|Table value does not correspond to any join|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
