##  Hazelcast-Lock

```Java
public class DistributedLock {
  public static void main(String[] args) {
    Config config = new Config();
    HazelcastInstance h = Hazelcast.newHazelcastInstance(config);
    Lock lock = h.getLock("my-distributed-lock");
    lock.lock();
    try {
      //do something here
      } finally {
        lock.unlock();
      }
    }
  }
```
