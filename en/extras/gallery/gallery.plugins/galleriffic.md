---
title: "Galleriffic"
_old_id: "881"
_old_uri: "revo/gallery/gallery.plugins/gallery.plugins.galleriffic"
---

## Gallerriffic Plugin for Gallery

The Gallerriffic Plugin allows you to quickly output a Gallery and display its images. It requires you to have jQuery already loaded in the page for it to work.

## Usage

Simply add this parameter to the Gallery snippet:

``` php
[[!Gallery? &plugin=`galleriffic`]]
```

## Available Properties

Galleriffic will override the following properties in the [Gallery](extras/gallery "Gallery") snippet. If you want to override them, simply pass the galleriffic-prefixed property instead.

| Name                    | Overrides    | Description                               | Default Value        |
| ----------------------- | ------------ | ----------------------------------------- | -------------------- |
| gallerifficThumbTpl     | thumbTpl     | The thumb Chunk to use for each Item.     | GallerifficItemThumb |
| gallerifficContainerTpl | containerTpl | The container Chunk to wrap content with. | Galleriffic          |
| gallerifficThumbWidth   | thumbWidth   | The width of the thumbnails.              | 75                   |
| gallerifficThumbHeight  | thumbHeight  | The height of the thumbnails.             | 75                   |

Galleriffic also comes with a few of its own, custom properties. You can pass these into the [Gallery](extras/gallery "Gallery") snippet to override their defaults.

| Name                      | Description                                                   | Default Value       |
| ------------------------- | ------------------------------------------------------------- | ------------------- |
| numThumbs                 | The number of thumbnails to show per page.                    | 15                  |
| navigationWidth           | The width, in pixels, of the navigation.                      | 300px               |
| enableTopPager            | Whether or not to show the top pagination.                    | 1                   |
| enableBottomPager         | Whether or not to show the bottom pagination.                 | 1                   |
| maxPagesToShow            | Maximum number of pages to show.                              | 7                   |
| renderSSControls          | Whether or not to render the slideshow controls.              | 1                   |
| renderNavControls         | Whether or not to render the navigation controls.             | 1                   |
| enableHistory             | Whether or not to enable history.                             | 0                   |
| autoStart                 | Whether or not to automatically start the slideshow.          | 0                   |
| defaultTransitionDuration | The duration, in milliseconds, of transitions.                | 500                 |
| thumbsContainerSel        | The CSS selector of the container holding the thumbnails.     | #gal-gaff-thumbs    |
| imageContainerSel         | The CSS selector of the container holding the main image.     | #gal-gaff-slideshow |
| captionContainerSel       | The CSS selector of the container holding the caption.        | #gal-gaff-caption   |
| controlsContainerSel      | The CSS selector of the container holding the nav controls.   | #gal-gaff-controls  |
| loadingContainerSel       | The CSS selector of the container holding the loading screen. | #gal-gaff-loading   |
| playLinkText              | The text used for the Play Slideshow link.                    |
| pauseLinkText             | The text used for the Pause Slideshow link.                   |
| prevLinkText              | The text used for the Previous Photo link.                    |
| nextLinkText              | The text used for the Next Photo link.                        |
| prevPageLinkText          | The text used for the Previous Page link.                     |
| nextPageLinkText          | The text used for the Next Page link.                         |

## Examples

Use the Galleriffic plugin, but only display 10 thumbs per page:

``` php
[[!Gallery?
   &toPlaceholder=`gallery`
   &album=`My Photos`
   &plugin=`galleriffic`
   &numThumbs=`10`
]]
```

Hide the pagination and 'show slideshow' controls, but automatically start the slideshow:

``` php
[[!Gallery?
   &toPlaceholder=`gallery`
   &album=`My Photos`
   &plugin=`galleriffic`
   &renderNavControls=`0`
   &renderSSControls=`0`
   &autoStart=`1`
]]
```

## See Also

1. [Gallery.Gallery](extras/gallery/gallery/index)
    1. [Gallery.Gallery.containerTpl](extras/gallery/gallery/containertpl)
    2. [Gallery.Gallery.thumbTpl](extras/gallery/gallery/thumbtpl)
2. [Gallery.GalleryAlbums](extras/gallery/gallery.galleryalbums)
    1. [Gallery.GalleryAlbums.containerTpl](extras/gallery/gallery.galleryalbums/containertpl)
    2. [Gallery.GalleryAlbums.rowTpl](extras/gallery/gallery.galleryalbums/rowtpl)
3. [Gallery.GalleryItem](extras/gallery/gallery.galleryitem)
    1. [Gallery.GalleryItem.albumTpl](extras/gallery/gallery.galleryitem/albumtpl)
    2. [Gallery.GalleryItem.GalleryItemPagination](extras/gallery/gallery.galleryitem/galleryitempagination)
    3. [Gallery.GalleryItem.tagTpl](extras/gallery/gallery.galleryitem/tagtpl)
    4. [Gallery.GalleryItem.tpl](extras/gallery/gallery.galleryitem/tpl)
4. [Gallery.Plugins](extras/gallery/gallery.plugins)
    1. [Gallery.Plugins.Galleriffic](extras/gallery/gallery.plugins/galleriffic)
    2. [Gallery.Plugins.Slimbox](extras/gallery/gallery.plugins/slimbox)
5. [Gallery.Setting Up Your Gallery](extras/gallery/gallery.setting-up-your-gallery)
6. [Gallery.Example1](extras/gallery/gallery.example1)
7. [Gallery.Setting Up the GalleryItem TV](extras/gallery/gallery.setting-up-the-galleryitem-tv)
