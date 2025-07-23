# Documentation
### CatalogName : Minimal_Cube_with_DrillThroughAction
### Schema Minimal_Cube_with_DrillThroughAction : 
---
### Cubes :

    Cube

### Cube "Cube" diagram:

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
c0["Cube"]{
M Measure1 ""
M Fact_Count ""
D Measures ""
D Dimension1 ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dimension1"] {
H Hierarchy1 ""
}
h010["Hierarchy1"] {
L _All_ ""
L H1_Level1 ""
L H1_Level2 ""
}
"c0" ||--|| "d01" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-"
"d01" ||--|| "h010" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-KEY"
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
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}
"H1_L1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"H2_L1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"HX_L2✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer H1L1_KEY "is null ✔"
Integer H2L1_KEY "is null ✔"
}

"Fact✔" ||--o{ "HX_L2✔" : "KEY-KEY"
"HX_L2✔" ||--o{ "H1_L1✔" : "H1L1_KEY-KEY"
```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
int KEY "is null (32.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cube_with_DrillThroughAction:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube: [0.1000, 0.0001]
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
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}
"H1_L1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"H2_L1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"HX_L2✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer H1L1_KEY "is null ✔"
Integer H2L1_KEY "is null ✔"
}

"Fact✔" ||--o{ "HX_L2✔" : "KEY-KEY"
"HX_L2✔" ||--o{ "H1_L1✔" : "H1L1_KEY-KEY"
```
---
## Validation result for catalog Minimal_Cube_with_DrillThroughAction
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
