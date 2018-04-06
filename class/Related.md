# Métodos da classe Related

---

* [ofType(types)](#oftypetypes)
* [relatedOn(date)](#relatedondate)
* [relatedOnOrAfter(date)](#relatedonorafterdate)
* [relatedOnOrBefore(date)](#relatedonorbeforedate)
* [relatedAfter(date)](#relatedafterdate)
* [relatedBefore(date)](#relatedbeforedate)
* [relatedBetween(date1, date2)](#relatedbetweendate1-date2)
* [offset(n)](#offsetn)
* [limit(n)](#limitn)
* [filter()](#filter)

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

## filter()

Retorna um objeto [Filter](Filter) para filtrar os atores/entidades da consulta.

### Parâmetros
n/a

### Retorno
[Filter](Filter) - objeto para filtrar os atores/entidades da consulta.

---

## order()

Retorna um objeto [Order](Order) para ordenar os atores/entidades da consulta.

### Parâmetros
n/a

### Retorno
[Order](Order) - objeto para ordenar os atores/entidades resultantes de uma consulta.

---

## count()
Realiza a consulta dos relacionamentos e retorna a quantidade de elementos encontrados.

Exemplo de uso:

```java
// contar a quantidade de clientes de uma loja
long clientes = loja.getChildren().ofType("cliente").count();
```

### Parâmetros
n/a

### Retorno
```long``` - a quantidade de elementos encontrados na consulta.

---

## iterator()

Retorna o [Iterator](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html) deste objeto, capaz de realizar a consulta dos relacionamentos e disponibilizar o resultado durante uma iteração.

Este método é chamado automaticamente em uma iteração ou quando este objeto é usado no construtor de uma [Collection](https://docs.oracle.com/javase/8/docs/api/java/util/Collection.html):

```java
Related related = loja.getChildren();

// related.iterator() invocado automaticamente
for(Entity entity : related) { 
  ...
}

// related.iterator() invocado automaticamente
List children = new ArrayList(related);
```

### Parâmetros
n/a

### Retorno
[Iterator](https://docs.oracle.com/javase/8/docs/api/java/util/Iterator.html) - objeto para iterar nos resultados da consulta.

---

## toList()

Realiza a consulta, itera nos resultados e os insere em uma lista.

Exemplo:

```java
// consulta os clientes de uma loja e os insere em uma lista
List<Actors> clientes = loja.getChildrenActors().ofType("cliente").toList();
```

### Parâmetros
n/a

### Retorno
[List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)<[Relatable](Relatable)> - o resultado da consulta em uma lista.

---
 ## toMap()
 Realiza a consulta, itera nos resultados e os insere em um mapa onde a chave é o ID do ator/entidade e o valor é o respectivo ator/entidade.
 
 Exemplo:
 
```java
// consulta os clientes de uma loja e os insere em um mapa
Map<String, Actor> clientePorId = loja.getChildrenActors().ofType("cliente").toMap();
```

### Parâmetros
n/a

### Retorno
[Map](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html)<```String```, [Relatable](Relatable)> - o resultado da consulta em um mapa indexado pelos identificadores dos resultados.

---

## groupByType()
Realiza a consulta, itera nos resultados e os insere em um mapa onde a chave é o tipo (configuração) do ator/entidade e o valor é o respectivo ator/entidade.

```java
// consulta os clientes de uma loja e os insere em um mapa indexado pelo tipo de cada cliente
Map<String, Actor> clientePorTipo = loja.getChildrenActors().ofType("cliente").groupByType();
```

### Parâmetros
n/a

### Retorno
[Map](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html)<```String```, [Relatable](Relatable)> - o resultado da consulta em um mapa indexado pelas configurações dos resultados.

---

## groupByAttr(name)
Realiza a consulta, itera nos resultados e os insere em um mapa onde a chave é valor de um atributo do ator/entidade e o valor é o respectivo ator/entidade.

```java
// consulta os clientes de uma loja e os insere em um mapa indexado pela idade de cada cliente
Map<String, Actor> clientePorIdade = loja.getChildrenActors().ofType("cliente").groupByAttr("idade");
```

### Parâmetros
* ```String``` name - nome do atributo usado para indexar o resultado.

### Retorno
[Map](https://docs.oracle.com/javase/8/docs/api/java/util/Map.html)<```String```, [Relatable](Relatable)> - o resultado da consulta em um mapa indexado pelo valor de um atributo dos resultados.

---
