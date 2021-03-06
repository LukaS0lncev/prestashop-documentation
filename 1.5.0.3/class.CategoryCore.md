Class CategoryCore
=====================





* Class name: CategoryCore
* Parent class: [ObjectModel](class.ObjectModelCore.md)
* Source: [classes/Category.php line 28](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L28)


Contents
--------


### Properties

* [$_links](#property-$_links)
* [$active](#property-$active)
* [$date_add](#property-$date_add)
* [$date_upd](#property-$date_upd)
* [$definition](#property-$definition)
* [$description](#property-$description)
* [$groupBox](#property-$groupBox)
* [$id](#property-$id)
* [$id_category](#property-$id_category)
* [$id_image](#property-$id_image)
* [$id_parent](#property-$id_parent)
* [$level_depth](#property-$level_depth)
* [$link_rewrite](#property-$link_rewrite)
* [$meta_description](#property-$meta_description)
* [$meta_keywords](#property-$meta_keywords)
* [$meta_title](#property-$meta_title)
* [$name](#property-$name)
* [$nleft](#property-$nleft)
* [$nright](#property-$nright)
* [$position](#property-$position)
* [$webserviceParameters](#property-$webserviceParameters)
* [$def](#property-$def)
* [$fieldsRequired](#property-$fieldsRequired)
* [$fieldsRequiredDatabase](#property-$fieldsRequiredDatabase)
* [$fieldsRequiredLang](#property-$fieldsRequiredLang)
* [$fieldsSize](#property-$fieldsSize)
* [$fieldsSizeLang](#property-$fieldsSizeLang)
* [$fieldsValidate](#property-$fieldsValidate)
* [$fieldsValidateLang](#property-$fieldsValidateLang)
* [$id_lang](#property-$id_lang)
* [$id_shop](#property-$id_shop)
* [$identifier](#property-$identifier)
* [$image_dir](#property-$image_dir)
* [$image_format](#property-$image_format)
* [$table](#property-$table)
* [$tables](#property-$tables)

### Methods

* [__construct](#method-__construct)
* [_subTree](#method-_subTree)
* [add](#method-add)
* [addFieldsRequiredDatabase](#method-addFieldsRequiredDatabase)
* [addGroups](#method-addGroups)
* [addGroupsIfNoExist](#method-addGroupsIfNoExist)
* [associateTo](#method-associateTo)
* [calcLevelDepth](#method-calcLevelDepth)
* [categoryExists](#method-categoryExists)
* [checkAccess](#method-checkAccess)
* [checkBeforeMove](#method-checkBeforeMove)
* [cleanGroups](#method-cleanGroups)
* [cleanPositions](#method-cleanPositions)
* [clearCache](#method-clearCache)
* [delete](#method-delete)
* [deleteImage](#method-deleteImage)
* [deleteSelection](#method-deleteSelection)
* [displayFieldName](#method-displayFieldName)
* [duplicateProductCategories](#method-duplicateProductCategories)
* [duplicateShops](#method-duplicateShops)
* [existsInDatabase](#method-existsInDatabase)
* [formatFields](#method-formatFields)
* [formatValue](#method-formatValue)
* [getAllChildren](#method-getAllChildren)
* [getCategories](#method-getCategories)
* [getCategoryInformations](#method-getCategoryInformations)
* [getChildren](#method-getChildren)
* [getChildrenWithNbSelectedSubCat](#method-getChildrenWithNbSelectedSubCat)
* [getChildrenWs](#method-getChildrenWs)
* [getDefinition](#method-getDefinition)
* [getDescriptionClean](#method-getDescriptionClean)
* [getDuplicatePosition](#method-getDuplicatePosition)
* [getEntity](#method-getEntity)
* [getFields](#method-getFields)
* [getFieldsLang](#method-getFieldsLang)
* [getFieldsRequiredDatabase](#method-getFieldsRequiredDatabase)
* [getGroups](#method-getGroups)
* [getHomeCategories](#method-getHomeCategories)
* [getInterval](#method-getInterval)
* [getLastPosition](#method-getLastPosition)
* [getLink](#method-getLink)
* [getLinkRewrite](#method-getLinkRewrite)
* [getName](#method-getName)
* [getParentsCategories](#method-getParentsCategories)
* [getProducts](#method-getProducts)
* [getProductsWs](#method-getProductsWs)
* [getRootCategory](#method-getRootCategory)
* [getSimpleCategories](#method-getSimpleCategories)
* [getSubCategories](#method-getSubCategories)
* [getTranslationsFields](#method-getTranslationsFields)
* [getUrlRewriteInformations](#method-getUrlRewriteInformations)
* [getValidationRules](#method-getValidationRules)
* [getWebserviceObjectList](#method-getWebserviceObjectList)
* [getWebserviceParameters](#method-getWebserviceParameters)
* [getWsNbProductsRecursive](#method-getWsNbProductsRecursive)
* [hydrate](#method-hydrate)
* [hydrateCollection](#method-hydrateCollection)
* [inShop](#method-inShop)
* [isAssociatedToGroupShop](#method-isAssociatedToGroupShop)
* [isAssociatedToShop](#method-isAssociatedToShop)
* [isCurrentlyUsed](#method-isCurrentlyUsed)
* [isLangMultishop](#method-isLangMultishop)
* [makeTranslationFields](#method-makeTranslationFields)
* [recalculateLevelDepth](#method-recalculateLevelDepth)
* [recurseCategory](#method-recurseCategory)
* [recurseLiteCategTree](#method-recurseLiteCategTree)
* [recursiveDelete](#method-recursiveDelete)
* [regenerateEntireNtree](#method-regenerateEntireNtree)
* [save](#method-save)
* [searchByName](#method-searchByName)
* [searchByNameAndParentCategoryId](#method-searchByNameAndParentCategoryId)
* [setDefinitionRetrocompatibility](#method-setDefinitionRetrocompatibility)
* [setNewGroupForHome](#method-setNewGroupForHome)
* [toggleStatus](#method-toggleStatus)
* [update](#method-update)
* [updateGroup](#method-updateGroup)
* [updatePosition](#method-updatePosition)
* [validateControler](#method-validateControler)
* [validateController](#method-validateController)
* [validateField](#method-validateField)
* [validateFields](#method-validateFields)
* [validateFieldsLang](#method-validateFieldsLang)




Properties
----------


### <a name="property-$_links"></a>$_links

```php
protected mixed $_links = array()
```





* Visibility: **protected**
* This property is **static**.
* Source: [classes/Category.php line 79](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L79).


### <a name="property-$active"></a>$active

```php
public boolean $active = 1
```





* Visibility: **public**
* Source: [classes/Category.php line 39](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L39).


### <a name="property-$date_add"></a>$date_add

```php
public string $date_add
```





* Visibility: **public**
* Source: [classes/Category.php line 72](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L72).


### <a name="property-$date_upd"></a>$date_upd

```php
public string $date_upd
```





* Visibility: **public**
* Source: [classes/Category.php line 75](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L75).


### <a name="property-$definition"></a>$definition

```php
public mixed $definition = array('table' => 'category', 'primary' => 'id_category', 'multilang' => true, 'multishop' => true, 'fields' => array('nleft' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'nright' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'level_depth' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'active' => array('type' => self::TYPE_BOOL, 'validate' => 'isBool', 'required' => true), 'id_parent' => array('type' => self::TYPE_INT, 'validate' => 'isUnsignedInt'), 'position' => array('type' => self::TYPE_INT), 'date_add' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'date_upd' => array('type' => self::TYPE_DATE, 'validate' => 'isDate'), 'name' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isCatalogName', 'required' => true, 'size' => 64), 'link_rewrite' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isLinkRewrite', 'required' => true, 'size' => 64), 'description' => array('type' => self::TYPE_HTML, 'lang' => true, 'validate' => 'isString'), 'meta_title' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isGenericName', 'size' => 128), 'meta_description' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isGenericName', 'size' => 255), 'meta_keywords' => array('type' => self::TYPE_STRING, 'lang' => true, 'validate' => 'isGenericName', 'size' => 255)))
```





* Visibility: **public**
* This property is **static**.
* Source: [classes/Category.php line 84](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L84).


### <a name="property-$description"></a>$description

```php
public string $description
```





* Visibility: **public**
* Source: [classes/Category.php line 45](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L45).


### <a name="property-$groupBox"></a>$groupBox

```php
public mixed $groupBox
```





* Visibility: **public**
* Source: [classes/Category.php line 77](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L77).


### <a name="property-$id"></a>$id

```php
public mixed $id
```





* Visibility: **public**
* Source: [classes/Category.php line 30](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L30).


### <a name="property-$id_category"></a>$id_category

```php
public integer $id_category
```





* Visibility: **public**
* Source: [classes/Category.php line 33](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L33).


### <a name="property-$id_image"></a>$id_image

```php
public string $id_image = 'default'
```





* Visibility: **public**
* Source: [classes/Category.php line 110](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L110).


### <a name="property-$id_parent"></a>$id_parent

```php
public integer $id_parent
```





* Visibility: **public**
* Source: [classes/Category.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L48).


### <a name="property-$level_depth"></a>$level_depth

```php
public integer $level_depth
```





* Visibility: **public**
* Source: [classes/Category.php line 51](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L51).


### <a name="property-$link_rewrite"></a>$link_rewrite

```php
public string $link_rewrite
```





* Visibility: **public**
* Source: [classes/Category.php line 60](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L60).


### <a name="property-$meta_description"></a>$meta_description

```php
public string $meta_description
```





* Visibility: **public**
* Source: [classes/Category.php line 69](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L69).


### <a name="property-$meta_keywords"></a>$meta_keywords

```php
public string $meta_keywords
```





* Visibility: **public**
* Source: [classes/Category.php line 66](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L66).


### <a name="property-$meta_title"></a>$meta_title

```php
public string $meta_title
```





* Visibility: **public**
* Source: [classes/Category.php line 63](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L63).


### <a name="property-$name"></a>$name

```php
public string $name
```





* Visibility: **public**
* Source: [classes/Category.php line 36](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L36).


### <a name="property-$nleft"></a>$nleft

```php
public integer $nleft
```





* Visibility: **public**
* Source: [classes/Category.php line 54](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L54).


### <a name="property-$nright"></a>$nright

```php
public integer $nright
```





* Visibility: **public**
* Source: [classes/Category.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L57).


### <a name="property-$position"></a>$position

```php
public integer $position
```





* Visibility: **public**
* Source: [classes/Category.php line 42](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L42).


### <a name="property-$webserviceParameters"></a>$webserviceParameters

```php
protected mixed $webserviceParameters = array('objectsNodeName' => 'categories', 'hidden_fields' => array('nleft', 'nright', 'groupBox'), 'fields' => array('id_parent' => array('xlink_resource' => 'categories'), 'level_depth' => array('setter' => false), 'nb_products_recursive' => array('getter' => 'getWsNbProductsRecursive', 'setter' => false)), 'associations' => array('categories' => array('getter' => 'getChildrenWs', 'resource' => 'category'), 'products' => array('getter' => 'getProductsWs', 'resource' => 'product')))
```





* Visibility: **protected**
* Source: [classes/Category.php line 112](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L112).


### <a name="property-$def"></a>$def

```php
protected array $def
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 122](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L122).


### <a name="property-$fieldsRequired"></a>$fieldsRequired

```php
protected mixed $fieldsRequired = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 72](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L72).


### <a name="property-$fieldsRequiredDatabase"></a>$fieldsRequiredDatabase

```php
protected mixed $fieldsRequiredDatabase = null
```





* Visibility: **protected**
* This property is **static**.
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 57](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L57).


### <a name="property-$fieldsRequiredLang"></a>$fieldsRequiredLang

```php
protected mixed $fieldsRequiredLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 87](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L87).


### <a name="property-$fieldsSize"></a>$fieldsSize

```php
protected mixed $fieldsSize = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 77](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L77).


### <a name="property-$fieldsSizeLang"></a>$fieldsSizeLang

```php
protected mixed $fieldsSizeLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 92](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L92).


### <a name="property-$fieldsValidate"></a>$fieldsValidate

```php
protected mixed $fieldsValidate = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 82](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L82).


### <a name="property-$fieldsValidateLang"></a>$fieldsValidateLang

```php
protected mixed $fieldsValidateLang = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 97](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L97).


### <a name="property-$id_lang"></a>$id_lang

```php
protected integer $id_lang = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 51](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L51).


### <a name="property-$id_shop"></a>$id_shop

```php
protected mixed $id_shop = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 53](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L53).


### <a name="property-$identifier"></a>$identifier

```php
protected mixed $identifier
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 67](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L67).


### <a name="property-$image_dir"></a>$image_dir

```php
protected string $image_dir = null
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 108](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L108).


### <a name="property-$image_format"></a>$image_format

```php
protected string $image_format = 'jpg'
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 111](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L111).


### <a name="property-$table"></a>$table

```php
protected mixed $table
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L62).


### <a name="property-$tables"></a>$tables

```php
protected mixed $tables = array()
```





* Visibility: **protected**
* This property is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 102](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L102).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed CategoryCore::__construct($id_category, $id_lang, $id_shop)
```





* Visibility: **public**
* Source: [classes/Category.php line 126](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L126)


#### Arguments
* $id_category **mixed**
* $id_lang **mixed**
* $id_shop **mixed**



### <a name="method-_subTree"></a>_subTree

```php
mixed CategoryCore::_subTree($categories, $id_category, $n)
```





* Visibility: **protected**
* This method is **static**.
* Source: [classes/Category.php line 375](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L375)


#### Arguments
* $categories **mixed**
* $id_category **mixed**
* $n **mixed**



### <a name="method-add"></a>add

```php
mixed CategoryCore::add($autodate, $nullValues)
```





* Visibility: **public**
* Source: [classes/Category.php line 143](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L143)


#### Arguments
* $autodate **mixed**
* $nullValues **mixed**



### <a name="method-addFieldsRequiredDatabase"></a>addFieldsRequiredDatabase

```php
mixed ObjectModelCore::addFieldsRequiredDatabase($fields)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 961](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L961)


#### Arguments
* $fields **mixed**



### <a name="method-addGroups"></a>addGroups

```php
mixed CategoryCore::addGroups($groups)
```





* Visibility: **public**
* Source: [classes/Category.php line 917](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L917)


#### Arguments
* $groups **mixed**



### <a name="method-addGroupsIfNoExist"></a>addGroupsIfNoExist

```php
mixed CategoryCore::addGroupsIfNoExist($id_group)
```





* Visibility: **public**
* Source: [classes/Category.php line 939](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L939)


#### Arguments
* $id_group **mixed**



### <a name="method-associateTo"></a>associateTo

```php
boolean ObjectModelCore::associateTo(integer|array $id_shops, string $type)
```

This function associate an item to its context



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1009](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1009)


#### Arguments
* $id_shops **integer|array**
* $type **string**



### <a name="method-calcLevelDepth"></a>calcLevelDepth

```php
integer CategoryCore::calcLevelDepth()
```

Get the depth level for the category



* Visibility: **public**
* Source: [classes/Category.php line 350](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L350)




### <a name="method-categoryExists"></a>categoryExists

```php
boolean CategoryCore::categoryExists($id_category)
```

Specify if a category already in base



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 902](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L902)


#### Arguments
* $id_category **mixed** - Category id



### <a name="method-checkAccess"></a>checkAccess

```php
boolean CategoryCore::checkAccess(mixed $id_customer)
```

checkAccess return true if id_customer is in a group allowed to see this category.



* Visibility: **public**
* Source: [classes/Category.php line 955](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L955)


#### Arguments
* $id_customer **mixed**



### <a name="method-checkBeforeMove"></a>checkBeforeMove

```php
boolean CategoryCore::checkBeforeMove(integer $id_category, integer $id_parent)
```

Check if category can be moved in another one.

The category cannot be moved in a child category.

* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 760](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L760)


#### Arguments
* $id_category **integer** - current category
* $id_parent **integer** - Parent candidate



### <a name="method-cleanGroups"></a>cleanGroups

```php
mixed CategoryCore::cleanGroups()
```





* Visibility: **public**
* Source: [classes/Category.php line 912](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L912)




### <a name="method-cleanPositions"></a>cleanPositions

```php
boolean CategoryCore::cleanPositions(mixed $id_category_parent)
```

cleanPositions keep order of category in $id_category_parent,
but remove duplicate position. Should not be used if positions
are clean at the beginning !



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 1044](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1044)


#### Arguments
* $id_category_parent **mixed**



### <a name="method-clearCache"></a>clearCache

```php
mixed ObjectModelCore::clearCache($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 975](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L975)


#### Arguments
* $all **mixed**



### <a name="method-delete"></a>delete

```php
mixed CategoryCore::delete()
```





* Visibility: **public**
* Source: [classes/Category.php line 265](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L265)




### <a name="method-deleteImage"></a>deleteImage

```php
boolean ObjectModelCore::deleteImage()
```

Delete images associated with the object



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1079](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1079)




### <a name="method-deleteSelection"></a>deleteSelection

```php
mixed CategoryCore::deleteSelection($categories)
```

Delete several categories from database

return boolean Deletion result

* Visibility: **public**
* Source: [classes/Category.php line 334](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L334)


#### Arguments
* $categories **mixed**



### <a name="method-displayFieldName"></a>displayFieldName

```php
mixed ObjectModelCore::displayFieldName($field, $className, $htmlentities, \Context $context)
```





* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 740](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L740)


#### Arguments
* $field **mixed**
* $className **mixed**
* $htmlentities **mixed**
* $context **[Context](class.ContextCore.md)**



### <a name="method-duplicateProductCategories"></a>duplicateProductCategories

```php
boolean CategoryCore::duplicateProductCategories(integer $id_old, boolean $id_new)
```

Copy products from a category to another



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 729](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L729)


#### Arguments
* $id_old **integer** - Source category ID
* $id_new **boolean** - Destination category ID



### <a name="method-duplicateShops"></a>duplicateShops

```php
mixed ObjectModelCore::duplicateShops($id)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1049](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1049)


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
* Source: [classes/ObjectModel.php line 1113](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1113)


#### Arguments
* $id_entity **integer**
* $table **string**



### <a name="method-formatFields"></a>formatFields

```php
array ObjectModelCore::formatFields(integer $id_lang)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 272](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L272)


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
* Source: [classes/ObjectModel.php line 319](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L319)


#### Arguments
* $value **mixed**
* $type **integer**
* $with_quotes **mixed**



### <a name="method-getAllChildren"></a>getAllChildren

```php
\Collection CategoryCore::getAllChildren(integer $id_lang)
```

Return an array of all children of the current category



* Visibility: **public**
* Source: [classes/Category.php line 678](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L678)


#### Arguments
* $id_lang **integer**



### <a name="method-getCategories"></a>getCategories

```php
array CategoryCore::getCategories(integer $id_lang, boolean $active, $order, $sql_filter, $sql_sort, $sql_limit)
```

Return available categories



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 428](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L428)


#### Arguments
* $id_lang **integer** - Language ID
* $active **boolean** - return only active categories
* $order **mixed**
* $sql_filter **mixed**
* $sql_sort **mixed**
* $sql_limit **mixed**



### <a name="method-getCategoryInformations"></a>getCategoryInformations

```php
Array CategoryCore::getCategoryInformations(Array $ids_category, integer $id_lang)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 1178](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1178)


#### Arguments
* $ids_category **Array**
* $id_lang **integer**



### <a name="method-getChildren"></a>getChildren

```php
array CategoryCore::getChildren(integer $id_parent, integer $id_lang, boolean $active)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 657](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L657)


#### Arguments
* $id_parent **integer**
* $id_lang **integer**
* $active **boolean**



### <a name="method-getChildrenWithNbSelectedSubCat"></a>getChildrenWithNbSelectedSubCat

```php
array CategoryCore::getChildrenWithNbSelectedSubCat(integer $id_parent, $selected_cat, integer $id_lang, \Shop $shop)
```

This method allow to return children categories with the number of sub children selected for a product



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 697](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L697)


#### Arguments
* $id_parent **integer**
* $selected_cat **mixed**
* $id_lang **integer**
* $shop **[Shop](class.ShopCore.md)**



### <a name="method-getChildrenWs"></a>getChildrenWs

```php
mixed CategoryCore::getChildrenWs()
```





* Visibility: **public**
* Source: [classes/Category.php line 1123](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1123)




### <a name="method-getDefinition"></a>getDefinition

```php
mixed ObjectModelCore::getDefinition($class, $field)
```





* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1209](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1209)


#### Arguments
* $class **mixed**
* $field **mixed**



### <a name="method-getDescriptionClean"></a>getDescriptionClean

```php
string CategoryCore::getDescriptionClean($description)
```

Allows to display the category description without HTML tags and slashes



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 138](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L138)


#### Arguments
* $description **mixed**



### <a name="method-getDuplicatePosition"></a>getDuplicatePosition

```php
array CategoryCore::getDuplicatePosition()
```

Search for another category with the same parent and the same position



* Visibility: **public**
* Source: [classes/Category.php line 1149](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1149)




### <a name="method-getEntity"></a>getEntity

```php
mixed ObjectModelCore::getEntity($entity)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1269](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1269)


#### Arguments
* $entity **mixed**



### <a name="method-getFields"></a>getFields

```php
array ObjectModelCore::getFields()
```

Prepare fields for ObjectModel class (add, update)
All fields are verified (pSQL, intval.

..)

* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 234](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L234)




### <a name="method-getFieldsLang"></a>getFieldsLang

```php
array ObjectModelCore::getFieldsLang()
```

Prepare multilang fields



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 249](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L249)




### <a name="method-getFieldsRequiredDatabase"></a>getFieldsRequiredDatabase

```php
mixed ObjectModelCore::getFieldsRequiredDatabase($all)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 953](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L953)


#### Arguments
* $all **mixed**



### <a name="method-getGroups"></a>getGroups

```php
mixed CategoryCore::getGroups()
```





* Visibility: **public**
* Source: [classes/Category.php line 926](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L926)




### <a name="method-getHomeCategories"></a>getHomeCategories

```php
array CategoryCore::getHomeCategories(integer $id_lang, boolean $active)
```

Return main categories



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 635](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L635)


#### Arguments
* $id_lang **integer** - Language ID
* $active **boolean** - return only active categories



### <a name="method-getInterval"></a>getInterval

```php
array CategoryCore::getInterval(integer $id)
```

Return nleft and nright fields for a given category



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 1096](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1096)


#### Arguments
* $id **integer**



### <a name="method-getLastPosition"></a>getLastPosition

```php
integer CategoryCore::getLastPosition(integer $id_category_parent)
```

this function return the number of category + 1 having $id_category_parent as parent.



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 1073](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1073)


#### Arguments
* $id_category_parent **integer** - the parent category



### <a name="method-getLink"></a>getLink

```php
mixed CategoryCore::getLink(\Link $link)
```





* Visibility: **public**
* Source: [classes/Category.php line 794](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L794)


#### Arguments
* $link **[Link](class.LinkCore.md)**



### <a name="method-getLinkRewrite"></a>getLinkRewrite

```php
mixed CategoryCore::getLinkRewrite($id_category, $id_lang)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 776](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L776)


#### Arguments
* $id_category **mixed**
* $id_lang **mixed**



### <a name="method-getName"></a>getName

```php
mixed CategoryCore::getName($id_lang)
```





* Visibility: **public**
* Source: [classes/Category.php line 801](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L801)


#### Arguments
* $id_lang **mixed**



### <a name="method-getParentsCategories"></a>getParentsCategories

```php
array CategoryCore::getParentsCategories(integer $id_lang)
```

Get Each parent category of this category until the root category



* Visibility: **public**
* Source: [classes/Category.php line 871](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L871)


#### Arguments
* $id_lang **integer** - Language ID



### <a name="method-getProducts"></a>getProducts

```php
mixed CategoryCore::getProducts(integer $id_lang, integer $p, integer $n, $order_by, $order_way, boolean $get_total, boolean $active, boolean $random, integer $random_number_products, boolean $check_access, \Context $context)
```

Return current category products



* Visibility: **public**
* Source: [classes/Category.php line 515](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L515)


#### Arguments
* $id_lang **integer** - Language ID
* $p **integer** - Page number
* $n **integer** - Number of products per page
* $order_by **mixed**
* $order_way **mixed**
* $get_total **boolean** - return the number of results instead of the results themself
* $active **boolean** - return only active products
* $random **boolean** - active a random filter for returned products
* $random_number_products **integer** - number of products to return if random is activated
* $check_access **boolean** - set to false to return all products (even if customer hasn&#039;t access)
* $context **[Context](class.ContextCore.md)**



### <a name="method-getProductsWs"></a>getProductsWs

```php
mixed CategoryCore::getProductsWs()
```





* Visibility: **public**
* Source: [classes/Category.php line 1134](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1134)




### <a name="method-getRootCategory"></a>getRootCategory

```php
mixed CategoryCore::getRootCategory($id_lang, \Shop $shop)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 640](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L640)


#### Arguments
* $id_lang **mixed**
* $shop **[Shop](class.ShopCore.md)**



### <a name="method-getSimpleCategories"></a>getSimpleCategories

```php
mixed CategoryCore::getSimpleCategories($id_lang)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 453](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L453)


#### Arguments
* $id_lang **mixed**



### <a name="method-getSubCategories"></a>getSubCategories

```php
array CategoryCore::getSubCategories(integer $id_lang, boolean $active)
```

Return current category childs



* Visibility: **public**
* Source: [classes/Category.php line 471](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L471)


#### Arguments
* $id_lang **integer** - Language ID
* $active **boolean** - return only active categories



### <a name="method-getTranslationsFields"></a>getTranslationsFields

```php
mixed ObjectModelCore::getTranslationsFields($fieldsArray)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 589](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L589)


#### Arguments
* $fieldsArray **mixed**



### <a name="method-getUrlRewriteInformations"></a>getUrlRewriteInformations

```php
mixed CategoryCore::getUrlRewriteInformations($id_category)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 1078](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1078)


#### Arguments
* $id_category **mixed**



### <a name="method-getValidationRules"></a>getValidationRules

```php
array ObjectModelCore::getValidationRules(string $className)
```

Returns object validation rules (fields validity)



* Visibility: **public**
* This method is **static**.
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 130](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L130)


#### Arguments
* $className **string** - Child class name for static use (optional)



### <a name="method-getWebserviceObjectList"></a>getWebserviceObjectList

```php
mixed ObjectModelCore::getWebserviceObjectList($sql_join, $sql_filter, $sql_sort, $sql_limit)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 929](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L929)


#### Arguments
* $sql_join **mixed**
* $sql_filter **mixed**
* $sql_sort **mixed**
* $sql_limit **mixed**



### <a name="method-getWebserviceParameters"></a>getWebserviceParameters

```php
mixed ObjectModelCore::getWebserviceParameters($wsParamsAttributeName)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 799](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L799)


#### Arguments
* $wsParamsAttributeName **mixed**



### <a name="method-getWsNbProductsRecursive"></a>getWsNbProductsRecursive

```php
mixed CategoryCore::getWsNbProductsRecursive()
```





* Visibility: **public**
* Source: [classes/Category.php line 1159](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1159)




### <a name="method-hydrate"></a>hydrate

```php
mixed ObjectModelCore::hydrate(array $data, integer $id_lang)
```

Fill an object with given data. Data must be an array with this syntax: array(objProperty => value, objProperty2 => value, etc.)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1148](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1148)


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
* Source: [classes/ObjectModel.php line 1167](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1167)


#### Arguments
* $class **string** - Class of objects to hydrate
* $datas **array** - List of data (multi-dimensional array)
* $id_lang **integer**



### <a name="method-inShop"></a>inShop

```php
boolean CategoryCore::inShop(\Shop $shop)
```

Check if current category is a child of shop root category



* Visibility: **public**
* Source: [classes/Category.php line 1113](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1113)


#### Arguments
* $shop **[Shop](class.ShopCore.md)**



### <a name="method-isAssociatedToGroupShop"></a>isAssociatedToGroupShop

```php
boolean ObjectModelCore::isAssociatedToGroupShop(integer $id_group_shop)
```

Check if current object is associated to a group shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1035](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1035)


#### Arguments
* $id_group_shop **integer**



### <a name="method-isAssociatedToShop"></a>isAssociatedToShop

```php
boolean ObjectModelCore::isAssociatedToShop(integer $id_shop)
```

Check if current object is associated to a shop



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 990](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L990)


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
* Source: [classes/ObjectModel.php line 1131](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1131)


#### Arguments
* $table **string** - name of table linked to entity
* $has_active_column **boolean** - true if the table has an active column



### <a name="method-isLangMultishop"></a>isLangMultishop

```php
mixed ObjectModelCore::isLangMultishop()
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1069](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1069)




### <a name="method-makeTranslationFields"></a>makeTranslationFields

```php
mixed ObjectModelCore::makeTranslationFields($fields, $fieldsArray, $id_language)
```





* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 605](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L605)


#### Arguments
* $fields **mixed**
* $fieldsArray **mixed**
* $id_language **mixed**



### <a name="method-recalculateLevelDepth"></a>recalculateLevelDepth

```php
mixed CategoryCore::recalculateLevelDepth(integer $id_category)
```

Updates level_depth for all children of the given id_category



* Visibility: **public**
* Source: [classes/Category.php line 395](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L395)


#### Arguments
* $id_category **integer** - parent category



### <a name="method-recurseCategory"></a>recurseCategory

```php
mixed CategoryCore::recurseCategory($categories, $current, $id_category, $id_selected)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 233](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L233)


#### Arguments
* $categories **mixed**
* $current **mixed**
* $id_category **mixed**
* $id_selected **mixed**



### <a name="method-recurseLiteCategTree"></a>recurseLiteCategTree

```php
array CategoryCore::recurseLiteCategTree(integer $max_depth, integer $current_depth, integer $id_lang, array $excluded_ids_array)
```

Recursive scan of subcategories



* Visibility: **public**
* Source: [classes/Category.php line 203](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L203)


#### Arguments
* $max_depth **integer** - Maximum depth of the tree (i.e. 2 =&gt; 3 levels depth)
* $current_depth **integer** - specify the current depth in the tree (don&#039;t use it, only for rucursivity!)
* $id_lang **integer** - Specify the id of the language used
* $excluded_ids_array **array** - specify a list of ids to exclude of results



### <a name="method-recursiveDelete"></a>recursiveDelete

```php
mixed CategoryCore::recursiveDelete($to_delete, array $id_category)
```

Recursively add specified category childs to $to_delete array



* Visibility: **protected**
* Source: [classes/Category.php line 249](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L249)


#### Arguments
* $to_delete **mixed**
* $id_category **array** - Parent category ID



### <a name="method-regenerateEntireNtree"></a>regenerateEntireNtree

```php
mixed CategoryCore::regenerateEntireNtree()
```

Re-calculate the values of all branches of the nested tree



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 365](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L365)




### <a name="method-save"></a>save

```php
boolean ObjectModelCore::save(boolean $null_values, boolean $autodate)
```

Save current object to database (add or update)



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 360](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L360)


#### Arguments
* $null_values **boolean**
* $autodate **boolean**



### <a name="method-searchByName"></a>searchByName

```php
array CategoryCore::searchByName(integer $id_lang, string $query, boolean $unrestricted)
```

Light back office search for categories



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 821](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L821)


#### Arguments
* $id_lang **integer** - Language ID
* $query **string** - Searched string
* $unrestricted **boolean** - allows search without lang and includes first category and exact match



### <a name="method-searchByNameAndParentCategoryId"></a>searchByNameAndParentCategoryId

```php
array CategoryCore::searchByNameAndParentCategoryId(integer $id_lang, string $category_name, integer $id_parent_category)
```

Retrieve category by name and parent category id



* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 851](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L851)


#### Arguments
* $id_lang **integer** - Language ID
* $category_name **string** - Searched category name
* $id_parent_category **integer** - parent category ID



### <a name="method-setDefinitionRetrocompatibility"></a>setDefinitionRetrocompatibility

```php
mixed ObjectModelCore::setDefinitionRetrocompatibility()
```

Retrocompatibility for classes without $definition static
Remove this in 1.6 !



* Visibility: **protected**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 1224](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L1224)




### <a name="method-setNewGroupForHome"></a>setNewGroupForHome

```php
mixed CategoryCore::setNewGroupForHome($id_group)
```





* Visibility: **public**
* This method is **static**.
* Source: [classes/Category.php line 991](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L991)


#### Arguments
* $id_group **mixed**



### <a name="method-toggleStatus"></a>toggleStatus

```php
mixed CategoryCore::toggleStatus()
```





* Visibility: **public**
* Source: [classes/Category.php line 186](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L186)




### <a name="method-update"></a>update

```php
void CategoryCore::update(mixed $nullValues)
```

update category positions in parent



* Visibility: **public**
* Source: [classes/Category.php line 162](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L162)


#### Arguments
* $nullValues **mixed**



### <a name="method-updateGroup"></a>updateGroup

```php
mixed CategoryCore::updateGroup(array $list)
```

Update customer groups associated to the object



* Visibility: **public**
* Source: [classes/Category.php line 982](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L982)


#### Arguments
* $list **array** - groups



### <a name="method-updatePosition"></a>updatePosition

```php
mixed CategoryCore::updatePosition($way, $position)
```





* Visibility: **public**
* Source: [classes/Category.php line 1001](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/Category.php#L1001)


#### Arguments
* $way **mixed**
* $position **mixed**



### <a name="method-validateControler"></a>validateControler

```php
mixed ObjectModelCore::validateControler($htmlentities)
```

TODO: refactor rename all calls to this to validateController



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 753](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L753)


#### Arguments
* $htmlentities **mixed**



### <a name="method-validateController"></a>validateController

```php
mixed ObjectModelCore::validateController($htmlentities)
```





* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 759](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L759)


#### Arguments
* $htmlentities **mixed**



### <a name="method-validateField"></a>validateField

```php
boolean|string ObjectModelCore::validateField(string $field, mixed $value, integer $id_lang)
```

Validate a single field



* Visibility: **public**
* This method is defined by [ObjectModelCore](class.ObjectModelCore.md).
* Source: [classes/ObjectModel.php line 704](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L704)


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
* Source: [classes/ObjectModel.php line 643](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L643)


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
* Source: [classes/ObjectModel.php line 669](https://github.com/PrestaShop/PrestaShop/blob/1.5.0.3/classes/ObjectModel.php#L669)


#### Arguments
* $die **boolean**
* $error_return **boolean**


