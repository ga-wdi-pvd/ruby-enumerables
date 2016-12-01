# ruby-enumerables
enumerables in ruby

## Framing
One of the most common things we do as developers is to iterate through data structures.

Whenever we talk about data in Ruby, its important to review how Ruby handles groups of data.

We learned how to work with collections of data in Javascript: looping through data, getting things into and out of arrays and hashes. Now we're going to learn how to work with collections of data in Ruby.

## Objectives
 - Review Ruby Classes, Instances and Modules
 - Learn about Enumerables in Ruby
 - Access the Ruby Docs to find information on methods and modules
 - What are the differences between Javascript and Ruby enumerables?
 - Use enumerables to traverse, search, sort and modify collections.
 - Implement a ruby class that is enumerable
 
## What is an Enumerable?
 - A Ruby Module
  - acts on a collection
   - hashes
   - arrays
 - Allows traversing, sorting, searching and modifying the collection
  - Open your `irb` and create an enumerable
    - What methods are available to your enumerable
      - `yourEnum.methods.sort`
    - You just sorted a collection!
  - How does the instance of the class you chose have all of the methods of the Enumerable module available to it?
 - Use in your classes by `include`ing the module
   - known as a `mixin`
   
## Ruby Docs
 - What methods are available in the Enumerable Module? 
   - `Enumerable.instance_methods.sort`
 - Does a class have a certain method implemented?
 - Easier to view here: [Enumerable?](https://ruby-doc.org/core-2.3.3/Enumerable.html)
 ### Group Exercise: Documentation Dive 

  - Instructions: Each group will spend 10 minutes using Ruby documentation to look up an assigned enumerable. Prepare the following for your demo:

  - Your own definition of what it does
  - An example
  - At a high level, try to find/think of a use case of this enumerable in the wild. It doesn't have to be the actual code, just conceptually similar.
  - The enumerables are:

  - `Each With Index`
  - `Reject`
  - `Find`
  - `Select`
  - `Sort By`
  - `Inject/Reduce`
  - `any?`
  - `all?`

Exercise

Print out every possible combination of the below ice cream flavors and toppings:

`flavors = [ "vanilla", "chocolate", "strawberry", "butter pecan", "cookies and cream", "rainbow" ]`
`toppings = [ "gummi bears", "hot fudge", "butterscotch", "rainbow sprinkles", "chocolate sprinkles" ]`

Hint: "nest"
------
What does this do?
```
(5..10).inject(1, :*)
```
How about this?

```
longest = %w{ cat sheep bear }.reduce do |memo, word|
   memo.length > word.length ? memo : word
end
longest
```
## Working with Collections
 #### Code Together:
 Let's create a
#### Most used enumerable methods available in ruby



#### Traversing, Sorting and Modifying

#### Sorting

### Map & Reduce
 - `map` to create an Array of transformed Enumerable elements
 - `reduce` to "summarize" the elements in an Enumerable
 

## Demo: Write our own class that implements Enumerable
 >The Enumerable mixin provides collection classes with several traversal and searching methods, and with the ability to sort. The class must provide a method each, which yields successive members of the collection. If Enumerable#max, #min, or #sort is used, the objects in the collection must also implement a meaningful <=> operator, as these methods rely on an ordering between members of the collection. - [The Docs](https://ruby-doc.org/core-2.3.3/Enumerable.html)
 
 - So your code to create a class that uses the Enumerable module will have at least four key things:
 - A class definition, so we know it's a class
 - an `include` statement to "mixin" the Enumerable module and gain all of it's superpower
 - an `each` method, which yields successive members of the collection
 - a `<=>` operator if Enumerable#max, #min, or #sort is used
 
 > When you design a class, think about the objects that will be created from that class type. Think about the things the object knows and the things the object does.

> Things an object knows about itself are called instance variables. They represent an object's state (the data - for example, the quantity and the product id), and can have unique values for each object of that type.

> Things an object can do are called methods. [RubyLearning.com](http://rubylearning.com/satishtalim/writing_our_own_class_in_ruby.html)

## BREAK!

## Group exercise - High Card

How do you compare cards?

In your squads, create and play a few rounds of the popular card game, "High Card!" 

You will:
 - use enumerable methods 
 - create an algorithm to determine which of two cards, if either, is "greater" than the other.
 - accept input from the command line that your program uses
 - switch off who is typing the code and who is researching methods
 - Talk through your approach, what you discovered or what you struggled with

Go here for the details and to get started: https://github.com/danman01/high_card

## Code Together:

- Adding the spaceship operator to our custom Card class
- compare cards and find the highest
 
## Homework:
https://github.com/danman01/state_capitals
