##  Hazelcast-EntryProcessor

```Java
public static class IncEntryProcessor extends AbstractEntryProcessor<String, Integer> {
    @Override
    public Object process(Map.Entry<String, Integer> entry) {
      int oldValue = entry.getValue();
      int newValue = oldValue + 1;
      entry.setValue(newValue);
      return null;
    }
  }
```
