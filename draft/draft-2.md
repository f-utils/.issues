- Unificação de funções/métodos

```python
def add(x, y):
    if type(x) is list and type(y) is Any:
        return A(x, y) = x.append(y)
    elif type(x) is str and type(y) is str:
        return B(x,y) = x+y
    elif type(x) is set and type(y) is Any:
        return C(x,y) = x.add(y)
    elif type(x) is list type(y) is list:
        return D(x, y) = x.extend(y)
    elif type(x) is list type(y) is set:
        ...
    ...
    else:
        raise TypeError('esses tipos não servem.')
```

- problemas:
    1. refatoração sempre que extensão é necessária
    2. ausência de type safety

----------------------------------

- Ver uma função como sendo um objeto com "estado".

a = [x, y, z] (estado inicial)

add(a, w) = [x, y, z, w] (novo estado)   (extensão)

null = [] (objeto nulo)

b = [x, z, y]

b = add(z,add(y,add(x, null)))

update([x0,x1,x2], (1, 2)) = [x0, x2, x1 ]

b = update(a, (1, 2))

----------------------

Conclusão:
1. objeto nulo + indução (linguagem) + extensão = construção de qualquer objeto 
2. (objeto nulo + indução + extensão) + update = contrução de qualquer objeto de forma otimizada.


---------------------------

```python
def retorno_padrao
f.func('name', 'descrição', retorno_padrao) = []
f.extend('name', (list, set), retorno_caso_lista_conj ) = [x]
f.extend('name', (list, lista), retorno_caso_lista_lista ) = [x, y]
......
f.info('name')
f.extend('name', (str, int), retorno_caso_str_int) = [a, z]
f.update('name', body)((list, set), novo_retorno_caso_lista_conj)
```
