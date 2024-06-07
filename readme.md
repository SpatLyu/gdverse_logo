
``` r
library(showtext)
showtext_auto(enable = TRUE)
font_add("ShineTypewriter", regular = "./ShineTypewriter-lgwzd.ttf")
library(magick)

image_read('./logo1.png') |> 
  image_resize("256x256")|> 
  image_annotate("gdverse",
                 gravity = "northwest",
                 location = "+84+111",
                 color = ggplot2::alpha('#ffffff',0.8),
                 size = 30,
                 font = "ShineTypewriter") |> 
  image_write('./gdverse_logo.png')
```

![](./gdverse_logo.png)

**Thanks to `Cao Yue` for her help on background image extraction.**
