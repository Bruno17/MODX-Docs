---
title: "xPDOCacheManager.copyFile"
_old_id: "1260"
_old_uri: "2.x/class-reference/xpdocachemanager/xpdocachemanager.copyfile"
---

## xPDOCacheManager::copyFile

Copies a file from a source file to a target directory. Takes the following options as an optional 3rd parameter:

- `copy_newer_only` - If the source file is older than the target, it will not copy the file.
- `copy_preserve_permissions` - xPDO will attempt to copy over the permission structure from the source file to the target. Defaults to false.
- `copy_preserve_filemtime` - xPDO will attempt to copy over the modified time from the source file to the target file. Defaults to true.
- `copy_return_file_stat` - Setting to true will return the php [stat()](http://www.php.net/stat) information in the return array. Defaults to false.
- `new_dir_permissions` - The permissions to set any new directories to that were created in the target. (Can also be the 4th parameter of copyFile.) Defaults to 0775.
- `new_file_permissions` - The permissions to set the new file to if  `copy_preserve_permissions` is false. Defaults to 0664.

## Syntax

API Docs: <http://api.modxcms.com/xpdo/cache/xPDOCacheManager.html#copyFile>

``` php
boolean|array copyFile (string $source, string $target, [array $options = array()])
```

## Example

Copy a file:

``` php
$xpdo->cacheManager->copyFile('/my/path/to/file.txt','/my/new/path/dir/');
```

## See Also

1. [xPDOCacheManager.copyFile](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.copyfile)
2. [xPDOCacheManager.copyTree](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.copytree)
3. [xPDOCacheManager.delete](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.delete)
4. [xPDOCacheManager.deleteTree](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.deletetree)
5. [xPDOCacheManager.endsWith](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.endswith)
6. [xPDOCacheManager.escapeSingleQuotes](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.escapesinglequotes)
7. [xPDOCacheManager.get](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.get)
8. [xPDOCacheManager.getCachePath](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.getcachepath)
9. [xPDOCacheManager.getCacheProvider](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.getcacheprovider)
10. [xPDOCacheManager.matches](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.matches)
11. [xPDOCacheManager.replace](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.replace)
12. [xPDOCacheManager.writeFile](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.writefile)
13. [xPDOCacheManager.set](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.set)
14. [xPDOCacheManager.writeTree](extending-modx/xpdo/class-reference/xpdocachemanager/xpdocachemanager.writetree)
15. [xPDOCacheManager](extending-modx/xpdo/class-reference/xpdocachemanager "xPDOCacheManager")
