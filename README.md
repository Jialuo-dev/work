# work
package pro;
import java.util.Scanner;


public class Account {

	public static void main(String[] args) {
	    int number1 = (int)(Math.random()*10);
	    int number2 = (int)(Math.random()*10);
    
	    //Create a Scanner
	    Scanner input = new Scanner(System.in);
	    
	    
	    
	    System.out.print(
	      "What is"+number1+"+"+number2 +"?");
	    
	    int i=0;
	    int[] answer=new int[100];
	    while( input.hasNextInt()){
		    answer[i]=input.nextInt();
		    int j=i;
		    for(j=0;j<i;++j){
		    	if(answer[i]==answer[j]){
		    		System.out.print("You already entered"+answer[i]);
		    		break;
		    	}
		    	
		    }
		    
		    i++;
	    }
	    if(number1 +number2!=answer[i]){
	    	System.out.print("Wrong answer. Try again.What is"
	    			+number1+"+"+number2+"?");
	    	answer[i+1] = input.nextInt();
	    }
	    
	    
	    System.out.println("You got it!");
	}

}
