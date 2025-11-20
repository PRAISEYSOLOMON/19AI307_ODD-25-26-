# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed.
## AIM:
To implement the Mediator Pattern by creating a ChatRoom mediator that controls communication between users. Instead of sending messages directly to each other, all messages must pass through the mediator. Two users send and receive messages only through the ChatRoom, ensuring loose coupling and centralized communication management.
## ALGORITHM :
1. Read the two usernames and create a ChatRoom object.
2. Register both users into the chat room.
3. Read how many messages will be sent.
4. For each message: read sender, receiver, and the message text.
5. Use the chat room to deliver the message to the receiver and display it.
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: PRAISEY S
RegisterNumber:  212222040117
*/
```

## SOURCE CODE:
```
import java.util.*;

class ChatRoom {
    private Map<String, User> users = new HashMap<>();
    public void registerUser(User user) {
        users.put(user.getName(), user);
    }

    public void sendMessage(String from, String to, String message) {
        User receiver = users.get(to);
        if (receiver != null) {
            receiver.receive(from, message);
        }
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
        chatRoom.registerUser(this); 
    }

    public String getName() {
        return name;
    }

    public void send(String to, String message) {
        chatRoom.sendMessage(name, to, message);
    }

    public void receive(String from, String message) {
        System.out.println(from + " to " + name + ": " + message);
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ChatRoom chatRoom = new ChatRoom();
        String user1Name = sc.nextLine();
        String user2Name = sc.nextLine();

        User user1 = new User(user1Name, chatRoom);
        User user2 = new User(user2Name, chatRoom);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sender = sc.nextLine();
            String receiver = sc.nextLine();
            String message = sc.nextLine();

            if (sender.equalsIgnoreCase(user1Name)) {
                user1.send(receiver, message);
            } else if (sender.equalsIgnoreCase(user2Name)) {
                user2.send(receiver, message);
            }
        }

        sc.close();
    }
}

```
## OUTPUT:

<img width="1170" height="746" alt="image" src="https://github.com/user-attachments/assets/64812140-6b91-4d7c-a8e1-11e7e0f1135e" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
