# Web Development in OutSystems 22% (11)
## General Development 8% (4)
## Screen Lifecycle 8% (4)
- Mandatory Input Variables set to value in request
- Other Input Variables and Local Variables set to default values
- Preparation fetches data for Screen Render (Server-side)
- Screen Render top to bottom
## Security 6% (3)
- HTTPS
- Integrated Authentication
- Access Control = Authentication (User) + Authorization (Roles)
- User - Username, Name, Password
- User Server Actions - Create
- Built-in Roles - Anonymous, Registered
- Role has Server Actions - Check, Grant, Revoke
- Can be Public - to be used by other Modules
- Can set Screen Roles
- Can set Group Roles
- Group has Server Actions
# Data Modeling 14% (7)
## Entities & Data Types 8% (4)
### Entities
- Entity = Database Table
- Instance = Database Table Row
- Attribute = Database Table Column
- Id Attribute - Primary Key
- Entity Actions - CRUD
- CreateOrUpdate, GetForUpdate
### Static Entities
- Record (Attribute values) defined at design time
- Cannot be created, updated or deleted (only Get Action) 
- Used like Enumerations
- 4 automatically created attributes - Id, Label, Order, Is Active
- Attributes can be changed, added
- Referenced by Record Name - Entities.&lt;StaticEntity&gt;.&lt;RecordName&gt;
## Data Relationships 6% (3)
# Aggregates & SQL Queries 16% (8)
## Designing Aggregates & SQL Queries 12% (6)
## General Capabilities 4% (2)
# Logic and Integrations 22% (11)
## Actions and Exceptions 14% (7)
## Input Validations 6% (3)
## Web Services 2% (1)
# UI Design 30% (15)
## Screens and Widgets 12% (6)
### Screen
- Empty or Template
- Hierarchy of various elements
- Input Variables (can be Mandatory)
- Local Variables
## RichWidgets 4% (2)
## Web Blocks and Events 6% (3)
## Themes, Styles and Templates 4% (2)
