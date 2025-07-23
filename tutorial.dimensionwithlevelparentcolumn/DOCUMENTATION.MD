# Documentation
### CatalogName : Minimal_Parent_Child_Hierarchy
### Schema Minimal_Parent_Child_Hierarchy : 
---
### Cubes :

    CubeParentChildOneTopMember

### Cube "CubeParentChildOneTopMember" diagram:

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
c0["CubeParentChildOneTopMember"]{
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
L Level1 ""
L Level2 ""
L Level3 ""
}
"c0" ||--|| "d01" : "DIM_KEY-KEY"
"d01" ||--|| "h010" : "KEY-"
"d01" ||--|| "h010" : "KEY-KEY"
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
Integer DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"Hier_One_Top_Member✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer PARENT_KEY "is null ✔"
}

"Fact✔" ||--o{ "Hier_One_Top_Member✔" : "DIM_KEY-KEY"
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
### Cube Matrix for Minimal_Parent_Child_Hierarchy:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeParentChildOneTopMember: [0.0500, 0.0001]
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
Integer DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"Hier_One_Top_Member✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer PARENT_KEY "is null ✔"
}

"Fact✔" ||--o{ "Hier_One_Top_Member✔" : "DIM_KEY-KEY"
```
---
## Validation result for catalog Minimal_Parent_Child_Hierarchy
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
