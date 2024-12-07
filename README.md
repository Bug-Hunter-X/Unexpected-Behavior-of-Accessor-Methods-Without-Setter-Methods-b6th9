# Ruby Accessor Method Bug

This repository demonstrates a subtle issue in Ruby related to accessor methods without corresponding setter methods.  If you attempt to assign a value directly to a getter method (without a defined setter), the instance variable will not be updated.

## Bug Description

The `bug.rb` file contains a class `MyClass` with a getter method `value` but no setter method.  Assigning a value directly to `my_object.value` doesn't change the instance variable; only using `instance_variable_set` works.

## Bug Solution

The `bugSolution.rb` file shows two solutions:

1.  Define a setter method (`value=`).
2.  Use `instance_variable_set` for direct manipulation of instance variables.

This illustrates a crucial aspect of Ruby's object model and the importance of clearly defining accessors.