Class SupplyOrderDetailCore
=====================

Represents one product ordered



* Class name: SupplyOrderDetailCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/stock/SupplyOrderDetail.php line 32](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L32)


Contents
--------


### Properties

* [$definition](#property-$definition)
* [$discount_rate](#property-$discount_rate)
* [$discount_value_te](#property-$discount_value_te)
* [$ean13](#property-$ean13)
* [$exchange_rate](#property-$exchange_rate)
* [$id_currency](#property-$id_currency)
* [$id_product](#property-$id_product)
* [$id_product_attribute](#property-$id_product_attribute)
* [$id_supply_order](#property-$id_supply_order)
* [$name](#property-$name)
* [$price_te](#property-$price_te)
* [$price_ti](#property-$price_ti)
* [$price_with_discount_te](#property-$price_with_discount_te)
* [$price_with_order_discount_te](#property-$price_with_order_discount_te)
* [$quantity_expected](#property-$quantity_expected)
* [$quantity_received](#property-$quantity_received)
* [$reference](#property-$reference)
* [$supplier_reference](#property-$supplier_reference)
* [$tax_rate](#property-$tax_rate)
* [$tax_value](#property-$tax_value)
* [$tax_value_with_order_discount](#property-$tax_value_with_order_discount)
* [$unit_price_te](#property-$unit_price_te)
* [$upc](#property-$upc)
* [$webserviceParameters](#property-$webserviceParameters)
* [$def](#property-$def)
* [$fieldsRequired](#property-$fieldsRequired)
* [$fieldsRequiredDatabase](#property-$fieldsRequiredDatabase)
* [$fieldsRequiredLang](#property-$fieldsRequiredLang)
* [$fieldsSize](#property-$fieldsSize)
* [$fieldsSizeLang](#property-$fieldsSizeLang)
* [$fieldsValidate](#property-$fieldsValidate)
* [$fieldsValidateLang](#property-$fieldsValidateLang)
* [$id](#property-$id)
* [$id_lang](#property-$id_lang)
* [$id_shop](#property-$id_shop)
* [$identifier](#property-$identifier)
* [$image_dir](#property-$image_dir)
* [$image_format](#property-$image_format)
* [$table](#property-$table)
* [$tables](#property-$tables)

### Methods

* [__construct](#method-__construct)
* [add](#method-add)
* [addFieldsRequiredDatabase](#method-addFieldsRequiredDatabase)
* [applyGlobalDiscount](#method-applyGlobalDiscount)
* [associateTo](#method-associateTo)
* [calculatePrices](#method-calculatePrices)
* [clearCache](#method-clearCache)
* [delete](#method-delete)
* [deleteImage](#method-deleteImage)
* [deleteSelection](#method-deleteSelection)
* [displayFieldName](#method-displayFieldName)
* [duplicateShops](#method-duplicateShops)
* [existsInDatabase](#method-existsInDatabase)
* [formatFields](#method-formatFields)
* [formatValue](#method-formatValue)
* [getDefinition](#method-getDefinition)
* [getFieldByLang](#method-getFieldByLang)
* [getFields](#method-getFields)
* [getFieldsLang](#method-getFieldsLang)
* [getFieldsRequiredDatabase](#method-getFieldsRequiredDatabase)
* [getTranslationsFields](#method-getTranslationsFields)
* [getValidationRules](#method-getValidationRules)
* [getWebserviceObjectList](#method-getWebserviceObjectList)
* [getWebserviceParameters](#method-getWebserviceParameters)
* [hydrate](#method-hydrate)
* [hydrateCollection](#method-hydrateCollection)
* [isAssociatedToGroupShop](#method-isAssociatedToGroupShop)
* [isAssociatedToShop](#method-isAssociatedToShop)
* [isCurrentlyUsed](#method-isCurrentlyUsed)
* [isLangMultishop](#method-isLangMultishop)
* [makeTranslationFields](#method-makeTranslationFields)
* [save](#method-save)
* [setDefinitionRetrocompatibility](#method-setDefinitionRetrocompatibility)
* [toggleStatus](#method-toggleStatus)
* [update](#method-update)
* [validateControler](#method-validateControler)
* [validateController](#method-validateController)
* [validateField](#method-validateField)
* [validateFields](#method-validateFields)
* [validateFieldsLang](#method-validateFieldsLang)




Properties
----------


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'supply_order_detail', 'primary' => 'id_supply_order_detail', 'fields' => array('id_supply_order' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'id_product' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'id_product_attribute' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'reference' => array('type' => self::TYPE_STRING, 'validate' => 'isReference'), 'supplier_reference' => array('type' => self::TYPE_STRING, 'validate' => 'isReference'), 'name' => array('type' => self::TYPE_STRING, 'validate' => 'isGenericName', 'required' => true), 'ean13' => array('type' => self::TYPE_STRING, 'validate' => 'isEan13'), 'upc' => array('type' => self::TYPE_STRING, 'validate' => 'isUpc'), 'id_currency' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedId', 'required' => true), 'exchange_rate' => array('type' => self::TYPE_FLOAT, 'validate' => 'isFloat', 'required' => true), 'unit_price_te' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'quantity_expected' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt', 'required' => true), 'quantity_received' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'price_te' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'discount_rate' => array('type' => self::TYPE_FLOAT, 'validate' => 'isFloat', 'required' => true), 'discount_value_te' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'price_with_discount_te' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'tax_rate' => array('type' => self::TYPE_FLOAT, 'validate' => 'isFloat', 'required' => true), 'tax_value' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'price_ti' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true), 'tax_value_with_order_discount' => array('type' => self::TYPE_FLOAT, 'validate' => 'isFloat', 'required' => true), 'price_with_order_discount_te' => array('type' => self::TYPE_FLOAT, 'validate' => 'isPrice', 'required' => true)))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/stock/SupplyOrderDetail.php line 149](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L149).


### <a name="property-$discount_rate"></a>$discount_rate

```php
public float $discount_rate
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 108](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L108).


### <a name="property-$discount_value_te"></a>$discount_value_te

```php
public float $discount_value_te
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 113](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L113).


### <a name="property-$ean13"></a>$ean13

```php
public integer $ean13
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 67](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L67).


### <a name="property-$exchange_rate"></a>$exchange_rate

```php
public float $exchange_rate
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 82](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L82).


### <a name="property-$id_currency"></a>$id_currency

```php
public integer $id_currency
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 77](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L77).


### <a name="property-$id_product"></a>$id_product

```php
public integer $id_product
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 42](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L42).


### <a name="property-$id_product_attribute"></a>$id_product_attribute

```php
public integer $id_product_attribute
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 47](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L47).


### <a name="property-$id_supply_order"></a>$id_supply_order

```php
public integer $id_supply_order
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L37).


### <a name="property-$name"></a>$name

```php
public integer $name
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L62).


### <a name="property-$price_te"></a>$price_te

```php
public float $price_te
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 103](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L103).


### <a name="property-$price_ti"></a>$price_ti

```php
public float $price_ti
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 133](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L133).


### <a name="property-$price_with_discount_te"></a>$price_with_discount_te

```php
public float $price_with_discount_te
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 118](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L118).


### <a name="property-$price_with_order_discount_te"></a>$price_with_order_discount_te

```php
public float $price_with_order_discount_te
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 144](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L144).


### <a name="property-$quantity_expected"></a>$quantity_expected

```php
public integer $quantity_expected
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 92](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L92).


### <a name="property-$quantity_received"></a>$quantity_received

```php
public integer $quantity_received
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 97](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L97).


### <a name="property-$reference"></a>$reference

```php
public string $reference
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 52](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L52).


### <a name="property-$supplier_reference"></a>$supplier_reference

```php
public string $supplier_reference
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L57).


### <a name="property-$tax_rate"></a>$tax_rate

```php
public integer $tax_rate
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 123](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L123).


### <a name="property-$tax_value"></a>$tax_value

```php
public float $tax_value
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 128](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L128).


### <a name="property-$tax_value_with_order_discount"></a>$tax_value_with_order_discount

```php
public float $tax_value_with_order_discount
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 138](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L138).


### <a name="property-$unit_price_te"></a>$unit_price_te

```php
public float $unit_price_te
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 87](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L87).


### <a name="property-$upc"></a>$upc

```php
public string $upc
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 72](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L72).


### <a name="property-$webserviceParameters"></a>$webserviceParameters

```php
protected mixed $webserviceParameters = array('objectsNodeName' => 'supply_order_details', 'objectNodeName' => 'supply_order_detail', 'fields' => array('id_supply_order' => array('xlink_resource' => 'supply_orders'), 'id_product' => array('xlink_resource' => 'products'), 'id_product_attribute' => array('xlink_resource' => 'combinations')), 'hidden_fields' => array('id_currency'))
```





* Visibility: **protected**
* Source: [classes/stock/SupplyOrderDetail.php line 181](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L181).


### <a name="property-$def"></a>$def

```php
protected array $def
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 122](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L122).


### <a name="property-$fieldsRequired"></a>$fieldsRequired

```php
protected mixed $fieldsRequired = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 72](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L72).


### <a name="property-$fieldsRequiredDatabase"></a>$fieldsRequiredDatabase

```php
protected mixed $fieldsRequiredDatabase = null
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L57).


### <a name="property-$fieldsRequiredLang"></a>$fieldsRequiredLang

```php
protected mixed $fieldsRequiredLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 87](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L87).


### <a name="property-$fieldsSize"></a>$fieldsSize

```php
protected mixed $fieldsSize = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 77](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L77).


### <a name="property-$fieldsSizeLang"></a>$fieldsSizeLang

```php
protected mixed $fieldsSizeLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 92](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L92).


### <a name="property-$fieldsValidate"></a>$fieldsValidate

```php
protected mixed $fieldsValidate = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 82](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L82).


### <a name="property-$fieldsValidateLang"></a>$fieldsValidateLang

```php
protected mixed $fieldsValidateLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 97](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L97).


### <a name="property-$id"></a>$id

```php
public integer $id
```





* Visibility: **public**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L48).


### <a name="property-$id_lang"></a>$id_lang

```php
protected integer $id_lang = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 51](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L51).


### <a name="property-$id_shop"></a>$id_shop

```php
protected mixed $id_shop = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 53](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L53).


### <a name="property-$identifier"></a>$identifier

```php
protected mixed $identifier
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 67](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L67).


### <a name="property-$image_dir"></a>$image_dir

```php
protected string $image_dir = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 108](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L108).


### <a name="property-$image_format"></a>$image_format

```php
protected string $image_format = 'jpg'
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 111](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L111).


### <a name="property-$table"></a>$table

```php
protected mixed $table
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L62).


### <a name="property-$tables"></a>$tables

```php
protected mixed $tables = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 102](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L102).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed ObjectModelCore::__construct(integer $id, integer $id_lang, integer $id_shop)
```

Build object



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 150](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L150)


#### Arguments
* $id **integer** - Existing object id in order to load object (optional)
* $id_lang **integer** - Required if object is multilingual (optional)
* $id_shop **integer** - ID shop for objects with multishop on langs



### <a name="method-add"></a>add

```php
mixed SupplyOrderDetailCore::add($autodate, $null_values)
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 207](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L207)


#### Arguments
* $autodate **mixed**
* $null_values **mixed**



### <a name="method-addFieldsRequiredDatabase"></a>addFieldsRequiredDatabase

```php
mixed ObjectModelCore::addFieldsRequiredDatabase($fields)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 925](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L925)


#### Arguments
* $fields **mixed**



### <a name="method-applyGlobalDiscount"></a>applyGlobalDiscount

```php
mixed SupplyOrderDetailCore::applyGlobalDiscount($discount_rate)
```

Applies a global order discount rate, for the current product (i.e detail)
Calls ObjectModel::update()



* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 246](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L246)


#### Arguments
* $discount_rate **mixed** - The discount rate in percent (Ex. 5 for 5 percents)



### <a name="method-associateTo"></a>associateTo

```php
boolean ObjectModelCore::associateTo(integer|array $id_shops, string $type)
```

This function associate an item to its context



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 973](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L973)


#### Arguments
* $id_shops **integer|array**
* $type **string**



### <a name="method-calculatePrices"></a>calculatePrices

```php
mixed SupplyOrderDetailCore::calculatePrices()
```

Calculates all prices for this product based on its quantity and unit price
Applies discount if necessary
Calculates tax value, function of tax rate



* Visibility: **protected**
* Source: [classes/stock/SupplyOrderDetail.php line 219](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L219)




### <a name="method-clearCache"></a>clearCache

```php
mixed ObjectModelCore::clearCache($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 939](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L939)


#### Arguments
* $all **mixed**



### <a name="method-delete"></a>delete

```php
boolean ObjectModelCore::delete()
```

Delete current object from database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 521](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L521)




### <a name="method-deleteImage"></a>deleteImage

```php
boolean ObjectModelCore::deleteImage()
```

Delete images associated with the object



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1047](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1047)




### <a name="method-deleteSelection"></a>deleteSelection

```php
boolean ObjectModelCore::deleteSelection(array $selection)
```

Delete several objects from database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 559](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L559)


#### Arguments
* $selection **array**



### <a name="method-displayFieldName"></a>displayFieldName

```php
mixed ObjectModelCore::displayFieldName($field, $class, $htmlentities, \Context $context)
```





* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 757](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L757)


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
* Source: [classes/ObjectModel.php line 1017](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1017)


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
* Source: [classes/ObjectModel.php line 1081](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1081)


#### Arguments
* $id_entity **integer**
* $table **string**



### <a name="method-formatFields"></a>formatFields

```php
array ObjectModelCore::formatFields(integer $id_lang)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 272](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L272)


#### Arguments
* $id_lang **integer** - If this parameter is given, only take lang fields



### <a name="method-formatValue"></a>formatValue

```php
mixed ObjectModelCore::formatValue(mixed $value, integer $type, $with_quotes)
```

Format a data



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 319](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L319)


#### Arguments
* $value **mixed**
* $type **integer**
* $with_quotes **mixed**



### <a name="method-getDefinition"></a>getDefinition

```php
array ObjectModelCore::getDefinition(string $class, string $field)
```

Get object definition



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1184](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1184)


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
* Source: [classes/ObjectModel.php line 1261](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1261)


#### Arguments
* $field_name **mixed**
* $id_lang **null**



### <a name="method-getFields"></a>getFields

```php
array ObjectModelCore::getFields()
```

Prepare fields for ObjectModel class (add, update)
All fields are verified (pSQL, intval.

..)

* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 234](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L234)




### <a name="method-getFieldsLang"></a>getFieldsLang

```php
array ObjectModelCore::getFieldsLang()
```

Prepare multilang fields



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 249](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L249)




### <a name="method-getFieldsRequiredDatabase"></a>getFieldsRequiredDatabase

```php
mixed ObjectModelCore::getFieldsRequiredDatabase($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 917](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L917)


#### Arguments
* $all **mixed**



### <a name="method-getTranslationsFields"></a>getTranslationsFields

```php
mixed ObjectModelCore::getTranslationsFields($fields_array)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 595](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L595)


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
* Source: [classes/ObjectModel.php line 130](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L130)


#### Arguments
* $class **string** - Child class name for static use (optional)



### <a name="method-getWebserviceObjectList"></a>getWebserviceObjectList

```php
mixed ObjectModelCore::getWebserviceObjectList($sql_join, $sql_filter, $sql_sort, $sql_limit)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 890](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L890)


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
* Source: [classes/ObjectModel.php line 816](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L816)


#### Arguments
* $ws_params_attribute_name **mixed**



### <a name="method-hydrate"></a>hydrate

```php
mixed SupplyOrderDetailCore::hydrate(array $data, $id_lang)
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 320](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L320)


#### Arguments
* $data **array**
* $id_lang **mixed**



### <a name="method-hydrateCollection"></a>hydrateCollection

```php
array ObjectModelCore::hydrateCollection(string $class, array $datas, integer $id_lang)
```

Fill (hydrate) a list of objects in order to get a collection of these objects



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1135](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1135)


#### Arguments
* $class **string** - Class of objects to hydrate
* $datas **array** - List of data (multi-dimensional array)
* $id_lang **integer**



### <a name="method-isAssociatedToGroupShop"></a>isAssociatedToGroupShop

```php
boolean ObjectModelCore::isAssociatedToGroupShop(integer $id_group_shop)
```

Check if current object is associated to a group shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1003](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1003)


#### Arguments
* $id_group_shop **integer**



### <a name="method-isAssociatedToShop"></a>isAssociatedToShop

```php
boolean ObjectModelCore::isAssociatedToShop(integer $id_shop)
```

Check if current object is associated to a shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 954](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L954)


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
* Source: [classes/ObjectModel.php line 1099](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1099)


#### Arguments
* $table **string** - name of table linked to entity
* $has_active_column **boolean** - true if the table has an active column



### <a name="method-isLangMultishop"></a>isLangMultishop

```php
mixed ObjectModelCore::isLangMultishop()
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1037](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1037)




### <a name="method-makeTranslationFields"></a>makeTranslationFields

```php
mixed ObjectModelCore::makeTranslationFields($fields, $fields_array, $id_language)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 611](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L611)


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
* Source: [classes/ObjectModel.php line 360](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L360)


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
* Source: [classes/ObjectModel.php line 1207](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L1207)




### <a name="method-toggleStatus"></a>toggleStatus

```php
boolean ObjectModelCore::toggleStatus()
```

Toggle object status in database



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 575](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L575)




### <a name="method-update"></a>update

```php
mixed SupplyOrderDetailCore::update($null_values)
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 197](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L197)


#### Arguments
* $null_values **mixed**



### <a name="method-validateControler"></a>validateControler

```php
mixed ObjectModelCore::validateControler($htmlentities)
```

TODO: refactor rename all calls to this to validateController



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 772](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L772)


#### Arguments
* $htmlentities **mixed**



### <a name="method-validateController"></a>validateController

```php
\$errors SupplyOrderDetailCore::validateController($htmlentities)
```





* Visibility: **public**
* Source: [classes/stock/SupplyOrderDetail.php line 268](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/stock/SupplyOrderDetail.php#L268)


#### Arguments
* $htmlentities **mixed** - Optional



### <a name="method-validateField"></a>validateField

```php
boolean|string ObjectModelCore::validateField(string $field, mixed $value, integer $id_lang)
```

Validate a single field



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 710](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L710)


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
* Source: [classes/ObjectModel.php line 649](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L649)


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
* Source: [classes/ObjectModel.php line 675](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.9/classes/ObjectModel.php#L675)


#### Arguments
* $die **boolean**
* $error_return **boolean**

