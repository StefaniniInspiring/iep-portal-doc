# Métodos da classe Actor

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

---

## getParentEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades pais deste ator, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais do ator
Related parents = actor.getParentEntities();
// recupera a 1a entidade relacionada com este ator
Entity parent = parents.next();
```

```java
// itera nas nas entidades relacionadas com este ator
for (Entity parent : actor.getParentEntities()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades relacionadas com este ator

---

## getSiblings()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores/entidades irmãos deste ator, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos do ator
Related siblings = actor.getSiblings();
// recupera o 1o irmão deste ator
Relatable sibling = siblings.next();
```

```java
// itera nas nos atores/entidades irmãos deste ator
for (Relatable sibling : actor.getSiblings()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores/entidades irmãos deste ator

---

## getSiblingActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores irmãos deste ator, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos do ator
Related siblings = actor.getSiblingActors();
// recupera o 1o irmão deste ator
Actor sibling = siblings.next();
```

```java
// itera nas nos atores irmãos deste ator
for (Actor sibling : actor.getSiblingActors()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores irmãos deste ator

---

## getSiblingEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades irmãs deste ator, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos do ator
Related siblings = actor.getSiblingEntities();
// recupera o 1o irmão deste ator
Entity sibling = siblings.next();
```

```java
// itera nas nas entidades irmãs deste ator
for (Entity sibling : actor.getSiblingEntities()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades irmãs deste ator

---
