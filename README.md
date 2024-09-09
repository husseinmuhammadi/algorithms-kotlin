# algorithms-kotlin
Algorithms in Kotlin 

```kotlin
fun dnaComplement(dna: String): String {
    if (dna.isBlank()) return ""
    val sb = StringBuilder(dna)
    var i = 0
    for (c in dna) {
        when(c) {
            'A' -> sb[i] = 'T'
            'T' -> sb[i] = 'A'
            'C' -> sb[i] = 'G'
            'G' -> sb[i] = 'C'
            else -> Unit
        }
        i++
    }
    return sb.toString()
}

fun fizzBuzz(n: Int): String {
    if (n < 1) return ""
    val strArr: MutableList<String> = ArrayList()
    for (i in 1..n) {
        if (i % 3 == 0 && i % 5 == 0) strArr.add("FizzBuzz")
        else if (i % 3 == 0) strArr.add("Fizz")
        else if (i % 5 == 0) strArr.add("Buzz")
        else strArr.add(i.toString())
    }
    return strArr.joinToString(separator = "\n")
}
```
