Interface Core_Foundation_Database_EntityInterface
=========================

2007-2015 PrestaShop

NOTICE OF LICENSE

This source file is subject to the Open Software License (OSL 3.0)
that is bundled with this package in the file LICENSE.txt.
It is also available through the world-wide-web at this URL:
http://opensource.org/licenses/osl-3.0.php
If you did not receive a copy of the license and are unable to
obtain it through the world-wide-web, please send an email
to license@prestashop.com so we can send you a copy immediately.

DISCLAIMER

Do not edit or add to this file if you wish to upgrade PrestaShop to newer
versions in the future. If you wish to customize PrestaShop for your
needs please refer to http://www.prestashop.com for more information.

* Interface name: Core_Foundation_Database_EntityInterface
* This is an **interface**
* Source: [Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.2/Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php#L27)

Contents
--------



### Methods

* [delete](#method-delete)
* [getRepositoryClassName](#method-getRepositoryClassName)
* [hydrate](#method-hydrate)
* [save](#method-save)






Methods
-------


### <a name="method-delete"></a>delete

```php
mixed Core_Foundation_Database_EntityInterface::delete()
```





* Visibility: **public**
* Source: [Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php line 39](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.2/Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php#L39)




### <a name="method-getRepositoryClassName"></a>getRepositoryClassName

```php
string Core_Foundation_Database_EntityInterface::getRepositoryClassName()
```

Returns the name of the repository class for this entity.

If unspecified, a generic repository will be used for the entity.

* Visibility: **public**
* This method is **static**.
* Source: [Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php line 35](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.2/Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php#L35)




### <a name="method-hydrate"></a>hydrate

```php
mixed Core_Foundation_Database_EntityInterface::hydrate(array $keyValueData)
```





* Visibility: **public**
* Source: [Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php line 41](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.2/Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php#L41)


#### Arguments
* $keyValueData **array**



### <a name="method-save"></a>save

```php
mixed Core_Foundation_Database_EntityInterface::save()
```





* Visibility: **public**
* Source: [Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.6.1.2/Core/Foundation/Database/Core_Foundation_Database_EntityInterface.php#L37)



