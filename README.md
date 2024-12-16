# Interest_rate_Java
//calculates interest rate 
import java.util.Scanner;
public class BankBalance{
	
	public static void main(String[] args) {
		double balance;
		int response;
		int months = 3;
		final double INT_RATE = 0.7;
		
		Scanner keyboard = new Scanner(System.in);
		System.out.print("Enter initial bank balance > ");
		balance = keyboard.nextDouble();
		keyboard.nextLine();
		do 
		{
			balance = balance + balance * INT_RATE;
			System.out.println("After year " + months + " at " + INT_RATE + 
					" interest rate, balance is R" + balance);
			months +=1;
			System.out.println("\nDo you want to see the balance " 
			+ "at the end of another year?");
			System.out.println("Enter 1 for yes");
			System.out.println(" or any other number for no >> ");
			response = keyboard.nextInt();
		}while(response == 1);
	}
}
