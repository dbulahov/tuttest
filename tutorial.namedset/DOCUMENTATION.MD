# Documentation
### CatalogName : Cube_with_NamedSet
### Schema Cube_with_NamedSet : 
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
M Measure1 ""
M Fact_Count ""
D Measures ""
D Dimension1 ""
D Dimension2 ""
NS NsWithFolderDimension1 ""
NS NsWithoutFolderDimension1 ""
NS NSInCubeWithFolder ""
NS NSInCubeWithoutFolder ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dimension1"] {
H Hierarchy ""
}
h010["Hierarchy"] {
L _All_ ""
L Level2 ""
}
d02["Dimension2"] {
H Hierarchy ""
}
h020["Hierarchy"] {
L _All_ ""
L Level2 ""
}
"c0" ||--|| "d01" : "KEY"
"d01" ||--|| "h010" : "KEY-"
"d01" ||--|| "h010" : "KEY-KEY"
"c0" ||--|| "d02" : "KEY"
"d02" ||--|| "h020" : "KEY-"
"d02" ||--|| "h020" : "KEY-KEY"
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
### Cube Matrix for Cube_with_NamedSet:
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
"Fact✔"{
Varchar KEY "is null ✔"
Integer VALUE "is null ✔"
}

```
---
## Validation result for catalog Cube_with_NamedSet
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
