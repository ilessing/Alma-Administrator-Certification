## User Management
##### Alma Management Certification
----



#### User Mngmt Quiz

  - staff roles can be assigned to both Staff or Public User Record Types
  - User Record Types do regulate:
    - filter by record type in find and manage users list
    - assign mandatory fields in based on record type

  - Scopes assigned to User Roles can limit what libraries a patron can borrow from.  
  Borrowing privs may be restricted by user roles.

  - Role Assignment rules are only applied when a new user is created.  Not applied to existing users.
  Role templates do not affect current users.  They only affect new users.

  - New users registered at the circ desk they always get user record type "Public".  
  - There are separate mandatory fields tables for "Public" and "Staff"
  - You can configure Mandatory fields
  - User registration rules allow configuration of:  fees, expiration dates etc.

  - SIS **import** mode is run manually (not scheduled).  Import mode can only add new users.  
    - Import mode does NOT update existing users.  
    - Sychronize mode does update existing users.

    - SIS job in **export mode** does not make changes to fines or fees of users.
    - Bursar job closes fines & fees **and** exports a file.

  - A single FTP profile **can** serve multiple integrations