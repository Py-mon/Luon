# LangIdea

Strives to be comment free of explaining comments by use of readable and clean code.

## Custom Features
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

  Has its own scope.

  Can be ran again if needed by `run xyz` (not a real function so `xyz()` won't work)
  
  Acts like a normal variable and a different type of function.

  ### Implicit Multiplication

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
  hald + 1/4 = 3/4
  ```

## Syntax
  ### Function
  ```
  x(number a, string b) -> number {
      ...
  }
  ```
  ### Class
  ```
  //  Class Methods
  namespace Car inheirts BaseCar {
      number AmountOfCars = 0
      number X = 5

      myClassMethod() -> x {
          
      }

  }

  }
  class Car [Cls] (string name, number year) {
      instance = BaseCar()
      instance._name = name
      instance.year = year
  
      instance.drive() {
          print("drive!")
      }
      property instance.name {
          setter [new_name] {
                  instance._name = new_name
              }
         getter -> string {
                  return instance._name.lower()
              }
      }
      +[instance, Cls addend] -> number {
          return instance.year + addend.year
      }
      return instance
 }



  ```
  

  ### Declaring Variable
  ```
  local number a = 5
  local string b = "Hello, world!"
  global string c = "I am everywhere"
  ```

  ### Comments
  ```
  // This is a comment.
  ```

