# Métodos da classe Entity

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
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades/atores pais desta entidade, ou seja, que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais da entidade
Related parents = entity.getParents();
// recupera o 1o ator/entidade relacionado com esta entidade
Relatable parent = parents.next();
```

```java
// itera nas nos atores/entidades relacionados com esta entidade
for (Relatable parent : entity.getParents()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades e atores relacionados com esta entidade

---

## getParentActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores pais desta entidade, ou seja, que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais da entidade
Related parents = entity.getParentActors();
// recupera o 1o ator relacionado com esta entidade
Actor parent = parents.next();
```

```java
// itera nas nos atores relacionados com esta entidade
for (Actor parent : entity.getParentActors()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores relacionados com esta entidade

---

## getParentEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades pais desta entidade, ou seja, que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os pais da entidade
Related parents = entity.getParentEntities();
// recupera a 1a entidade relacionada com esta entidade
Entity parent = parents.next();
```

```java
// itera nas nas entidades relacionadas com esta entidade
for (Entity parent : entity.getParentEntities()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades relacionadas com esta entidade

---

## getSiblings()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores/entidades irmãos desta entidade, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos da entidade
Related siblings = entity.getSiblings();
// recupera o 1o irmão desta entidade
Relatable sibling = siblings.next();
```

```java
// itera nas nos atores/entidades irmãos desta entidade
for (Relatable sibling : entity.getSiblings()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores/entidades irmãos desta entidade

---

## getSiblingActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores irmãos desta entidade, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos da entidade
Related siblings = entity.getSiblingActors();
// recupera o 1o irmão desta entidade
Actor sibling = siblings.next();
```

```java
// itera nas nos atores irmãos desta entidade
for (Actor sibling : entity.getSiblingActors()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores irmãos desta entidade

---

## getSiblingEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades irmãs desta entidade, ou seja, que são relacionadas com entidades que possuem um relacionamento bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os irmãos da entidade
Related siblings = entity.getSiblingEntities();
// recupera o 1o irmão desta entidade
Entity sibling = siblings.next();
```

```java
// itera nas nas entidades irmãs desta entidade
for (Entity sibling : entity.getSiblingEntities()) {
    ...
}
```
### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades irmãs desta entidade

---

## getChildren()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores/entidades filhos desta entidade, ou seja, que são relacionadas de forma bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos da entidade
Related children = entity.getChildren();
// recupera o 1o ator/entidade filho desta entidade
Relatable child = children.next();
```

```java
// itera nas nos atores/entidades filhos desta entidade
for (Relatable child : entity.getChildren()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades e atores filhos desta entidade

---

## getChildrenActors()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta os atores filhos desta entidade, ou seja, que são relacionadas de forma bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos da entidade
Related children = entity.getChildrenActors();
// recupera o 1o ator filho desta entidade
Actor child = children.next();
```

```java
// itera nas nos atores filhos desta entidade
for (Actor child : entity.getChildrenActors()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar atores filhos desta entidade.

---

## getChildrenEntities()
Constrói um objeto do tipo [Related](Related) que quando iterado consulta as entidades filhas desta entidade, ou seja, que são relacionadas de forma bidirecional ou unidirecional com esta entidade.

Exemplo de uso:

```java
// constrói o objeto capaz de consultar os filhos da entidade
Related children = entity.getChildrenEntities();
// recupera a 1a entidade filha desta entidade
Entity child = children.next();
```

```java
// itera nas nas entidades filhas desta entidade
for (Entity child : entity.getChildrenEntities()) {
    ...
}
```

### Parâmetros
n/a

### Retorno
[Related](Related) - um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html) que contém a query para consultar entidades filhas desta entidade

---
