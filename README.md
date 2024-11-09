# lab1complete

**LAB TASK 1:**

**1.	Write a program that initialize five different strings using all the above-mentioned ways, i.e., 
  a) string literals 
b)	new keyword 
also use intern method and show string immutability.**

package com.mycompany.lab1labtask1;

public class Lab1labtask1 {

    public static void main(String[] args) {
        String A1="Aijaz";
        String A2="Mobariz";
        String A3="Aijaz";
        String A4=new String("Mobariz");
        String A5=new String("Aijaz").intern();
        
        System.out.println(A1==A3);
        System.out.println(A2==A4);
        System.out.println(A1==A5);
    }
}


**LAB TASK 2:**

**2. Write a program to convert primitive data type Double into its respective wrapper object.**

package com.mycompany.lab1labtask2;
public class Lab1labtask2 {

    public static void main(String[] args) {
        double Num1=786;
        Double Num2=Num1;
        System.out.println(Num2);
    }
}


**LAB TASK 3:**

**3. Write a program that initialize five different strings and perform the following operations. 
      a) Concatenate all five stings. 
      b) Convert fourth string to uppercase. 
c)	Find the substring from the concatenated string from 8 to onward **


package com.mycompany.lab1labtask3;

public class Lab1labtask3 {

    public static void main(String[] args) {
        String A1 = "Aijaz";
        String A2 = "Wasay";
        String A3 = "Talha";
        String A4 = "Mobariz";
        String A5 = "Hassam";

        String concatenatedString =A1+" ," + A2+" ,"+ A3 +" ,"+ A4 +" ,"+A5;
        System.out.println("Concatenated String:- " + concatenatedString);


        String upperCaseStr4 = A4.toUpperCase();
        System.out.println("Fourth String in Uppercase:- " + upperCaseStr4);

        String Concatinate = concatenatedString.substring(8);
        System.out.println("Substring from index 8 onwards:- " + Concatinate);
        
    }
}

**LAB TASK 4:**

**4. You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. 
If a string is longer than the other, append the additional letters onto the end of the merged string. Return the merged string**

package com.mycompany.lab1labtask4;

public class Lab1labtask4 {

    public static String mergeStrings(String word1, String word2) {
        StringBuilder sb = new StringBuilder();

        int maxLength = Math.max(word1.length(), word2.length());
        for (int i = 0; i < maxLength; i++) {
            if (i < word1.length()) {
                sb.append(word1.charAt(i));
            }
            if (i < word2.length()) {
                sb.append(word2.charAt(i));
            }
        }

        return sb.toString();
    }

    public static void main(String[] args) {
        String word1 = "Aijaz";
        String word2 = "Qadri";
        String mergedString = mergeStrings(word1, word2);
        System.out.println(mergedString);
    }
}


**LAB TASK 5:**

**5. Write a Java program to find the minimum and maximum values of Integer, Float, and Double using the respective wrapper class constants.**


package com.mycompany.lab1labtask5;

public class Lab1labtask5 {

    public static void main(String[] args) {
      
        int I1 = 10;
        int I2 = 20;
        
        float F1 = 10.5f;
        float F2 = 20.3f;

        double D1 = 10.5;
        double D2 = 20.3;
        
        int minInt = Math.min(I1, I2);
        int maxInt = Math.max(I1, I2);
        System.out.println("Minimum Integer value: " + minInt);
        System.out.println("Maximum Integer value: " + maxInt);

        float minFloat = Math.min(F1, F2);
        float maxFloat = Math.max(F1, F2);
        System.out.println("Minimum Float value: " + minFloat);
        System.out.println("Maximum Float value: " + maxFloat);

        double minDouble = Math.min(D1, D2);
        double maxDouble = Math.max(D1, D2);
        System.out.println("Minimum Double value: " + minDouble);
        System.out.println("Maximum Double value: " + maxDouble);
    }
}

**HOME TASK 1:**

**1.	Write a JAVA program to perform Autoboxing and also implement different methods of wrapper class.**

	 
package com.mycompany.lab1hometask1;

public class Lab1hometask1 {

    public static void main(String[] args) {
        int I = 10;
        Integer integer = I;
        System.out.println(integer);

        char c = 'a';
        Character character = c;
        System.out.println(character);
        
        Integer int1 = new Integer(20);
        Integer int2 = new Integer(15);
        
        System.out.println("Int1 is greater than Int2: " + int1.compareTo(int2));
        
        boolean isEqual = int1.equals(int2);
        System.out.println("Integer1 is equal to Integer2: " + isEqual);
        
    }
}

**HOME TASK 2:**

**2.	Write a Java program to count the number of even and odd digits in a given integer using Autoboxing and Unboxing.**

package com.mycompany.lab1hometask2;

import java.util.*;
public class Lab1hometask2 {

    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter an integer: ");
        int number = scanner.nextInt();
        
        Integer evenCount = 0; 
        Integer oddCount = 0;        
  
        while (number != 0) {
            int digit = number % 10; 
            
            if (digit % 2 == 0) {
                evenCount++; 
            } else {
                oddCount++; 
            }
            
            number /= 10; 
        }   
        System.out.println("Number of even digits: " + evenCount);
        System.out.println("Number of odd digits: " + oddCount);   
    }
}


**HOME TASK 3:**

**3. Write a Java program to find the absolute value, square root, and power of a number using Math class methods, while utilizing Autoboxing and Wrapper classes.**

package com.mycompany.lab1hometask3;
import java.util.*;
public class Lab1hometask3 {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        double number = sc.nextDouble();

  
        double absoluteValue = Math.abs(number);
        double squareRoot = Math.sqrt(number);
        double power = Math.pow(number, 2);

        if (number < 0) {
            System.out.println("Square root is not possible for negative numbers.");
        } else {
            System.out.println("Square root: " + squareRoot);
        }

        System.out.println("Absolute value: " + absoluteValue);
        System.out.println("Power: " + power);
    }
}

**HOME TASK 4:**

**4.	Write a Java program to reverse only the vowels in a string.**


package com.mycompany.lab1hometask4;
import java.util.*;

public class Lab1hometask4 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String s = scanner.nextLine();
        char[] chars = s.toCharArray();
        String vowels = "AEIOUaeiou";
        int left = 0, right = s.length() - 1;
        while (left < right) {
            if (vowels.indexOf(chars[left]) == -1) {
                left++;
            } else if (vowels.indexOf(chars[right]) == -1) {
                right--;
            } else {
                char temp = chars[left];
                chars[left] = chars[right];
                chars[right] = temp;
                left++;
                right--;
            }
        }
        System.out.println("After reversing vowels: " + new String(chars));

    }
}


**HOME TASK 5:**

**5. Write a Java program to find the longest word in a sentence.**

package com.mycompany.lab1hometask5;

import java.util.Scanner;
public class Lab1hometask5 {

    public static void main(String[] args) {
       Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a sentence: ");
        String sentence = scanner.nextLine();

        String[] words = sentence.split(" ");

        String longestWord = "";
        for (String word : words) {
            if (word.length() > longestWord.length()) {
                longestWord = word;
            }
        }

        System.out.println("The longest word is: " + longestWord);
    }
}
