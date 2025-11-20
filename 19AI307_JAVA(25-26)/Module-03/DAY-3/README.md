# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class GameScore with an abstract method finalScore().
Define two subclasses:

ArcadeGame → final score = baseScore + (level × 100)

PuzzleGame → final score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

The program should read the game type (1 for Arcade, 2 for Puzzle) and the required inputs, then calculate and print the final score.
## AIM:
To develop a program using abstraction that calculates the final score for Arcade and Puzzle games by implementing the abstract method in their respective subclasses.
## ALGORITHM :
1. Start the program and read the user's choice for game type.
2. If the choice is ArcadeGame, read base score and level, create an ArcadeGame object, and compute the final score.
3. If the choice is PuzzleGame, read number of attempts, create a PuzzleGame object, and compute the final score.
4. Print the final score returned by the overridden finalScore() method.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;
    
    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;
    
    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();

        if (choice == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            GameScore game = new ArcadeGame(base, level);
            System.out.println(game.finalScore());
        } else if (choice == 2) {
            int attempts = sc.nextInt();
            GameScore game = new PuzzleGame(attempts);
            System.out.println(game.finalScore());
        }
        sc.close();
    }
}
```
## OUTPUT:

<img width="632" height="212" alt="image" src="https://github.com/user-attachments/assets/de4cf65e-eb64-4f39-8166-2af7a314796b" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
