# Java Assessment Question 1

Suppose that the following two classes have been declared: 

```java
    public class Car {
        public void m1() {
            System.out.println("car 1");
        }

        public void m2() {
            System.out.println("car 2");
        }

        public String toString() {
            return "vroom";
        }
    }

    public class Truck extends Car {
        public void m1() {
            System.out.println("truck 1");
        }

        public void m2() {
            super.m1();
        }

        public String toString() {
            return super.toString() + super.toString();
        }
    }
```

Write a class `MonsterTruck` whose methods have the behavior below. Don't just print/return the output; whenever possible, use inheritance to reuse behavior from the superclass. 

```
    Method              Output

    m1()                monster 1
    m2()                truck1()
                        car1()
    toString()          "monster vroom vroom"
```