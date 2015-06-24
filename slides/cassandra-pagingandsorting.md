##  Cassandra-PagingAndSorting
```Java
public interface PagingAndSortingRepository<T, ID extends Serializable>
extends CrudRepository<T, ID> {

  Iterable<T> findAll(Sort sort);

  Page<T> findAll(Pageable pageable);
}

```

note:
Put your speaker notes here.
You can see them pressing 's'.
