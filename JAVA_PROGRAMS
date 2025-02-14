### Perfect,Abudant, Deficient Number
````
In Java, Perfect, Abundant, and Deficient Numbers are classified based on the sum of their proper divisors:
Perfect Number: The sum of its proper divisors is equal to the number itself.
Example: 6 → (1 + 2 + 3 = 6)
Abundant Number: The sum of its proper divisors is greater than the number.
Example: 12 → (1 + 2 + 3 + 4 + 6 = 16 > 12)
Deficient Number: The sum of its proper divisors is less than the number.
Example: 8 → (1 + 2 + 4 = 7 < 8)
````
````java
import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int n=s.nextInt();
	    int sum=0;
	    for(int i=1;i<n;i++){
	        if(n%i==0){
	        sum+=i;
	    }
	    }
	    if(sum==n){
		System.out.println("PERFECT");
	}
	else if(sum>n){
	    System.out.println("ABUNDANT");
	}
	else{
	System.out.println("DEFICIENT");
}
}
}
````
