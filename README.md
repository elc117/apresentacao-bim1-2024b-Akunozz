# apresentacao-bim1-2024b-Akunozz
apresentacao-bim1-2024b-Akunozz created by GitHub Classroom


Função 7
Crie uma função para validar a lista de bounding boxes. Uma bounding box é válida se x2 >= x1 e y2 >= y1. A função retornará True se todas as bounding boxes da lista forem válidas, ou False em caso contrário.
Resolva esta função sem usar lambda.

<h2>Resolução:</h2>

```
areBoundingBoxesValid :: [(Float, Float, Float, Float)] -> Bool
areBoundingBoxesValid ((x1, y1, x2, y2):rest) = 
  (x2 >= x1 && y2 >= y1) && areBoundingBoxesValid rest 
``` 

<h3>Passo a passo:</h3>
<h5>1. Tipo da Função:</h5>

```
areBoundingBoxesValid :: [(Float, Float, Float, Float)] -> Bool
```

Definição do nome e tipo da funçao.

<h5>2. Função:</h5>

```
areBoundingBoxesValid ((x1, y1, x2, y2):rest) = 
```

Pega a primeira caixa e separa do restante (rest).
<h5>3. Condição de Validação:</h5>

```
(x2 >= x1 && y2 >= y1) && areBoundingBoxesValid rest 
```

Verfica as coordenadas se pode ser um retangulo e retorna True caso for, se não retorna False.


Outra tentativa:
```
areBoundingBoxesValid :: [(Float, Float, Float, Float)] -> Bool
areBoundingBoxesValid ((x1, y1, x2, y2):rest) =
  if isValid
  then areBoundingBoxesValid rest
  else False
  where
    isValid = x2 >= x1 && y2 >= y1
```

Referências:
https://wiki.haskell.org/Let_vs._Where
https://pt.wikibooks.org/wiki/Haskell/Casamento_de_padr%C3%B5es,_if_e_let
https://haskell.tailorfontela.com.br/input-and-output
