Class ProductDownloadCore
=====================





* Class name: ProductDownloadCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/ProductDownload.php line 28](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L28)


Contents
--------


### Properties

* [$_productIds](#property-$_productIds)
* [$active](#property-$active)
* [$date_add](#property-$date_add)
* [$date_expiration](#property-$date_expiration)
* [$definition](#property-$definition)
* [$display_filename](#property-$display_filename)
* [$filename](#property-$filename)
* [$id_product](#property-$id_product)
* [$is_shareable](#property-$is_shareable)
* [$nb_days_accessible](#property-$nb_days_accessible)
* [$nb_downloadable](#property-$nb_downloadable)
* [$def](#property-$def)
* [$fieldsRequired](#property-$fieldsRequired)
* [$fieldsRequiredDatabase](#property-$fieldsRequiredDatabase)
* [$fieldsRequiredLang](#property-$fieldsRequiredLang)
* [$fieldsSize](#property-$fieldsSize)
* [$fieldsSizeLang](#property-$fieldsSizeLang)
* [$fieldsValidate](#property-$fieldsValidate)
* [$fieldsValidateLang](#property-$fieldsValidateLang)
* [$get_shop_from_context](#property-$get_shop_from_context)
* [$id](#property-$id)
* [$id_lang](#property-$id_lang)
* [$id_shop](#property-$id_shop)
* [$id_shop_list](#property-$id_shop_list)
* [$identifier](#property-$identifier)
* [$image_dir](#property-$image_dir)
* [$image_format](#property-$image_format)
* [$table](#property-$table)
* [$tables](#property-$tables)
* [$update_fields](#property-$update_fields)
* [$webserviceParameters](#property-$webserviceParameters)

### Methods

* [__construct](#method-__construct)
* [add](#method-add)
* [addFieldsRequiredDatabase](#method-addFieldsRequiredDatabase)
* [associateTo](#method-associateTo)
* [checkFile](#method-checkFile)
* [checkWritableDir](#method-checkWritableDir)
* [clearCache](#method-clearCache)
* [delete](#method-delete)
* [deleteFile](#method-deleteFile)
* [deleteImage](#method-deleteImage)
* [deleteSelection](#method-deleteSelection)
* [displayFieldName](#method-displayFieldName)
* [duplicateShops](#method-duplicateShops)
* [existsInDatabase](#method-existsInDatabase)
* [formatFields](#method-formatFields)
* [formatValue](#method-formatValue)
* [getAssociatedShops](#method-getAssociatedShops)
* [getDeadline](#method-getDeadline)
* [getDefinition](#method-getDefinition)
* [getFieldByLang](#method-getFieldByLang)
* [getFields](#method-getFields)
* [getFieldsLang](#method-getFieldsLang)
* [getFieldsRequiredDatabase](#method-getFieldsRequiredDatabase)
* [getFieldsShop](#method-getFieldsShop)
* [getFilenameFromFilename](#method-getFilenameFromFilename)
* [getFilenameFromIdProduct](#method-getFilenameFromIdProduct)
* [getHash](#method-getHash)
* [getHtmlLink](#method-getHtmlLink)
* [getIdFromFilename](#method-getIdFromFilename)
* [getIdFromIdProduct](#method-getIdFromIdProduct)
* [getNewFilename](#method-getNewFilename)
* [getTextLink](#method-getTextLink)
* [getTranslationsFields](#method-getTranslationsFields)
* [getValidationRules](#method-getValidationRules)
* [getWebserviceObjectList](#method-getWebserviceObjectList)
* [getWebserviceParameters](#method-getWebserviceParameters)
* [hasMultishopEntries](#method-hasMultishopEntries)
* [hydrate](#method-hydrate)
* [hydrateCollection](#method-hydrateCollection)
* [isAssociatedToShop](#method-isAssociatedToShop)
* [isCurrentlyUsed](#method-isCurrentlyUsed)
* [isFeatureActive](#method-isFeatureActive)
* [isLangMultishop](#method-isLangMultishop)
* [isMultishop](#method-isMultishop)
* [makeTranslationFields](#method-makeTranslationFields)
* [save](#method-save)
* [setDefinitionRetrocompatibility](#method-setDefinitionRetrocompatibility)
* [setFieldsToUpdate](#method-setFieldsToUpdate)
* [toggleStatus](#method-toggleStatus)
* [update](#method-update)
* [updateMultishopTable](#method-updateMultishopTable)
* [validateControler](#method-validateControler)
* [validateController](#method-validateController)
* [validateField](#method-validateField)
* [validateFields](#method-validateFields)
* [validateFieldsLang](#method-validateFieldsLang)




Properties
----------


### <a name="property-$_productIds"></a>$_productIds

```php
protected mixed $_productIds = array()
```





* Visibility: **protected**
* This property is **static**.
* Source: [classes/ProductDownload.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L57).


### <a name="property-$active"></a>$active

```php
public boolean $active = 1
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 52](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L52).


### <a name="property-$date_add"></a>$date_add

```php
public string $date_add
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 40](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L40).


### <a name="property-$date_expiration"></a>$date_expiration

```php
public string $date_expiration
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 43](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L43).


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'product_download', 'primary' => 'id_product_download', 'fields' => array('id_product' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'display_filename' => array('type' => self::TYPE_STRING, 'validate' => 'isGenericName', 'size' => 255), 'filename' => array('type' => self::TYPE_STRING, 'validate' => 'isSha1', 'size' => 255), 'date_add' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'date_expiration' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'nb_days_accessible' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt', 'size' => 10), 'nb_downloadable' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt', 'size' => 10), 'active' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool'), 'is_shareable' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool')))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/ProductDownload.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L62).


### <a name="property-$display_filename"></a>$display_filename

```php
public string $display_filename
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 34](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L34).


### <a name="property-$filename"></a>$filename

```php
public string $filename
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L37).


### <a name="property-$id_product"></a>$id_product

```php
public integer $id_product
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 31](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L31).


### <a name="property-$is_shareable"></a>$is_shareable

```php
public boolean $is_shareable
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 55](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L55).


### <a name="property-$nb_days_accessible"></a>$nb_days_accessible

```php
public string $nb_days_accessible
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 46](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L46).


### <a name="property-$nb_downloadable"></a>$nb_downloadable

```php
public string $nb_downloadable
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 49](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L49).


### <a name="property-$def"></a>$def

```php
protected array $def
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 131](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L131).


### <a name="property-$fieldsRequired"></a>$fieldsRequired

```php
protected mixed $fieldsRequired = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 81](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L81).


### <a name="property-$fieldsRequiredDatabase"></a>$fieldsRequiredDatabase

```php
protected mixed $fieldsRequiredDatabase = null
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 66](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L66).


### <a name="property-$fieldsRequiredLang"></a>$fieldsRequiredLang

```php
protected mixed $fieldsRequiredLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 96](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L96).


### <a name="property-$fieldsSize"></a>$fieldsSize

```php
protected mixed $fieldsSize = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 86](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L86).


### <a name="property-$fieldsSizeLang"></a>$fieldsSizeLang

```php
protected mixed $fieldsSizeLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 101](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L101).


### <a name="property-$fieldsValidate"></a>$fieldsValidate

```php
protected mixed $fieldsValidate = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 91](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L91).


### <a name="property-$fieldsValidateLang"></a>$fieldsValidateLang

```php
protected mixed $fieldsValidateLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 106](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L106).


### <a name="property-$get_shop_from_context"></a>$get_shop_from_context

```php
protected mixed $get_shop_from_context = true
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 64](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L64).


### <a name="property-$id"></a>$id

```php
public integer $id
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 55](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L55).


### <a name="property-$id_lang"></a>$id_lang

```php
protected integer $id_lang = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 58](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L58).


### <a name="property-$id_shop"></a>$id_shop

```php
protected mixed $id_shop = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 60](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L60).


### <a name="property-$id_shop_list"></a>$id_shop_list

```php
public mixed $id_shop_list = null
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L62).


### <a name="property-$identifier"></a>$identifier

```php
protected mixed $identifier
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 76](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L76).


### <a name="property-$image_dir"></a>$image_dir

```php
protected string $image_dir = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 117](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L117).


### <a name="property-$image_format"></a>$image_format

```php
protected string $image_format = 'jpg'
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 120](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L120).


### <a name="property-$table"></a>$table

```php
protected mixed $table
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 71](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L71).


### <a name="property-$tables"></a>$tables

```php
protected mixed $tables = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 111](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L111).


### <a name="property-$update_fields"></a>$update_fields

```php
protected array $update_fields = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 136](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L136).


### <a name="property-$webserviceParameters"></a>$webserviceParameters

```php
protected array $webserviceParameters = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 114](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L114).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed ProductDownloadCore::__construct(integer $id_product_download)
```

Build a virtual product



* Visibility: **public**
* Source: [classes/ProductDownload.php line 83](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L83)


#### Arguments
* $id_product_download **integer** - Existing productDownload id in order to load object (optional)



### <a name="method-add"></a>add

```php
mixed ProductDownloadCore::add($autodate, $null_values)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 102](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L102)


#### Arguments
* $autodate **mixed**
* $null_values **mixed**



### <a name="method-addFieldsRequiredDatabase"></a>addFieldsRequiredDatabase

```php
mixed ObjectModelCore::addFieldsRequiredDatabase($fields)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1040](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1040)


#### Arguments
* $fields **mixed**



### <a name="method-associateTo"></a>associateTo

```php
boolean ObjectModelCore::associateTo(integer|array $id_shops)
```

This function associate an item to its context



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1087](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1087)


#### Arguments
* $id_shops **integer|array**



### <a name="method-checkFile"></a>checkFile

```php
boolean ProductDownloadCore::checkFile()
```

Check if file exists



* Visibility: **public**
* Source: [classes/ProductDownload.php line 153](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L153)




### <a name="method-checkWritableDir"></a>checkWritableDir

```php
boolean ProductDownloadCore::checkWritableDir()
```

Check if download repository is writable



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 164](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L164)




### <a name="method-clearCache"></a>clearCache

```php
mixed ObjectModelCore::clearCache($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1054](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1054)


#### Arguments
* $all **mixed**



### <a name="method-delete"></a>delete

```php
mixed ProductDownloadCore::delete($delete)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 125](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L125)


#### Arguments
* $delete **mixed**



### <a name="method-deleteFile"></a>deleteFile

```php
boolean ProductDownloadCore::deleteFile(integer $id_product_download)
```

Delete the file



* Visibility: **public**
* Source: [classes/ProductDownload.php line 139](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L139)


#### Arguments
* $id_product_download **integer** - : if we need to delete a specific product attribute file



### <a name="method-deleteImage"></a>deleteImage

```php
boolean ObjectModelCore::deleteImage()
```

Delete images associated with the object



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1214](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1214)




### <a name="method-deleteSelection"></a>deleteSelection

```php
boolean ObjectModelCore::deleteSelection(array $selection)
```

Delete several objects from database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 669](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L669)


#### Arguments
* $selection **array**



### <a name="method-displayFieldName"></a>displayFieldName

```php
mixed ObjectModelCore::displayFieldName($field, $class, $htmlentities, \Context $context)
```





* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 869](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L869)


#### Arguments
* $field **mixed**
* $class **mixed**
* $htmlentities **mixed**
* $context **[Context](class.ContextCore.md)**



### <a name="method-duplicateShops"></a>duplicateShops

```php
mixed ObjectModelCore::duplicateShops($id)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1131](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1131)


#### Arguments
* $id **mixed**



### <a name="method-existsInDatabase"></a>existsInDatabase

```php
boolean ObjectModelCore::existsInDatabase(integer $id_entity, string $table)
```

Specify if an ObjectModel is already in database



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1248](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1248)


#### Arguments
* $id_entity **integer**
* $table **string**



### <a name="method-formatFields"></a>formatFields

```php
array ObjectModelCore::formatFields(integer $type, integer $id_lang)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 327](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L327)


#### Arguments
* $type **integer** - FORMAT_COMMON or FORMAT_LANG or FORMAT_SHOP
* $id_lang **integer** - If this parameter is given, only take lang fields



### <a name="method-formatValue"></a>formatValue

```php
mixed ObjectModelCore::formatValue(mixed $value, integer $type, $with_quotes)
```

Format a data



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 373](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L373)


#### Arguments
* $value **mixed**
* $type **integer**
* $with_quotes **mixed**



### <a name="method-getAssociatedShops"></a>getAssociatedShops

```php
array ObjectModelCore::getAssociatedShops()
```

Get the list of associated id_shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1116](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1116)




### <a name="method-getDeadline"></a>getDeadline

```php
string ProductDownloadCore::getDeadline()
```

Return a deadline



* Visibility: **public**
* Source: [classes/ProductDownload.php line 277](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L277)




### <a name="method-getDefinition"></a>getDefinition

```php
array ObjectModelCore::getDefinition(string $class, string $field)
```

Get object definition



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1351](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1351)


#### Arguments
* $class **string** - Name of object
* $field **string** - Name of field if we want the definition of one field only



### <a name="method-getFieldByLang"></a>getFieldByLang

```php
mixed ObjectModelCore::getFieldByLang($field_name, null $id_lang)
```

Return the field value for the specified language if the field is multilang, else the field value.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1428](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1428)


#### Arguments
* $field_name **mixed**
* $id_lang **null**



### <a name="method-getFields"></a>getFields

```php
array ProductDownloadCore::getFields()
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 93](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L93)




### <a name="method-getFieldsLang"></a>getFieldsLang

```php
array ObjectModelCore::getFieldsLang()
```

Prepare multilang fields



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 292](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L292)




### <a name="method-getFieldsRequiredDatabase"></a>getFieldsRequiredDatabase

```php
mixed ObjectModelCore::getFieldsRequiredDatabase($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1032](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1032)


#### Arguments
* $all **mixed**



### <a name="method-getFieldsShop"></a>getFieldsShop

```php
array ObjectModelCore::getFieldsShop()
```

Prepare fields for multishop
Fields are not validated here, we considere they are already validated in getFields() method, this
not the best solution but this is the only one possible for retro compatibility.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 278](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L278)




### <a name="method-getFilenameFromFilename"></a>getFilenameFromFilename

```php
string ProductDownloadCore::getFilenameFromFilename(string $filename)
```

Return the display filename from a physical filename



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 230](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L230)


#### Arguments
* $filename **string** - Filename physically



### <a name="method-getFilenameFromIdProduct"></a>getFilenameFromIdProduct

```php
string ProductDownloadCore::getFilenameFromIdProduct(integer $id_product)
```

Return the filename from an id_product



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 214](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L214)


#### Arguments
* $id_product **integer** - Product the id



### <a name="method-getHash"></a>getHash

```php
string ProductDownloadCore::getHash()
```

Return a hash for control download access



* Visibility: **public**
* Source: [classes/ProductDownload.php line 290](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L290)




### <a name="method-getHtmlLink"></a>getHtmlLink

```php
string ProductDownloadCore::getHtmlLink(string $class, boolean $admin, boolean $hash)
```

Return html link



* Visibility: **public**
* Source: [classes/ProductDownload.php line 262](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L262)


#### Arguments
* $class **string** - CSS selector
* $admin **boolean** - specific to backend
* $hash **boolean** - hash code in table order detail



### <a name="method-getIdFromFilename"></a>getIdFromFilename

```php
integer ProductDownloadCore::getIdFromFilename(string $filename)
```

Return the display filename from a physical filename



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 200](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L200)


#### Arguments
* $filename **string** - Filename physically



### <a name="method-getIdFromIdProduct"></a>getIdFromIdProduct

```php
integer ProductDownloadCore::getIdFromIdProduct(integer $id_product)
```

Return the id_product_download from an id_product



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 175](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L175)


#### Arguments
* $id_product **integer** - Product the id



### <a name="method-getNewFilename"></a>getNewFilename

```php
string ProductDownloadCore::getNewFilename()
```

Return a sha1 filename



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 301](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L301)




### <a name="method-getTextLink"></a>getTextLink

```php
string ProductDownloadCore::getTextLink(boolean $admin, string $hash)
```

Return html link



* Visibility: **public**
* Source: [classes/ProductDownload.php line 246](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L246)


#### Arguments
* $admin **boolean** - specific to backend (optionnal)
* $hash **string** - hash code in table order detail (optionnal)



### <a name="method-getTranslationsFields"></a>getTranslationsFields

```php
mixed ObjectModelCore::getTranslationsFields($fields_array)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 701](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L701)


#### Arguments
* $fields_array **mixed**



### <a name="method-getValidationRules"></a>getValidationRules

```php
array ObjectModelCore::getValidationRules(string $class)
```

Returns object validation rules (fields validity)



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 144](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L144)


#### Arguments
* $class **string** - Child class name for static use (optional)



### <a name="method-getWebserviceObjectList"></a>getWebserviceObjectList

```php
mixed ObjectModelCore::getWebserviceObjectList($sql_join, $sql_filter, $sql_sort, $sql_limit)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1005](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1005)


#### Arguments
* $sql_join **mixed**
* $sql_filter **mixed**
* $sql_sort **mixed**
* $sql_limit **mixed**



### <a name="method-getWebserviceParameters"></a>getWebserviceParameters

```php
mixed ObjectModelCore::getWebserviceParameters($ws_params_attribute_name)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 931](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L931)


#### Arguments
* $ws_params_attribute_name **mixed**



### <a name="method-hasMultishopEntries"></a>hasMultishopEntries

```php
boolean ObjectModelCore::hasMultishopEntries()
```

Check if there is entries in associated shop table for current entity



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1156](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1156)




### <a name="method-hydrate"></a>hydrate

```php
mixed ObjectModelCore::hydrate(array $data, integer $id_lang)
```

Fill an object with given data. Data must be an array with this syntax: array(objProperty => value, objProperty2 => value, etc.)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1283](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1283)


#### Arguments
* $data **array**
* $id_lang **integer**



### <a name="method-hydrateCollection"></a>hydrateCollection

```php
array ObjectModelCore::hydrateCollection(string $class, array $datas, integer $id_lang)
```

Fill (hydrate) a list of objects in order to get a collection of these objects



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1302](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1302)


#### Arguments
* $class **string** - Class of objects to hydrate
* $datas **array** - List of data (multi-dimensional array)
* $id_lang **integer**



### <a name="method-isAssociatedToShop"></a>isAssociatedToShop

```php
boolean ObjectModelCore::isAssociatedToShop(integer $id_shop)
```

Check if current object is associated to a shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1069](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1069)


#### Arguments
* $id_shop **integer**



### <a name="method-isCurrentlyUsed"></a>isCurrentlyUsed

```php
boolean ObjectModelCore::isCurrentlyUsed(string $table, boolean $has_active_column)
```

This method is allow to know if a entity is currently used



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1266](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1266)


#### Arguments
* $table **string** - name of table linked to entity
* $has_active_column **boolean** - true if the table has an active column



### <a name="method-isFeatureActive"></a>isFeatureActive

```php
boolean ProductDownloadCore::isFeatureActive()
```

This method is allow to know if a feature is used or active



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 314](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L314)




### <a name="method-isLangMultishop"></a>isLangMultishop

```php
mixed ObjectModelCore::isLangMultishop()
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1169](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1169)




### <a name="method-isMultishop"></a>isMultishop

```php
mixed ObjectModelCore::isMultishop()
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1164](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1164)




### <a name="method-makeTranslationFields"></a>makeTranslationFields

```php
mixed ObjectModelCore::makeTranslationFields($fields, $fields_array, $id_language)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 717](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L717)


#### Arguments
* $fields **mixed**
* $fields_array **mixed**
* $id_language **mixed**



### <a name="method-save"></a>save

```php
boolean ObjectModelCore::save(boolean $null_values, boolean $autodate)
```

Save current object to database (add or update)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 417](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L417)


#### Arguments
* $null_values **boolean**
* $autodate **boolean**



### <a name="method-setDefinitionRetrocompatibility"></a>setDefinitionRetrocompatibility

```php
mixed ObjectModelCore::setDefinitionRetrocompatibility()
```

Retrocompatibility for classes without $definition static
Remove this in 1.6 !



* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1374](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1374)




### <a name="method-setFieldsToUpdate"></a>setFieldsToUpdate

```php
mixed ObjectModelCore::setFieldsToUpdate(array $fields)
```

Set a list of specific fields to update
array(field1 => true, field2 => false, langfield1 => array(1 => true, 2 => false))



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1454](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1454)


#### Arguments
* $fields **array**



### <a name="method-toggleStatus"></a>toggleStatus

```php
boolean ObjectModelCore::toggleStatus()
```

Toggle object status in database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 685](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L685)




### <a name="method-update"></a>update

```php
mixed ProductDownloadCore::update($null_values)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 114](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ProductDownload.php#L114)


#### Arguments
* $null_values **mixed**



### <a name="method-updateMultishopTable"></a>updateMultishopTable

```php
boolean ObjectModelCore::updateMultishopTable(string $classname, array $data, string $where, string $specific_where)
```

Update a table and splits the common datas and the shop datas



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1184](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L1184)


#### Arguments
* $classname **string**
* $data **array**
* $where **string**
* $specific_where **string** - Only executed for common table



### <a name="method-validateControler"></a>validateControler

```php
mixed ObjectModelCore::validateControler($htmlentities)
```

TODO: refactor rename all calls to this to validateController



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 884](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L884)


#### Arguments
* $htmlentities **mixed**



### <a name="method-validateController"></a>validateController

```php
mixed ObjectModelCore::validateController($htmlentities)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 890](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L890)


#### Arguments
* $htmlentities **mixed**



### <a name="method-validateField"></a>validateField

```php
boolean|string ObjectModelCore::validateField(string $field, mixed $value, integer $id_lang)
```

Validate a single field



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 822](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L822)


#### Arguments
* $field **string** - Field name
* $value **mixed** - Field value
* $id_lang **integer**



### <a name="method-validateFields"></a>validateFields

```php
boolean|string ObjectModelCore::validateFields(boolean $die, boolean $error_return)
```

Check for fields validity before database interaction



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 755](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L755)


#### Arguments
* $die **boolean**
* $error_return **boolean**



### <a name="method-validateFieldsLang"></a>validateFieldsLang

```php
boolean|string ObjectModelCore::validateFieldsLang(boolean $die, boolean $error_return)
```

Check for multilingual fields validity before database interaction



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 784](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.13/classes/ObjectModel.php#L784)


#### Arguments
* $die **boolean**
* $error_return **boolean**


