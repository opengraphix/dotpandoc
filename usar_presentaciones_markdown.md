# Usar presentaciones en texto plano

Para crear la diapositivas, escribe lo siguiente:

### S5
~~~
pandoc -t s5 -s habitos.txt -o habitos.html
~~~

### Slidy
~~~
pandoc -t slidy -s habitos.txt -o habitos.html
~~~

### Slideous
~~~
pandoc -t slideous -s habitos.txt -o habitos.html
~~~

### DZSlides
~~~
pandoc -t dzslides -s habitos.txt -o habitos.html
~~~

## Beamer
~~~
pandoc -t beamer habitos.txt -o habitos.pdf
~~~

Usando temas, ejemplo: Warsaw

~~~
pandoc -t beamer habitos.txt -V theme:Warsaw -o habitos.pdf
~~~

## Beamer theme Metropolis
~~~
pandoc --toc --slide-level 2 -V theme:metropolis -t beamer --latex-engine=xelatex archivo.md -o archivo.pdf
~~~

## Con fuentes
~~~
pandoc --toc --slide-level 2 -V header-includes:"\usepackage[]{ctex}" -V mainfont:"Fira Sans Book" -V sansfont:"Fira Sans Book" -V monofont:"Fira Sans Book" -V theme:metropolis -V header-includes:"\metroset{background=light}" -t beamer --latex-engine=xelatex archivo.md -o archivo.pdf
~~~

## Reveal JS
~~~
pandoc -t revealjs -s habitos.txt -o SLIDES.html
~~~

~~~
pandoc -t html5 -s --template=template-revealjs.html --standalone --section-divs --variable theme="league" -o habitos.html habitos.txt
~~~

## Template uso de HTML
~~~
pandoc archivo.md -o archivo.html --template template.html --css template.css --self-contained --toc --toc-depth 2
~~~


Soporte:
- Texto centrado
- Controle activados
- Soporte a ecuaciones matemáticas




# Referencias
- [http://pages.stat.wisc.edu/~yandell/statgen/ucla/Help/Producing%20slide%20shows%20with%20Pandoc.html](http://pages.stat.wisc.edu/~yandell/statgen/ucla/Help/Producing%20slide%20shows%20with%20Pandoc.html)
- [https://github.com/hakimel/reveal.js#configuration](https://github.com/hakimel/reveal.js#configuration)
- [https://github.com/dsanson/pandoc-templates/blob/master/default.revealjs](https://github.com/dsanson/pandoc-templates/blob/master/default.revealjs)
