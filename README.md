# Palindrome-or-not-

package palindromes;

import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.PrintWriter;
import java.util.Scanner;

public class main {

	public static void main(String[] args) throws Throwable {
		// TODO Auto-generated method stub

		Scanner in = new Scanner(new FileReader("palin.in"));;
		PrintWriter out = new PrintWriter (new FileWriter("palin.out"));

		int k;
		k = Integer.parseInt(in.nextLine());

		for(int i = 0; i < k; i ++){

			String N = in.nextLine();

			if(isPalin(N) == true){
				out.println("Yes");

			}else{out.println("No");


			}

		}

		
		out.close();
	}


	public static boolean isPalin(String name){

		name = name.toLowerCase();

		name = name.replaceAll("[^a-z]", "");

		StringBuilder s = new StringBuilder(name);

		if(s.reverse().toString().equals(name)){

			return true;
		}

		return false;

	}
}
