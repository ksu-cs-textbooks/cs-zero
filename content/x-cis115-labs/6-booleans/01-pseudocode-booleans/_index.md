---
title: "Pseudocode Booleans"
pre: "1. "
weight: 10
date: 2021-02-11T00:00:01-05:00
---

{{< youtube huGbQGAO-OY >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

In pseudocode, we can create variables that store values using the **Boolean** data type. These variables can only store one of two values: `true` or `false`. So, a Boolean value is really the simplest data value we can imagine - it is a single binary bit representing a value of `true` or `false`. In some systems, we may also refer to these values as `0` or `1`, but in pseudocode we'll just use `true` and `false`.

To create a variable that stores a Boolean value in pseudocode, we can use the following assignment statements:

```tex
x <- true
y <- false
```

In pseudocode, both `true` and `false` are **keywords** in the language. They represent the special boolean values `true` and `false`, and cannot be used as the name of a variable or procedure. Since they are values and not strings, we do not have to put them in quotation marks.

## Converting Between Data Types

We can use the special `BOOLEAN()` procedure to convert any value to a Boolean value. Here are the basic rules for that conversion:

* Strings: `"true"` will evaluate to `true` and `"false"` will evaluate to `false`. Capitalization doesn't matter. All other values are undefined.
* Numbers: `0` will evaluate to `false`, and any other value will be `true`.

The reverse works as well - Boolean values can be provided as input to the `STRING()` or `NUMBER()` procedures, and the outputs produced there will match these rules. Specifically, the `true` value will convert to the number $1$, but any non-zero number would be valid. 
