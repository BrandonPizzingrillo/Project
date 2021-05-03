# Project
package McdonaldsProject;
import java.util.Scanner;


public class Intro {
	// Intro

	public static void main(String []args) {
	int time;	
	Scanner sc = new Scanner(System.in);	
		double egg = 2.79; // Price of Eggs
		double sausage = 2.99; // Price of Sausages
		double big = 5.49; // Price of Big Breakfast
		double hot = 2.49; // Price of Hot Cakes
		double pc = 5.79; // Price of McNuggets
		double mac = 4.99; // Price of Big Mac
		double quart = 5.49; // Price of Quarter Pounder
		double happy = 5.29; // Price of Happy Meal
		double breakfast = 0; // Total
		double lunch = 0;
		double sub = 0; // Constantly changing variable for subtotal		
		int order;
		int order2;
		int quantity = 0;
		int meal = 0;
		int complete = 0;
		int complete2 = 0;	
				
		// INTRODUCTION:
		System.out.println("Welome to McDonalds!");
		System.out.println("Please input the current time where you are. (No Colon)");
		time = sc.nextInt();	
				
	// The time variable is placed into the following if statement to determine whether breakfast is still being served		
		// This if statement contains all of the code for breakfast
		if(time <= 1000 && time >= 700) {
			System.out.println("");
	System.out.println("We're currently still serving breakfast, please choose the number option from our breakfast menu:");			
			System.out.println("	1. Egg McMuffin [$2.79]");
			System.out.println("	2. Sausage McMuffin [$2.99] *OUT OF STOCK* ");
			System.out.println("	3. Big Breakfast With Hotcakes [$5.49]");
			System.out.println("	4. 3 Hotcakes [$2.49]");
			order = sc.nextInt();			
					// BREAKFAST
	switch(order) {
		
	// This switch allows for us to determine what the customer wants
case 1: // Egg McMuffin
	System.out.println("Egg McMuffin:");
			System.out.println("Select Quantity");
			System.out.println("1");
			System.out.println("2");
			System.out.println("3");
			System.out.println("0. None");
			quantity = sc.nextInt();
				switch(quantity) {
				case 1:
						System.out.println("1 Egg McMuffin: " + egg); // Egg variables are defined to hold a set price, multiplied by the quantity selected
						System.out.println("Would you like to make it a meal for an extra 2 dollars?");
						System.out.println("1. Yes || 2. No");
					meal = sc.nextInt();
					switch(meal) {
					case 0:
						break;
					case 1:
						System.out.println("Egg McMuffin Meal: " + egg +2); // CURRENT BUG
						breakfast = sub + egg + 2; // Breakfast variable keeps track of total 
						break;
					case 2:
						System.out.println("Egg McMuffin: " + egg);
						breakfast = sub + egg;
						break;
					}
			
					break;
					
				case 2:
									System.out.println("2 Egg McMuffins: " + egg*2);
				System.out.println("Would you like to make it a meal for an extra 2 dollars?");
				System.out.println("1. Yes || 2. No");
					meal = sc.nextInt();
					switch(meal) {
					case 1:
						System.out.println("Egg McMuffin Meal: " +egg*2 +2); // CURRENT BUG
						breakfast = sub + egg*2 + 2;
						break;
					case 2:
						System.out.println("Egg McMuffin: " + egg*2);
						breakfast = sub + egg*2;
															break;
					}
			
					break;
					
				case 3:
					System.out.println("3 Egg McMuffins: " + egg*3);
								System.out.println("Would you like to make it a meal for an extra 2 dollars?");
				System.out.println("1. Yes || 2. No");
													meal = sc.nextInt();
					switch(meal) {
					case 1:
						System.out.println("Egg McMuffin Meal: " + egg*3 +2); // CURRENT BUG
						breakfast = sub + egg*3 + 3;
						break;
					case 2:
						System.out.println("Egg McMuffin: " + egg*3);
						breakfast = sub + egg*3;
						break;
					}
			
					break;
					
				default:
					System.out.println("Please choose between 1 and 3");
				}
		break;		
			// meal is a variable used to determine whether they would like to make it a meal, putting 1 prints out the new subtotal
case 2: // Sausage McMuffin
			System.out.println("Sausage McMuffin:");
			System.out.println("We regret to inform you that we've run out of Sausage McMuffins.");			
		
		break;
case 3: // Big Breakfast
			System.out.println("Big Breakfast With Hotcakes:");
			System.out.println("Select Quantity");
			System.out.println("1");
			System.out.println("2");
			System.out.println("3");
			System.out.println("0. None");
			quantity = sc.nextInt();
					switch(quantity) {
				case 0:		
					break;
				case 1:
			System.out.println("1 Big Breakfast With Hotcakes: " + big); // Egg variables are defined to hold a set price, multiplied by the quantity selected
			System.out.println("Would you like to make it a meal for an extra 2 dollars?");
			System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
					switch(meal) {
				case 1:
				System.out.println("Big Breakfast Meal: " + big +2); // CURRENT BUG
				breakfast = sub + big + 2;
				break;
				case 2:
				System.out.println("Big Breakfast: " + big);
				breakfast = sub + big;
				break;
			}
	
			break;
			
		case 2:
			System.out.println("2 Big Breakfast Meals: " + big*2);
		System.out.println("Would you like to make it a meal for an extra 2 dollars?");
		System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
			switch(meal) {
			case 1:
				System.out.println("Big Breakfast Meal: " +big*2 +2); // CURRENT BUG
				breakfast = sub + big*2 + 2;
				break;
			case 2:
				System.out.println("Big Breakfast: " + big*2);
				breakfast = sub + big*2;
				break;
			}
	
			break;
			
		case 3:
			System.out.println("3 Big Breakfast Meals: " + big*3);
		System.out.println("Would you like to make it a meal for an extra 2 dollars?");
		System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
			switch(meal) {
			case 1:
				System.out.println("Big Breakfast Meal: " + big*3 +2); // CURRENT BUG
				breakfast = sub + big*3 + 2;
				break;
			case 2:
				System.out.println("Big Breakfast: " + big*3);
				breakfast = sub + big*3;
				break;
			}
	
			break;
			
		default:
			System.out.println("Please choose between 1 and 3");
		}
		break;
case 4: // Hotcakes
			System.out.println("Hotcakes:");
			System.out.println("Select Quantity");
			System.out.println("1");
			System.out.println("2");
			System.out.println("3");
			System.out.println("0. None");
			quantity = sc.nextInt();
				switch(quantity) {
				case 0:
					break;
		case 1:
			System.out.println("1 Hotcake: " + big); // Egg variables are defined to hold a set price, multiplied by the quantity selected
			System.out.println("Would you like to make it a meal for an extra 2 dollars?");
			System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
				switch(meal) {
		case 1:
			System.out.println("Hotcakes Meal: " + hot +2); // CURRENT BUG
			breakfast = sub + hot + 2;
			break;
		case 2:
			System.out.println("Hotcakes: " + hot);
			breakfast = sub + hot;
			break;
	}

			break;
	
		case 2:
			System.out.println("2 Hotcake Meals: " + hot*2);
			System.out.println("Would you like to make it a meal for an extra 2 dollars?");
			System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
				switch(meal) {
		case 1:
			System.out.println("Hotcake Meal: " +hot*2 +2); // CURRENT BUG
			breakfast = sub + hot*2 + 2;
			break;
		case 2:
			System.out.println("Hotcakes: " + hot*2);
			breakfast = sub + hot*2;
			break;
	}

			break;
	
		case 3:
			System.out.println("3 Hotcake Meals: " + hot*3);
			System.out.println("Would you like to make it a meal for an extra 2 dollars?");
			System.out.println("1. Yes || 2. No");
			meal = sc.nextInt();
				switch(meal) {
		case 1:
			System.out.println("Hotcake Meal: " + hot*3 +2); // CURRENT BUG
			breakfast = sub + hot*3 + 2;
			break;
		case 2:
			System.out.println("Hotcakes: " + hot*3);
			breakfast = sub + hot*3;
			break;
				}

			break;
	
		default:
			System.out.println("Please choose between 1 and 3");
}
				break;
				default:
					System.out.println("Please choose a valid number from the menu");
} // Order Switch	
	
	
	
	
	
	System.out.println("Subtotal: " + breakfast);
	
	
	
	
	
	
	
} else if (time >= 1000 && time <= 2000) { // Time between 1000 and 2000 allows the user to choose from the lunch menu
	System.out.println("");
	System.out.println("We're currently serving lunch/dinner, please choose the number option from our menu:");			
	System.out.println("	1. 10 Pc. McNuggets [$5.79]");
	System.out.println("	2. Big Mac [$4.99]");
	System.out.println("	3. Double Quarter Pounder [$5.49]");
	System.out.println("	4. Happy Meal [$5.29]");
	order2 = sc.nextInt();
	
	switch(order2) {
	case 1:
		System.out.println("10 Pc. McNuggets:");
		System.out.println("Select Quantity");
		System.out.println("1");
		System.out.println("2");
		System.out.println("3");
		System.out.println("0. None");
		quantity = sc.nextInt();
			switch(quantity) {
			case 1:
				System.out.println("10 Pc. McNuggets: " + pc); // PC variables are defined to hold a set price, multiplied by the quantity selected
			System.out.println("Would you like to add French Fries for an extra  dollar?");
			System.out.println("1. Yes || 2. No");
				meal = sc.nextInt();
				switch(meal) {
				case 0:
					break;
				case 1:
					System.out.println("10 Pc. McNuggets Meal: " + pc +1); // CURRENT BUG
					lunch = sub + pc + 1; // Breakfast variable keeps track of total 
					break;
				case 2:
					System.out.println("10 Pc. McNuggets: " + pc);
					lunch = sub + pc;
					break;
				}
		
				break;
				
			case 2:
				System.out.println("2 10 Pc. McNuggets: " + pc*2);
			System.out.println("Would you like to add French Fries for an extra dollar?");
			System.out.println("1. Yes || 2. No");
				meal = sc.nextInt();
				switch(meal) {
				case 1:
					System.out.println("10 Pc. McNuggets Meal: " +pc*2 +1); // CURRENT BUG
					lunch = sub + pc*2 + 1;
					break;
				case 2:
					System.out.println("10 Pc. McNuggets: " + pc*2);
					lunch = sub + pc*2;
					break;
				}
		
				break;
				
			case 3:
				System.out.println("3 10 Pc. McNuggets: " + pc*3);
			System.out.println("Would you like to add French Fries for an extra dollar?");
			System.out.println("1. Yes || 2. No");
				meal = sc.nextInt();
				switch(meal) {
				case 1:
					System.out.println("10 Pc. McNuggets Meal: " + pc*3 +1); // CURRENT BUG
					lunch = sub + pc*3 + 1;
					break;
				case 2:
					System.out.println("10 Pc. McNuggets: " + pc*3);
					lunch = sub + pc*3;
					break;
				}
		
				break;
				
			default:
				System.out.println("Please choose between 1 and 3");
			}
	break;		
		// meal is a variable used to determine whether they would like to make it a meal, putting 1 prints out the new subtotal
case 2:
		System.out.println("Big Mac:");
		System.out.println("Select Quantity");			
		System.out.println("1");
		System.out.println("2");
		System.out.println("3");
		System.out.println("0. None");
		quantity = sc.nextInt();
					switch(quantity) {
				case 0:
					break;
				case 1:
			System.out.println("1 Big Mac: " + mac); // Egg variables are defined to hold a set price, multiplied by the quantity selected
			System.out.println("Would you like to add French Fries for an extra dollar?");
			System.out.println("1. Yes || 2. No");
	meal = sc.nextInt();
			switch(meal) {
				case 1:
			System.out.println("Big Mac Meal: " +mac + 1); // CURRENT BUG
			lunch = sub + mac + 1;
			break;
				case 2:
			System.out.println("Big Mac: " + mac);
			lunch = sub + mac;
			break;
		}

		break;
		
				case 2:
		System.out.println("2 Big Macs: " + mac*2);
		System.out.println("Would you like to add French Fries for an extra dollar?");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
			switch(meal) {
				case 1:
			System.out.println("Big Mac Meal: " +mac*2 +1); // CURRENT BUG
			lunch = sub + mac*2 + 1;
			break;
				case 2:
			System.out.println("Big Mac: " + mac*2);
			lunch = sub + mac;
			break;
		}

		break;
		
				case 3:
		System.out.println("3 Big Macs: " + mac*3);
		System.out.println("Would you like to add French Fries for an extra dollar?");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
			switch(meal) {
				case 1:
			System.out.println("Big Mac Meal: " + mac*3 +1); // CURRENT BUG
			lunch = sub + mac*3 + 1;
			break;
				case 2:
			System.out.println("Big Mac: " + mac*3);
			lunch = sub + mac*3;
			break;
		}

		break;
		
	default:
		System.out.println("Please choose between 1 and 3");
	}
	break;
case 3:
		System.out.println("Double Quarter Pounder:");
		System.out.println("Select Quantity");
		System.out.println("1");
		System.out.println("2");
		System.out.println("3");
		System.out.println("0. None");
		quantity = sc.nextInt();
				switch(quantity) {
			case 0:		
				break;
			case 1:
		System.out.println("1 Double Quarter Pounder: " + quart); // Egg variables are defined to hold a set price, multiplied by the quantity selected
		System.out.println("Would you like to add French Fries for an extra dollar?");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
				switch(meal) {
			case 1:
			System.out.println("Double Quarter Pounder Meal: " + quart +1); // CURRENT BUG
			lunch = sub + quart + 1;
			break;
			case 2:
			System.out.println("Double Quarter Pounder: " + quart);
			lunch = sub + quart;
			break;
		}

		break;
		
	case 2:
		System.out.println("2 Double Quarter Pounders: " + quart*2);
	System.out.println("Would you like to add French Fries for an extra dollar?");
	System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
		switch(meal) {
		case 1:
			System.out.println("Double Quarter Pounder Meal: " +quart*2 +1); // CURRENT BUG
			lunch = sub + quart*2 + 1;
			break;
		case 2:
			System.out.println("Double Quarter Pounder: " + quart*2);
			lunch = sub + quart*2;
			break;
		}

		break;
		
	case 3:
		System.out.println("3 Double Quarter Pounders: " + quart*3);
	System.out.println("Would you like to add French Fries for an extra dollar?");
	System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
		switch(meal) {
		case 1:
			System.out.println("Double Quarter Pounder Meal: " + quart*3 +1); // CURRENT BUG
			lunch = sub + quart*3 + 1;
			break;
		case 2:
			System.out.println("Double Quarter Pounder: " + quart*3);
			lunch = sub + quart*3;
			break;
		}

		break;
		
	default:
		System.out.println("Please choose between 1 and 3");
	}
	break;
case 4:
		System.out.println("Happy Meal:");
		System.out.println("Select Quantity");
		System.out.println("1");
		System.out.println("2");
		System.out.println("3");
		System.out.println("0. None");
		quantity = sc.nextInt();
			switch(quantity) {
			case 0:
				break;
	case 1:
		System.out.println("1 Happy Meal: " + happy); // Egg variables are defined to hold a set price, multiplied by the quantity selected
		System.out.println("Would you like to Supersize it for an extra 3 dollars??");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
			switch(meal) {
	case 1:
		System.out.println("Supersized Happy Meal: " + happy +3); // CURRENT BUG
		lunch = sub + happy + 3;
		break;
	case 2:
		System.out.println("Happy Meal: " + happy);
		lunch = sub + happy;
		break;

}

		break;

	case 2:
		System.out.println("2 Happy Meals: " + hot*2);
		System.out.println("Would you like to Supersize it for an extra 3 dollars??");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
			switch(meal) {
	case 1:
		System.out.println("Supersized Happy Meal: " +happy*2 +3); // CURRENT BUG
		lunch = sub + happy*2 + 3;
		break;
	case 2:
		System.out.println("Happy Meal: " + happy*2);
		lunch = sub + happy*2;
		break;
}

		break;

case 3:
		System.out.println("3 Happy Meals: " + happy*3);
		System.out.println("Would you like to Supersize it for an extra 3 dollars?");
		System.out.println("1. Yes || 2. No");
		meal = sc.nextInt();
			switch(meal) {
	case 1:
		System.out.println("Hotcake Meal: " + happy*3 +3); // CURRENT BUG
		lunch = sub + happy*3 + 3;
		break;
	case 2:
		System.out.println("Hotcakes: " + happy*3);
		lunch = sub + happy*3;
		break;
			}

		break;

	default:
		System.out.println("Please choose between 1 and 3");
}
			break;	
		
	}
	
		System.out.println("Subtotal: " +lunch);
		
	
}
} // Main Class	
}// Public Class

