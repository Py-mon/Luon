Strives to be comment free of explaining comments by use of readable and clean code.

- Classless but with Instances
- High Readability

# Unique Features

### Group Blocks of Code

```
run xyz {
    ...
}
```

Basically a self-ran, zero-argument function

Used for

- Titling a block of code and seeing exactly what it applies to (unlike a comment would)
- Repeating code blocks without arguments
- Making a function, would require you to call it after you make it.

Has its own scope.

Can be ran again if needed by `run xyz` (not a real function so `xyz()` won't work)

### Implicit Multiplication

```
2(2) => 4
5(3 + 2) => 25
```

### Namespaces

```
namespace getMax {
  health() -> number {
    ...
  }
  stamina() -> number {
    ...
  }
}
```

```
getMax.stamina()
```

### Enum

```
enum Colors {
  RED,
  BLUE
}
```

```
Colors.RED
```

### Fraction Type

```
local fraction half = 1/2
```

```
half + 1/4 = 3/4
```

# Syntax

## Function

<!-- => [1, 2] Literals? -->

```
x(number a, string b) -> number {
    ...
}
```

### Literals
Notice `=>` vs `->`
```
x(number a, string b) => 1  {
    return 1
}
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

# Declaring Variable
```
local number a = 5
local string b = "Hello, world!"
global string c = "I am everywhere"

```

## Comments
```
// This is a comment.
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

## Multiple Constructors
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
