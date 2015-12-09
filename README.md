# HW10
# Project 1:WH10


## Source Code
```
package Aziz;
import java.util.Scanner;

public class homework10 {
	public static void main(String[] args) {
		//System.out.println("Hello ");
		
		//assigning the addgame as the syntax.
		addgame();
	}
	public static void addgame() {
		//System.out.println("Inside the addition game method.");
		
		int hrdns = 5;
		int hrdnsfwd = 2;
		int points = 0;
		
		// Set up my for loop to go through the number of rounds
		int roundsOfNum = 3;
		for(int getroundedNum = 1; 
		getroundedNum <= roundsOfNum;  
		getroundedNum = getroundedNum + 1){
			//System.out.println("Inside the for loop. Round: " + getroundedNum);
			System.out.print("Round " + getroundedNum + " of " + roundsOfNum + ". ");
			boolean isAnswerCorrect = getAndCheckStudentAnswer(hrdns);
			if(isAnswerCorrect){
				System.out.print("Your points was " + points + " and is now ");
				points = points + hrdns;
				System.out.print(points + ". ");
				
				if(getroundedNum<roundsOfNum){
					System.out.print("Your hrdns was " + hrdns + " and is now ");
					hrdns = hrdns * hrdnsfwd;
					System.out.println(hrdns + ".");
				}
			}else{
				System.out.print("Your points is " + points + ". ");
				if(getroundedNum<roundsOfNum){
					System.out.print("Your hrdns was " + hrdns + " and is now ");
					if(hrdns>5){
						hrdns = hrdns / hrdnsfwd;
					}
					System.out.println(hrdns + ".");
					
				}
				
			}
		}
		System.out.print("\nThe game is complete. ");
		System.out.println("Your final points was " + points );
	}
	
	public static boolean getAndCheckStudentAnswer(int hrdns) {
		//System.out.println("Inside get and check student answer method.");
		int num1 = (int)(Math.random()*hrdns);
		int num2 = (int)(Math.random()*hrdns);
		System.out.print("Add " + num1 + " and " + num2 +": ");
		//Scanner input = new Scanner(System.in);
		//int answer = input.nextInt();
		Scanner get = new Scanner(System.in);
		int answer = get.nextInt();
		if(answer == (num1 + num2)){
			System.out.print("Correct. ");
			return true;
		}else{
			System.out.println("Nice try, but the correct answer was " 
					+ (num1 + num2) + ".");
			return false;
		}
	}
}
```

## Console Output
```
Round 1 of 3. Add 1 and 1: 4
Nice try, but the correct answer was 2.
Your points is 0. Your hrdns was 5 and is now 5.
Round 2 of 3. Add 2 and 1: 5
Nice try, but the correct answer was 3.
Your points is 0. Your hrdns was 5 and is now 5.
Round 3 of 3. Add 4 and 1: 6
Nice try, but the correct answer was 5.
Your points is 0. 
The game is complete. Your final points was 0


```


## console history using git.


git push: add the changes to gir
git pull: to retrev the information from git
git add: to add the information to git

