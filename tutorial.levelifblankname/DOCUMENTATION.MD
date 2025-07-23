# Documentation
### CatalogName : Minimal_Single_Hierarchy_Hidden_Members_with_IfBlankName
### Schema Minimal_Single_Hierarchy_Hidden_Members_with_IfBlankName : 
---
### Cubes :

    HiddenMembersIfBlankName

### Cube "HiddenMembersIfBlankName" diagram:

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
c0["HiddenMembersIfBlankName"]{
M Measure1 ""
M Fact_Count ""
D Measures ""
D DimensionMembersHiddenIfBlankName ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["DimensionMembersHiddenIfBlankName"] {
H Hierarchy1 ""
}
h010["Hierarchy1"] {
L _All_ ""
L Level1 ""
L Level2 ""
}
"c0" ||--|| "d01" : "DIM_KEY-KEY"
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
Integer DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"Fact_Multiple✔"{
Integer DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"Level_1_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"Level_2_NULL✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L1_KEY "is null ✔"
}
"Level_1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"Level_2_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L1_KEY "is null ✔"
}
"Level_3_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L2_KEY "is null ✔"
}

"Fact✔" ||--o{ "Level_2_NULL✔" : "DIM_KEY-KEY"
"Level_2_NULL✔" ||--o{ "Level_1✔" : "L1_KEY-KEY"
"Fact✔" ||--o{ "Level_2_NULL✔" : "DIM_KEY-KEY"
"Level_2_NULL✔" ||--o{ "Level_1✔" : "L1_KEY-KEY"
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
### Cube Matrix for Minimal_Single_Hierarchy_Hidden_Members_with_IfBlankName:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube HiddenMembersIfBlankName: [0.1000, 0.0001]
Cube HiddenMembersIfBlankName: [0.1000, 0.0001]
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
"Fact_Multiple✔"{
Integer DIM_KEY "is null ✔"
Integer VALUE "is null ✔"
}
"Level_1_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"Level_2_NULL✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L1_KEY "is null ✔"
}
"Level_1✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
}
"Level_2_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L1_KEY "is null ✔"
}
"Level_3_Multiple✔"{
Integer KEY "is null ✔"
Varchar NAME "is null ✔"
Integer L2_KEY "is null ✔"
}

"Fact✔" ||--o{ "Level_2_NULL✔" : "DIM_KEY-KEY"
"Level_2_NULL✔" ||--o{ "Level_1✔" : "L1_KEY-KEY"
"Fact✔" ||--o{ "Level_2_NULL✔" : "DIM_KEY-KEY"
"Level_2_NULL✔" ||--o{ "Level_1✔" : "L1_KEY-KEY"
```
---
## Validation result for catalog Minimal_Single_Hierarchy_Hidden_Members_with_IfBlankName
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
