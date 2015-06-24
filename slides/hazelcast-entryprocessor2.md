##  Hazelcast-EntryProcessor2

```Java
public static void main(String[] args) {
  HazelcastInstance hz = Hazelcast.newHazelcastInstance();
  IMap<String, Integer> map = hz.getMap("map");
  map.put("key", 0);
  map.executeOnKey("key", new IncEntryProcessor());
  System.out.println("new value:" + map.get("key"));
}
```
