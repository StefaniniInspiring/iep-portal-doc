# Como consultar relacionamentos

## O que são relacionamentos

Relacionamentos são ligações entre entitades e atores que possuem uma afinidade conceitual.

Entidades podem ser relacionadas com outras entidades ou atores.

Atores apenas podem se relacionar com entidades.

## Tipos de relacionamentos
Exitem 2 tipos de relacionamentos: bidirecional e unidirecional

### Bidirecional
Em um relacionamento bidirecional, cada uma das partes possui um relacionamento com a outra parte, ou seja, o relacionamento é reconhecido por seus 2 integrantes.

No exemplo abaixo, a entitdade/ator **A** possui um relacionamento com a entitade/ator **B**. De forma análoga, **B** possui uma relacionamento com **A**:

```
A <====> B
```

### Unidirecional
No relacionamento unidirecional, apenas uma das partes conhece o relacionamento, ficando a outra parte alheia ao relacionamento.

No exemplo abaixo, a entidade/ator **A** possui um relacionamento com a entidade/ator **B**, porém esta NÃO possui relacionamento com **A**:

```
A ----> B
```

## Hierarquia
Um conjunto de entidades/atores relacionados entre si pode ser visto como uma árvore genealógica:
![Imagem 3](../image/rel3.png)

Na imagem acima, **A** é pai de **B** e **C**, **B** e **C** são irmãos entre si.

Porém, como as entidades podem se relacionar livremente, a relação de parentesco pode se tornar complexa, ficando um pouco diferente da forma como conhecemos:
![](../image/rel4.png)

Na imagem acima, 

## Consulta de relacionamentos
