1. What is the difference between a functional and non-functional requirement?

    **rah**

2. Give two example functional requirements for Instagram.com.

    **rah**

3. Give two example non-functional requirements for Instagram.com.

    **rah**

4. Draw a use case diagram for Instagram.com with at least three uses cases shown, where at least one use case extends another, and there are two actors.

    **rah**

5. Why has software engineering evolved to often embrace agile development models over waterfall ones?

    **rah**

6. Draw a diagram where there are at least two interconnected paths: a critical path, and at least one non-critical path.

    **rah**

7. What is the difference between a design pattern and a java library?

    **rah**

8. Using the Singleton pattern, write code/pseudocode that ensures that only one database connection object is ever instantiated.

    **rah**

9. Assume there is an Animal abstract parent class that has the following constructor: public Animal(String name, int weight).

    Using the Factory pattern, write code/pseudocode that sets up a factory for two child classes of Animal: Bird and Mammal. Each of these has a constructor with the same arguments as those of the parent class.

    **rah**

10. Imagine we have some code for an aquarium that works nicely to schedule feeding the fish in all the tanks, and cleaning the tanks:

    ````
    public class Aquarium {
        public void feedAll(ArrayList<Fish> tanks, int numFishInTank) {...}
        public void cleanAll(ArrayList<Fish> tanks)
    }
    ````
    This code works well with the following Fish class:
    ````
    public class Fish{
        public void feed(String food, int weight) {...}
        public void clean(String cleaningProduct) {...}
    }
    ````
    We also, one day, inherit an animal hospital, where each patient is solo in a cage. We want to be able to use the code above to feed and clean the cages of all the animals, but our hospital has the following API for the mammals they serve:

    ````
    public class Mammal{
        public void feed(String food, int weight, String medication) {...}
        public void clean() {...}
    }
    ````
    Use the Adapter pattern to allow us to use the Mammal class with the Aquarium class above. Each animal is housed alone in its cage during its visit. All mammals are given the same medication, namely, "antibiotics".

    **rah**

11. What is the benefit of the Bridge design pattern? Why use one?

    **rah**

12. When would you use Java over C++? C++ over Java?

    **rah**

13. What is static versus dynamic typing? How is dynamic binding related to these concepts?

    **rah**
