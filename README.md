<<<<<<< HEAD
Strives to be comment free of explaining comments by use of titled, readable, clean code.
=======
# Luon 
(Lua + C-like languages + Python)

A programming language concept.
>>>>>>> a9ed4bc55450f5eef03cbec7e68a3fa25e8042ca

- Typed Language
- High Readability
- Classless but with Instances and Constructors
- Built-in enum, overloading, fractions and more

# Unique Features

### Group and Title Blocks of Code
```
run xyz {
    ...
}
```

Basically a self-ran, zero-argument function

Used for:

- Titling a block of code and seeing exactly what it applies to (unlike a comment would).
- Allows for less explaining comments by having titled sections of code, making everything more readable.
- Repeating code-blocks without arguments.
- Making a function, would require you to call it after you make it.

Can be ran again if needed by `run xyz` (not a real function so `xyz()` won't work)

### Implicit Multiplication
Multiply numbers and variables next to eachother using parentheses.
```
2(2) => 4
5(3 + 2) => 25
```
```
x = 5
2(x) => 10
```

### Namespaces
Organize and group functions and other variables.
```
namespace getMax {
  health() -> Number {
    ...
  }
  stamina() -> Number {
    ...
  }
}
```
```
getMax.stamina()
```

### Enum
Store empty values.
```
enum Color {
  RED,
  BLUE
}
```
```
local Color x = Color.RED
```

### Fraction Type
```
local Fraction half = 1/2
```
```
half + 1/4 = 3/4
```

# Syntax

## Function
```
x(Number a, String b) -> Number {
    ...
}
```

### Literals
Notice the difference in `=>` and `->`
```
x(Number a, String b) => 1  {
    return 1
}
```

## Declaring Variable
```
local number a = 5
local string b = "Hello, world!"
global string c = "I am everywhere"
```

## Comments
```
// This is a comment.
```

# Instances
```
instance = Instance()
instance._name = "Cleo"
instance.age = 6

instance.hello() {
    print("hi")
}
```

### Properties
```
property instance.name {
    setter [string new_name] {
        instance._name = new_name
    }
    getter -> string {
        return instance._name.lower()
    }
}
```

```
instance.name => cleo
```

### Math Operations
```
+[instance, number addend] -> number {
    return instance.age + addend
}
```

```
instance + 5 => 11
```

### Overloading
```
overload +[instance, string addend] -> number {
    return instance.name + addend
}
```

```
instance + "n" => "cleon"
```

# Instance Constructors
```
Animal(string name, number age) -> [Animal] {
    instance = Instance()
    instance.name = name
    instance.age = age

    instance.cry() {
        print("asdf")
    }

    return instance
}
local Cat = Animal("Cleo", 6)
```

### Multiple Constructors
```
namespace Animal {
    createNewborn(string name) -> Animal {
        return Animal(name, 0)
    }
}
local Cat = Animal("Cleo", 6)
```

### Sub-Constructors
```
Dog(string name, number age, string species) -> [Dog] {
    instance = Animal(name, age)
    instance.species = species

    instance.cry() {
        print("woof")
    }

    return instance

}
local Doggie = Dog("Doggie", 2, "German Shepard")
```

### Inheriting Namespaces
```
namespace Dog inherits Animal

Dog.createNewborn("Baby")
```

# Keywords
- `namespace`
- `inheirts`
- `local`
- `global`
- `overload`
- `property`
    - `getter`
    - `setter`
- `enum`
- `run`

## Keys 
- `->` Returning a type
  - `-> [X]` Returning a new type of Instance called `X`
- `=>` Returning literal values
- `x[]` Implict Arguments (Only for Math Operations and setter right now: `x + y` -> `+[x, y]`, `x.name = y` -> `setter [y] {...}`)
- `{}` Bounds of Contents / Indentation / New Scope
- `//` Comments
- `"""` Multi-line Comments
- `#` Get length of
- `()` Calling Function
- `""` Strings

## Types
- string
- number
- fraction

## Built-In
- print
- Instance

# Brainstorm Next
- Arrays
- Loops
- Automatically assign types when first init a variable?
