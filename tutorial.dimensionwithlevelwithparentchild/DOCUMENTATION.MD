# Documentation
### CatalogName : Minimal_Cube_with_cube_dimension_level_with_closure_table
### Schema Minimal_Cube_with_cube_dimension_level_with_closure_table : 
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
D Employees ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Employees"] {
H Employees ""
}
h010["Employees"] {
L _All_ ""
L Employee_Id1 ""
L Employee_Id2 ""
L Employee_Id3 ""
L Employee_Id4 ""
}
"c0" ||--|| "d01" : "employee_id-employee_id"
"d01" ||--|| "h010" : "employee_id-"
"d01" ||--|| "h010" : "employee_id-employee_id"
"d01" ||--|| "h010" : "employee_id-employee_id"
"d01" ||--|| "h010" : "employee_id-employee_id"
"d01" ||--|| "h010" : "employee_id-employee_id"
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
Integer employee_id "is null ✔"
Varchar full_name "is null ✔"
Integer supervisor_id "is null ✔"
Varchar marital_status "is null ✔"
Varchar position_title "is null ✔"
Varchar gender "is null ✔"
Integer salary "is null ✔"
Integer education_level "is null ✔"
Varchar management_role "is null ✔"
}
"employee_closure✔"{
Integer supervisor_id "is null ✔"
Integer employee_id "is null ✔"
Integer distance "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"Fact✔"{
int employee_id "is null (32.0) ✔"
string full_name "is null (1000000000.0) ✔"
int supervisor_id "is null (32.0) ✔"
string marital_status "is null (1000000000.0) ✔"
string position_title "is null (1000000000.0) ✔"
string gender "is null (1000000000.0) ✔"
int salary "is null (32.0) ✔"
int education_level "is null (32.0) ✔"
string management_role "is null (1000000000.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cube_with_cube_dimension_level_with_closure_table:
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
Integer employee_id "is null ✔"
Varchar full_name "is null ✔"
Integer supervisor_id "is null ✔"
Varchar marital_status "is null ✔"
Varchar position_title "is null ✔"
Varchar gender "is null ✔"
Integer salary "is null ✔"
Integer education_level "is null ✔"
Varchar management_role "is null ✔"
}
"employee_closure✔"{
Integer supervisor_id "is null ✔"
Integer employee_id "is null ✔"
Integer distance "is null ✔"
}

```
---
## Validation result for catalog Minimal_Cube_with_cube_dimension_level_with_closure_table
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
