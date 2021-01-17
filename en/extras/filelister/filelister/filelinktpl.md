---
title: "fileLinkTpl"
_old_id: "846"
_old_uri: "revo/filelister/filelister.filelister/filelister.filelister.filelinktpl"
---

## FileLister's fileLinkTpl Chunk

This is the Chunk displayed with the &fileLinkTpl property on the [FileLister](extras/filelister/filelister "FileLister.FileLister") snippet. Used for the links for each result.

## Default Value

``` php
<a href="[[+url]]">[[+filename]]</a>
```

## Available Placeholders

| Name     | Description                             |
| -------- | --------------------------------------- |
| url      | The URL that is generated for browsing. |
| filename | The base name of the file or directory. |

## See Also

1. [FileLister.FileLister](extras/filelister)
   1. [FileLister.FileLister.directoryTpl](extras/filelister/filelister/directorytpl)
   2. [FileLister.FileLister.fileLinkTpl](extras/filelister/filelister/filelinktpl)
   3. [FileLister.FileLister.fileTpl](extras/filelister/filelister/filetpl)
2. [FileLister.FileLister.pathTpl](extras/filelister/filelister/pathtpl)
3. [FileLister.Roadmap](extras/filelister/filelister.roadmap)
