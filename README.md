

### Live preview

```
echo sections/1.tex | entr latex main.tex
xdvi -watchfile 0.5 main.dvi
```

```
echo sections/slide01.tex | entr pdflatex presentation.tex
```

```
ls presentation.tex sections/*tex | entr pdflatex -shell-escape presentation.tex
```
