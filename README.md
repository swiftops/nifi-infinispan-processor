# Infinispan cache processor of Apache Nifi

#### GetFromInfinispanCache : 
This processor will get the value from Infinispan cache for the given Cache Name and Cache Key.
##### Relationships:
 - It has two relationships Success and Failure
##### Properties:
  - Infinispan Host
  - Infinispan Port
  - Cache Name
  - Cache Key
  - Put Cache Value In Attribute - Fill this only if the Cache value should be set as a FlowFile Attribute else it will set the Cache value in FlowFile content. This supports expression language of Variable registry and FlowFile Attribute

#### PutInInfinispanCache
This processor will put the value in Infinispan cache for the given Cache Name and Cache Key and Cache Value.

##### Relationships
 - It has two relationships Success and Failure
##### Properties:
  - Infinispan Host
  - Infinispan Port
  - Cache Name
  - Cache Key
  - Cache Value - This supports expression language of Variable registry and FlowFile Attribute


#### Steps to add these processors in any Nifi setup: 
- Build the application from root application's pom.xml
- This will generate a nar file `nifi-infinispanCache-nar-1.0.nar` in ``{nifi-infinispan-processor}\nifi-putInInfinispanCache-nar\target\ folder``
- Copy this nar file in nifi instance lib folder `{nifi-home}\lib`
- Restart Nifi
- Processor will be available in the repository
