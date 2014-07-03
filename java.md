#Layperson introduction with some of the specs, strengths, and use cases:

Java, unlike Ruby, is a strongly-typed, compiled language. I've so far used it for the same old stuff, building APIs and loading data, but I'll keep you posted if I learn more about it's specialness. I will admit that so far, it has seemed less buggy.

Strongly typed: Every data structure must be explicitly defined. For example, in Ruby, we might type x = 4. In Java, we would need to declare that x is an int by typing 'int x = 4'. This actually is pretty useful in terms of clarity of code.

While Ruby compiles at runtime, Java has to build and compiled before it can be run. Any errors or issues with code will make the code fail to compile, so you'll have to fix it then.

#Install guide and/or notes on expected preinstalled tools (only for dependencies)

Java can be downloaded from the internet, as can a free version of an IDE of your choosing (essentially your text editor). I use Intellij, although lots of people seem to use Eclipse. It's actually pretty fancy-- prompt indications of errors and some cool ways to click through each file.

"Hello World" (or equivalent) tutorial

1. Create a new package with the same name as the class. For example, HelloWorldApp (we camelcase our java)
2. Create a class with that same name.
3. Create a constructor that will print the phrase "Hello World!" 

`class HelloWorldApp {`

    public static void main(String[] args) {

       System.out.println("Hello World!"); // Display the string.

    }

`}`

#A link to the official docs and at least 3 other resources

Official Docs: <http://docs.oracle.com/javase/7/docs/api/>

Other resources:
<http://practiceit.cs.washington.edu/practiceit/>

<https://www.codehunt.com/>

<https://netbeans.org/kb/articles/learn-java.html>