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
loja.getChildren().ofType("cliente").filter().createdBefore(natal2015);
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

## updatedOn(date)

Filtra os atores/entidades com data de última atualização igual a data informada.

Exemplo de uso:

```java
// filtra os clientes atualizados no natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().updatedOn(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## updatedOnOrAfter(date)

Filtra os atores/entidades com data da última atualização igual ou posterior a data informada.

Exemplo de uso:

```java
// filtra os clientes atualizados no natal de 2015 ou posteriormente a esta data
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().updatedOnOrAfter(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## updatedOnOrBefore(date)

Filtra os atores/entidades com data da última atualização igual ou anterior a data informada.

Exemplo de uso:

```java
// filtra os clientes atualizados no natal de 2015 ou anteriormente a esta data
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().updatedOnOrBefore(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## updatedAfter(date)

Filtra os atores/entidades com data da última atualização posterior a data informada.

Exemplo de uso:

```java
// filtra os clientes atualizados após o natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().updatedAfter(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## updatedBefore(date)

Filtra os atores/entidades com data da última atualização anterior a data informada.

Exemplo de uso:

```java
// filtra os clientes atualizados anteriormente ao natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().updateBefore(natal2015);
```

### Parâmetros
* ```Date``` date - data de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## updatedBetween(date1, date2)

Filtra os atores/entidades com data da última atualização dentro de um período, inclusive.

Exemplo de uso:

```java
// filtra os clientes atualizados entre o natal de 2015 e o reveillon de 2016
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
Date reveillon2016 = new SimpleDateFormat("dd/MM/yyyy").parse("01/01/2016");
loja.getChildren().ofType("cliente").filter().updatedBetween(natal2015, reveillon2016);
```

### Parâmetros
* ```Date``` date1 - data inicial do período de filtro da última atualização do ator/entidade.
* ```Date``` date2 - data final do período de filtro da última atualização do ator/entidade.

### Retorno
[Filter](Filter) - este objeto

---

## not()

Nega um único filtro invocado na sequencia deste método.

Exemplo de uso:

```java
// filtra os clientes que NÃO contenham o atributo "uf" com valor "sp"
loja.getChildren().ofType("cliente").filter().not().withAttr("uf", "sp");

// filtra os clientes que contenham o atributo "uf" inciados em "m" mas que não seja "ma"
loja.getChildren().ofType("cliente").filter().not().withAttr("uf", "ma").withAttr("uf", "m?");

// filtra os clientes que NÃO foram criados no natal de 2015
Date natal2015 = new SimpleDateFormat("dd/MM/yyyy").parse("25/12/2015");
loja.getChildren().ofType("cliente").filter().not().createdOn(natal2015);
```

### Parâmetros
n/a

### Retorno
[Filter](Filter) - este objeto

---

## or()

Aplica um __OR__ entre o filtro invocado anteriormente a este metodo e o filtro invocado na sequencia deste método.

Este método só tem efeito se invocado entre dois outros métodos de filtro.

Exemplo de uso:

```java
// filtra os clientes que contenham o atributo "uf" com valor "sp" OU "mg"
loja.getChildren().ofType("cliente").filter().withAttr("uf", "sp").or().withAttr("uf", "mg");
```

### Parâmetros
n/a

### Retorno
[Filter](Filter) - este objeto

---

## and()

Aplica um __AND__ entre o filtro invocado anteriormente a este metodo e o filtro invocado na sequencia deste método.

Este método só tem efeito se invocado entre dois outros métodos de filtro.

Este método é opcional, o mesmo efeito é obtido ao se invocar dois métodos de filtro em sequencia.

Exemplo de uso:

```java
// filtra os clientes que contenham o atributo "uf" com valor "sp" E o atributo idade com valor "33"
loja.getChildren().ofType("cliente").filter().withAttr("uf", "sp").and().withAttr("idade", "33");

// Idem ao exemplo acima, omitindo-se o método and()
loja.getChildren().ofType("cliente").filter().withAttr("uf", "sp").withAttr("idade", "33");
```

### Parâmetros
n/a

### Retorno
[Filter](Filter) - este objeto

---

## openBrackets()

Insere os filtros invocados posteriormentes a este método entre um par de parênteses. Utilizado para garantir o resultado de filtros complexos.

Este método deve ser invocado em conjunto com [closeBrackets](#closebrackets).

Caso os parênteses não sejam fechados (não se invocar [closeBrackets](#closebrackets) após este método), todos os filtros invocados após este método serão considerados dentro dos parênteses.

Exemplo de uso:

```java
// filtra os clientes com nome "João" ou "Maria" e que tenham idade igual a "30" ou "40"
loja.getChildren().ofType("cliente").filter()
  .openBrackets().withAttr("nome", "João").or().withAttr("nome", "Maria").closeBrackets()
  .and()
  .openBrackets().withAttr("idade", "30").or().withAttr("idade", "40").closeBrackets()
```

### Parâmetros
n/a

### Retorno
[Filter](Filter) - este objeto

---

## closeBrackets()

Fecha os parênteses abertos pela anterior invocação do método [openBrackets](#openbrackets).

Este método não tem efeito se os parênteses não tenham sido previamente abertos (não se invocar [openBrackets](#openbrackets) antes deste método).

Exemplo de uso:

```java
// filtra os clientes com nome "João" ou "Maria" e que tenham idade igual a "30" ou "40"
loja.getChildren().ofType("cliente").filter()
  .openBrackets().withAttr("nome", "João").or().withAttr("nome", "Maria").closeBrackets()
  .and()
  .openBrackets().withAttr("idade", "30").or().withAttr("idade", "40").closeBrackets()
```

### Parâmetros
n/a

### Retorno
[Filter](Filter) - este objeto
