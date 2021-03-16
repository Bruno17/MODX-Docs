---
title: "rowTpl"
_old_id: "874"
_old_uri: "revo/gallery/gallery.galleryalbums/gallery.galleryalbums.rowtpl"
---

## GalleryAlbums' rowTpl Chunk

This chunk is used for each Album iterated through by the [GalleryAlbums](extras/gallery/gallery.galleryalbums "Gallery.GalleryAlbums") snippet.

## Default Value

``` php
<li[[+cls:notempty=``]]><a href="[[~[[*id]]? &[[+albumRequestVar]]=`[[+id]]`]]">[[+showName:notempty=`[[+name]]`]]</a></li>
```

## Available Placeholders

| Name            | Description                                                                                                                                              |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id              | The ID of the Album.                                                                                                                                     |
| name            | The name of the Album.                                                                                                                                   |
| parent          | The parent ID of the Album. Defaults to 0.                                                                                                               |
| description     | The description of the Album.                                                                                                                            |
| createdon       | A timestamp of when the Album was created.                                                                                                               |
| createdby       | The ID of the User that created this Album.                                                                                                              |
| rank            | The 'rank', or order, in which this Album is stored as.                                                                                                  |
| active          | Whether or not this Album is marked "Active". Can be 1 or 0.                                                                                             |
| prominent       | Whether or not this Album is marked "Prominent". Can be 1 or 0.                                                                                          |
| albumRequestVar | The albumRequestVar parameter passed to the [GalleryAlbums](extras/gallery/gallery.galleryalbums "Gallery.GalleryAlbums") snippet. Defaults to galAlbum. |
| image           | The link to an image as determined by the GalleryAlbums snippet.                                                                                         |

When you use the image placeholder in your template as the source for an image tag, it doesn't seem to obey the thumbnail properties given in the snippet-call. But no worries, you can add them yourself as this image-placeholder is actually a call to phpthumb. So, lets say you want your thumbnail to be 240x160 with zoomcrop, you can do:

``` php
<img src="[[+image]]&w=240&h=160&zc=1" alt="[[+name]]" />
```

## See Also

1. [Gallery.Gallery](extras/gallery/gallery/index)
   1. [Gallery.Gallery.containerTpl](extras/gallery/gallery/containertpl)
   2. [Gallery.Gallery.thumbTpl](extras/gallery/gallery/thumbtpl)
2. [Gallery.GalleryAlbums](extras/gallery/gallery.galleryalbums)
   1. [Gallery.GalleryAlbums.rowTpl](extras/gallery/gallery.galleryalbums/rowtpl)
3. [Gallery.GalleryItem](extras/gallery/gallery.galleryitem)
   1. [Gallery.GalleryItem.albumTpl](extras/gallery/gallery.galleryitem/albumtpl)
   2. [Gallery.GalleryItem.GalleryItemPagination](extras/gallery/gallery.galleryitem/galleryitempagination)
   3. [Gallery.GalleryItem.tagTpl](extras/gallery/gallery.galleryitem/tagtpl)
4. [Gallery.GalleryItem.tpl](extras/gallery/gallery.galleryitem/tpl)
5. [Gallery.Plugins](extras/gallery/gallery.plugins)
   1. [Gallery.Plugins.Galleriffic](extras/gallery/gallery.plugins/galleriffic)
   2. [Gallery.Plugins.Slimbox](extras/gallery/gallery.plugins/slimbox)
6. [Gallery.Setting Up Your Gallery](extras/gallery/gallery.setting-up-your-gallery)
7. [Gallery.Example1](extras/gallery/gallery.example1)
8. [Gallery.Setting Up the GalleryItem TV](extras/gallery/gallery.setting-up-the-galleryitem-tv)
