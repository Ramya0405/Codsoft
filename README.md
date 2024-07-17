package Codsoft;
import java.util.Scanner;
public class Numbers_game {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the target number:");
        int target = sc.nextInt();
        System.out.print("Maximum no.of attempts:");
        int max_attempts = sc.nextInt();
        int attempts =0;
        int score =0;
        while(true){
            while(attempts<max_attempts){
                System.out.print("Enter the number you guess:");
                int guess = sc.nextInt();
                attempts++;
                if(guess == target){
                    System.out.println("Correct");
                    score++;
                }else if(guess > target){
                    System.out.println("To high");
                }else if(guess < target){
                    System.out.println("Too low");
                }
                if(attempts == max_attempts){
                    System.out.println("Reached the maximum attempt");
                }
            }
            System.out.println("You have Scored:"+(score*100));
            break;
        }
        sc.close();

    }
}
