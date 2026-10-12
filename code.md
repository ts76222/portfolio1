import java.util.scanner;

public class stand
{
    
    static scanner input= new scanner(System.in);
    
	double cash = 100.00;
	int lemons = 0;
	int sugar = 0;
	int recipesugar = 0;
	int recipelemon = 0;
	int recipewater =0;
	int cupprice = 1.00;
	int pitcher =0;
	int day = 0;
}

public static void main(String [] args) {
    System.out.println("Welcome to My Lemonade Stand Game!");
    
    boolean preptime = true;
    
    while (preptime) {
        System.out.println("Day 1: Preparation Phase\n");
        System.out.println("Prepare for the Day\n");
        System.out.println("---------------------\n");
        System.out.println("Lemons: 0\n");
        System.out.println("Sugar Cups: 0\n");
        System.out.println("Water Cups: Infinite\n");
        System.out.println("Current Pitchers: 0\n");
        System.out.println("Cash: $100\n");
        
        System.out.println("1. Buy Ingredients\n");
        System.out.println("2. Tweak the Recipe\n");
        System.out.println("3. Set the Price\n");
        System.out.println("4. Make Pitchers of Lemonade");
        System.out.println("5. Move Onto the Selling Phase");
        
        System.out.println("What would you like to do?");
        int choose = input.nextInt();
        
        switch (choose) {
            case 1:
                buyingredients();
                break;
            case 2:
                tweakrecipe();
                break;
            case 3:
                setprice();
                break;
            case 4:
                makepitchers();
                break;
            case 5:
                preptime = false;
                System.out.println("Moving to the Selling Phase.");
                break:
            default:
            System.out.println("What would you like to do now?");
        
        }
    }
    input.close();
}

public static void buyingredients() {
    System.out.println("Lemons are $1 each.\n");
    System.out.println("Sugar is $0.50 per cup.\n");
    
    System.out.println("How many lemons would you like to buy?\n");
    int buylemons=input.nextInt();
    
    System.out.println("How many cups of sugar would you like to buy?\n");
    int buysugar= input.nextInt();
    
    double cost= buylemons + (buysugar*0.50);
    
    if cost>cash) {
        System.out.println("You do not have enough money for this purchase\n");
        return;
    }
    
    lemons += buylemons;
    sugar += buysugar;
    cash -= cost;
}
