# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.
## AIM:
To write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

## ALGORITHM :
1. Start the program and read the type of animal from the user.
2. Based on the input, create an object of Bird, Cat, or the base Animal class.
3. Call the Sound() method using the created object.
4. The method that belongs to the specific object’s class is executed (polymorphism).
5. End the program.
## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: PRAISEY S 
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    void Sound() {
        System.out.println("Animal makes a sound");
    }
}

class Bird extends Animal {
    @Override
    void Sound() {
        System.out.println("Bird chirps");
    }
}

class Cat extends Animal {
    @Override
    void Sound() {
        System.out.println("Cat meows");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.next().toLowerCase();

        Animal animal;

        if (type.equals("bird")) {
            animal = new Bird();
        } else if (type.equals("cat")) {
            animal = new Cat();
        } else {
            animal = new Animal();
        }

        animal.Sound();
        sc.close();
    }
}

```
## OUTPUT:

<img width="797" height="250" alt="image" src="https://github.com/user-attachments/assets/12fb78ef-c640-40e3-83b9-945bed0c3b91" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
