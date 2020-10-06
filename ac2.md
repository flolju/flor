Pontificia Universidad Católica de Chile\
Departamento de Ciencia de la Computación\
IIC3745 - Testing\

\

\

\

\

* * * * *

Cobertura {#cobertura .unnumbered}
=========

Predicados: {#predicados .unnumbered}
-----------

-   p1: if is\_hardcover

-   p2: if is\_frecuent\_client

-   p3: if total\_pages $> 500$ && total\_pages\_images $>= 6$

-   p4: if is\_premium\_book && (pages\_of\_text $> 300$ II
    total\_pages\_images $>=5$) && !is\_frecuent\_client

Cláusulas: {#cláusulas .unnumbered}
----------

-   c1: is\_hardcover

-   c2: is\_frecuent\_client

-   c3: total\_pages $> 500$

-   c4: total\_pages\_images $>= 6$

-   c5: if is\_premium\_book

-   c6: pages\_of\_text $> 300$

-   c7: total\_pages\_images $>=5$

-   c8: !is\_frecuent\_client

TR para CC: {#tr-para-cc .unnumbered}
-----------

-   TR1: c1 es TRUE

-   TR2: c1 es FALSE

-   TR3: c2 es TRUE

-   TR4: c2 es FALSE

-   TR5: c3 es TRUE

-   TR6: c3 es FALSE

-   TR7: c4 es TRUE

-   TR8: c4 es FALSE

-   TR9: c5 es TRUE

-   TR10: c5 es FALSE

-   TR11:c6 es TRUE

-   TR12: c6 es FALSE

-   TR13: c7 es TRUE

-   TR14: c7 es FALSE

-   TR15: c8 es TRUE

-   TR16: c8 es FALSE

TR para CC: {#tr-para-cc-1 .unnumbered}
-----------

1.  TC que cumplen con TR1, TR3, TR5, TR7, TR9, TR12, TR13 y TR16:\
    INPUT:

    is\_hardcover= TRUE\
    is\_frecuent\_client = TRUE\
    pages\_of\_text = 250\
    images = 100\
    double\_pages\_images= 100\
    is\_premium\_book = TRUE.\

    OUTPUT: 10.000\

2.  TC que cumplen con TR2, TR6 y TR10.\
    INPUT:

    is\_hardcover= FALSE\
    is\_frecuent\_client = TRUE (NOT EVALUATED)\
    pages\_of\_text = 100\
    images = 6\
    double\_pages\_images= 6\
    is\_premium\_book = FALSE.\

    OUTPUT: 4000\

3.  TC que cumplen con TR1, TR4, TR5, TR8, TR11 y TR15.\
    INPUT:\

    is\_hardcover= TRUE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 500\
    images = 0\
    double\_pages\_images= 1\
    is\_premium\_book = TRUE.\

    OUTPUT: 16.000\

4.  TC que cumplen con TR1, TR4, TR6, TR9, TR12 y TR14.\
    INPUT:\

    is\_hardcover= TRUE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 150\
    images = 1\
    double\_pages\_images= 1\
    is\_premium\_book = TRUE.\

    OUTPUT: 8.000\

TR para CACC: {#tr-para-cacc .unnumbered}
-------------

-   TR1: c1 es TRUE y p1 es TRUE

-   TR2: c1 es FALSE y p1 es FALSE

-   TR3: c2 es TRUE y p2 es TRUE

-   TR4: c2 es FALSE y p2 es FALSE

-   TR5: c3 es TRUE y p3 es TRUE

-   TR6: c3 es FALSE y p3 es FALSE

-   TR7: c4 es TRUE y p3 es TRUE

-   TR8: c4 es FALSE y p3 es FALSE

-   TR9: c5 es TRUE y p4 es TRUE

-   TR10: c5 es FALSE y p4 es FALSE

-   TR11: c6 es TRUE y p4 es TRUE

-   TR12: c6 es FALSE y p4 es FALSE

-   TR13: c7 es TRUE y p4 es TRUE

-   TR14: c7 es FALSE y p4 es FALSE

-   TR15: c8 es TRUE y p4 es TRUE (esto implica c2 FALSE)

-   TR16: c8 es FALSE y p4 es FALSE (esto implica c2 TRUE)

TR para CACC: {#tr-para-cacc-1 .unnumbered}
-------------

1.  TC que cumplen con TR1, TR3, TR5, TR7 y TR16 :\
    INPUT:

    is\_hardcover= TRUE\
    is\_frecuent\_client = TRUE\
    pages\_of\_text = 500\
    images = 100\
    double\_pages\_images= 100\
    is\_premium\_book = TRUE.\

    OUTPUT: 10.000\

2.  TC que cumplen con TR2, TR8, TR9, TR11 y TR15.\
    INPUT:

    is\_hardcover= FALSE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 600\
    images = 2\
    double\_pages\_images= 1\
    is\_premium\_book = TRUE.\

    OUTPUT: 8000\

3.  TC que cumplen con TR1, TR4, TR6, TR12 y TR14.\
    INPUT:\

    is\_hardcover= TRUE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 10\
    images = 1\
    double\_pages\_images= 1\
    is\_premium\_book = TRUE.\

    OUTPUT: 8.000\

4.  TC que cumplen con TR1, TR4, TR6, TR10.\
    INPUT:\

    is\_hardcover= TRUE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 400\
    images = 3\
    double\_pages\_images= 3\
    is\_premium\_book = FALSE\

    OUTPUT: 8.000\

5.  TC que cumplen con TR1, TR4, TR6, TR13.\
    INPUT:\

    is\_hardcover= TRUE\
    is\_frecuent\_client = FALSE\
    pages\_of\_text = 200\
    images = 3\
    double\_pages\_images= 3\
    is\_premium\_book = TRUE\

    OUTPUT: 16.000\


