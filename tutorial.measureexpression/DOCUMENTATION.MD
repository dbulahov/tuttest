# Documentation
### CatalogName : Minimal_Cubes_With_MeasureExpression
### Schema Minimal_Cubes_With_MeasureExpression : 
---
### Cubes :

    CubeOneNumericMeasureDifferentFormatStrings

### Cube "CubeOneNumericMeasureDifferentFormatStrings" diagram:

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
c0["CubeOneNumericMeasureDifferentFormatStrings"]{
M Measure1-Sum ""
M Measure2-Sum ""
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
"FACT✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
Numeric VALUE_NUMERIC "is null ✔"
}
"MEASURE_TABLE❌"{
Integer ID "is null ✔"
Integer VALUE "is null ✔"
Integer FLAG "is null ✔"
Varchar measureExpression1 "is null ✔"
Varchar measureExpression2 "is null ✔"
Varchar measureExpression1 "is null ❌"
Varchar measureExpression2 "is null ❌"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"FACT✔"{
int KEY "is null (32.0) ✔"
int VALUE "is null (32.0) ✔"
double VALUE_NUMERIC "is null (100000.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cubes_With_MeasureExpression:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeOneNumericMeasureDifferentFormatStrings: [0.0000, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"FACT✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
Numeric VALUE_NUMERIC "is null ✔"
}
"MEASURE_TABLE❌"{
Integer ID "is null ✔"
Integer VALUE "is null ✔"
Integer FLAG "is null ✔"
Varchar measureExpression1 "is null ✔"
Varchar measureExpression2 "is null ✔"
Varchar measureExpression1 "is null ❌"
Varchar measureExpression2 "is null ❌"
}

```
---
## Validation result for catalog Minimal_Cubes_With_MeasureExpression
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|DATABASE|Column measureExpression2 does not exist in table MEASURE_TABLE|
|DATABASE|Column measureExpression1 does not exist in table MEASURE_TABLE|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
