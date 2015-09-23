Class AdminModulesControllerCore
=====================





* Class name: AdminModulesControllerCore
* Parent class: [AdminController](class.AdminControllerCore.md)
* Source: [controllers/admin/AdminModulesController.php line 27](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L27)


Contents
--------


### Properties

* [$_modules_ad](#property-$_modules_ad)
* [$filter_configuration](#property-$filter_configuration)
* [$id_employee](#property-$id_employee)
* [$iso_default_country](#property-$iso_default_country)
* [$list_modules_categories](#property-$list_modules_categories)
* [$list_natives_modules](#property-$list_natives_modules)
* [$list_partners_modules](#property-$list_partners_modules)
* [$map](#property-$map)
* [$modules_authors](#property-$modules_authors)
* [$nb_modules_activated](#property-$nb_modules_activated)
* [$nb_modules_installed](#property-$nb_modules_installed)
* [$nb_modules_total](#property-$nb_modules_total)
* [$serial_modules](#property-$serial_modules)
* [$xml_modules_list](#property-$xml_modules_list)

### Methods

* [__construct](#method-__construct)
* [ajaxProcessGetModuleQuickView](#method-ajaxProcessGetModuleQuickView)
* [ajaxProcessGetTabModulesList](#method-ajaxProcessGetTabModulesList)
* [ajaxProcessLogOnAddonsWebservices](#method-ajaxProcessLogOnAddonsWebservices)
* [ajaxProcessLogOutAddonsWebservices](#method-ajaxProcessLogOutAddonsWebservices)
* [ajaxProcessRefreshModuleList](#method-ajaxProcessRefreshModuleList)
* [ajaxProcessReloadModulesList](#method-ajaxProcessReloadModulesList)
* [ajaxProcessSaveFavoritePreferences](#method-ajaxProcessSaveFavoritePreferences)
* [ajaxProcessSaveTabModulePreferences](#method-ajaxProcessSaveTabModulePreferences)
* [ajaxProcessSetFilter](#method-ajaxProcessSetFilter)
* [checkCategoriesNames](#method-checkCategoriesNames)
* [displayAjaxRefreshModuleList](#method-displayAjaxRefreshModuleList)
* [extractArchive](#method-extractArchive)
* [generateHtmlMessage](#method-generateHtmlMessage)
* [getCurrentUrl](#method-getCurrentUrl)
* [getModulesByInstallation](#method-getModulesByInstallation)
* [initContent](#method-initContent)
* [initModal](#method-initModal)
* [initModulesList](#method-initModulesList)
* [isModuleFiltered](#method-isModuleFiltered)
* [makeModulesStats](#method-makeModulesStats)
* [postProcess](#method-postProcess)
* [postProcessCallback](#method-postProcessCallback)
* [postProcessDelete](#method-postProcessDelete)
* [postProcessDisable_Device](#method-postProcessDisable_Device)
* [postProcessDownload](#method-postProcessDownload)
* [postProcessEnable](#method-postProcessEnable)
* [postProcessEnable_Device](#method-postProcessEnable_Device)
* [postProcessFilterCategory](#method-postProcessFilterCategory)
* [postProcessFilterModules](#method-postProcessFilterModules)
* [postProcessReset](#method-postProcessReset)
* [postProcessResetFilterModules](#method-postProcessResetFilterModules)
* [postProcessUnfilterCategory](#method-postProcessUnfilterCategory)
* [recursiveDeleteOnDisk](#method-recursiveDeleteOnDisk)
* [renderKpis](#method-renderKpis)
* [resetFilterModules](#method-resetFilterModules)
* [setFilterModules](#method-setFilterModules)
* [setMedia](#method-setMedia)




Properties
----------


### <a name="property-$_modules_ad"></a>$_modules_ad

```php
private mixed $_modules_ad = array('blockcart' => array('cartabandonmentpro'), 'blocklayered' => array('pm_advancedsearch4'))
```





* Visibility: **private**
* Source: [controllers/admin/AdminModulesController.php line 29](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L29).


### <a name="property-$filter_configuration"></a>$filter_configuration

```php
protected mixed $filter_configuration = array()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 60](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L60).


### <a name="property-$id_employee"></a>$id_employee

```php
protected mixed $id_employee
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 58](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L58).


### <a name="property-$iso_default_country"></a>$iso_default_country

```php
protected mixed $iso_default_country
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 59](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L59).


### <a name="property-$list_modules_categories"></a>$list_modules_categories

```php
protected mixed $list_modules_categories = array()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 47](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L47).


### <a name="property-$list_natives_modules"></a>$list_natives_modules

```php
protected mixed $list_natives_modules = array()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 49](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L49).


### <a name="property-$list_partners_modules"></a>$list_partners_modules

```php
protected mixed $list_partners_modules = array()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 48](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L48).


### <a name="property-$map"></a>$map

```php
protected mixed $map = array('check' => 'check', 'install' => 'install', 'uninstall' => 'uninstall', 'configure' => 'getContent', 'update' => 'update', 'delete' => 'delete', 'checkAndUpdate' => 'checkAndUpdate')
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 37](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L37).


### <a name="property-$modules_authors"></a>$modules_authors

```php
protected mixed $modules_authors = array()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 56](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L56).


### <a name="property-$nb_modules_activated"></a>$nb_modules_activated

```php
protected mixed $nb_modules_activated
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 53](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L53).


### <a name="property-$nb_modules_installed"></a>$nb_modules_installed

```php
protected mixed $nb_modules_installed
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 52](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L52).


### <a name="property-$nb_modules_total"></a>$nb_modules_total

```php
protected mixed $nb_modules_total
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 51](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L51).


### <a name="property-$serial_modules"></a>$serial_modules

```php
protected mixed $serial_modules = ''
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 55](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L55).


### <a name="property-$xml_modules_list"></a>$xml_modules_list

```php
protected mixed $xml_modules_list = 'api.prestashop.com/xml/modules_list_16.xml'
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 62](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L62).


Methods
-------


### <a name="method-__construct"></a>__construct

```php
mixed AdminModulesControllerCore::__construct()
```

Admin Modules Controller Constructor
Init list modules categories
Load id employee
Load filter configuration
Load cache file



* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 72](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L72)




### <a name="method-ajaxProcessGetModuleQuickView"></a>ajaxProcessGetModuleQuickView

```php
mixed AdminModulesControllerCore::ajaxProcessGetModuleQuickView()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1581](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1581)




### <a name="method-ajaxProcessGetTabModulesList"></a>ajaxProcessGetTabModulesList

```php
mixed AdminModulesControllerCore::ajaxProcessGetTabModulesList()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 258](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L258)




### <a name="method-ajaxProcessLogOnAddonsWebservices"></a>ajaxProcessLogOnAddonsWebservices

```php
mixed AdminModulesControllerCore::ajaxProcessLogOnAddonsWebservices()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 216](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L216)




### <a name="method-ajaxProcessLogOutAddonsWebservices"></a>ajaxProcessLogOutAddonsWebservices

```php
mixed AdminModulesControllerCore::ajaxProcessLogOutAddonsWebservices()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 237](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L237)




### <a name="method-ajaxProcessRefreshModuleList"></a>ajaxProcessRefreshModuleList

```php
mixed AdminModulesControllerCore::ajaxProcessRefreshModuleList($force_reload_cache)
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 156](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L156)


#### Arguments
* $force_reload_cache **mixed**



### <a name="method-ajaxProcessReloadModulesList"></a>ajaxProcessReloadModulesList

```php
mixed AdminModulesControllerCore::ajaxProcessReloadModulesList()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 246](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L246)




### <a name="method-ajaxProcessSaveFavoritePreferences"></a>ajaxProcessSaveFavoritePreferences

```php
mixed AdminModulesControllerCore::ajaxProcessSaveFavoritePreferences()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 308](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L308)




### <a name="method-ajaxProcessSaveTabModulePreferences"></a>ajaxProcessSaveTabModulePreferences

```php
mixed AdminModulesControllerCore::ajaxProcessSaveTabModulePreferences()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 334](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L334)




### <a name="method-ajaxProcessSetFilter"></a>ajaxProcessSetFilter

```php
mixed AdminModulesControllerCore::ajaxProcessSetFilter()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 302](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L302)




### <a name="method-checkCategoriesNames"></a>checkCategoriesNames

```php
mixed AdminModulesControllerCore::checkCategoriesNames($a, $b)
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 139](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L139)


#### Arguments
* $a **mixed**
* $b **mixed**



### <a name="method-displayAjaxRefreshModuleList"></a>displayAjaxRefreshModuleList

```php
mixed AdminModulesControllerCore::displayAjaxRefreshModuleList()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 210](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L210)




### <a name="method-extractArchive"></a>extractArchive

```php
mixed AdminModulesControllerCore::extractArchive($file, $redirect)
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 372](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L372)


#### Arguments
* $file **mixed**
* $redirect **mixed**



### <a name="method-generateHtmlMessage"></a>generateHtmlMessage

```php
string AdminModulesControllerCore::generateHtmlMessage($module_errors)
```

Generate html errors for a module process



* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 1106](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1106)


#### Arguments
* $module_errors **mixed**



### <a name="method-getCurrentUrl"></a>getCurrentUrl

```php
mixed AdminModulesControllerCore::getCurrentUrl($remove)
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 356](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L356)


#### Arguments
* $remove **mixed**



### <a name="method-getModulesByInstallation"></a>getModulesByInstallation

```php
mixed AdminModulesControllerCore::getModulesByInstallation($tab_modules_list)
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 1023](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1023)


#### Arguments
* $tab_modules_list **mixed**



### <a name="method-initContent"></a>initContent

```php
mixed AdminModulesControllerCore::initContent()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1341](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1341)




### <a name="method-initModal"></a>initModal

```php
mixed AdminModulesControllerCore::initModal()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1306](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1306)




### <a name="method-initModulesList"></a>initModulesList

```php
mixed AdminModulesControllerCore::initModulesList($modules)
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1126](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1126)


#### Arguments
* $modules **mixed**



### <a name="method-isModuleFiltered"></a>isModuleFiltered

```php
mixed AdminModulesControllerCore::isModuleFiltered($module)
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1167](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1167)


#### Arguments
* $module **mixed**



### <a name="method-makeModulesStats"></a>makeModulesStats

```php
mixed AdminModulesControllerCore::makeModulesStats($module)
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1150](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1150)


#### Arguments
* $module **mixed**



### <a name="method-postProcess"></a>postProcess

```php
mixed AdminModulesControllerCore::postProcess()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1067](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1067)




### <a name="method-postProcessCallback"></a>postProcessCallback

```php
mixed AdminModulesControllerCore::postProcessCallback()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 693](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L693)




### <a name="method-postProcessDelete"></a>postProcessDelete

```php
mixed AdminModulesControllerCore::postProcessDelete()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 659](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L659)




### <a name="method-postProcessDisable_Device"></a>postProcessDisable_Device

```php
mixed AdminModulesControllerCore::postProcessDisable_Device()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 637](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L637)




### <a name="method-postProcessDownload"></a>postProcessDownload

```php
mixed AdminModulesControllerCore::postProcessDownload()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 539](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L539)




### <a name="method-postProcessEnable"></a>postProcessEnable

```php
mixed AdminModulesControllerCore::postProcessEnable()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 590](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L590)




### <a name="method-postProcessEnable_Device"></a>postProcessEnable_Device

```php
mixed AdminModulesControllerCore::postProcessEnable_Device()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 615](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L615)




### <a name="method-postProcessFilterCategory"></a>postProcessFilterCategory

```php
mixed AdminModulesControllerCore::postProcessFilterCategory()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 480](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L480)




### <a name="method-postProcessFilterModules"></a>postProcessFilterModules

```php
mixed AdminModulesControllerCore::postProcessFilterModules()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 468](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L468)




### <a name="method-postProcessReset"></a>postProcessReset

```php
mixed AdminModulesControllerCore::postProcessReset()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 499](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L499)




### <a name="method-postProcessResetFilterModules"></a>postProcessResetFilterModules

```php
mixed AdminModulesControllerCore::postProcessResetFilterModules()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 474](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L474)




### <a name="method-postProcessUnfilterCategory"></a>postProcessUnfilterCategory

```php
mixed AdminModulesControllerCore::postProcessUnfilterCategory()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 487](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L487)




### <a name="method-recursiveDeleteOnDisk"></a>recursiveDeleteOnDisk

```php
mixed AdminModulesControllerCore::recursiveDeleteOnDisk($dir)
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 421](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L421)


#### Arguments
* $dir **mixed**



### <a name="method-renderKpis"></a>renderKpis

```php
mixed AdminModulesControllerCore::renderKpis()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 1261](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L1261)




### <a name="method-resetFilterModules"></a>resetFilterModules

```php
mixed AdminModulesControllerCore::resetFilterModules()
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 454](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L454)




### <a name="method-setFilterModules"></a>setFilterModules

```php
mixed AdminModulesControllerCore::setFilterModules($module_type, $country_module_value, $module_install, $module_status)
```





* Visibility: **protected**
* Source: [controllers/admin/AdminModulesController.php line 446](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L446)


#### Arguments
* $module_type **mixed**
* $country_module_value **mixed**
* $module_install **mixed**
* $module_status **mixed**



### <a name="method-setMedia"></a>setMedia

```php
mixed AdminModulesControllerCore::setMedia()
```





* Visibility: **public**
* Source: [controllers/admin/AdminModulesController.php line 147](https://github.com/PrestaShop/PrestaShop/blob/1.6.0.12/controllers/admin/AdminModulesController.php#L147)


