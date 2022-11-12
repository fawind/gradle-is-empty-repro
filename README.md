**Reproducer for a bug in `org.gradle.api.internal.collections.IterationOrderRetainingSetElementSource`**

In some instances of `IterationOrderRetainingSetElementSource`, `Collection#size` will return `0` while `Collection#isEmpty` will return `false`.

#### Reproducer

````
$ ./gradlew

> Configure project :
configuration ':apiElements', isEmpty = false, size = 0
configuration ':runtimeElements', isEmpty = false, size = 0

[...]
```
