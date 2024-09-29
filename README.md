# apresentacao-bim1-2024b-Akunozz
apresentacao-bim1-2024b-Akunozz created by GitHub Classroom


Função 7
Crie uma função para validar a lista de bounding boxes. Uma bounding box é válida se x2 >= x1 e y2 >= y1. A função retornará True se todas as bounding boxes da lista forem válidas, ou False em caso contrário.
Resolva esta função sem usar lambda.

##Resolução:
```
areBoundingBoxesValid :: [(Float, Float, Float, Float)] -> Bool
areBoundingBoxesValid [] = True 
areBoundingBoxesValid ((x1, y1, x2, y2):rest) = 
  (x2 >= x1 && y2 >= y1) && areBoundingBoxesValid rest 
```
###Passo a passo:
1. Tipo da Função:
areBoundingBoxesValid :: [(Float, Float, Float, Float)] -> Bool
Definição do nome e tipo da funçao.

2. Caso Base
areBoundingBoxesValid [] = True
Este é o caso base da recursão

3. Caso Recursivo
areBoundingBoxesValid ((x1, y1, x2, y2):rest) = 
  (x2 >= x1 && y2 >= y1) && areBoundingBoxesValid rest

Aqui, a função utiliza pattern matching para decompor a lista de caixas delimitadoras. Ela pega o primeiro retangulo (representada por (x1, y1, x2, y2)) e o restante da lista (rest).

Referências:
https://wiki.haskell.org/Let_vs._Where
https://pt.wikibooks.org/wiki/Haskell/Casamento_de_padr%C3%B5es,_if_e_let
https://haskell.tailorfontela.com.br/input-and-output
