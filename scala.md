# Programming Language Notes

## Pattern Matching

```Scala
object Chien extends App {
    def match(x: Any): Any = x match {
        case "1" => 1
        case "two" => 2
        case "one" => 1
    }

    println(match("two"))
}
```

## Actor 
- Using actor avoid concurrent.
- Concurrent is different from Parallel. Concurrent means the problems when two thread access in the same object at the same time. Parallel means only parallel.
- To avoid concurrent, we can place that object in a Actor, and the other actors can change that object state undirectly by sending message to the actor contains that object. 

## Immutable
Function programming often use immutable type which avoid many problems when we use mutable type. Thanks to shared memory that we can reduce memory for creating too many different objects.

```scala
// add a element to a existed list => the only way is create new list
def addList[A](originList: List[A], elem: A): List[A] = { elem :: originList }
```



