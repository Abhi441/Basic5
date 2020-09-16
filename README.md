# Basic5
Pattern number and Stars

Take as input N, a number. Print the pattern as given in output section for corresponding input.

Input Format
Enter value of N

Constraints
Output Format
All numbers and stars are Space separated

Sample Input
5
Sample Output
1 2 3 4 5
1 2 3 4 * 
1 2 3 * * *
1 2 * * * * *
1 * * * * * * *
Explanation
Catch the pattern for the corresponding input and print them accordingly.


Solution
import java.util.*;
public class Main {
    public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int ndt = n;
		int nst = 0;
		// row
		int row = 1;
		while(row <= n){
			// work
			int cdt = 1;
			while(cdt <= ndt){
				System.out.print(cdt +"\t");
				cdt++;
			}
			int cst = 1;
			while(cst <= nst){
				System.out.print("*" +"\t");
				cst++;

			}
			//preparation
            System.out.println();
			row = row + 1;
			ndt = ndt - 1;
			if(row == 2){
				nst = nst + 1;
			}
			else
            nst = nst + 2;
			
		}
		

    }
}
