##  Cassandra-Repositories-continued
```Java
public interface UserRepository extends CrudRepository<User, Long> {

  Long deleteByLastname(String lastname);

  List<User> removeByLastname(String lastname);

}
```
note:
    You can see them pressing 's'.
