# Documentation
### CatalogName : Minimal_Virtual_Cubes_With_Measures_only
### Schema Minimal_Virtual_Cubes_With_Measures_only : 
---
### Cubes :

    Cube1, VirtualCubeMeasureOnly, Cube2

### Cube "Cube1" diagram:

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
c0["Cube1"]{
M C1-Measure-Sum ""
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
"C1_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}
"C2_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"C1_Fact✔"{
string KEY "is null (1000000000.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube "VirtualCubeMeasureOnly" diagram:

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
c1["VirtualCubeMeasureOnly"]{
M C1-Measure-Sum ""
M C2-Measure-Sum ""
M Calculation1 ""
D Measures ""
}
d10["Measures"] {
H Measures ""
}
h100["Measures"] {
L MeasuresLevel ""
}
```
---
### Cube "Cube2" diagram:

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
c2["Cube2"]{
M C2-Measure-Sum ""
M Fact_Count ""
D Measures ""
}
d20["Measures"] {
H Measures ""
}
h200["Measures"] {
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
"C1_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}
"C2_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"C2_Fact✔"{
string KEY "is null (1000000000.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Minimal_Virtual_Cubes_With_Measures_only:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube1: [0.0000, 0.0001]
Cube Cube2: [0.0000, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"C1_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}
"C2_Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
## Validation result for catalog Minimal_Virtual_Cubes_With_Measures_only
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|SCHEMA|VirtualCube with name VirtualCubeMeasureOnly must contain dimensions |
|SCHEMA|Hierarchy must be set for CalculatedMember with name Calculation1|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
