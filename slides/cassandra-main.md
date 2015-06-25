##  Cassandra-Main

```Java
  Cluster cluster = Cluster.builder().addContactPoints(InetAddress.getLocalHost()).build();
  Session session = cluster.connect("mykeyspace");
  CassandraOperations cassandraOps = new CassandraTemplate(session);
  cassandraOps.insert(new Person("1234567890", "David", 40));
  Select s = QueryBuilder.select().from("person");
  s.where(QueryBuilder.eq("id", "1234567890"));
  LOG.info(cassandraOps.queryForObject(s, Person.class).getId());
  cassandraOps.truncate("person");
  ```
note:
    Put your speaker notes here.
    You can see them pressing 's'.
