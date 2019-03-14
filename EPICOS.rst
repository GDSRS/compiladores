=====================================
Hacking em cima de linguagens maduras
=====================================

Épicos relacionados à linguagens de programação de uso industrial. Exige um pouco de coragem.

Operador pipe para Python ou Lua (10,0 pts)
==========================================

Python e Lua são duas linguagens conhecidas por possuir uma sintaxe relativamente simples e interpretadores fáceis de modificar. No entanto, nenhuma delas possui o operador de "pipe" nativo. Este operador é comum em linguagens funcionais e permite escrever longas cadeias de funções aninhadas de um modo fácil de ler e entender.

A idéia é oferecer uma sintaxe alternativa para a chamada de função onde ``f(x)`` pode ser escrito como ``x |> f`` ou ``f <| x``.   Apesar de parecer uma mudança desenecessária nos casos, simples, pode ser útil em chamadas de função muito aninhadas como:

>>> squared(minimum(normalize_items(list_of_items)))
>>> list_of_items |> normalize_items |> minimum |> squared

A segunda forma tende a ser mais legível pois a ordem de leitura segue a ordem de aplicação das funções.

Este épico consiste em implementar o operador de pipe (substituindo-o pela chamada de função correspondente) em uma destas linguagens. Este épico pode ser modificado para outras linguagens de programação. Note que várias linguagens possuem gramáticas muito complexas (ex.: Ruby) e/ou compiladores/interpretadores muito sofisticados e difíceis de modificar (ex.: JavaScript). Python e Lua foram seleciondos devido à simplicidade da implementação padrão.


==========
Transpyler
==========


Operador pipe para Python no Framework Transpyler (7,0 pts)
===========================================================

Como no caso anterior, mas ao invés de modificar diretamente o interpretador, utiliza a estrutura do Transpyler (https://github.com/transpyler/transpyler/) para fazer a tradução do código para Python puro.

Bonus:

* (1,0pt) Permitir a importação direta deste Python extendido (*.py+) de um programa Python qualquer. Isto é possível utilizando os import Hooks do Python.




  
