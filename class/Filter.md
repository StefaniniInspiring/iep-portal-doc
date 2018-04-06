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

## createdOn(date)

Filtra os atores/entidades com data de criação igual a data informada.

Exemplo de uso:

```java
// filtra os clientes criados no natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().createdOn(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## createdOnOrAfter(date)

Filtra os atores/entidades com data de criação igual ou posterior a data informada.

Exemplo de uso:

```java
// filtra os clientes criados no natal de 2015 ou posteriormente a esta data
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().createdOnOrAfter(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## createdOnOrBefore(date)

Filtra os atores/entidades com data de criação igual ou anterior a data informada.

Exemplo de uso:

```java
// filtra os clientes criados no natal de 2015 ou anteriormente a esta data
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().createdOnOrBefore(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## createdAfter(date)

Filtra os atores/entidades com data de criação posterior a data informada.

Exemplo de uso:

```java
// filtra os clientes criados após o natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().createdAfter(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## createdBefore(date)

Filtra os atores/entidades com data de criação anterior a data informada.

Exemplo de uso:

```java
// filtra os clientes criados anteriormente ao natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().createdOnOrBefore(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## createdBetween(date1, date2)

Filtra os atores/entidades com data de criação dentro de um período, inclusive.

Exemplo de uso:

```java
// filtra os clientes criados entre o natal de 2015 e o reveillon de 2016
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
Date reveillon2016 = new SimpleDateFormat("dd/MM/yyyy").parse("01/01/2016");
loja.getChildren().ofType("cliente").filter().createdBetween(natal2015, reveillon2016);
```

### Parâmetros
* ```Date``` date1 - data inicial do período de filtro da criação do ator/entidade.
* ```Date``` date2 - data final do período de filtro da criação do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---
