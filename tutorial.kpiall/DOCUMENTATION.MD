# Documentation
### CatalogName : Minimal_Cubes_With_KPI_all_Properties
### Schema Minimal_Cubes_With_KPI_all_Properties : 
---
### Cubes :

    CubeKPI

### Cube "CubeKPI" diagram:

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
c0["CubeKPI"]{
M Measure1-Sum ""
M Measure2-Count ""
M Fact_Count ""
M CalculatedValue ""
M CalculatedGoal ""
M CalculatedStatus ""
M CalculatedTrend ""
D Measures ""
KPI Kpi1 "Kpi with all parameters"
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
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
Integer VALUE_NUMERIC "is null ✔"
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
double VALUE_NUMERIC "is null (100000.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cubes_With_KPI_all_Properties:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube CubeKPI: [0.0000, 0.0001]
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
Integer VALUE_NUMERIC "is null ✔"
}

```
---
## Validation result for catalog Minimal_Cubes_With_KPI_all_Properties
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|SCHEMA|Hierarchy must be set for CalculatedMember with name CalculatedStatus|
|SCHEMA|Hierarchy must be set for CalculatedMember with name CalculatedGoal|
|SCHEMA|Hierarchy must be set for CalculatedMember with name CalculatedValue|
|SCHEMA|Hierarchy must be set for CalculatedMember with name CalculatedTrend|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
