import java.util.Random;
import java.util.Scanner;

public class RockPaperScissor {
    public static void main(String [] args) {

        int rock = 0;
        int paper = 1;
        int scissor = 2;

        boolean playAgain = true;

        Scanner input = new Scanner(System.in);

        while (playAgain) {
        System.out.println("0. Rock");
        System.out.println("1. Paper");
        System.out.println("2. Scissor");
        System.out.print("Choose Rock, Paper or Scissor: ");
        int playerChoice = input.nextInt();

        Random random = new Random();
        int computerChoice = random.nextInt(3);

        if (playerChoice == computerChoice) {
            System.out.println("Its a tie!");
        } 
        else if (playerChoice == rock && computerChoice == scissor) {
            System.out.println("You Win!");
        }
        else if (playerChoice == rock && computerChoice == paper) {
            System.out.println("You lose!");
        }
        else if (playerChoice == paper && computerChoice == scissor) {
            System.out.println("You lose!");
        }
        else if (playerChoice == paper && computerChoice == rock) {
            System.out.println("You Win!");
        }
        else if (playerChoice == scissor && computerChoice == paper) {
            System.out.println("You Win!");
        }
        else if (playerChoice == scissor && computerChoice == rock) {
            System.out.println("You Lose!");
        }
        else {
            System.out.println("You did not choose anything.");
        }

        System.out.println("Do you still want to play(No/Yes)? ");

        input.nextLine();
        String yesnoPlay = input.nextLine();

        if (yesnoPlay.equalsIgnoreCase("yes")) {
            playAgain = true;
        }
        else if (yesnoPlay.equalsIgnoreCase("no")) {
            playAgain = false;
        }

        }

        System.out.println("You have stopped playing.");
    }
}
