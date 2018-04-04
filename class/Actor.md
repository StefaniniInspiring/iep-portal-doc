# Actor API

---

## getParents()
Prepara a query para consultar as entidades/atores que possuem um relacionamento bidirecional ou unidirecional com este ator.
Exemplo de uso:
```
Relatable parent = actor.getParents().next(); // recupera o 1o ator/entidade relacionado com este ator
```
```
for (Relatable parent : actor.getParents()) { // itera nas nos atores/entidades relacionaods com este ator
    ...
}
```
### Parâmetros
n/a
### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades e atores relacionados com este ator

---

## getParentActors()
Prepara a query para consultar os atores que possuem um relacionamento bidirecional ou unidirecional com este ator.
### Parâmetros
n/a
### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores relacionados com este ator
