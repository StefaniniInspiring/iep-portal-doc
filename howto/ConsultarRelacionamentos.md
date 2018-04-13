# Como consultar relacionamentos

## O que são relacionamentos

Relacionamentos são ligações entre entitades e atores que possuem uma afinidade conceitual.

Entidades podem ser relacionadas com outras entidades ou atores.

Atores apenas podem se relacionar com entidades.

## Direção
Exitem 2 tipos de relacionamentos: bidirecional e unidirecional

### Bidirecional
Em um relacionamento bidirecional, cada uma das partes possui um relacionamento com a outra parte, ou seja, o relacionamento é reconhecido por seus 2 integrantes.

No exemplo abaixo, a entitdade/ator **A** possui um relacionamento com a entitade/ator **B**. De forma análoga, **B** possui uma relacionamento com **A**:

![Imagem 1](../image/rel1.png)

### Unidirecional
No relacionamento unidirecional, apenas uma das partes conhece o relacionamento, ficando a outra parte alheia.

No exemplo abaixo, a entidade/ator **A** possui um relacionamento com a entidade/ator **B**, porém esta NÃO possui relacionamento com **A**:

![Imagem 2](../image/rel2.png)

## Hierarquia
Um conjunto de entidades/atores relacionados entre si pode ser visto como uma árvore genealógica:

![Imagem 3](../image/rel3.png)

Na imagem acima, **A** é pai de **B** e **C**, **B** e **C** são irmãos.

Porém, como as entidades podem se relacionar livremente, a relação de parentesco pode se tornar complexa, ficando um pouco diferente da forma como conhecemos:

![Imagem 4](../image/rel4.png)

Na imagem acima, temos os mesmos graus de parentescos da imagem anterior, porém com uma peculiaridadade: **B** além de irmão de **C**, também é pai de **C**. Assim como **C** além de irmão de **B**, pode ser visto como filho deste.

A hierarquia pode se tornar mais complexa com relacionamentos bidirecionais:

![Imagem 1](../image/rel1.png)

Na imagem acima, temos **A** sendo pai e filho de **B** ao mesmo tempo, assim como **B** também é pai e filho de **A**.

### Conclusão
O conceito de hierarquia de parentesco (pai, filho e irmão) é utilizado como ponto de partida para se navegar entre os relacionamentos.

Deve-se levar em conta a liberdade que as entidades/atores tem de se relacionar entre si e a direção do relacionamento ao se realizar uma busca, para assim, evitar resultados inesperados.

