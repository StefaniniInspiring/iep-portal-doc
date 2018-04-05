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
* types - um ou mais tipos (códigos de configuração) de ator ou entitade.

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
* date - data de criação do relacionamento

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
* date - data de criação do relacionamento

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
* date - data de criação do relacionamento

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
* date - data de criação do relacionamento

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
* date - data de criação do relacionamento

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
* date - data de criação do relacionamento

### Retorno
[Related](Related) - este objeto

---

## offset(n)

Usado para paginação, desconsidera os primeiros n resultados da consulta.

O primeiro elemento é indexado na posição 0.

Exemplo de uso:

```java
// consulta o 2o filho da entidade
entity.getChildren().offset(1).next();
```

### Parâmetros
* n - número de resultados a serem descartados em uma consulta

### Retorno
[Related](Related) - este objeto

---
