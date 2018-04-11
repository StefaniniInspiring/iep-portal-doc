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
A partir de uma instância de ator ou entidade, é possível navegar por toda [hierarquia](#hierarquia) de relacionamentos deste objeto e selecionar os relacionamentos que atendem a um certo critério.

Abaixo temos uma visão expandida de todos os métodos que podem ser usados em uma consulta:

entity
  * [getParents()](../class/Entity#getparents)
  * [getParentActors()](../class/Entity#getparentactors)
  * [getParentEntities]()](../class/Entity#getparententities)
  * [getSiblings()](../class/Entity#getsiblings)
  * [getSiblingActors()](../class/Entity#getsiblingactors)
  * [getSiblingEntities()](../class/Entity#getsiblingentities)
  * [getChildren()](../class/Entity#getchildren)
  * [getChildrenActors()](../class/Entity#getchildrenactors)
  * [getChildrenEntities()](../class/Entity#getchildrenentities)
    * [ofType(types)](../class/Related#oftype)
    * [relatedOn(date)](../class/Related#relatedon)
    * [relatedOnOrAfter(date)](../class/Related#relatedonorafterdate)
    * [relatedOnOrBefore(date)](../class/Related#relatedonorbeforedate)
    * [relatedAfter(date)](../class/Related#relatedafterdate)
    * [relatedBefore(date)](../class/Related#relatedbeforedate)
    * [relatedBetween(date1, date2)](../class/Related#relatedbetweendate1_date2)
    * [offset(n)](../class/Related#offsetn)
    * [limit(n)](../class/Related#limitn)
    * [filter()](../class/Related#filter)
      * [withAttr(name, value)](../class/Filter#)
      * [withAttrLike(name, value)](../class/Filter#withattrlikename_value)
      * [createdOn(date)](../class/Filter#createdondate)
      * [createdOnOrAfter(date)](../class/Filter#createdonorafterdate)
      * [createdOnOrBefore(date)](../class/Filter#createdonorbeforedate)
      * [createdAfter(date)](../class/Filter#createdafterdate)
      * [createdBefore(date)](../class/Filter#createdbeforedate)
      * [createdBetween(date1, date2)](../class/Filter#createdbetweendate1_date2)
      * [updatedOn(date)](../class/Filter#updatedondate)
      * [updatedOnOrAfter(date)](../class/Filter#updatedonorafterdate)
      * [updatedOnOrBefore(date)](../class/Filter#updatedonorbeforedate)
      * [updatedAfter(date)](../class/Filter#updatedafterdate)
      * [updatedBefore(date)](../class/Filter#updatedbeforedate)
      * [updatedBetween(date1, date2)](../class/Filter#updatedbetweendate1_date2)
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
  * [groupByAttr(name)](../class/Related#groupbyattrname
  
