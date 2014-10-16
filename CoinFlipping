import java.util.Random;
import java.util.Scanner;

public class Main {
	static int coins = 0;
	static int[] coinValue = null;
	static int amtHeads = 0;
	static int amtTails = 0;
	static int bal = 1;

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scan = new Scanner(System.in);
		Random rand = new Random();
		boolean play = true;
		boolean coinsloop = true;
		while (play) {
			if (bal == 0) {
				System.err.println("You went bankrupt.");
				System.exit(0);
			}
			System.out.println("Welcome. How many coins to flip?");
			coinsloop = true;

			try {
				coins = scan.nextInt();
				coinsloop = false;
			} catch (Exception e) {
				System.err
						.println("Try again, with a real number this time...");
				System.exit(0);
			}
			coinValue = new int[coins + 1];
			// ************** Flipping the Coins ***********************
			for (int i = 1; i <= coins; i++) {

				coinValue[i] = rand.nextInt(2);
				// System.out.println("Coin " + i + " equals " + coinValue[i]);
			}
			// ************** Coin Value Assigning ********************
			for (int i = 1; i < coinValue.length; i++) {
				if (coinValue[i] == 1) {
					// System.out.println("Coin " + i + " is HEADS");
					amtHeads++;
				} else {
					// System.out.println("Coin " + i + " is TAILS");
					amtTails++;
				}
			}
			System.out.println("Out of " + coins
					+ " coins, How many were heads?");
			int headGuess = 0;
			try {
				headGuess = scan.nextInt();
			} catch (Exception e) {
				System.err
						.println("Try again, with a real number this time...");
				System.exit(0);
			}
			int bet = 0;
			System.out.println("How much do you want to bet? Your balance is "
					+ bal);
			try {
				bet = scan.nextInt();
			} catch (Exception e) {
				System.err
						.println("Try again, with a real number this time...");
				System.exit(0);
			}
			if (headGuess == amtHeads) {
				bal = bal + bet;
			} else {
				bal = bal - bet;
			}
			System.out.println("Heads: " + amtHeads);

		}

	}
}
