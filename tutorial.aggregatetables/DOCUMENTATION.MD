# Documentation
### CatalogName : Cube_with_Aggregate_tables
### Schema Cube_with_Aggregate_tables : 
---
### Cubes :

    Sales

### Cube "Sales" diagram:

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
c0["Sales"]{
M Store_Cost ""
M Fact_Count ""
D Measures ""
D Product ""
}
d00["Measures"] {
H Measures ""
}
h000["Measures"] {
L MeasuresLevel ""
}
d01["Product"] {
H Product_Family ""
}
h010["Product_Family"] {
L _All_ ""
L Product_Family ""
}
"c0" ||--|| "d01" : "PRODUCT_ID-PRODUCT_ID"
"d01" ||--|| "h010" : "PRODUCT_ID-"
"d01" ||--|| "h010" : "PRODUCT_ID-PRODUCT_FAMILE"
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"SALES_FACT_1997✔"{
Integer PRODUCT_ID "is null ✔"
Decimal STORE_COST "is null (10.4) ✔"
}
"PRODUCT✔"{
Integer PRODUCT_CLASS_ID "is null ✔"
Integer PRODUCT_ID "is null ✔"
Varchar brand_name "is null (60) ✔"
Varchar brand_name "is null (60) ✔"
}
"PRODUCT_CLASS✔"{
Integer PRODUCT_CLASS_ID "is null ✔"
Varchar PRODUCT_FAMILE "is null (60) ✔"
}
"AGG_C_SPECIAL_SALES_FACT_1997✔"{
Integer PRODUCT_ID "is null ✔"
Decimal STORE_COST_SUM "is null (10.4) ✔"
Integer FACT_COUNT "is null ✔"
}
"AGG_C_14_SALES_FACT_1997✔"{
}
"AGG_LC_100_SALES_FACT_1997✔"{
}

"SALES_FACT_1997✔" ||--o{ "PRODUCT✔" : "PRODUCT_ID-PRODUCT_ID"
"PRODUCT✔" ||--o{ "PRODUCT_CLASS✔" : "PRODUCT_CLASS_ID-PRODUCT_CLASS_ID"
```
---
" Aggregation section:

---
```mermaid
   erDiagram
"SALES_FACT_1997✔"{
int PRODUCT_ID "is null (32.0) ✔"
double STORE_COST "is null (10.4) ✔"
}
"SALES_FACT_1997✔"{
int PRODUCT_ID "is null (32.0) ✔"
double STORE_COST "is null (10.4) ✔"
}
"excludes❌"{
x AGG_C_14_SALES_FACT_1997
x AGG_LC_100_SALES_FACT_1997
}
```
---
### Cube Matrix for Cube_with_Aggregate_tables:
```mermaid
quadrantChart
title Cube Matrix
x-axis small level number --> high level number
y-axis Low row count --> High row count
quadrant-1 Complex
quadrant-2 Deep
quadrant-3 Simple
quadrant-4 Wide

Cube Sales: [0.0500, 0.0001]
```
---
### Database :
---
```mermaid
---
title: Diagram;
---
erDiagram
"SALES_FACT_1997✔"{
Integer PRODUCT_ID "is null ✔"
Decimal STORE_COST "is null (10.4) ✔"
}
"PRODUCT✔"{
Integer PRODUCT_CLASS_ID "is null ✔"
Integer PRODUCT_ID "is null ✔"
Varchar brand_name "is null (60) ✔"
Varchar brand_name "is null (60) ✔"
}
"PRODUCT_CLASS✔"{
Integer PRODUCT_CLASS_ID "is null ✔"
Varchar PRODUCT_FAMILE "is null (60) ✔"
}
"AGG_C_SPECIAL_SALES_FACT_1997✔"{
Integer PRODUCT_ID "is null ✔"
Decimal STORE_COST_SUM "is null (10.4) ✔"
Integer FACT_COUNT "is null ✔"
}
"AGG_C_14_SALES_FACT_1997✔"{
}
"AGG_LC_100_SALES_FACT_1997✔"{
}

"SALES_FACT_1997✔" ||--o{ "PRODUCT✔" : "PRODUCT_ID-PRODUCT_ID"
"PRODUCT✔" ||--o{ "PRODUCT_CLASS✔" : "PRODUCT_CLASS_ID-PRODUCT_CLASS_ID"
```
---
## Validation result for catalog Cube_with_Aggregate_tables
## <span style='color: blue;'>WARNING</span> : 
|Type|   |
|----|---|
|DATABASE|Table: Schema must be set|
