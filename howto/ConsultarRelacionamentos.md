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

* entity
  * [getParents()](../class/Entity#getparents)
  * [getParentActors()](../class/Entity#getparentactors)
  * [getParentEntities]()](../class/Entity#getparententities)
  * [getSiblings()](../class/Entity#getsiblings)
  * [getSiblingActors()](../class/Entity#getsiblingactors)
  * [getSiblingEntities()](../class/Entity#getsiblingentities)
  * [getChildren()](../class/Entity#getchildren)
  * [getChildrenActors()](../class/Entity#getchildrenactors)
  * [getChildrenEntities()](../class/Entity#getchildrenentities)
    * [ofType(types)](../class/Entity#oftype)
    * [relatedOn(date)](../class/Entity#relatedon)
    * [relatedOnOrAfter(date)](../class/Entity#relatedonorafterdate)
    * [relatedOnOrBefore(date)](../class/Entity#relatedonorbeforedate)
    * [relatedAfter(date)](../class/Entity#relatedafterdate)
    * [relatedBefore(date)](../class/Entity#relatedbeforedate)
    * [relatedBetween(date1, date2)](../class/Entity#relatedbetweendate1_date2)
    * [offset(n)](../class/Entity#offsetn)
    * [limit(n)](../class/Entity#limitn)
    * [filter()](../class/Entity#filter)
      * [withAttr(name, value)](../class/Entity#)(../class/Entity#withattrname_value)
      * [withAttrLike(name, value)](../class/Entity#withattrlikename_value)
      * [createdOn(date)](../class/Entity#createdondate)
      * [createdOnOrAfter(date)](../class/Entity#createdonorafterdate)
      * [createdOnOrBefore(date)](../class/Entity#createdonorbeforedate)
      * [createdAfter(date)](../class/Entity#createdafterdate)
      * [createdBefore(date)](../class/Entity#createdbeforedate)
      * [createdBetween(date1, date2)](../class/Entity#createdbetweendate1_date2)
      * [updatedOn(date)](../class/Entity#updatedondate)
      * [updatedOnOrAfter(date)](../class/Entity#updatedonorafterdate)
      * [updatedOnOrBefore(date)](../class/Entity#updatedonorbeforedate)
      * [updatedAfter(date)](../class/Entity#updatedafterdate)
      * [updatedBefore(date)](../class/Entity#updatedbeforedate)
      * [updatedBetween(date1, date2)](../class/Entity#updatedbetweendate1_date2)
      * [not()](../class/Entity#not)
      * [or()](../class/Entity#or)
      * [and()](../class/Entity#and)
      * [openBrackets()](../class/Entity#openbrackets)
      * [closeBrackets()](../class/Entity#closebrackets)
    * [order()](../class/Entity#order)
      * [byId()](../class/Entity#byid)
      * [byAttr(name)](../class/Entity#byattrname)
      * [byCreateDate()](../class/Entity#bycreatedate)
      * [byUpdateDate()](../class/Entity#byupdatedate)
      * [desc()](../class/Entity#desc)
  * [count()](../class/Entity#count)
  * [iterator()](../class/Entity#iterator)
  * [toList()](../class/Entity#tolist)
  * [toMap()](../class/Entity#tomap)
  * [groupByType()](../class/Entity#groupbytype)
  * [groupByAttr(name)](../class/Entity#groupbyattrname)
  
