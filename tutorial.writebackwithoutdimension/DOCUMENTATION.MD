# Documentation
### CatalogName : Writeback_without_dimension
### Schema Writeback_without_dimension : 
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
"FACT❌"{
Integer VAL "is null ✔"
Integer VAL1 "is null ✔"
Varchar VALUE "is null (100) ✔"
Varchar VALUE "is null (100) ❌"
}
"FACTWB✔"{
Integer VAL "is null ✔"
Integer VAL1 "is null ✔"
Varchar L2 "is null (100) ✔"
Varchar ID "is null (100) ✔"
Varchar USER "is null (100) ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"FACT❌"{
int VAL "is null (32.0) ✔"
int VAL1 "is null (32.0) ✔"
Varchar VALUE "is null (100) ❌"
}
```
---
### Cube Matrix for Writeback_without_dimension:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube C: [0.0000, 0.0001]
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
Varchar VALUE "is null (100) ✔"
Varchar VALUE "is null (100) ❌"
}
"FACTWB✔"{
Integer VAL "is null ✔"
Integer VAL1 "is null ✔"
Varchar L2 "is null (100) ✔"
Varchar ID "is null (100) ✔"
Varchar USER "is null (100) ✔"
}

```
---
## Validation result for catalog Writeback_without_dimension
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|DATABASE|Column VALUE does not exist in table FACT|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
