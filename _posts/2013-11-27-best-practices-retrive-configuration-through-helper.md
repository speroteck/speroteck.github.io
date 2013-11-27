

Best practices.

Retrive configuration value by config name through Helper

This practice appeared to simplify using configuration settings.
Example: to retrive next configuration value `speroteck_pagecache/pagecache_config/black_list` is not 
convinient, especialy in case of often usage. 

```php
  <?php
  Mage::getStoreConfig("speroteck_pagecache/pagecache_config/black_list");
```
  
As developer, I'm working on extension and I'm in the context of it. There is no need for me 
to use additional markers to retreive it's settings.
Next example is easier to read and should be used as best practice.

```php
  <?php
  Mage::helper('speroteck_pagecache')->getConfig('black_list'));
```

Implementation looks like this.

```php
  <?php
    /**
     * Return config value by name
     * @see
     * @param $field
     *
     * @return mixed
     * @throws Exception
     */
    public function getConfig($field)
    {
        if (empty($field)) {
            throw new Exception("Field should not be empty.");
        }

        return Mage::getStoreConfig("speroteck_pagecache/pagecache_config/{$field}");
    }
```
