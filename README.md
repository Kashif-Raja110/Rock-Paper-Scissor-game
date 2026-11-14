# Rock-Paper-Scissor-game
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        Random random = new Random();

        System.out.print("Choose rock, paper, or scissors: ");
        String player = input.nextLine().toLowerCase();

        String[] choices = {"rock", "paper", "scissors"};
        String computer = choices[random.nextInt(3)];

        System.out.println("You chose: " + player);
        System.out.println("Computer chose: " + computer);

        if (!player.equals("rock")
                && !player.equals("paper")
                && !player.equals("scissors")) {
            System.out.println("Invalid choice. Please run the game again.");
        } else if (player.equals(computer)) {
            System.out.println("It's a tie!");
        } else if ((player.equals("rock") && computer.equals("scissors"))
                || (player.equals("paper") && computer.equals("rock"))
                || (player.equals("scissors") && computer.equals("paper"))) {
            System.out.println("You win!");
        } else {
            System.out.println("Computer wins!");
        }

        input.close();
    }
}
