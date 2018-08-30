// Created by orglce

import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
import javax.swing.text.html.HTMLDocument.RunElement;

public class SieveOfEratosthenes {

    // WARNING:
    // if the number is replaced with zero
    // (in the array) that means that it is not prime

    // My idea branch

	public static void main(String[] args) {

		  // user input of biggest number
		  Scanner in = new Scanner(System.in);
		  int MAX = in.nextInt();

		  // list of potencial prime numbers
		  List<Integer> prime_num = new ArrayList<Integer>();

		  //array of numbers from 0 to MAX
		  int[] numbers = new int[MAX+1];

		  // fill the array with numbers and delete the
		  // first number of the array, 1.
		for(int i = 1; i < numbers.length; i++)
		{
			  numbers[i] = i;
			  numbers[1] = 0;
		}

	  	for(int i = 1; i < numbers.length; i++)
		{

			// if the smallest number of the list to
		    // to the power of 2 is bigger than MAX
		    // than all the remaining numbers are prime.
	  		if (Math.pow(numbers[i], 2) > MAX)
	  		  	break;

			 // if the number isn't prime then
			 // remove all the following numbers who
			 // are marked as prime but are divisible with
			 // the last marked prime number
			 else if (numbers[i] != 0)
			 {
	  		     for(int j = 1; j < numbers.length; j++)
		  		 {
			  	   	 if (numbers[j] % i == 0)
					 {
				  		 if (j == i) { }
						 else { numbers[j] = 0; }
					 }
				 }
			 }
		}

		// add numbers from array which
		// are not equals to zero to the list
		for(int i = 1; i < numbers.length; i++)
		{
			if (numbers[i] != 0)
				prime_num.add(numbers[i]);
		}

		// print the prime numbers
		System.out.println(prime_num);
	}
}
