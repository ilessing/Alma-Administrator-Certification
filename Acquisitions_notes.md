## Acquisitions

#### Acquisitions Quiz

  - Import Profiles
    - Only a New Order Import Profile can create new purchase order lines.
    - A Repository Import Profile creates Bibliographic records and _may_ create inventory records but can not create Purchase Order Lines.

    - Each vendor may encode ordering information in their [EOD](https://knowledge.exlibrisgroup.com/Voyager/Knowledge_Articles/What_is_Embedded_Order_Data_(EOD)%3F) files differently than another vendor.  Therefore you may need to configure a distinct New Order Import Profile for each vendor.

    - An update inventory import profile can be used to load additional info from a vendor but preserve PO Lines and ordering info.  Matching the new vendor info to existing info is done with matching PO lines.

    - Update Inventory Profiles can not change a portfolio type.  It can update Stand Alone portfolios or portfolios that are part of Package but can not change a package type from Stand Alone to Package or vise versa.

    - A PO Line that is missing Mandatory info will go to the review workbench regardless of any Purchasing Review rule.

    - Purchase Review Rules based on high price must meet **all** of these conditions to work properly:
      1. `assertion_over_po_line_price` parameter 
      2. `Price limit reached` assertion code
      3. acting on an order created via EOD (embedded order data)
    Purchase Review Rules only work on EOD orders not on manual orders.  Manual orders always go to the review workbench.
    Purchase Review Rules are only consulted once during the order work flow.  If a user clicks _Save & Continue_ in the Review Workbench any order previously paused due to a rule will resume its progress along the work flow.

    - Alma does not allow creation of new PO Line Types.  You only get the ones ExLibris created. (Electronic, Physical, One Time, Continious)

    - Reporting Codes are labels you can add to PO Lines and Invoice lines and are configurable.

    - Validation Checks before leaving receiving department:
      - Bib is a Full record rather than a Brief record
      - Item has a barcode.