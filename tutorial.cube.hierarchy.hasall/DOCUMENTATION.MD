# Documentation
### CatalogName : Hierarchy - HasAll-Level
### Schema Hierarchy - HasAll-Level : 
---
### Cubes :

    HasAll Cube

### Cube "HasAll Cube" diagram:

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
c0["HasAll Cube"]{
M theMeasure ""
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
H Hierarchy_-_with_HasAll ""
H Hierarchy_-_with_HasAll_and_Names ""
H Hierarchy_-_Without_HasAll ""
}
h010["Hierarchy_-_with_HasAll"] {
L _All_ ""
L theLevel ""
}
h011["Hierarchy_-_with_HasAll_and_Names"] {
L theAllLevelName ""
L theLevel ""
}
h012["Hierarchy_-_Without_HasAll"] {
L theLevel ""
}
"c0" ||--|| "d01" : "KEY"
"d01" ||--|| "h010" : "KEY-"
"d01" ||--|| "h010" : "KEY-KEY"
"c0" ||--|| "d01" : "KEY"
"d01" ||--|| "h011" : "KEY-"
"d01" ||--|| "h011" : "KEY-KEY"
"c0" ||--|| "d01" : "KEY"
"d01" ||--|| "h012" : "KEY-KEY"
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
### Cube Matrix for Hierarchy - HasAll-Level:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube HasAll_Cube: [0.1500, 0.0001]
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
## Validation result for catalog Hierarchy - HasAll-Level
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
