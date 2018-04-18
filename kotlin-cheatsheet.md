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
fun max(a: Int, b: Int) = if (a > b) a else b // Type inference done by compiler
```

#### Variables
* **val** (from value) - immutable reference - can't be changed after it's initialized (equals final in Java)
* **var** (from variable) - mutable reference - can be changed

```kotlin
val something: Int = 23
```
Actually, **Int** can be omitted here, so
```kotlin
val something = 23
```
is okay. If a variable isn't initialized right away, you need to specify its type explicitly.
```kotlin
val something: Int
// some magic
something = 23
```

A **val** variable must be initialized exactly once. Although a **val** reference is immutable, the object
that it points to may be mutable.
```kotlin
val sweets = arrayListOf("snickers")
sweets.add("mars")
```
