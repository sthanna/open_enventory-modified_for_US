TO DO:
- Changing location inside normal OE window does not record in History text
- Sigma-Aldrich cannot be accessed from A2 Hosting?????
- Add global_settings for root user to turn on location sharing (show locations for users of other databases)


2019-07-17:
- Added date style to yyyy-mm-dd hh:mm:ss when display in OE so there is no confusion in date style
- Added a new login page with mobile responsive
- Modified sidenav, topnav to use Bootstrap4
- Added option for admin user to turn Bootstrap 4 option on/off in global_settings


2019-07-03:
- fixed bug in Terminal mode: barcodeTerminalAsync.php and lib_language_en.php
        while doing inventory for a container (inventory mode or "Set storage 
        for all following containers"), if you scan a non-existing barcode, 
        the location will be removed. When a non-existent barcode is scanned,
        an error pop-up window appears.
- modified History log text to add storage_name; also added History log text
        when changing storage in edit mode (lib_db_manip.php, lib_db_manip_edit.php)


2019-06-11:
- import.php, lib_import.php: added importing function for locations and
        users using tab-separated text file
- lib_import.php: fix for importing chemical_storage_barcode bug. 
        When import tab-dilimited text file of chemical containers, if the
        barcode column is the last column, it will add white space or \n
        character, making the barcodes inaccurate. The fix will trim all the
        white space (\t\n) on the right side of the input column
- topnav.php, style.css.php, lib_global_funcs.php, lib_sidenav_funcs.php
        sidenav.php: edited some fonts, styles


2019-06-04
- lib_language_en.php, sidenav.php, barcode_autogeneration.php: 
        Creating option for admin user to auto generate all location and 
        user barcodes while using "Existing barcodes" functions


2019-05-25
- lib_db_manip.php: edit logging text to reflect chemical containers when 
    being moved from one location to another


2019-05-23
- multiple files: Fixed functions for php7 warning
- Fixed "Set storage for all following containers" in Terminal
- Added barcode Type 128 generation for user using existing barcode
- import.php, lib_import.php: Fixed added order_date and open_date in 
        Import tab-separated text file function