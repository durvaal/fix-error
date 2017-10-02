# fix-error

## Java

--------

### Hibernate

#### org.hibernate.TransientObjectException: The given object has a null identifier

Normalmente, este erro ocorre quando tenta-se efetuar um update em uma tabela. Para solucionar, verifique se a propriedade `generator` da annotation `@JsonIdentifyInfo` de sua classe model está com o valor `ObjectIdGenerators.IntSequenceGenerator.class`. Se sim, modifique para  `ObjectIdGenerators.PropertyGenerator.class`.

