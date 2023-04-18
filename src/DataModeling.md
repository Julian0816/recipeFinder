# Data Modeling

## Steps to follow

1. Identidy the entities in the system. DONE
1. Itentify the attributes for each entity. DONE
1. Identify primary and foreign keys. DONE
1. Define the right nomenclature for the entities and attributes. DONE
1. Identify the pivot entities in the system.
1. Identify the catalog entities in the system.
1. Identify the relationships in the system.
1. Create the entity-relation model.
1. Create the database relational model.
1. Identify the data types for the attributes and the entities in the system.
1. Identify the attributes that might be unique in the system.
1. Identify the business rules (CRUD Operations).

## Glosary

- **PK**: _Primary Key_
- **FK**: _Foreign Key_
- **UQ**: _Unique Atribute_
- **ED**: _Data Entity_
- **EP**: _Pivot Data_
- **EC**: _Catalog Data_

# RecipeFinderAPI database design

## List of Entities

### users **(ED)**

- user_id **(PK)**
- username **(UQ)**
- avatar
- password
- email **(UQ)**
- name
- surname
- created_date

### recipes **(ED)**

- recipe_id **(PK)**
- title
- description
- video
- rating
- image
- user_id **(FK)**

### cuisine_types **EC**

- cuisine_type_id **(PK)**
- cuisine_name
- image
- recipe_id **(FK)**

### main_dishes **EC**

- main_dish_id **(PK)**
- dish_name
- image
- recipe_id **(FK)**

### events **ED**

- event_id **(PK)**
- location
- theme
- time
- description
- image
- user_id **(FK)**



