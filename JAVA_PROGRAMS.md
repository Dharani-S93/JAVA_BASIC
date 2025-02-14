1. Perfect,Abudant, Deficient Number
2. LCM ,  GCD
3. Ampicable Pair
4. Betrothed Pair
5. Sqaure Free Numbers
6. Ugly Number 
7. Kaperakar Number
8. Armstrong NUmber
9. Adam Number
10. Digit Odd even Segregate
11. Palindrome or Not(Digit)12.  Happy Number
13. Pyramid Pattern
14. Double Right Arrow(Butterfly Pattern)
15.Hollow Square Pattern
16.  Second Largest Element in the Array
17. Majority Element
18. Sum of Right side elements
19. Left Rotation
20. Swap those position values in the array
21. Remove Duplicates
22.Kth Largest element in the array
23. Monotonic Array
24. Array Odd Even Seggregation
25. SLL reverse()
26. DLL Search_Delete()
27. SLL sort_unsorted()
28. DLL Palindrome
29. DLL SortedInsert()
30. SLL reverse()
31.Stock Buy and Sell – Max one Transaction Allowed
32.Remove All Occurrences of an Element in an Array
33.Remove duplicates from Sorted Array
34.Minimum Swaps required to group all 1’s together
35.Implement two Stacks in an Array                                                                                                                                                   36. How to efficiently implement k stacks in a single array?
37.Implement Stack using Queues
38.Inverted Right-Angle Triangle Pattern
39.Pyramid Pattern
40.Array Right Rotation


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

### GCD, LCM


````java
import java.util.*;
public class Main
{
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int n1=s.nextInt();
	    int n2=s.nextInt();
	    int a=n1;
	    int b=n2;
	    while(n1!=n2){
	        if(n1>n2){
	            n1-=n2;
	        }
	        else{
	            n2-=n1;
	        }
	    }
	  int gcd=n1;
	  System.out.println(gcd);
	    int lcm=(a*b)/gcd;
	    System.out.println(lcm);
}
}

````java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n1 = s.nextInt();
        int n2 = s.nextInt();
        s.close();
        
        int a = n1, b = n2; // Store original values for LCM calculation

        // Find GCD using Euclidean Algorithm (Modulo Method)
        while (n2 != 0) {
            int temp = n2;
            n2 = n1 % n2;
            n1 = temp;
        }

        int gcd = n1; // GCD is stored in n1 after loop ends
        int lcm = (a * b) / gcd; // Correct formula for LCM

        System.out.println("GCD: " + gcd);
        System.out.println("LCM: " + lcm);
    }
}
````

### Amicable Pair in Java
What is an Amicable Pair?
Two numbers (a, b) are called amicable numbers if the sum of proper divisors of a equals b, and the sum of proper divisors of b equals a.

````java
import java.util.*;
public class Main
{
    public static int SumofDiv(int n){
        int sum=0;
        for(int i=1;i<n;i++){
            if(n%i==0){
                sum+=i;
            }
        }
            return sum;
        
    }
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int n1=s.nextInt();
	    int n2=s.nextInt();
	    
	    int sum1=SumofDiv(n1);
	    int sum2=SumofDiv(n2);
	    
	    if(sum1==n2 && sum2==n1){
	        System.out.println("Amicable Pair");
	    }
	    else{
	        System.out.println("Not Amicable Pair");
	    }
	   
	
}
}
````

### Betrothed Pair in Java
What is a Betrothed Pair?
Two numbers (a, b) are called a betrothed pair if:
sum of proper divisors of a=b+1
sum of proper divisors of b=a+1

````java
import java.util.*;
public class Main
{
    public static int SumofDiv(int n){
        int sum=0;
        for(int i=1;i<n;i++){
            if(n%i==0){
                sum+=i;
            }
        }
            return sum;
        
    }
	public static void main(String[] args) {
	    Scanner s=new Scanner(System.in);
	    int n1=s.nextInt();
	    int n2=s.nextInt();
	    
	    int sum1=SumofDiv(n1);
	    int sum2=SumofDiv(n2);
	    
	    if(sum1==n2+1 && sum2==n1+1){
	        System.out.println("Betrothed Pair");
	    }
	    else{
	        System.out.println("Not Betrothed Pair");
	    }
	   
	
}
}

### 1. Square-Free Number
A square-free number is a number that is not divisible by any perfect square greater than 1.

Example:
✅ 10 → Factors: {1, 2, 5, 10} (No square factors)
❌ 12 → Factors: {1, 2, 3, 4, 6, 12} (Contains 4, which is 2²)


````java
import java.util.Scanner;

public class Main {
    public static boolean isSquareFree(int num) {
        for (int i = 2; i * i <= num; i++) {
            if (num % (i * i) == 0) { // Checking for square factor
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        s.close();

        if (isSquareFree(n)) {
            System.out.println("Square free number");
        } else {
            System.out.println("Not a square free number");
        }
    }
}

