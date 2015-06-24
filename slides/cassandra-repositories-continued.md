##  Cassandra-Repositories-continued
```Java
public interface UserRepository extends CrudRepository<User, Long> {

  Long countByLastname(String lastname);
}
```
note:
  Query creation from method names
