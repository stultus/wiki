# Losslessly optimising images



Glenn Randers-Pehrson’s [pngcrush](https://pmt.sourceforge.io/pngcrush/):

```
$ pngcrush -reduce -verbose $IN.png $OUT.png
```

Timo Kokkonen’s [jpegoptim](https://github.com/tjko/jpegoptim):

```
$ jpegoptim --all-normal --verbose $IN.jpg $OUT.jpg
```

Eddie Kohler’s [gifsicle](https://www.lcdf.org/gifsicle/):

```
$ gifsicle -O3 --verbose -i $IN.gif -o $OUT.gif
```

Jeff Schiller and Louis Simard’s [scour](https://github.com/scour-project/scour):

```
$ scour -i $IN.svg -o $OUT.svg
```
