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
### Entity Id
- Entity must have Id - long integer, automatically numbered, mandatory, Text, Long or other Entity Id
- Simple Primary Keys, no Composite
- Referenced by Id - Attribute of type Entity Id
- Can be mandatory or not
- Default = NullIdentifier()
### Relationships
- 1-to-1 - Extension, Change Id to Entity Id, Mandatory, Address performance issues, Base Entity is read-only (e.g. User)
- 1-to-n - Reference Attribute, may or not Mandatory, Master-Detail (Detail has MasterEntity Id Attribute), multiple Reference Attributes
- n-to-n - Use Junction Entity, has Id, Entity1 Id, Entity2 Id, Unique Index with both Reference Attribute if unique
### Indexes
- Speed up read, additional writes, additional storage
- Automatically created for Reference Attributes
- Can create Custom
- Can define Unique
- Can combine Attributes
### Referential Integrity
- Protect - Cannot delete Detail, Dark Grey
- Delete - Cascade (Delete Detail will Delete Master), Red
- Ignore - None (Can Delete Detail without Delete Master, Light Grey
# Aggregates & SQL Queries 16% (8)
## Designing Aggregates & SQL Queries 12% (6)
### Multiple Sources
- Only With = INNER JOIN
- With or Without = LEFT JOIN
- With = FULL OUTER JOIN
### Calculated Attributes
- Expressions
- Hide only for previewing purpose
- Outsystems further optimize by removing unused columns
### Aggregated Functions
- Sum, Average, Min, Max, Count
- Only aggregated (blue) columns are returned
### SQL Tool
- Syntax Checking
- Code Highlighting
- DBMS Specific
- {Entity}.[Attribute]
- Input - Query Parameters @Parameters
- Must have at least one Output Entities/Structures
- SELECT must follow order of Output Entities/Structures Attributes
- Output same as Aggregates - List, Count
- Test - Max Records
- Can execute Non-Select
## General Capabilities 4% (2)
# Logic and Integrations 22% (11)
## Actions and Exceptions 14% (7)
## Input Validations 6% (3)
### Built-in
- Mandatory
- Data Type
- Submit - has validation
- Navigate - no validation
- Valid - specific styling (e.g. red border)
- ValidationMessage - when input gains focus
### Validations
- Server - All on server
- Client & Server - Built-in on client, custom on server
- None - No Built-in, custom on server
## Web Services 2% (1)
### SOAP
- WSDL (URL/file), Choose Methods, XML 
### REST
- No contract (URL), fill parameter values, Copy JSON response to body, JSON
- Generate methods as Actions, compound data types as Structures
- Can change generated
- Callbacks - OnBeforeRequest, OnAfterResponse - debug, customize requests
- Expose REST, add methods (Server Actions)
# UI Design 30% (15)
## Screens and Widgets 12% (6)
### Screen
- Empty or Template
- Hierarchy of various elements
- Input Variables (can be Mandatory)
- Local Variables
## RichWidgets 4% (2)
- DropDownMenu
- Icon
- List_Navigation - ListWidgetId, LineCount, TotalRowCount, OnNotify
- List_Sort
## Web Blocks and Events 6% (3)
## Themes, Styles and Templates 4% (2)
