# Documentation
### CatalogName : Cube_with_role_access_all_none_custom
### Schema Cube_with_role_access_all_none_custom : 
---
### Cubes :

    Cube1, Cube2

### Roles :
##### Role: "role1"

##### Role: "role11"

##### Role: "role12"

##### Role: "role2"

##### Role: "role3"

##### Role: "role3"

##### Role: "manager"

##### Role: "role_u"

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
M Measure1 ""
M Fact_Count ""
D Measures ""
D Dimension1 ""
D Dimension2 ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Dimension1"] {
H Hierarchy1 ""
}
h010["Hierarchy1"] {
L Level2 ""
}
d02["Dimension2"] {
H Hierarchy1 ""
}
h020["Hierarchy1"] {
L Level2 ""
}
"c0" ||--|| "d01" : "KEY-KEY"
"d01" ||--|| "h010" : "KEY-KEY"
"c0" ||--|| "d02" : "KEY-KEY"
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
M Fact_Count ""
D Measures ""
D Dimension1 ""
}
d10["Measures"] {
H Measures ""
}
h100["Measures"] {
L MeasuresLevel ""
}
d11["Dimension1"] {
H Hierarchy1 ""
}
h110["Hierarchy1"] {
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
### Cube Matrix for Cube_with_role_access_all_none_custom:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube1: [0.1000, 0.0001]
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
## Validation result for catalog Cube_with_role_access_all_none_custom
## <span style='color: red;'>ERROR</span> : 
|Type|   |
|----|---|
|SCHEMA|MemberGrant member use Dimension1 dimension which absent in cube with name Cube1|
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
