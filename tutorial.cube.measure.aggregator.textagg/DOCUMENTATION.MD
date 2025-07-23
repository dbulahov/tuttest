# Documentation
### CatalogName : Measure - Text Aggregator
### Schema Measure - Text Aggregator : 
---
### Cubes :

    MeasuresTextAggregatorsCube

### Cube "MeasuresTextAggregatorsCube" diagram:

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
c0["MeasuresTextAggregatorsCube"]{
M Sum_of_Value ""
M Comment ""
M Fact_Count ""
D Measures ""
D Town ""
D Time ""
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
L Continent ""
L Country ""
L Town ""
}
d02["Time"] {
H TimeHierarchy ""
}
h020["TimeHierarchy"] {
L Year ""
L Month ""
}
"c0" ||--|| "d01" : "COUNTRY-KEY"
"d01" ||--|| "h010" : "KEY-CONTINENT"
"d01" ||--|| "h010" : "KEY-COUNTRY"
"d01" ||--|| "h010" : "KEY-KEY"
"c0" ||--|| "d02" : "YEAR-KEY"
"d02" ||--|| "h020" : "KEY-YEAR"
"d02" ||--|| "h020" : "KEY-MONTH"
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
Varchar COUNTRY "is null ✔"
Varchar CONTINENT "is null ✔"
Integer YEAR "is null ✔"
Integer MONTH "is null ✔"
Varchar MONTH_NAME "is null ✔"
Varchar USER "is null ✔"
Varchar COMMENT "is null ✔"
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
string COUNTRY "is null (1000000000.0) ✔"
string CONTINENT "is null (1000000000.0) ✔"
int YEAR "is null (32.0) ✔"
int MONTH "is null (32.0) ✔"
string MONTH_NAME "is null (1000000000.0) ✔"
string USER "is null (1000000000.0) ✔"
string COMMENT "is null (1000000000.0) ✔"
}
```
---
### Cube Matrix for Measure - Text Aggregator:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube MeasuresTextAggregatorsCube: [0.2500, 0.0001]
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
Varchar COUNTRY "is null ✔"
Varchar CONTINENT "is null ✔"
Integer YEAR "is null ✔"
Integer MONTH "is null ✔"
Varchar MONTH_NAME "is null ✔"
Varchar USER "is null ✔"
Varchar COMMENT "is null ✔"
}

```
---
## Validation result for catalog Measure - Text Aggregator
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
