# Documentation
### CatalogName : Minimal_Cube_with_cube_dimension_level_with_parent_child_with_closure
### Schema Minimal_Cube_with_cube_dimension_level_with_parent_child_with_closure : 
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
M Value ""
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
H Dimension ""
}
h010["Dimension"] {
L Name1 ""
L Name2 ""
L Name3 ""
}
"c0" ||--|| "d01" : "NAME-NAME"
"d01" ||--|| "h010" : "NAME-NAME"
"d01" ||--|| "h010" : "NAME-NAME"
"d01" ||--|| "h010" : "NAME-NAME"
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
Varchar NAME "is null ✔"
Varchar PARENT "is null ✔"
Integer VALUE "is null ✔"
}
"Closure✔"{
Integer NAME "is null ✔"
Varchar PARENT "is null ✔"
Integer DISTANCE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
string NAME "is null (1000000000.0) ✔"
string PARENT "is null (1000000000.0) ✔"
int VALUE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cube_with_cube_dimension_level_with_parent_child_with_closure:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube: [0.0500, 0.0001]
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
Varchar NAME "is null ✔"
Varchar PARENT "is null ✔"
Integer VALUE "is null ✔"
}
"Closure✔"{
Integer NAME "is null ✔"
Varchar PARENT "is null ✔"
Integer DISTANCE "is null ✔"
}

```
---
## Validation result for catalog Minimal_Cube_with_cube_dimension_level_with_parent_child_with_closure
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
