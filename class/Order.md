
# Métodos da classe Order

---

---

## byId()

Ordena os atores/entidades resultantes de uma consulta pelo seu respectivo identificador único.

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

Exemplo de uso:

```java
// ordena os clientes pelo atributo "nome"
loja.getChildren().ofType("cliente").order().byAttr("nome");
```

## Parâmetros
* ```String``` nome - nome do atributo usado para ordenação

### Retorno
[Order](Order) - este objeto

---

## byCreateDate()

Ordena os atores/entidades resultantes de uma consulta pela respectiva data de criação.

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

