##  Hazelcast-Aggregation

```Java
public class DistributedAggregation {
  public static void main(String[] args) {
    Config config = new Config();
    HazelcastInstance h = Hazelcast.newHazelcastInstance(config);
    IMap<String, Integer> salaries = h.getMap("salaries");
    fillInSalaries(salaries);
    Supplier<String, Integer, Integer> supplier = Supplier.all();
    int sum = salaries.aggregate(supplier, Aggregations.integerSum());
    System.out.println("Aggregated sum: " + sum);
  }
}
```
