# Java_ClassNotes
Java exercises and solutions for new beginners
I am here to share my studies and also the previous work that helped me to learn programming language Java.
Hopefully it will be beneficial for those who are in the beginning level and seeking simple solutions for their tasks.

A simple solution for the Towers of Hanoi problem with recursive method.

public class Main {

    public static void main(String[] args) {  //using recursive method to solve classic Towers of Hanoi problem
        Scanner input = new Scanner(System.in);
        System.out.print("Enter number of disks: ");
        int n = input.nextInt();

        //Find solution recursively
        System.out.println("The moves are:");
        moveDisks(n,'A', 'B', 'C');
    }
    //creating the method for moving n disks from one tower to another
    public static void moveDisks(int n, char fromTower, char toTower, char auxTower){
        if(n == 1) //base or stopping condition
            System.out.println("Move disk " + n + " from " + fromTower + " to " + toTower);
        else {
            moveDisks(n-1,fromTower,auxTower,toTower);
            System.out.println("Move disk " + n + " from " + fromTower + " to " + toTower);
            moveDisks(n-1,auxTower,toTower,fromTower);
        }
    }
}
