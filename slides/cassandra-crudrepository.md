##  Cassandra-CrudRepository
```Java
public interface CrudRepository<T, ID extends Serializable>
extends Repository<T, ID> {

  <S extends T> S save(S entity);

  T findOne(ID primaryKey);

  Iterable<T> findAll();

  Long count();

  void delete(T entity);

  boolean exists(ID primaryKey);  

  //
}
```

note:
    Put your speaker notes here.
    You can see them pressing 's'.
