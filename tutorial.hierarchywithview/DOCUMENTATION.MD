# Documentation
### CatalogName : Cube_with_share_dimension_with hierarchy_with_view_reference
### Schema Cube_with_share_dimension_with hierarchy_with_view_reference : 
---
### Cubes :

    CubeOneMeasure

### Cube "CubeOneMeasure" diagram:

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
c0["CubeOneMeasure"]{
M Measure1 ""
M Fact_Count ""
D Measures ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
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
Varchar DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"HT✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer VALUE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
int DIM_KEY "is null (32.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Cube_with_share_dimension_with hierarchy_with_view_reference:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeOneMeasure: [0.0000, 0.0001]
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
Varchar DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"HT✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer VALUE "is null ✔"
}

```
---
## Validation result for catalog Cube_with_share_dimension_with hierarchy_with_view_reference
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
