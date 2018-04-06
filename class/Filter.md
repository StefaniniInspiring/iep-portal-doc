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
