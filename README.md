# 20.STRING-OPERATIONS
package stringoperationsenhanced;
import java.util.Scanner;


public class Stringoperationsenhanced {

    public static void main(String[] args) {
        
        try (Scanner scanner = new Scanner (System.in)) {
            System.out.println("enter the first string:");
            String str1=scanner.nextLine();
            System.out.println("enter the second string:");
            String str2=scanner.nextLine();
            System.out.println("\n choose a string function");
            System.out.println("1.find length");
            System.out.println("2.convert to upper case");
            System.out.println("3.convert to lower case");
            System.out.println("4.reverse the string");
            System.out.println("5.concatenate the string");
            System.out.println("6.compare the string");
            System.out.println("7.check if substring exists");
            System.out.println("8.replace a character");
            System.out.println("9.find character at index");
            System.out.println("10.split the string");
            System.out.println("11.trim whitespace");
            System.out.println("12.check if string is empty");
            System.out.println("13.convert to character array");
            System.out.println("14.exit");
            
            int choice;
            do{
                System.out.println("\nEnter your choice");
                choice=scanner.nextInt();
                scanner.nextLine();
                switch(choice){
                    case 1:
                        System.out.println("lenght of first string"+str1.length());
                        System.out.println("lenght of second string"+str2.length());
                        break;
                    case 2:
                        System.out.println("first string in upper case:"+str1.toUpperCase());
                        System.out.println("second string in upper case:"+str2.toUpperCase());
                        break;
                    case 3:
                        System.out.println("first string in lower case:"+str1.toLowerCase());
                        System.out.println("second string in lower case:"+str2.toLowerCase());
                        break;
                    case 4:
                        System.out.println("Reversed first string: "+new StringBuilder(str1).reverse());
                        System.out.println("reversed second string: "+new StringBuilder(str2).reverse());
                        break;
                    case 5:
                        System.out.println("concatenated string is:"+str1.concat(str2));
                        break;
                    case 6:
                        int comparision = str1.compareTo(str2);
                        if(comparision==0) {
                            System.out.println("the strings are equal");
                        } else if(comparision > 0) {
                            System.out.println("the first string is lexicographically greater");
                        }else {
                            System.out.println("the second string is lexicographically greater");
                        }
                        break;
                    case 7:
                        System.out.println("enter the substring to check in the first string");
                        String substring = scanner.nextLine();
                        System.out.println("the substring exists in the first string"+str1.contains(substring));
                        break;
                    case 8:
                        System.out.println("enter the character to replace: ");
                        char oldchar = scanner.next().charAt(0);
                        System.out.println("enter the new character");
                        char newchar = scanner.next().charAt(0);
                        System.out.println("First string after replacement: "+ str1.replace(oldchar, newchar));
                        System.out.println("Second string after replacement: "+ str2.replace(oldchar, newchar));
                        break;
                    case 9:
                        System.out.print("Enter the index to find the character (0-based):");
                        int index = scanner.nextInt();
                        try {
                            System.out.println("Character at index "+ index + " in first string: "+ str1.charAt(index));
                            System.out.println("Character at index "+ index + "in second string: " + str2.charAt(index)); 
                        } catch (IndexOutOfBoundsException e) {
                            System.out.println("Index out of range!");
                        }
                        break;
                    case 10:
                        System.out.print("Enter the delimiter to split the first string: ");
                        String delimiter = scanner.nextLine();
                        String[] parts = str1.split(delimiter);
                        System.out.println("First string split into parts:");
                        for (String part : parts) {
                            System.out.println(part);
                        }
                        break;
                    case 11:
                        System.out.println("First string after trimming: [" + str1.trim() + "]");
                        System.out.println("Second string after trimming: [" + str2.trim() + "]");
                        break;
                    case 12:
                        System.out.println("Is the first string empty? "+ str1.isEmpty());
                        System.out.println("Is the second string empty? " + str2.isEmpty());
                        break;
                    case 13:
                        System.out.println("Character array of first string:");
                        for (char c : str1.toCharArray()) {
                            System.out.print(c + "");
                        }
                        System.out.println();
                        break;
                    case 14:
                        System.out.println("Exiting...");
                        break;
                    default:
                        System.out.println("Invalid choice. Please try again.");
                }
            } while (choice != 14);
        }
     }
}

O/P
Enter the first string:
Akshaya
Enter the second string:
Vetrivel
/n Choose a string operation:
1.Find Lenth
2.Convert to uppercase
3.Convert to lowercase
4.Reverse the string
5.Concatenate the strings
6.Compare the strings
7.Check if substring exists
8.Replace a character
9.Find character at index
10.Split the string
11.TRim white spaces
12.Check if string is empty
13.Concert to cahrater array
14.Exit
/nEnter your choice:

1
Lenth of frist string:7
Lrngth of the second string:8
/nEnter your choice:
2
Frist string in uppercaseAKSHAYA
Second string in uppercaseVETRIVEL
/nEnter your choice:
3
Frist string in lowercaseakshaya
Second strin g in lowercasevetrivel
/nEnter your choice:
4
Frist dtring Reversed:ayahskA
Second String reversed:levirteV
/nEnter your choice:
5
Concatenated String :AkshayaVetrivel
/nEnter your choice:
6
First string is lexicologically greater
/nEnter your choice:
7
Enetr a substring to check the first string
s
Substring exist in the first string:true
/nEnter your choice:
8
Enter the character to replace:
s
Enter the new character:
i
The string after the replacemetAkihaya
The second string after the replacement:Vetrivel
/nEnter your choice:
10
Enter the delimetre to split the frist string:
h
First string split into parts:
Aks
aya
/nEnter your choice:
11
Frist string after trimming:[Akshaya]
Second string after trimming:[Vetrivel]
/nEnter your choice:
12
Is the frist string Empty?false
Is the second string Empty?false
/nEnter your choice:
13
Charater aaray if first string:
A 
k 
s 
h 
a 
y 
a 

/nEnter your choice:
14
Exiting........
BUILD SUCCESSFUL (total time: 1 minute 55 seconds)


        
