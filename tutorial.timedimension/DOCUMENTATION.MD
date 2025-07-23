# Documentation
### CatalogName : Minimal_Cube_with_Time_Dimension
### Schema Minimal_Cube_with_Time_Dimension : 
---
### Cubes :

    CubeTimeDimension

### Cube "CubeTimeDimension" diagram:

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
c0["CubeTimeDimension"]{
M Measure-Sum ""
M Fact_Count ""
D Measures ""
D Time ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Time"] {
H Time ""
}
h010["Time"] {
L _All_ ""
L Years ""
L Quarters ""
L Months ""
L Week ""
L Day ""
}
"c0" ||--|| "d01" : "DATE_KEY"
"d01" ||--|| "h010" : "DATE_KEY-"
"d01" ||--|| "h010" : "DATE_KEY-YEAR_ID"
"d01" ||--|| "h010" : "DATE_KEY-QTR_NAME"
"d01" ||--|| "h010" : "DATE_KEY-MONTH_NAME"
"d01" ||--|| "h010" : "DATE_KEY-WEEK_IN_MONTH"
"d01" ||--|| "h010" : "DATE_KEY-DAY_IN_MONTH"
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
Timestamp DATE_KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
timestamp DATE_KEY "is null (26.6) ✔"
int VALUE "is null (32.0) ✔"
int YEAR_ID "is null (32.0) ✔"
string QTR_ID "is null (1000000000.0) ✔"
string QTR_NAME "is null (1000000000.0) ✔"
string MONTH_ID "is null (1000000000.0) ✔"
string MONTH_NAME "is null (1000000000.0) ✔"
int WEEK_IN_MONTH "is null (32.0) ✔"
int DAY_IN_MONTH "is null (32.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cube_with_Time_Dimension:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeTimeDimension: [0.2500, 0.0001]
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
Timestamp DATE_KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
## Validation result for catalog Minimal_Cube_with_Time_Dimension
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
