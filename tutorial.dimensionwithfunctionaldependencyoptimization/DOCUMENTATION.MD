# Documentation
### CatalogName : Minimal_Cube_with_cube_dimension_with_functional_dependency_optimizations
### Schema Minimal_Cube_with_cube_dimension_with_functional_dependency_optimizations : 
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
D Automotive ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Automotive"] {
H Automotive ""
}
h010["Automotive"] {
L _All_ ""
L Make ""
L Model ""
L ManufacturingPlant ""
L Vehicle_Identification_Number ""
L LicensePlateNum ""
}
"c0" ||--|| "d01" : "AUTO_DIM_ID"
"d01" ||--|| "h010" : "AUTO_DIM_ID-"
"d01" ||--|| "h010" : "AUTO_DIM_ID-MAKE_ID"
"d01" ||--|| "h010" : "AUTO_DIM_ID-MODEL_ID"
"d01" ||--|| "h010" : "AUTO_DIM_ID-PLANT_ID"
"d01" ||--|| "h010" : "AUTO_DIM_ID-VEHICLE_ID"
"d01" ||--|| "h010" : "AUTO_DIM_ID-VEHICLE_ID"
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"AUTOMOTIVE_DIM✔"{
Integer AUTO_DIM_ID "is null ✔"
Integer MAKE_ID "is null ✔"
Varchar MAKE "is null (100) ✔"
Integer MODEL_ID "is null ✔"
Varchar MODEL "is null (100) ✔"
Integer PLANT_ID "is null ✔"
Varchar PLANT "is null (100) ✔"
Integer PLANT_STATE_ID "is null ✔"
Integer PLANT_CITY_ID "is null ✔"
Integer VEHICLE_ID "is null ✔"
Integer COLOR_ID "is null ✔"
Integer TRIM_ID "is null ✔"
Integer LICENSE_ID "is null ✔"
Varchar LICENSE "is null (100) ✔"
Integer LICENSE_STATE_ID "is null ✔"
Integer PRICE "is null ✔"
}

```
---
" Aggregation section:

---
```mermaid
   erDiagram
"AUTOMOTIVE_DIM✔"{
int AUTO_DIM_ID "is null (32.0) ✔"
int MAKE_ID "is null (32.0) ✔"
string MAKE "is null (100.0) ✔"
int MODEL_ID "is null (32.0) ✔"
string MODEL "is null (100.0) ✔"
int PLANT_ID "is null (32.0) ✔"
string PLANT "is null (100.0) ✔"
int PLANT_STATE_ID "is null (32.0) ✔"
int PLANT_CITY_ID "is null (32.0) ✔"
int VEHICLE_ID "is null (32.0) ✔"
int COLOR_ID "is null (32.0) ✔"
int TRIM_ID "is null (32.0) ✔"
int LICENSE_ID "is null (32.0) ✔"
string LICENSE "is null (100.0) ✔"
int LICENSE_STATE_ID "is null (32.0) ✔"
int PRICE "is null (32.0) ✔"
}
```
---
### Cube Matrix for Minimal_Cube_with_cube_dimension_with_functional_dependency_optimizations:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Cube: [0.2500, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"AUTOMOTIVE_DIM✔"{
Integer AUTO_DIM_ID "is null ✔"
Integer MAKE_ID "is null ✔"
Varchar MAKE "is null (100) ✔"
Integer MODEL_ID "is null ✔"
Varchar MODEL "is null (100) ✔"
Integer PLANT_ID "is null ✔"
Varchar PLANT "is null (100) ✔"
Integer PLANT_STATE_ID "is null ✔"
Integer PLANT_CITY_ID "is null ✔"
Integer VEHICLE_ID "is null ✔"
Integer COLOR_ID "is null ✔"
Integer TRIM_ID "is null ✔"
Integer LICENSE_ID "is null ✔"
Varchar LICENSE "is null (100) ✔"
Integer LICENSE_STATE_ID "is null ✔"
Integer PRICE "is null ✔"
}

```
---
## Validation result for catalog Minimal_Cube_with_cube_dimension_with_functional_dependency_optimizations
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
