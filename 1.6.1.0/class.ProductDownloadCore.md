Class ProductDownloadCore
=====================





* Class name: ProductDownloadCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/ProductDownload.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L27)


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
* [$cache_objects](#property-$cache_objects)
* [$db](#property-$db)
* [$def](#property-$def)
* [$fieldsRequired](#property-$fieldsRequired)
* [$fieldsRequiredDatabase](#property-$fieldsRequiredDatabase)
* [$fieldsRequiredLang](#property-$fieldsRequiredLang)
* [$fieldsSize](#property-$fieldsSize)
* [$fieldsSizeLang](#property-$fieldsSizeLang)
* [$fieldsValidate](#property-$fieldsValidate)
* [$fieldsValidateLang](#property-$fieldsValidateLang)
* [$force_id](#property-$force_id)
* [$get_shop_from_context](#property-$get_shop_from_context)
* [$id](#property-$id)
* [$id_lang](#property-$id_lang)
* [$id_shop](#property-$id_shop)
* [$id_shop_list](#property-$id_shop_list)
* [$identifier](#property-$identifier)
* [$image_dir](#property-$image_dir)
* [$image_format](#property-$image_format)
* [$loaded_classes](#property-$loaded_classes)
* [$table](#property-$table)
* [$tables](#property-$tables)
* [$update_fields](#property-$update_fields)
* [$webserviceParameters](#property-$webserviceParameters)

### Methods

* [__construct](#method-__construct)
* [add](#method-add)
* [addFieldsRequiredDatabase](#method-addFieldsRequiredDatabase)
* [associateTo](#method-associateTo)
* [cacheFieldsRequiredDatabase](#method-cacheFieldsRequiredDatabase)
* [checkFile](#method-checkFile)
* [checkWritableDir](#method-checkWritableDir)
* [clearCache](#method-clearCache)
* [delete](#method-delete)
* [deleteFile](#method-deleteFile)
* [deleteImage](#method-deleteImage)
* [deleteSelection](#method-deleteSelection)
* [disableCache](#method-disableCache)
* [displayFieldName](#method-displayFieldName)
* [duplicateObject](#method-duplicateObject)
* [duplicateShops](#method-duplicateShops)
* [enableCache](#method-enableCache)
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
* [getRepositoryClassName](#method-getRepositoryClassName)
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
* [isMultiShopField](#method-isMultiShopField)
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
* [validateFieldsRequiredDatabase](#method-validateFieldsRequiredDatabase)




Properties
----------


### <a name="property-$_productIds"></a>$_productIds

```php
protected mixed $_productIds = array()
```





* Visibility: **protected**
* This property is **static**.
* Source: [classes/ProductDownload.php line 56](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L56).


### <a name="property-$active"></a>$active

```php
public boolean $active = 1
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 51](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L51).


### <a name="property-$date_add"></a>$date_add

```php
public string $date_add
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 39](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L39).


### <a name="property-$date_expiration"></a>$date_expiration

```php
public string $date_expiration
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 42](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L42).


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'product_download', 'primary' => 'id_product_download', 'fields' => array('id_product' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'display_filename' => array('type' => self::TYPE_STRING, 'validate' => 'isGenericName', 'size' => 255), 'filename' => array('type' => self::TYPE_STRING, 'validate' => 'isSha1', 'size' => 255), 'date_add' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'date_expiration' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'nb_days_accessible' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt', 'size' => 10), 'nb_downloadable' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt', 'size' => 10), 'active' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool'), 'is_shareable' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool')))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/ProductDownload.php line 61](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L61).


### <a name="property-$display_filename"></a>$display_filename

```php
public string $display_filename
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 33](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L33).


### <a name="property-$filename"></a>$filename

```php
public string $filename
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 36](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L36).


### <a name="property-$id_product"></a>$id_product

```php
public integer $id_product
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 30](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L30).


### <a name="property-$is_shareable"></a>$is_shareable

```php
public boolean $is_shareable
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 54](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L54).


### <a name="property-$nb_days_accessible"></a>$nb_days_accessible

```php
public string $nb_days_accessible
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 45](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L45).


### <a name="property-$nb_downloadable"></a>$nb_downloadable

```php
public string $nb_downloadable
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L48).


### <a name="property-$cache_objects"></a>$cache_objects

```php
protected boolean $cache_objects = true
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 164](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L164).


### <a name="property-$db"></a>$db

```php
protected \Db $db = false
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 156](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L156).


### <a name="property-$def"></a>$def

```php
protected array $def
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 150](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L150).


### <a name="property-$fieldsRequired"></a>$fieldsRequired

```php
protected array $fieldsRequired = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 88](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L88).


### <a name="property-$fieldsRequiredDatabase"></a>$fieldsRequiredDatabase

```php
protected array $fieldsRequiredDatabase = null
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 70](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L70).


### <a name="property-$fieldsRequiredLang"></a>$fieldsRequiredLang

```php
protected array $fieldsRequiredLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 106](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L106).


### <a name="property-$fieldsSize"></a>$fieldsSize

```php
protected array $fieldsSize = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 94](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L94).


### <a name="property-$fieldsSizeLang"></a>$fieldsSizeLang

```php
protected array $fieldsSizeLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 112](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L112).


### <a name="property-$fieldsValidate"></a>$fieldsValidate

```php
protected array $fieldsValidate = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 100](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L100).


### <a name="property-$fieldsValidateLang"></a>$fieldsValidateLang

```php
protected array $fieldsValidateLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 118](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L118).


### <a name="property-$force_id"></a>$force_id

```php
public boolean $force_id = false
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 159](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L159).


### <a name="property-$get_shop_from_context"></a>$get_shop_from_context

```php
protected boolean $get_shop_from_context = true
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 67](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L67).


### <a name="property-$id"></a>$id

```php
public integer $id
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 55](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L55).


### <a name="property-$id_lang"></a>$id_lang

```php
protected integer $id_lang = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 58](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L58).


### <a name="property-$id_shop"></a>$id_shop

```php
protected integer $id_shop = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 61](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L61).


### <a name="property-$id_shop_list"></a>$id_shop_list

```php
public array $id_shop_list = null
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 64](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L64).


### <a name="property-$identifier"></a>$identifier

```php
protected string $identifier
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 82](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L82).


### <a name="property-$image_dir"></a>$image_dir

```php
protected string $image_dir = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 130](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L130).


### <a name="property-$image_format"></a>$image_format

```php
protected String $image_format = 'jpg'
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 133](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L133).


### <a name="property-$loaded_classes"></a>$loaded_classes

```php
protected array $loaded_classes = array()
```

Holds compiled definitions of each ObjectModel class.

Values are assigned during object initialization.

* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 147](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L147).


### <a name="property-$table"></a>$table

```php
protected string $table
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 76](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L76).


### <a name="property-$tables"></a>$tables

```php
protected array $tables = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 124](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L124).


### <a name="property-$update_fields"></a>$update_fields

```php
protected array $update_fields = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 153](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L153).


### <a name="property-$webserviceParameters"></a>$webserviceParameters

```php
protected array $webserviceParameters = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 127](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L127).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed ProductDownloadCore::__construct(integer $id_product_download)
```

Build a virtual product



* Visibility: **public**
* Source: [classes/ProductDownload.php line 82](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L82)


#### Arguments
* $id_product_download **integer** - Existing productDownload id in order to load object (optional)



### <a name="method-add"></a>add

```php
mixed ProductDownloadCore::add($autodate, $null_values)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 101](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L101)


#### Arguments
* $autodate **mixed**
* $null_values **mixed**



### <a name="method-addFieldsRequiredDatabase"></a>addFieldsRequiredDatabase

```php
boolean ObjectModelCore::addFieldsRequiredDatabase(array $fields)
```

Sets required field for this class in the database.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1340](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1340)


#### Arguments
* $fields **array**



### <a name="method-associateTo"></a>associateTo

```php
boolean|void ObjectModelCore::associateTo(integer|array $id_shops)
```

This function associate an item to its context



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1408](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1408)


#### Arguments
* $id_shops **integer|array**



### <a name="method-cacheFieldsRequiredDatabase"></a>cacheFieldsRequiredDatabase

```php
mixed ObjectModelCore::cacheFieldsRequiredDatabase(boolean $all)
```

Caches data about required objects fields in memory



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1319](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1319)


#### Arguments
* $all **boolean** - If true, caches required fields of all object classes.



### <a name="method-checkFile"></a>checkFile

```php
boolean ProductDownloadCore::checkFile()
```

Check if file exists



* Visibility: **public**
* Source: [classes/ProductDownload.php line 145](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L145)




### <a name="method-checkWritableDir"></a>checkWritableDir

```php
boolean ProductDownloadCore::checkWritableDir()
```

Check if download repository is writable



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 156](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L156)




### <a name="method-clearCache"></a>clearCache

```php
mixed ObjectModelCore::clearCache(boolean $all)
```

Clears cache entries that have this object's ID.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1360](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1360)


#### Arguments
* $all **boolean** - If true, clears cache for all objects



### <a name="method-delete"></a>delete

```php
mixed ProductDownloadCore::delete($delete_file)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 117](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L117)


#### Arguments
* $delete_file **mixed**



### <a name="method-deleteFile"></a>deleteFile

```php
boolean ProductDownloadCore::deleteFile(integer $id_product_download)
```

Delete the file



* Visibility: **public**
* Source: [classes/ProductDownload.php line 131](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L131)


#### Arguments
* $id_product_download **integer** - : if we need to delete a specific product attribute file



### <a name="method-deleteImage"></a>deleteImage

```php
boolean ObjectModelCore::deleteImage(boolean $force_delete)
```

Delete images associated with the object



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1585](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1585)


#### Arguments
* $force_delete **boolean**



### <a name="method-deleteSelection"></a>deleteSelection

```php
boolean ObjectModelCore::deleteSelection(array $ids)
```

Deletes multiple objects from the database at once



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 765](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L765)


#### Arguments
* $ids **array** - Array of objects IDs.



### <a name="method-disableCache"></a>disableCache

```php
mixed ObjectModelCore::disableCache()
```

Disables object caching



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1892](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1892)




### <a name="method-displayFieldName"></a>displayFieldName

```php
string ObjectModelCore::displayFieldName(string $field, string $class, boolean $htmlentities, \Context|null $context)
```

Returns field name translation



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1051](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1051)


#### Arguments
* $field **string** - Field name
* $class **string** - ObjectModel class name
* $htmlentities **boolean** - If true, applies htmlentities() to result string
* $context **[Context](class.ContextCore.md)|null** - Context object



### <a name="method-duplicateObject"></a>duplicateObject

```php
\ObjectModel|false ObjectModelCore::duplicateObject()
```

Takes current object ID, gets its values from database,
saves them in a new row and loads newly saved values as a new object.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 534](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L534)




### <a name="method-duplicateShops"></a>duplicateShops

```php
boolean|void ObjectModelCore::duplicateShops($id)
```

Copies shop association data from object with specified ID.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1462](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1462)


#### Arguments
* $id **mixed**



### <a name="method-enableCache"></a>enableCache

```php
mixed ObjectModelCore::enableCache()
```

Enables object caching



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1884](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1884)




### <a name="method-existsInDatabase"></a>existsInDatabase

```php
boolean ObjectModelCore::existsInDatabase(integer $id_entity, string $table)
```

Checks if an object exists in database.



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1624](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1624)


#### Arguments
* $id_entity **integer**
* $table **string**



### <a name="method-formatFields"></a>formatFields

```php
array ObjectModelCore::formatFields(integer $type, integer $id_lang)
```

Formats values of each fields.



* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 322](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L322)


#### Arguments
* $type **integer** - FORMAT_COMMON or FORMAT_LANG or FORMAT_SHOP
* $id_lang **integer** - If this parameter is given, only take lang fields



### <a name="method-formatValue"></a>formatValue

```php
mixed ObjectModelCore::formatValue(mixed $value, integer $type, boolean $with_quotes, boolean $purify, boolean $allow_null)
```

Formats a value



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 373](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L373)


#### Arguments
* $value **mixed**
* $type **integer**
* $with_quotes **boolean**
* $purify **boolean**
* $allow_null **boolean**



### <a name="method-getAssociatedShops"></a>getAssociatedShops

```php
array ObjectModelCore::getAssociatedShops()
```

Gets the list of associated shop IDs



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1440](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1440)




### <a name="method-getDeadline"></a>getDeadline

```php
string ProductDownloadCore::getDeadline()
```

Return a deadline



* Visibility: **public**
* Source: [classes/ProductDownload.php line 269](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L269)




### <a name="method-getDefinition"></a>getDefinition

```php
array ObjectModelCore::getDefinition(string $class, string|null $field)
```

Returns object definition



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1740](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1740)


#### Arguments
* $class **string** - Name of object
* $field **string|null** - Name of field if we want the definition of one field only



### <a name="method-getFieldByLang"></a>getFieldByLang

```php
mixed ObjectModelCore::getFieldByLang(string $field_name, integer|null $id_lang)
```

Return the field value for the specified language if the field is multilang,
else the field value.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1849](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1849)


#### Arguments
* $field_name **string**
* $id_lang **integer|null**



### <a name="method-getFields"></a>getFields

```php
array ProductDownloadCore::getFields()
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 92](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L92)




### <a name="method-getFieldsLang"></a>getFieldsLang

```php
array ObjectModelCore::getFieldsLang()
```

Prepare multilang fields



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 284](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L284)




### <a name="method-getFieldsRequiredDatabase"></a>getFieldsRequiredDatabase

```php
array|null ObjectModelCore::getFieldsRequiredDatabase(boolean $all)
```

Returns an array of required fields



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1306](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1306)


#### Arguments
* $all **boolean** - If true, returns required fields of all object classes.



### <a name="method-getFieldsShop"></a>getFieldsShop

```php
array ObjectModelCore::getFieldsShop()
```

Prepare fields for multishop
Fields are not validated here, we consider they are already validated in getFields() method,
this is not the best solution but this is the only one possible for retro compatibility.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 267](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L267)




### <a name="method-getFilenameFromFilename"></a>getFilenameFromFilename

```php
string ProductDownloadCore::getFilenameFromFilename(string $filename)
```

Return the display filename from a physical filename



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 222](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L222)


#### Arguments
* $filename **string** - Filename physically



### <a name="method-getFilenameFromIdProduct"></a>getFilenameFromIdProduct

```php
string ProductDownloadCore::getFilenameFromIdProduct(integer $id_product)
```

Return the filename from an id_product



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 206](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L206)


#### Arguments
* $id_product **integer** - Product the id



### <a name="method-getHash"></a>getHash

```php
string ProductDownloadCore::getHash()
```

Return a hash for control download access



* Visibility: **public**
* Source: [classes/ProductDownload.php line 282](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L282)




### <a name="method-getHtmlLink"></a>getHtmlLink

```php
string ProductDownloadCore::getHtmlLink(string $class, boolean $admin, boolean $hash)
```

Return html link



* Visibility: **public**
* Source: [classes/ProductDownload.php line 254](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L254)


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
* Source: [classes/ProductDownload.php line 192](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L192)


#### Arguments
* $filename **string** - Filename physically



### <a name="method-getIdFromIdProduct"></a>getIdFromIdProduct

```php
integer ProductDownloadCore::getIdFromIdProduct(integer $id_product)
```

Return the id_product_download from an id_product



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 167](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L167)


#### Arguments
* $id_product **integer** - Product the id



### <a name="method-getNewFilename"></a>getNewFilename

```php
string ProductDownloadCore::getNewFilename()
```

Return a sha1 filename



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 293](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L293)




### <a name="method-getRepositoryClassName"></a>getRepositoryClassName

```php
mixed ObjectModelCore::getRepositoryClassName()
```

Returns the name of the repository class for this entity.

If unspecified, a generic repository will be used for the entity.

* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 166](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L166)




### <a name="method-getTextLink"></a>getTextLink

```php
string ProductDownloadCore::getTextLink(boolean $admin, string $hash)
```

Return html link



* Visibility: **public**
* Source: [classes/ProductDownload.php line 238](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L238)


#### Arguments
* $admin **boolean** - specific to backend (optionnal)
* $hash **string** - hash code in table order detail (optionnal)



### <a name="method-getTranslationsFields"></a>getTranslationsFields

```php
array ObjectModelCore::getTranslationsFields(array $fields_array)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 806](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L806)


#### Arguments
* $fields_array **array**



### <a name="method-getValidationRules"></a>getValidationRules

```php
array ObjectModelCore::getValidationRules(string $class)
```

Returns object validation rules (fields validity)



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 178](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L178)


#### Arguments
* $class **string** - Child class name for static use (optional)



### <a name="method-getWebserviceObjectList"></a>getWebserviceObjectList

```php
array|null ObjectModelCore::getWebserviceObjectList(string $sql_join, string $sql_filter, string $sql_sort, string $sql_limit)
```

Returns webservice object list.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1230](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1230)


#### Arguments
* $sql_join **string**
* $sql_filter **string**
* $sql_sort **string**
* $sql_limit **string**



### <a name="method-getWebserviceParameters"></a>getWebserviceParameters

```php
array ObjectModelCore::getWebserviceParameters(string|null $ws_params_attribute_name)
```

Returns webservice parameters of this object.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1140](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1140)


#### Arguments
* $ws_params_attribute_name **string|null**



### <a name="method-hasMultishopEntries"></a>hasMultishopEntries

```php
boolean ObjectModelCore::hasMultishopEntries()
```

Checks if there is more than one entry in associated shop table for current object.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1488](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1488)




### <a name="method-hydrate"></a>hydrate

```php
mixed ObjectModelCore::hydrate(array $data, integer|null $id_lang)
```

Fill an object with given data. Data must be an array with this syntax:
array(objProperty => value, objProperty2 => value, etc.)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1666](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1666)


#### Arguments
* $data **array**
* $id_lang **integer|null**



### <a name="method-hydrateCollection"></a>hydrateCollection

```php
array ObjectModelCore::hydrateCollection(string $class, array $datas, integer|null $id_lang)
```

Fill (hydrate) a list of objects in order to get a collection of these objects



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1688](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1688)


#### Arguments
* $class **string** - Class of objects to hydrate
* $datas **array** - List of data (multi-dimensional array)
* $id_lang **integer|null**



### <a name="method-isAssociatedToShop"></a>isAssociatedToShop

```php
boolean ObjectModelCore::isAssociatedToShop(integer|null $id_shop)
```

Checks if current object is associated to a shop.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1375](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1375)


#### Arguments
* $id_shop **integer|null**



### <a name="method-isCurrentlyUsed"></a>isCurrentlyUsed

```php
boolean ObjectModelCore::isCurrentlyUsed(string|null $table, boolean $has_active_column)
```

Checks if an object type exists in the database.



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1644](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1644)


#### Arguments
* $table **string|null** - Name of table linked to entity
* $has_active_column **boolean** - True if the table has an active column



### <a name="method-isFeatureActive"></a>isFeatureActive

```php
boolean ProductDownloadCore::isFeatureActive()
```

This method is allow to know if a feature is used or active



* Visibility: **public**
* This method is **static**.
* Source: [classes/ProductDownload.php line 306](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L306)




### <a name="method-isLangMultishop"></a>isLangMultishop

```php
boolean ObjectModelCore::isLangMultishop()
```

Checks if the object is both multi-language and multi-shop.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1523](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1523)




### <a name="method-isMultiShopField"></a>isMultiShopField

```php
boolean ObjectModelCore::isMultiShopField(string $field)
```

Checks if a field is a multi-shop field.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1513](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1513)


#### Arguments
* $field **string**



### <a name="method-isMultishop"></a>isMultishop

```php
boolean ObjectModelCore::isMultishop()
```

Checks if object is multi-shop object.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1501](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1501)




### <a name="method-makeTranslationFields"></a>makeTranslationFields

```php
mixed ObjectModelCore::makeTranslationFields(array $fields, array $fields_array, integer $id_language)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 827](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L827)


#### Arguments
* $fields **array**
* $fields_array **array**
* $id_language **integer**



### <a name="method-save"></a>save

```php
boolean ObjectModelCore::save(boolean $null_values, boolean $auto_date)
```

Saves current object to database (add or update)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 429](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L429)


#### Arguments
* $null_values **boolean**
* $auto_date **boolean**



### <a name="method-setDefinitionRetrocompatibility"></a>setDefinitionRetrocompatibility

```php
mixed ObjectModelCore::setDefinitionRetrocompatibility()
```

Retrocompatibility for classes without $definition static



* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1778](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1778)




### <a name="method-setFieldsToUpdate"></a>setFieldsToUpdate

```php
mixed ObjectModelCore::setFieldsToUpdate(array $fields)
```

Set a list of specific fields to update
array(field1 => true, field2 => false,
langfield1 => array(1 => true, 2 => false))



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1876](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1876)


#### Arguments
* $fields **array**



### <a name="method-toggleStatus"></a>toggleStatus

```php
boolean ObjectModelCore::toggleStatus()
```

Toggles object status in database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 783](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L783)




### <a name="method-update"></a>update

```php
mixed ProductDownloadCore::update($null_values)
```





* Visibility: **public**
* Source: [classes/ProductDownload.php line 106](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ProductDownload.php#L106)


#### Arguments
* $null_values **mixed**



### <a name="method-updateMultishopTable"></a>updateMultishopTable

```php
boolean ObjectModelCore::updateMultishopTable(string $classname, array $data, string $where, string $specific_where)
```

Updates a table and splits the common datas and the shop datas.



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1539](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1539)


#### Arguments
* $classname **string**
* $data **array**
* $where **string**
* $specific_where **string** - Only executed for common table



### <a name="method-validateControler"></a>validateControler

```php
array ObjectModelCore::validateControler(boolean $htmlentities)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1071](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1071)


#### Arguments
* $htmlentities **boolean**



### <a name="method-validateController"></a>validateController

```php
array ObjectModelCore::validateController(boolean $htmlentities)
```

Validates submitted values and returns an array of errors, if any.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1084](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1084)


#### Arguments
* $htmlentities **boolean** - If true, uses htmlentities() for field name translations in errors.



### <a name="method-validateField"></a>validateField

```php
true|string ObjectModelCore::validateField(string $field, mixed $value, integer|null $id_lang, array $skip, boolean $human_errors)
```

Validate a single field



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 946](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L946)


#### Arguments
* $field **string** - Field name
* $value **mixed** - Field value
* $id_lang **integer|null** - Language ID
* $skip **array** - Array of fields to skip.
* $human_errors **boolean** - If true, uses more descriptive, translatable error strings.



### <a name="method-validateFields"></a>validateFields

```php
boolean|string ObjectModelCore::validateFields(boolean $die, boolean $error_return)
```

Checks if object field values are valid before database interaction



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 867](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L867)


#### Arguments
* $die **boolean**
* $error_return **boolean**



### <a name="method-validateFieldsLang"></a>validateFieldsLang

```php
boolean|string ObjectModelCore::validateFieldsLang(boolean $die, boolean $error_return)
```

Checks if multilingual object field values are valid before database interaction.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 898](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L898)


#### Arguments
* $die **boolean**
* $error_return **boolean**



### <a name="method-validateFieldsRequiredDatabase"></a>validateFieldsRequiredDatabase

```php
array ObjectModelCore::validateFieldsRequiredDatabase(boolean $htmlentities)
```

Validate required fields.



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1275](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.0/classes/ObjectModel.php#L1275)


#### Arguments
* $htmlentities **boolean**


