# Métodos da classe Actor

---

* [getParents()](#getparents)
* [getParentActors()](#getparentactors)
* [getParentEntities()](#getparententities)
* [getSiblings()](#getsiblings)
* [getSiblingActors()](#getsiblingactors)
* [getSiblingEntities()](#getsiblingentities)
* [getChildren()](#getchildren)
* [getChildrenActors()](#getchildrenactors)
* [getChildrenEntities()](#getchildrenentities)

---

## getParents()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades/atores pais deste ator, ou seja, que possuem um relacionamento bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais do ator
parents = actor.getParents();
// recupera o 1o ator/entidade relacionado com este ator
parent = parents.next();
```

```java
// itera nas nos atores/entidades relacionados com este ator
for (parent : actor.getParents()) {
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
parents = actor.getParentActors();
// recupera o 1o ator relacionado com este ator
parent = parents.next();
```

```java
// itera nas nos atores relacionados com este ator
for (parent : actor.getParentActors()) {
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
parents = actor.getParentEntities();
// recupera a 1a entidade relacionada com este ator
parent = parents.next();
```

```java
// itera nas nas entidades relacionadas com este ator
for (parent : actor.getParentEntities()) {
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
siblings = actor.getSiblings();
// recupera o 1o irmão deste ator
sibling = siblings.next();
```

```java
// itera nas nos atores/entidades irmãos deste ator
for (sibling : actor.getSiblings()) {
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
siblings = actor.getSiblingActors();
// recupera o 1o irmão deste ator
sibling = siblings.next();
```

```java
// itera nas nos atores irmãos deste ator
for (sibling : actor.getSiblingActors()) {
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
siblings = actor.getSiblingEntities();
// recupera o 1o irmão deste ator
sibling = siblings.next();
```

```java
// itera nas nas entidades irmãs deste ator
for (sibling : actor.getSiblingEntities()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades irmãs deste ator

---

## getChildren()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores/entidades filhos deste ator, ou seja, que são relacionadas de forma bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos do ator
children = actor.getChildren();
// recupera o 1o ator/entidade filho deste ator
child = children.next();
```

```java
// itera nas nos atores/entidades filhos deste ator
for (child : actor.getChildren()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades e atores filhos deste ator

---

## getChildrenActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores filhos deste ator, ou seja, que são relacionadas de forma bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos do ator
children = actor.getChildrenActors();
// recupera o 1o ator filho deste ator
child = children.next();
```

```java
// itera nas nos atores filhos deste ator
for (child : actor.getChildrenActors()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores filhos deste ator

---

## getChildrenEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades filhas deste ator, ou seja, que são relacionadas de forma bidirecional ou unidirecional com este ator.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos do ator
children = actor.getChildrenEntities();
// recupera a 1a entidade filha deste ator
child = children.next();
```

```java
// itera nas nas entidades filhas deste ator
for (child : actor.getChildrenEntities()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades filhas deste ator

---

