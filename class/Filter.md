# Métodos da classe Filter

---

* [withAttr(name, value)](#withattrname-value)

---

## withAttr(name, value)

Filtra os atores/entitades que possuem um dado atributo com um valor específico.

Exemplo de uso:

```java
// filtra os clientes que contenham o atributo "uf" com valor "sp"
loja.getChildren().ofType("cliente").filter().withAttr("uf", "sp");
```

### Parâmetros
* ```String``` name - nome do atributo a ser filtrado
* ```String``` value - valor do atributo a ser filtrado

### Retorno
[Filter](Filter) - este objeto

---

---

## withAttrLike(name, value)

Filtra os atores/entitades que possuem um dado atributo com um valor semelhante ao informado.

No valor, pode-se utilizar os _wildcards_ __*__ e/ou __?__, onde __*__ denota uma _string_ de qualquer comprimento e __?__ corresponde a um único caracter na _string_.

Exemplo de uso:

```java
// filtra os clientes que contenham o atributo "nome" terminados em "aulo"
loja.getChildren().ofType("cliente").filter().withAttrLike("nome", "*aulo");

// filtra os clientes que contenham o atributo "nome" iniciados em "S"
loja.getChildren().ofType("cliente").filter().withAttrLike("nome", "S*");

// filtra os clientes que contenham o atributo "nome" que contenha "aul"
loja.getChildren().ofType("cliente").filter().withAttrLike("nome", "*aul*");

// filtra os clientes que contenham o atributo "nome" iniciado com qualquer letra e que contenha "aul"
loja.getChildren().ofType("cliente").filter().withAttrLike("nome", "?aul*");

// filtra os clientes que contenham o atributo "nome" com exatamente 5 caracteres
loja.getChildren().ofType("cliente").filter().withAttrLike("nome", "?????");
```

### Parâmetros
* ```String``` name - nome do atributo a ser filtrado
* ```String``` value - valor do atributo a ser filtrado por semelhança

### Retorno
[Filter](Filter) - este objeto

---
