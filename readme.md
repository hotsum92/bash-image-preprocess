## image size

512x768

256
320
640
1024
1280
1920

## see image

```
feh *.png
```

## to png

```
convert src.jpg dst.png
```

## generate image

```
convert -size 320x256 -background "#C0C0C0" -fill "#FFFF00" caption:"L" src.jpg
```

## download lena image

```
curl -O https://www.cosy.sbg.ac.at/~pmeerw/Watermarking/lena_color.gif
convert lena_color.gif -resize 320x512! src.jpg
```

<img src="src.jpg" width="256">

## resize stretch

```
convert src.jpg -resize 256x256! resize-stretch.png
```

![resize-stretch.png](resize-stretch.png)

## resize fitting longest side

```
convert src.jpg -resize 256x256 resize-longest.png
```

![resize-longest.png](resize-longest.png)

## resize fitting shortest side

```
convert src.jpg -resize 256x256^ resize-shortest.png
```

![resize-shortest.png](resize-shortest.png)

## resize fitting longest side and crop

```
convert src.jpg -resize 256x256 -background "#C0C0C0" -gravity center -extent 256x256 resize-longest-crop.png
```

![resize-longest-crop.png](resize-longest-crop.png)

## resize fitting shortest side and crop

```
convert src.jpg -resize 256x256^ -gravity center -extent 256x256 resize-shortest-crop.png
```

![resize-shortest-crop.png](resize-shortest-crop.png)


## identify image

```
identify -format '%w %h' img.png
feh -l img.png
```

## sprite image

##### horizontal

```
convert *.png -append sprite.png
```

##### vertical

```
convert *.png +append sprite.png
```

##### nxm

```
montage *.png  -geometry +0+0 -tile 2x2 sprite.png
montage *.png  -geometry +0+0 -tile 2x sprite.png
```


