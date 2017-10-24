# GIFEncoder

This class can be used to generate a GIF animation from a set of individual frames in GIF image format.
The class takes as input parameters the list of GIF frame image files, the animation delay between each frame, the horizontal and vertical offset of each frame image.
It combines all image frames and generates a single animated GIF file using only PHP code without using the GD library or other image extensions or external programs .
The animation background may be set to a given color or be made transparent.

> Example with image sources

```php
<?php
  include "GIFEncoder.class.php";
  
  $gif = new GIFEncoder(
    array("image01.gif", "image02.gif", "image03.gif", ...),
    array(5, 5, 5, ...),
    0,
    2,
    255, 255, 255,
    "url"
  );
  
  header ( 'Content-type:image/gif' );
  echo	$gif->GetAnimation ( );
?>
```

Parameters:
1 array of images
2 array of delays
3 animation loop, use 0 is for ever, (1, 2, 3, 4, ...) integer for how many times repeat the animation
5 transparent color declaration as RGB color
6 source
