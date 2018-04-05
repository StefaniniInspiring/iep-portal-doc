# Actor API

---

## getParents()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades/atores pais deste ator, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais do ator
Related parents = actor.getParents();
// recupera o 1o ator/entidade relacionado com este ator
Relatable parent = parents.next();
```

```java
// itera nas nos atores/entidades relacionados com este ator
for (Relatable parent : actor.getParents()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades e atores relacionados com este ator

---

## getParentActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores pais deste ator, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais do ator
Related parents = actor.getParentActors();
// recupera o 1o ator relacionado com este ator
Actor parent = parents.next();
```

```java
// itera nas nos atores relacionados com este ator
for (Actor parent : actor.getParentActors()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores relacionados com este ator
