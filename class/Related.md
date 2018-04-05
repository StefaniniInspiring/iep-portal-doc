# Métodos da classe Related

---

## ofType(types)

Filtra os relacionamentos pelo tipo ou configuração da entitade ou ator relacionado.
Pode se informado um ou mais tipos. No caso de vários tipos, estes serão tratados como um OR: tipo1 or tipo2 ... or tipoN.

Exemplo de uso:

```java
// consulta os relacionamentos do tipo "cliente"
loja.getChildren().ofType("cliente");
```

### Parâmetros
  * types - um ou mais tipos (códigos de configuração) de ator ou entitade.

### Retorno
[Related](Related) - este objeto
