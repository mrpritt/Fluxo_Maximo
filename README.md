# Fluxo Máximo
Código de suporte para o trabalho prático em problemas de fluxo máximo.


## Gerador Washington

>To use:
>
>         cc washington.c -o gengraph
>
>         gengraph function arg1 arg2 arg3
>
>Command line arguments have the following meanings:
>
>         function:           index of desired graph type
>         arg1, arg2, arg3:   meanings depend on graph type (briefly listed below: see code comments for more info)
>Mesh Graph:          1 rows  cols  maxcapacity
> 
>Random Level Graph:  2 rows  cols  maxcapacity
> 
>Random 2-Level Graph:3 rows  cols  maxcapacity
> 
>Matching Graph:      4 vertices  degree
> 
>Square Mesh:         5 side  degree  maxcapacity
> 
>Basic Line:          6 rows  cols  degree
> 
>Exponential Line:    7 rows  cols  degree
> 
>Double Exponential   8 rows  cols  degree
> 
>DinicBadCase:        9 vertices
> 
>(causes n augmentation phases)
> 
>GoldBadCase         10 vertices
> 
>Cheryian            11 dim1 dim2  range
> 
>(last 2 are bad for goldberg's algorithm)

| No. | Nome | Parâmetros | Descrição | n | m |
|--|--|--|--|--|--|
|   1 | Mesh | r,c | Grade, 3 viz. 1 direita | rc+2 | 3r(c-1) |
|   2 | Random level | r,c | Grade, 3 viz. rand. 1 direita | rc+2 | 3r(c-1) |
|   3 | Random 2-level | r,c | Grade, 3 viz. rand. 2 direita | rc+2 | 3r(c-1) |
|   4 | Matching | n,d | Bipart. n-n, d viz. rand. | 2n+2 | n(d+2) |
|   5 | Square Mesh | d,D | Quadr. mesh dxd, grau D | d*d+2 | (d-1)dD+2d |
|   6 | BasicLine | n,m,D | Linha, grau D| nm+2 | nmD+2m |
|   7 | ExpLine | n,m,D | Linha, grau D | nm+2 | nmD+2m |
|   8 | DExpLine | n,m,D | Linha, grau D | nm+2 | nmD+2m |
|   9 | DinicBad | n | Linha | n | 2n-3|
|  10 | GoldBad | n | | 3n+3 | 4n+1 |
