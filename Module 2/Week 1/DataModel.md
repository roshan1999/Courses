# Data Model

Data Models characteristics/components:
  Structure - gives more insight of the data than just plain text(using keys)
  Operation - Performing data arithmetic with the data (specifically with the field of the orgainzation or structure.)
  Constraints - provides a means to call out erroneous data.

Data Model Structure -
  - Data having structure
  - What is structure?
    - File is uniform with each line(record) having data property / attributes.
    - Content grows but pattern of data organization
    - This repetition of pattern makes it a structure.
      - Even if a value is missing it doesn't mean that the data is not structured.
    - When do files have the same data model?
          - When they have similar data structure that only varies by the parameters(i.e. no of fields).  
    - Incomprehensible data- like compress data, and encrypted data are usually unstructured.
2. Operation -
   - operations specify the methods to manipulate the data.
     - Commomn operations
       - 1. Subsetting - extract part of collection from the entirety of it.
         - Depending on context also called selection or filtering.
       - 2. sUBSTRUCTURE extraction - extract **part** of data structure.
         - Produces a new collection of records having the very field required.
         - AKA Projection.
       - 3. Union
         - Combining 2 collection into larger one.
         - Duplicate elemination.
      - 4. Join
        - Done when 2 data items have different records but have the same field.
3. Constraints:
   - Logical statement - one can compute and test the true or false of the statement.

> TODO : Strucutral Constraints
>       Types of constraints.


# Relational Data Models

  - Simplest and the most frequent data model
  - Basis for mYSQL oracle..
  - Primary structure of relational data model is table
  - Table represents set of tuples(informally record).
    - Unless and otherwise stated every tuple is atomic.
  - By defn of sets : Its a collection of distinct elements
  - Hence duplicate entries of same tuple is not allowed.
  - Also the order of the field matters and must be same to be added.
  - Header of the table provides the schema / the order in which the fields must be specified.
  - The order of the field specified by attributes of the relational table.
  - Schema can also specify Constraints
  - **Primary key** - This field is unique for each employee.
    - Hence this logically implies that duplicacy is not allowed.
  - **Foreign Key** - References means values in this column exist only if the value exist in the parent table or referenced table. Foreign key is the primary key of another / parent table.
    - Ex : Employee and empsalaries table (slides)
  - Joining uses this primary key and foreign key connection -
    - Join operation is one of the most expensive (time and space consuming).
    - With larger analytical application easily becomes a bottleneck
    - A suitable management platform make this operation efficient.
    - Spreadsheet doesnt conform and enforce principles of relational data models.
    - Hence a lot of time is spent cleaning up and correcting data errors after migration from spreadsheet.
    - Problems with spreadsheet :
      - Allows a column to be non atomic - i.e. have more than one value
              - ex:  terrorism.csv - **automatic firearm;explosive**
      - Does not make sure that the attribute values are seperated into constraints and values..
              - ex: Minor (likely<1$)
              - While possible to segregate data by substring operation - it is more expensive to do so.
      - DOesn't provide a primary key foriegn key relation
              - Ex : attack type and attack (one to many relation preferable to be a seperate table.)

# Semistructured Data model

> TODO
