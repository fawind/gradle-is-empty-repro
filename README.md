In some cases `DependencySet#size` will return `0` while `DependencySet#isEmpty` will return `false`.

For more details see https://github.com/gradle/gradle/issues/22707

#### Reproducer

````
$ ./gradlew

> Configure project :
configuration ':apiElements', isEmpty = false, size = 0
configuration ':runtimeElements', isEmpty = false, size = 0

[...]
```
