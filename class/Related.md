# Métodos da classe Related

---

## ofType(types)

Filtra os relacionamentos pelo tipo ou configuração da entitade ou ator relacionado.

Pode se informado um ou mais tipos. No caso de vários tipos, estes serão tratados como um OR: tipo1 or tipo2 ... or tipoN.

Exemplo de uso:

```java
// consulta os relacionamentos dos tipos "cliente" ou "empregado"
loja.getChildren().ofType("cliente", "empregado");
```

### Parâmetros
* types - um ou mais tipos (códigos de configuração) de ator ou entitade.

### Retorno
[Related](Related) - este objeto

---

## relatedOn(date)

Filtra os relacionamentos que foram criados em uma data específica.

Exemplo de uso:

```java
// consulta os relacionamentos que foram criados ontem
Date yesterday = DateUtils.addDays(new Date(), -1);
entity.getChildren().relatedOn(yesterday);
```

### Parâmetros
* date - data de criação do relacionamento

### Retorno
[Related](Related) - este objeto

---

