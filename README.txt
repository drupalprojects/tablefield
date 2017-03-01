# TableField #

Provides a simple, generic form/widget to input tabular data. The
form allows the user to select the number of rows/columns in the table, then
enter the data via textfields. Since this is a field it is revision capable,multi-value capable and has integration with Views.


## INSTALLATION ##

- Copy tablefield directory to ../sites/all/modules.
- Enable module at ../admin/modules.


## GET STARTED ##

Add a tablefield to any entity:
- For nodes at ../admin/structure/types. Then click 'manage fields' for the
  desired content type.
- For users at ../admin/config/people/accounts/fields.
- For taxonomies at ../admin/structure/taxonomy. Then click 'edit vocabulary'
  for the desired vocabulary.
- For files using the File Entity (fieldable files) module
  (https://www.drupal.org/project/file_entity) at
  ../admin/structure/file-types. Then click 'manage fields' for the desired file type.


## FEATURES ##

### Per table (in Edit mode) ###
- Change number of rows/columns per table (even within multi-value instances).
  Optionally restict that to users with the permission 'Rebuild tablefied'
  (see field settings below).
- Optionally lock cells with default values from editing, e.g. header values.
- Rows can be rearranged with drag and drop.
- Upload a CSV file to be converted into a table on the fly. The used
  separator can be defined at ../admin/config/content/tablefield.
- Copy paste tables e.g. from Excel.
- Add a table caption.
- Use any role allowed text format for the cells or limit it to plain text.
- Easily remove tables from a multi-value field with the button provided by
  https://www.drupal.org/project/multiple_fields_remove_button. Just install and enable that module.

### Per field (field settings) ###
For nodes field settings for some of the below options can be found through 'manage fields' at ../admin/structure/types. For others entities see above.

- Restrict rebuilding to users with the permission "rebuild tablefield"
- Lock table header so default values cannot be changed.
- Table cell processing (radios)
  * Plain text
  * Filtered text (user selects input format)

### Per display mode (display settings) ###
For nodes display settings for the below options can be found through 'manage display' at ../admin/structure/types. For others entities see above under 'GET STARTED'. Display options can be set per view mode e.g. 'Default' or 'Teaser'.

The options of all of the below settings are 'Yes'/'No' (checkbox) unless stated otherwise.

#### Tabular view ####
- Sticky header
- Hide table header
- Hide empty columns ignoring column header
- Trim empty trailing rows
- Trim empty trailing columns
- Hide empty rows
- Hide empty columns
- Show link to export table data as CSV depending on permission

#### Raw data (JSON) ####
This format is intended when table data should be provided as a service.
- Use first row/column values as array keys (if not empty). (select)
  * No
  * Header only
  * Both first row and first column (two headers)
- Vertical header (first column instead of first row)
- Table data only (no caption)


## CREDITS ##

- Original author: Kevin Hankens (http://www.kevinhankens.com)
- Maintainer: vitalie (https://www.drupal.org/u/vitalie)
- Maintainer: jenlampton (https://www.drupal.org/u/jenlampton)
- Maintainer D7: lolandese (https://www.drupal.org/u/lolandese)
