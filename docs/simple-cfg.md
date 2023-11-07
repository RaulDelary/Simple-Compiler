# Gramática Livre de Contexto

Gramática livre de contexto que reconhece a linguagem de programação SIMPLE:

```plain
G = ({PROGRAMA, COMANDO, INPUT, PRINT, REM, IF, LET, GOTO, END, EXPR, TERMO, FATOR, CONDICAO,
      ITEM, RELACAO, INTEIRO, SINAL, PALAVRA, LABEL, VARIAVEL, DIGITO, LETRA}, {0, 1, 2, 3, 4,
      5, 6, 7, 8, 9, a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y,
      z, (, ), =, !, <, >, +, -, *, /}, P, PROGRAMA)
P = {< PROGRAMA >  ->  < PROGRAMA > < LABEL > < COMANDO >
                   |   < LABEL > < COMANDO >
     < COMANDO >   ->  < INPUT >
                   |   < PRINT >
                   |   < REM >
                   |   < IF >
                   |   < LET >
                   |   < GOTO >
                   |   < END >
     < INPUT >     ->  input < VARIAVEL >
     < PRINT >     ->  print < VARIAVEL >
     < REM >       ->  rem < PALAVRA >
     < IF >        ->  if < CONDICAO > goto < LABEL >
     < LET >       ->  let < VARIAVEL > = < EXPR >
     < GOTO >      ->  goto < LABEL >
     < END >       ->  end
     < EXPR >      ->  < EXPR > + < TERMO >
                   |   < EXPR > - < TERMO >
                   |   < TERMO >
     < TERMO >     ->  < TERMO > * < FATOR >
                   |   < TERMO > / < FATOR >
                   |   < FATOR >
     < FATOR >     ->  ( < EXPR > )
                   |   < ITEM >
     < CONDICAO >  ->  < ITEM > < RELACAO > < ITEM >
     < ITEM >      ->  < VARIAVEL >
                   |   < INTEIRO >
     < RELACAO >   ->  ==
                   |   !=
                   |   >
                   |   >=
                   |   <
                   |   <=                    
     < INTEIRO >   ->  < SINAL > < LABEL >
     < SINAL >     ->  -
                   |   +
                   |   ε
     < PALAVRA >   ->  < PALAVRA > < DIGITO >
                   |   < PALAVRA > < LETRA >
                   |   < DIGITO >
                   |   < LETRA >
     < LABEL >     ->  < LABEL > < DIGITO >
                   |   < DIGITO >
     < VARIAVEL >  ->  < LETRA >
     < DIGITO >    ->  0
                   |   1
                   |   2
                   |   3
                   |   4
                   |   5
                   |   6
                   |   7
                   |   8
                   |   9
     < LETRA >     ->  a
                   |   b
                   |   c
                   |   d
                   |   e
                   |   f
                   |   g
                   |   h
                   |   i
                   |   j
                   |   k
                   |   l
                   |   m
                   |   n
                   |   o
                   |   p
                   |   q
                   |   r
                   |   s
                   |   t
                   |   u
                   |   v
                   |   w
                   |   x
                   |   y
                   |   z  }
```
