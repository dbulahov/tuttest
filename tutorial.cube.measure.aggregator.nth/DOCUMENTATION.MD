# Documentation
### CatalogName : Measure - NTH value Aggragator
### Schema Measure - NTH value Aggragator : 
---
### Cubes :

    MeasuresAggregatorsCube

### Cube "MeasuresAggregatorsCube" diagram:

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
c0["MeasuresAggregatorsCube"]{
M NthAgg1 ""
M NthAgg2 ""
M NthAgg3 ""
M NthAgg4 ""
M NthAgg5 ""
M NthAgg6 ""
M NthAgg7 ""
M Fact_Count ""
D Measures ""
D Dim ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dim"] {
H Hierarchy ""
}
h010["Hierarchy"] {
L Value ""
}
"c0" ||--|| "d01" : "ID-ID"
"d01" ||--|| "h010" : "ID-VALUE"
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"Fact❌"{
Integer ID "is null ✔"
Integer VALUE "is null ✔"
Varchar NAME "is null ✔"
Varchar NAME "is null ❌"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact❌"{
int ID "is null (32.0) ✔"
int VALUE "is null (32.0) ✔"
string LEVEL "is null (1000000000.0) ✔"
Varchar NAME "is null ❌"
}
```
---
### Cube Matrix for Measure - NTH value Aggragator:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube MeasuresAggregatorsCube: [0.0500, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"Fact❌"{
Integer ID "is null ✔"
Integer VALUE "is null ✔"
Varchar NAME "is null ✔"
Varchar NAME "is null ❌"
}

```
---
## Validation result for catalog Measure - NTH value Aggragator
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|DATABASE|Column NAME does not exist in table Fact|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
