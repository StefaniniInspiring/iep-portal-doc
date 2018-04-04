# Actor API

---

## getParents()
Prepara a query para consultar as entidades/atores pais deste ator, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// recupera o 1o ator/entidade relacionado com este ator
Relatable parent = actor.getParents().next();
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
Prepara a query para consultar os atores pais, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// recupera o 1o ator relacionado com este ator
Actor parent = actor.getParentActors().next();
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