## Consulta
A partir de uma instância de ator ou entidade, é possível navegar por toda [hierarquia](#hierarquia) de relacionamentos deste objeto e selecionar os relacionamentos, assim como os objetos relacionados, que atendem a um certo critério.

Abaixo temos uma visão expandida de todos os métodos que podem ser usados em uma consulta:

* entity
  * [getParents()](../class/Entity#getparents)
  * [getParentActors()](../class/Entity#getparentactors)
  * [getParentEntities()](../class/Entity#getparententities)
  * [getSiblings()](../class/Entity#getsiblings)
  * [getSiblingActors()](../class/Entity#getsiblingactors)
  * [getSiblingEntities()](../class/Entity#getsiblingentities)
  * [getChildren()](../class/Entity#getchildren)
  * [getChildrenActors()](../class/Entity#getchildrenactors)
  * [getChildrenEntities()](../class/Entity#getchildrenentities)
    * [ofType(types)](../class/Related#oftypetypes)
    * [relatedOn(date)](../class/Related#relatedondata)
    * [relatedOnOrAfter(date)](../class/Related#relatedonorafterdate)
    * [relatedOnOrBefore(date)](../class/Related#relatedonorbeforedate)
    * [relatedAfter(date)](../class/Related#relatedafterdate)
    * [relatedBefore(date)](../class/Related#relatedbeforedate)
    * [relatedBetween(date1, date2)](../class/Related#relatedbetweendate1-date2)
    * [offset(n)](../class/Related#offsetn)
    * [limit(n)](../class/Related#limitn)
    * [filter()](../class/Related#filter)
      * [withAttr(name, value)](../class/Filter#withattrname-value)
      * [withAttrLike(name, value)](../class/Filter#withattrlikename-value)
      * [createdOn(date)](../class/Filter#createdondate)
      * [createdOnOrAfter(date)](../class/Filter#createdonorafterdate)
      * [createdOnOrBefore(date)](../class/Filter#createdonorbeforedate)
      * [createdAfter(date)](../class/Filter#createdafterdate)
      * [createdBefore(date)](../class/Filter#createdbeforedate)
      * [createdBetween(date1, date2)](../class/Filter#createdbetweendate1-date2)
      * [updatedOn(date)](../class/Filter#updatedondate)
      * [updatedOnOrAfter(date)](../class/Filter#updatedonorafterdate)
      * [updatedOnOrBefore(date)](../class/Filter#updatedonorbeforedate)
      * [updatedAfter(date)](../class/Filter#updatedafterdate)
      * [updatedBefore(date)](../class/Filter#updatedbeforedate)
      * [updatedBetween(date1, date2)](../class/Filter#updatedbetweendate1-date2)
      * [not()](../class/Filter#not)
      * [or()](../class/Filter#or)
      * [and()](../class/Filter#and)
      * [openBrackets()](../class/Filter#openbrackets)
      * [closeBrackets()](../class/Filter#closebrackets)
    * [order()](../class/Order#order)
      * [byId()](../class/Order#byid)
      * [byAttr(name)](../class/Order#byattrname)
      * [byCreateDate()](../class/Order#bycreatedate)
      * [byUpdateDate()](../class/Order#byupdatedate)
      * [desc()](../class/Order#desc)
  * [count()](../class/Related#count)
  * [iterator()](../class/Related#iterator)
  * [toList()](../class/Related#tolist)
  * [toMap()](../class/Related#tomap)
  * [groupByType()](../class/Related#groupbytype)
  * [groupByAttr(name)](../class/Related#groupbyattrname)
  
### Primeiro passo
Com um objeto relacionável em mãos (ator ou entidade) a consulta deve ser iniciada por um dos seguintes métodos:

  * [getParents()](../class/Entity#getparents)
  * [getParentActors()](../class/Entity#getparentactors)
  * [getParentEntities()](../class/Entity#getparententities)
  * [getSiblings()](../class/Entity#getsiblings)
  * [getSiblingActors()](../class/Entity#getsiblingactors)
  * [getSiblingEntities()](../class/Entity#getsiblingentities)
  * [getChildren()](../class/Entity#getchildren)
  * [getChildrenActors()](../class/Entity#getchildrenactors)
  * [getChildrenEntities()](../class/Entity#getchildrenentities)

Todos esses métodos retornam um objeto do tipo [Related](../class/Related) que pode atuar como
1. um [Iterable](https://docs.oracle.com/javase/8/docs/api/java/lang/Iterable.html);
2. um [Builder](https://blog.crisp.se/2013/10/09/perlundholm/another-builder-pattern-for-java).

### Iterable
Com o _Itetarable_ é possível iterar nos relacionamentos
```java
for(child : entity.getChildren()) {
 ...
}
```
pode-se navegar na hierarquia de relacionamentos
```java
for(child : entity.getChildren()) {
 for(grandson : child.getChildren() {
  for(greatGrandson : grandson.getChildren() {
   ...
  }
 }
}
```
ou inseri-los em uma [Collection](https://docs.oracle.com/javase/8/docs/api/java/util/Collection.html)
```java
list = new ArrayList(entity.getChildren());
```
> :exclamation: **Atenção**
>
> Sempre que possível, limitar a quantidade de resultados usando [limit(n)](../class/Related#limitn) para não sobrecarregar os recursos físicos.
>
> Principalmente no caso de se delegar a uma _Collection_, pois todos os relacionamentos são retornados de uma só vez e a quantidade de relacionamentos pode ultrapassar a quantidade de memória disponível.

### Builder
Com o _builder_ é possível preparar a busca, aplicando filtros e ordenações, afim de refinar os resultados.

> :grey_exclamation: **Dica**
>
> Todos os métodos retornados pelo builder, exceto os [finalizadores](#finalização), retornam um objeto que pode continuar atuar como um _builder_ ou atuar como um [_iterable_](###iterable).

Assim que todos os métodos de preparação foram invocados, pode-se iterar o objeto resultante para que a busca seja realizada e os resultados retornados a cada iteração. Também pode-se invocar um método [finalizador](#finalização) para se obter um resultado específico. 

As categorias de métodos são opcionais - pode-se ordenar sem aplicar filtros, por exemplo - e devem respeitar a ordem abaixo:

#### 1. Filtros de relacionamentos
Os primeiros filtros que podem ser aplicados se referem aos relacionamentos do o ator ou entidade em questão.

> :exclamation: **Atenção**
>
> Não confundir com [filtros de relacionáveis](#filtros-de-relacionáveis). Aqui são considerados os aspectos do relacionamento em si enquanto o outro visa as contrapartes deste relacionamento.

Os métodos são:

  * [ofType(types)](../class/Related#oftypetypes)
  * [relatedOn(date)](../class/Related#relatedondata)
  * [relatedOnOrAfter(date)](../class/Related#relatedonorafterdate)
  * [relatedOnOrBefore(date)](../class/Related#relatedonorbeforedate)
  * [relatedAfter(date)](../class/Related#relatedafterdate)
  * [relatedBefore(date)](../class/Related#relatedbeforedate)
  * [relatedBetween(date1, date2)](../class/Related#relatedbetweendate1-date2)
  * [offset(n)](../class/Related#offsetn)
  * [limit(n)](../class/Related#limitn)

Exemplo:

```java
// prepara a busca dos clientes de uma loja
clientes = loja.getChildrenActors() // acesso ao builder referente aos relacionamentos de atores filhos
               .ofType("cliente") // filtra os relacionamentos com atores configurados como "cliente"
               .relatedOnOrBefore(lastMonth) // filtra os relacionamentos criados a mais de um mês
               .limit(10); // limita os resultados em 10
 
// a busca é executada e os resultados iterados
for(cliente : clientes) {
 ...
}
```

> :exclamation: **Atenção**
>
> Sempre que possível, limitar a quantidade de resultados usando [limit(n)](../class/Related#limitn) para não sobrecarregar os recursos físicos.
>
> Principalmente no caso de se delegar a uma _Collection_, pois todos os relacionamentos são retornados de uma só vez e a quantidade de relacionamentos pode ultrapassar a quantidade de memória disponível.
 
#### 2. Filtros de relacionáveis
São filtros usados para selecionar os atores ou entidades relacionadas.

> :exclamation: **Atenção**
>
> Não confundir com [filtros de relacionamentos](#filtros-de-relacionamentos). Aqui são consideradas as contrapartes de um  relacionamento enquanto o outro visa os aspectos do relacionamento em si.


Para inicializar um filtro, deve-se invocar o método [**filter()**](../class/Related#filter) após os [filtros de relacionamentos](#filtros-de-relacionamentos)

```java
entity.getChildren()
      .ofType("cliente")
      .filter() 
      ...
```

ou diretamente após os métodos iniciais (caso não for usar [filtros de relacionamentos](#filtros-de-relacionamentos))

```java
entity.getChildren()
      .filter()
      ...
```

Os métodos usado para filtragem são:
  * [withAttr(name, value)](../class/Filter#withattrname-value)
  * [withAttrLike(name, value)](../class/Filter#withattrlikename-value)
  * [createdOn(date)](../class/Filter#createdondate)
  * [createdOnOrAfter(date)](../class/Filter#createdonorafterdate)
  * [createdOnOrBefore(date)](../class/Filter#createdonorbeforedate)
  * [createdAfter(date)](../class/Filter#createdafterdate)
  * [createdBefore(date)](../class/Filter#createdbeforedate)
  * [createdBetween(date1, date2)](../class/Filter#createdbetweendate1-date2)
  * [updatedOn(date)](../class/Filter#updatedondate)
  * [updatedOnOrAfter(date)](../class/Filter#updatedonorafterdate)
  * [updatedOnOrBefore(date)](../class/Filter#updatedonorbeforedate)
  * [updatedAfter(date)](../class/Filter#updatedafterdate)
  * [updatedBefore(date)](../class/Filter#updatedbeforedate)
  * [updatedBetween(date1, date2)](../class/Filter#updatedbetweendate1-date2)
  * [not()](../class/Filter#not)
  * [or()](../class/Filter#or)
  * [and()](../class/Filter#and)
  * [openBrackets()](../class/Filter#openbrackets)
  * [closeBrackets()](../class/Filter#closebrackets)
  
Exemplo:

```java
```

#### 2. Ordenação
Para ordernar os atores e entidades resultantes de uma busca, deve-se invocar o método [**order()**](../class/Related#order) logo após os [filtros de relacionamentos](#filtros-de-relacionamentos) e [filtros de relacionáveis](#filtros-de-relacionaveis) quando presentes e, em seguida, invocar o(s) método(s) referentes à ordenação:

  * [byId()](../class/Order#byid)
  * [byAttr(name)](../class/Order#byattrname)
  * [byCreateDate()](../class/Order#bycreatedate)
  * [byUpdateDate()](../class/Order#byupdatedate)
  * [desc()](../class/Order#desc)
  
Exemplo:

```java
// consulta os clientes pela data de criação, do mais recente para o mais antigo
loja.getChildrenActors()
    .ofType("cliente")
    .order() // acesso ao ordenador
    .byCreationDate() // prepara uma ordenação pela data de criação
    .desc(); // inverte a ordem de criação (descrescente)
```
#### 3. Finalização
São métodos que relaziam a consulta e transformam os resultados em um objeto específico.

Devem ser invocados após todos os filtros e ordenações.

Os métodos finalizadores possíveis são:
  * [count()](../class/Related#count)
  * [iterator()](../class/Related#iterator)
  * [toList()](../class/Related#tolist)
  * [toMap()](../class/Related#tomap)
  * [groupByType()](../class/Related#groupbytype)
  * [groupByAttr(name)](../class/Related#groupbyattrname)
  
> :exclamation: **Atenção**
>
> Sempre que possível, e quando aplicável, limitar a quantidade de resultados usando [limit(n)](../class/Related#limitn) para não sobrecarregar os recursos físicos, pois nos métodos acima, todos os relacionamentos são retornados de uma só vez e a quantidade de relacionamentos pode ultrapassar a quantidade de memória disponível.

Exemplos:
```java
// conta o total de clientes de uma loja
total = loja.getChildrenActors()
            .ofType("cliente")
            .count();
```

```java
// recupera o cliente mais antigo de uma loja utilizando iterator
it = loja.getChildrenActors()
         .ofType("cliente")
         .order()
         .byCreationDate()
         .desc()
         .limit(1)
         .iterator(); // realiza a consulta e insere o resultado em um Iterator

// utiliza o cliente caso este exista 
if(it.hasNext()) {
 cliente = it.next();
 ...
}
```
