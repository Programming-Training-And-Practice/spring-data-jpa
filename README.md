# Spring Data JPA.





## Contents at a Glance.
* [About.](#about)
* [Documentation.](#documentation)
* [Help.](#help)





## About.





## Documentation.





## Annotation Entity.
Classes annotated with this annotation must adhere to the following rules:

* If using the classic Java Beans pattern, the class must have a public no-arg (zero arguments) constructor. Absence of 
  a public no-arg constructor assumes that the class is using the Builder pattern.
* For Builder pattern, the class must have a public static builder method that returns an instance of corresponding Builder class.
* When using the Builder pattern, the Builder class must have a public build method.
* Must have exactly one field annotated with @Identifier annotation.
* The type of identifier field must be a supported type as defined in the Identifier documentation.
* May contain zero or more fields. All fields that need to be persisted to the Cloud Datastore must have public accessor methods.
* For classic Java Beans pattern, all persistable fields must also have their corresponding mutator methods.
* For the Builder pattern, all persistable fields must have their corresponding mutator methods in the Builder class. 
  The mutator methods may use any of the below naming conventions:
  * setXXX (e.g. setFirstName)
  * withXXX (e.g. withFirstName)
  * xxx (e.g. firstName)
* If a field is to be skipped by the EntityManager, it needs to have @ Ignore annotation.
* May have no more than one field with @Key annotation which will hold the full key to the entity.
* Field annotated with @Key must have a data type of DatastoreKey .
* May have no more than one field with @ParentKey annotation which will hold the full key to the parent entity.
* Field annotated with @ParentKey must have a data type of DatastoreKey.
* May have zero or more embedded objects with an annotation of @Embedded.
* All other fields can be any of the types for which a Mapper exists. The framework provides Mappers for various commonly 
  used types. CustomMappers can be specified using MapperFactory.setDefaultMapper(java.lang.reflect.Type, Mapper) or 
  PropertyMapper annotation.






## Help.

