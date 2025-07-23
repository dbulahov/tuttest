# Documentation
### CatalogName : Measure - Percentile Aggragator
### Schema Measure - Percentile Aggragator : 
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
M Percentile_disc_0_25 ""
M Percentile_cont_0_25 ""
M Percentile_disc_0_42 ""
M Percentile_cont_0_42 ""
M Percentile_disc_0_5 ""
M Percentile_cont_0_5 ""
M Percentile_disc_0_75 ""
M Percentile_cont_0_75 ""
M Percentile_disc_1_00 ""
M Percentile_cont_1_00 ""
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
L _All_ ""
L Level ""
}
"c0" ||--|| "d01" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-"
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

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
string KEY "is null (1000000000.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Measure - Percentile Aggragator:
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
"Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
## Validation result for catalog Measure - Percentile Aggragator
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
