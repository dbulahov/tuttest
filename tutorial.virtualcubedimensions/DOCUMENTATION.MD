# Documentation
### CatalogName : Cube_with_virtual_cube
### Schema Cube_with_virtual_cube : 
---
### Cubes :

    Cube1Cube2, Cube2, Cube1

### Cube "Cube1Cube2" diagram:

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
c0["Cube1Cube2"]{
M MeasureCube1 ""
M MeasureCube2 ""
D Measures ""
D Cube1Dimension1 ""
D Cube2Dimension1 ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Cube1Dimension1"] {
H HierarchyWithoutHasAll ""
}
h010["HierarchyWithoutHasAll"] {
L Level2 ""
}
d02["Cube2Dimension1"] {
H HierarchyWithoutHasAll ""
}
h020["HierarchyWithoutHasAll"] {
L Level2 ""
}
"c0" ||--|| "d01" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-KEY"
"c0" ||--|| "d02" : "KEY-KEY"
"d02" ||--|| "h020" : "KEY-KEY"
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
c1["Cube2"]{
M MeasureCube2 ""
M Fact_Count ""
D Measures ""
D Cube2Dimension1 ""
}
d10["Measures"] {
H Measures ""
}
h100["Measures"] {
L MeasuresLevel ""
}
d11["Cube2Dimension1"] {
H HierarchyWithoutHasAll ""
}
h110["HierarchyWithoutHasAll"] {
L Level2 ""
}
"c1" ||--|| "d11" : "KEY-KEY"
"d11" ||--|| "h110" : "KEY-KEY"
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
c2["Cube1"]{
M MeasureCube1 ""
M Fact_Count ""
D Measures ""
D Cube1Dimension1 ""
}
d20["Measures"] {
H Measures ""
}
h200["Measures"] {
L MeasuresLevel ""
}
d21["Cube1Dimension1"] {
H HierarchyWithoutHasAll ""
}
h210["HierarchyWithoutHasAll"] {
L Level2 ""
}
"c2" ||--|| "d21" : "KEY-KEY"
"d21" ||--|| "h210" : "KEY-KEY"
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
### Cube Matrix for Cube_with_virtual_cube:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube1: [0.0500, 0.0001]
Cube Cube2: [0.0500, 0.0001]
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
## Validation result for catalog Cube_with_virtual_cube
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
