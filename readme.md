## image size

512x768

256
320
640
1024
1280
1920

## generate image

```
convert -size 512x768 -background "#C0C0C0" -fill "#FFFF00" caption:"L" src.jpg
```

![src.jpg](src.jpg)

## to png

```
convert src.jpg dst.png
```

## resize stretch

```
convert src.jpg -resize 256x256! dst.png
```

## resize fitting longest side

```
convert src.jpg -resize 256x256 dst.png
```

## resize fitting shortest side

```
convert src.jpg -resize 256x256^ dst.png
```

## resize fitting longest side and crop

```
convert src.jpg -resize 256x256 -gravity center -extent 256x256 dst.png
```

## resize fitting shortest side and crop

```
convert src.jpg -resize 256x256^ -gravity center -extent 256x256 dst.png
```

## resize square and crop

```
convert src.jpg 
```
