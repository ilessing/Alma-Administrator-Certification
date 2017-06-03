## Resource Management
### Resource Mngmt 3

#### Normalization rules:
  are used to edit Marc21 Bib records or Holdings records.
  - Capable of:
    - Add or Remove fields and subfields.
    - Replace Fields, subfields, indicators with other fields, subfields & indicators
    - Add or Replace text in subfields
  - Can be applied conditionally
  - Can apply to individual records or sets of records.
  - Configured in MD editor by users with Catalog Admin role.
  - Can be shared among all users or kept private for just their creator
  - Processes contain Normalization Rules and allow Norm. Rules to be run as a job on a set of records or on an idividual record.
  - Can be associated as "Processes" for easy application to records as a job.

#### Merge Methods:
combine 2 records into 1. user defines which fields are kept, overwritten etc.
  - similar to Normalization Rules as they use similar syntax.
  - Merge methods act on Preferred record with values on Non-Preferred records.
    - When using an import profile or OCLC the Preferred record in the local record.
    - When using external search sources the Preferred record is the incoming record.
  - Configured in MD editor -> Rules Tab -> Merge Rules Folder
  - can be private or shared
  - Primarily used when importing records

####  Match Methods
  search for duplicate records, lets you define what is a match.  Define which fields will be matched on such as ISBN, ISSN. etc.   i.e. what the unique id will be.

  - Determine how a match is defined
  - Use Cases:
    1. Lets you search for records in the catalog with an open record in the MD editor
    2. When importing records via import profile, external search sources, OCLC connection
  - Allows you to reject, save, merge or overlay incoming records
  - Should not be customized
  - 7 for serials
  - 7 for non-serials
  - the "001 to MMS_ID Match Method" should be used when importing records previously exported from Alma

###### Norm rules, Merge Methods, Match Methods can be applied to:
  1. a single record in MD editor
  2. importing bib records from external search source
  3. importing bibs from OCLC connection
  4. importing records in batch mode via an Import Profile

---------------------------------------

### Resource Mngmt 4

#### Metadata Customization
  Marc21 Bib & holdings MD Schema customization
  The Marc21 standard allow for limited customization
  - customization examples:
    - whether fields or subfields can be repeated
    - whether fields or subfields are mandatory
  - can NOT add fields, subfields or indicators
  - you can configure invalid exception profiles which will display a warning but not prevent saving.

#### Controlled Vocabs
  - lists of terms that a cataloger can select from
  - are assigned to fields in MD Customization
  - Steps
    - create controlled vocab
    - add it to a field in the MD config
  - can be re-used in multiple sub-fields
  - a locally defined vocab will only be available for a particular sub-field


#### Resource Mngmt 5 - Import Profiles

##### Allows you to create Bib and Inventory records via batch process
  - Normalizes & validates incoming records to conform to Marc21 and local customizations
  - can search for matches (using Match Methods)
  - can merge with existing records (using Merge Methods)
  - can apply mngmt flags such as suppressed or sync with OCLC
  - will not CREATE a package but can add to existing package / portfolio
  - requires Marc21 records in imported file
  - can be scheduled to import from FTP server
  - can be run manually
  - Must be Catalog Admin to configure Import Profiles
  - Allows creation of brief records which in turn can be used for ordering

#### Resource Management 6 - misc
  - Provenance Codes
    - History of an item stored in Provenance field
    - populates the drop down selector in item record provenance field.
    - can be a default field but that will apply to all records
  - Accession Numbers
    - Alma can generate unique accession numbers
    - unique within a location
    - for holdings records
    - distinct accession sequence for each location
    - accession placement params determine which field (852p,852h,852j) the accession number will be stored in the Marc record
    - configured in the "Physical locations" for any particular library
    - Methods:
      - prefix + sequence
      - sequence + time stamp
    - you may select a sequence start number higher than 1
  - E task statuses
    - allows staff manage work flows of electronic resources
    - can be customized by Resource Mgr.
  - Call number parsing
    - Useful for printing labels
    - determines how call numbers will be formatted & broken into lines for printing
    - Repository Admin role is required to configure
    - configured for each call number type (examples of Call Number types???)
  - Barcode generation
    - prefix + sequence
    - prefix can be set by Resource config mgr.
  - description templates
    - used for Serials item records
    - populates description field in item record
    - relies on chronology an enumeration fields
    - may include prefixes, suffixes, formatting characters (commas, parens)
    - based on rules with input and output params
  - Physical item sort routines
    - for lists of physical items
    - used in:
      - receive new material workbench (Acquistions)
      - Get it tab in Primo (discovery)
    - List of physical items in journals (Alma)
    - you can select 1 sort routine as Default
    - populate "sort routines" drop down selector

#### Resource Management Quiz
  - Work Orders
    - Work order types can be configured at Institution level or Library level
    - Institution level Work Order Types can be associated with departments at multiple Libraries.
    - Library level Work Order Types can only be associated with that Library's depts.
    - Work Order statuses are part of a Work Order Type (not Dept)
    - Work Order statuses are descriptive.  They do Not Define a work flow.
  - Brief Records created at checkout automatically trigger a Technical Services work order.  It may trigger a recall which may shorten the loan period.  Configure the Tech Serve work order type to regulate if a recall is created.
  - Search Indexes can not be customized in Alma for normal fields.
  - External Search Resources are ruled by ExLibris.  But you can "Enable" the ones you want.
