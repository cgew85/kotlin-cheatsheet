# Kotlin cheatsheet

#### Functions

```kotlin
fun max(a: Int, b: Int) : Int {
    return if (a > b) a else b
}
```

* **fun** keyword is used to declare a function
* functions can be declared at the top level of a file, doesn't need to be inside a class

The max function can be simplified:

```kotlin
fun max(a: Int, b: Int) : Int = if (a > b) a else b
```
Only works with expression bodies. In this case the function can be simplified even more.

```kotlin
fun max(a: Int, b: Int) = if (a > b) a else b // Type inference by done compiler
```


