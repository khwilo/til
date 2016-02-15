# HASH

If you have a hash with a key "apple" and you want to get it then you do this:  

```
mystuff = {'apple' => "I AM APPLES!"}
puts mystuff['apple']
```  

# MODULE

## Properties of a module:

1. A Ruby file with some functions or variables in it inside a `module .. end` block
2. You import a file
3. Access the variables or functions in the module using the . (dot) operator

*Example of a module with a function and variable in it*  

```
module MyStuff
  def MyStuff.apple()
    puts "I AM APPLES!"
  end

  TANGERINE = "Living reflection of a dream"
end
```  

*Accessing the function and variable*  

```
require "./mystuff.rb"

MyStuff.apple()
puts MyStuff::TANGERINE
```

# CLASS

Creating a class just like the `mystuff.rb` module above:  

```
class MyStuff

  def initialize()
    @tangerine = "Living reflection of a dream"
  end

  attr_reader :tangerine

  def apple()
    puts "I AM APPLES!"
  end

end
```

To access the function and the variable first *instantiate* the class by calling the class `new` function:  

```
thing = MyStuff.new()
thing.apple()
puts thing.tangerine
```

### NOTE 
The `initialize` function is used to initialize a newly created object
