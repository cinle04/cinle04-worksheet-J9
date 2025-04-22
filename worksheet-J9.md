1. What is the difference between a functional and non-functional requirement?

    **All requirements are testable. However, non-functional requirements focus on -ity concerns such as security, safety, and integrity.**

2. Give two example functional requirements for Instagram.com.

    **(1) allowing uesrs to follow other people (2) allowing  users to share a post**

3. Give two example non-functional requirements for Instagram.com.

    **(1) should be able to handle multiple users on the website (2) should load videos and videos quickly**

4. Draw a use case diagram for Instagram.com with at least three uses cases shown, where at least one use case extends another, and there are two actors.

    **![Answer to Question 4](https://github.com/cinle04/cinle04-worksheet-J9/blob/main/AnswerTo4.png)**

5. Why has software engineering evolved to often embrace agile development models over waterfall ones?

    **Agile development models focus on creating small pieces of the system before fully fleshing it out at a time. This is often embraced as sometimes, good requirements can not be gathered up front since cliets may not know what they want. A benefit of this is that it reduces the number of changes that need to be incorporated later.**

6. Draw a diagram where there are at least two interconnected paths: a critical path, and at least one non-critical path.

ADD LATER CRIT = LONGEST

    **![Answer to Question 6](https://github.com/cinle04/cinle04-worksheet-J8/blob/main/Question2.png)**

7. What is the difference between a design pattern and a java library?

    **Design pattern is a concept that provides a conceptual solution to a commonnly-occuring software engineering problem. Java libraries are tools that are tools that have concrete solutions. Design patterns provide conceptual solutions, java libraries provide concrete solutions.**

8. Using the Singleton pattern, write code/pseudocode that ensures that only one database connection object is ever instantiated.

    ````
    public class dataConnection {

        private static dataConnection singleton;
        private static dataConnection connection;

        private dataConnection(){
            connection = new dataConnection("cindy", "12345", "SCHEMA1");
        }
    }

    public static dataConnection getInstance(){
        if (singleton == null){
            singleton = new dataConnection();
        }

    }
    ````

9. Assume there is an Animal abstract parent class that has the following constructor: public Animal(String name, int weight).

    Using the Factory pattern, write code/pseudocode that sets up a factory for two child classes of Animal: Bird and Mammal. Each of these has a constructor with the same arguments as those of the parent class.

    ````
    public class AnimalFactory {

    public static Animal getAnimal(String type, String name, int weight){
        switch(type){
            case "MAMMAL":
                return new Mammal(name, weight);
            case "BIRD":
                return new Bird(name, weight);
        }
        return null;
        }
    }
    ````

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

    ````
    public class MammalAdapter extends Fish {
        private Mammal mammal;
    
        public MammalAdapter (Mammal m){
            mammal = m;
        }

        public void food(String food, int weight){
            return mammal.feed(food, weight, "antibiotics");
        }

        public void clean(cleaningProduct){
            return mammal.clean();
        }
    }
    ````

11. What is the benefit of the Bridge design pattern? Why use one?

    **The benefit is that it separates abstraction from implementation which makes it flexible. Using one reduces the amount of classes to manage.**

12. When would you use Java over C++? C++ over Java?

    **Java over C++ when you want to use its garbage collection function. Java if you don't have to managing memory isn't a concern. C++ over Java when you need to have a fine-grained manual control over memory allocation and dellocation. It's useful for operating systems.**

13. What is static versus dynamic typing? How is dynamic binding related to these concepts?

    **Static typing forces you to declare types at compile time. So, the complier can catch type mismatches before you're allowed to run. In dynamic typing, the type of an assignment is determined at runtime. Dynamic binding is related as methods are determined at runtime, similar to dynamic typing.**
