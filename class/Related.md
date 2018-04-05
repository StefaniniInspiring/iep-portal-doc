# Métodos da classe Related

---

## ofType(types)

Filtra os relacionamentos pelo tipo ou configuração da entitade ou ator relacionado.

Pode se informado um ou mais tipos. No caso de vários tipos, estes serão tratados como um OR: tipo1 or tipo2 ... or tipoN.

Exemplo de uso:

```java
// filtra os relacionamentos dos tipos "cliente" ou "empregado"
loja.getChildren().ofType("cliente", "empregado");
```

### Parâmetros
* ```String``` types - um ou mais tipos (códigos de configuração) de ator ou entitade.

### Retorno
[Related](Related) - este objeto

---

## relatedOn(date)

Filtra os relacionamentos criados em uma data específica.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedOn(yesterday);
```

### Parâmetros
* ```Date``` date - data de criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## relatedOnOrAfter(date)

Filtra os relacionamentos criados a partir de uma data específica.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados desde ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedOnOrAfter(yesterday);
```

### Parâmetros
* ```Date``` date - data de criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## relatedOnOrBefore(date)

Filtra os relacionamentos criados anteriormente ou em uma data específica.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados ontem ou anteriormente
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedOnOrBefore(yesterday);
```

### Parâmetros
* ```Date``` date - data de criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## relatedAfter(date)

Filtra os relacionamentos criados após um data específica.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados após a data de ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedAfter(yesterday);
```

### Parâmetros
* ```Date``` date - data de criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## relatedBefore(date)

Filtra os relacionamentos criados anteriormente a uma data específica.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados antes de ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedBefore(yesterday);
```

### Parâmetros
* ```Date``` date - data de criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## relatedBetween(date1, date2)

Filtra os relacionamentos criados entre duas datas específicas, inclusive.

Exemplo de uso:

```java
// filtra os relacionamentos que foram criados entre antes de ontem e ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
Date beforeYesterday = DateUtils.addDays(yersterday, -1);
entity.getChildren().relatedBetween(beforeYesterday, yesterday);
```

### Parâmetros
* ```Date``` date1 - data inicial do período que compara a criação do relacionamento.
* ```Date``` date2 - data final do período que compara a criação do relacionamento.

### Retorno
[Related](Related) - este objeto

---

## offset(n)

Usado para paginação, desconsidera os primeiros n resultados da consulta.

Pode-se pensar também como _n_ sendo indice do primeiro relacionamento a se retornar, com o primeiro elemento indexado na posição 0, o segundo em 1 e assim por diante.

Exemplo de uso:

```java
// consulta o 2o filho da entidade
entity.getChildren().offset(1).next();
```

### Parâmetros
* ```int``` n - número de resultados a serem descartados em uma consulta.

### Retorno
[Related](Related) - este objeto

---

## limit(n)

Limita a quantidade máxima de relacionamentos da consulta.

Exemplo de uso:

```java
// limita a consulta em no máximo 10 resultados
entity.getChildren().limit(10);
```

### Parâmetros
* ```int``` n - quantidade máxima de resultados na consulta.

### Retorno
[Related](Related) - este objeto

---
