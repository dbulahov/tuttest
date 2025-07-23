# Documentation
### CatalogName : Minimal_Cube_with_cube_dimension_level_with_expressions
### Schema Minimal_Cube_with_cube_dimension_level_with_expressions : 
---
### Cubes :

    Cube

### Cube "Cube" diagram:

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
c0["Cube"]{
M Measure ""
M Fact_Count ""
D Measures ""
D Dimension ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dimension"] {
H HierarchyWithHasAll ""
}
h010["HierarchyWithHasAll"] {
L _All_ ""
L Level1 ""
L Level2 ""
}
"c0" ||--|| "d01" : "KEY"
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
"Fact❌"{
Varchar KEY "is null ✔"
Varchar KEY1 "is null ✔"
Integer VALUE "is null ✔"
Varchar nameExpression "is null ✔"
Varchar keyExpression "is null ✔"
Varchar captionExpression "is null ✔"
Varchar ordinalExpression "is null ✔"
Varchar nameExpression "is null ❌"
Varchar keyExpression "is null ❌"
Varchar captionExpression "is null ❌"
Varchar ordinalExpression "is null ❌"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact❌"{
string KEY "is null (1000000000.0) ✔"
string KEY1 "is null (1000000000.0) ✔"
int VALUE "is null (32.0) ✔"
Varchar nameExpression "is null ❌"
Varchar keyExpression "is null ❌"
Varchar captionExpression "is null ❌"
Varchar ordinalExpression "is null ❌"
}
```
---
### Cube Matrix for Minimal_Cube_with_cube_dimension_level_with_expressions:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube: [0.1000, 0.0001]
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
Varchar KEY "is null ✔"
Varchar KEY1 "is null ✔"
Integer VALUE "is null ✔"
Varchar nameExpression "is null ✔"
Varchar keyExpression "is null ✔"
Varchar captionExpression "is null ✔"
Varchar ordinalExpression "is null ✔"
Varchar nameExpression "is null ❌"
Varchar keyExpression "is null ❌"
Varchar captionExpression "is null ❌"
Varchar ordinalExpression "is null ❌"
}

```
---
## Validation result for catalog Minimal_Cube_with_cube_dimension_level_with_expressions
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|DATABASE|Column captionExpression does not exist in table Fact|
|DATABASE|Column ordinalExpression does not exist in table Fact|
|DATABASE|Column keyExpression does not exist in table Fact|
|DATABASE|Column nameExpression does not exist in table Fact|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
