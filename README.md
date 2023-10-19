# Number-Game
import java.util.*;
class guessingNumber{
    public static void guessNumber() {
        Scanner sc = new Scanner(System.in);

        int number = 1 + (int)(100 * Math.random());

        int m = 5;
        int i , guess;

        System.out.println("Guess the number between 1 to 100 within 5 trials.");

        for(i=0; i<m; i++) {
            System.out.print("Guess the Number : ");

            guess = sc.nextInt();
            if(number == guess) {
                System.out.println("That's great... You guessed the right number..");
                break;

            }
            else if(number > guess && i != m-1) {
                System.out.println("The number is greater than "+guess);

            }
            else if(number < guess && i != m-1) {
                System.out.println("The number is less than "+guess);
            }
        }
        if(i==m) {
            System.out.print("Sorry, you have run out of attempts.");

            System.out.println("The number was "+number);
        }
    }
    public static void main(String[] args) {
        guessNumber();
    }
}
