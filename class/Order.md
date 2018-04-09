
# Métodos da classe Order

---

* [byId()](#byid)
* [byAttr(name)](#byattrname)
* [byCreateDate()](#bycreatedate)
* [byUpdateDate()](#byupdatedate)
* [desc()](#desc)

---

## byId()

Ordena os atores/entidades resultantes de uma consulta pelo seu respectivo identificador único.

A ordenação é crescente, para ordenar de forma decrescente, deve-se invocar o método [desc()](#desc) logo após este método.

Exemplo de uso:

```java
// ordena os clientes por ID
loja.getChildren().ofType("cliente").order().byId();
```

## Parâmetros
n/a

### Retorno
[Order](Order) - este objeto

---

## byAttr(name)

Ordena os atores/entidades resultantes de uma consulta pelo valor de um atributo específico.

A ordenação é crescente, para ordenar de forma decrescente, deve-se invocar o método [desc()](#desc) logo após este método.

Exemplo de uso:

```java
// ordena os clientes pelo atributo "nome"
loja.getChildren().ofType("cliente").order().byAttr("nome");
```

## Parâmetros
* ```String``` name - nome do atributo usado para ordenação

### Retorno
[Order](Order) - este objeto

---

## byCreateDate()

Ordena os atores/entidades resultantes de uma consulta pela respectiva data de criação.

A ordenação é crescente, para ordenar de forma decrescente, deve-se invocar o método [desc()](#desc) logo após este método.

Exemplo de uso:

```java
// ordena os clientes pela data de criação
loja.getChildren().ofType("cliente").order().byCreateDate();
```

## Parâmetros
n/a

### Retorno
[Order](Order) - este objeto

---

## byUpdateDate()

Ordena os atores/entidades resultantes de uma consulta pela respectiva data de última atualização.

A ordenação é crescente, para ordenar de forma decrescente, deve-se invocar o método [desc()](#desc) logo após este método.

Exemplo de uso:

```java
// ordena os clientes pela data de última atualização
loja.getChildren().ofType("cliente").order().byUpdateDate();
```

## Parâmetros
n/a

### Retorno
[Order](Order) - este objeto

---

## desc()

Torna a ordenação invocada anterior a este método no sentido decrescente.

Exemplo de uso:

```java
// ordena os clientes pelo atributo "nome" de forma decrescente
loja.getChildren().ofType("cliente").order().byAttr("nome").desc();
```

### Parâmetros
n/a

### Retorno
[Order](Order) - este objeto

---
