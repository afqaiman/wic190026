# WIX1002 Fundamentals of Programming
###### MUHAMMAD AFIQ AIMAN BIN MOHD SHUHAIMI (WIC190026)
## Tutorial 5 Arrays
### 1. Write statements for each of the following
#### a. Declare an array that used to store 12 floating point numbers.
```
float[]arr = new float[11];
```
#### b. Initialize an array that used to store the value of A to E.
```
char[] letter = new char[4];
```
#### c. Declare an array that used to store 100 students name.
```
int[] student = new int[99];
```
#### d. Declare an array for a table with 6 rows 2 columns that used to store integer value.
```
int[][] value = new int[6][2];
```
#### e. Initialize an array with the following value:
```
int[][] arr = {{6,9},{2,5},{4,6}};
```
#### f. After initialize the array, modify the value of the above array:
```
int[][] arr = {{6,9},{2,4},{3,7}};
```
#### g. Display all the values of an array name contact in separate lines.
```
```
### 2. Correct the error for the following statements.
#### a.
#### String[] code = {'AAA', 'AAB', 'AAC', 'AAD'};
```
String[] code = {"AAA", "AAB", "AAC", "AAD"};
```
#### b.
#### int[] num = new num[10];
#### for(int k=0; k<=num.length(); k++)
#### sum+=num;
```
int[] num = new int[10];
for(int k=0; k<=num.length(); k++)
 sum+=num;
```
### c.
#### int [][]t = new int[3][];
#### t[1][2] = 5;
```
int [][]t = new int[3][];
t[1][] = 5;
```
#### d.
#### int i=4;
#### int []score = new int[5];
#### score [1] = 78;
#### score[++i] = 100;
```
int i=4;
int []score = new int[5];
score [1] = 78;
score[++i] = 100;
```
### 3. Determine the values of each element of array marks. Assume the array was declaredas:
#### int i = 0, j = 1;
#### marks[i] = 12;
#### marks[j] = marks[i] + 19;
#### marks[j-1] = marks[j] * marks [j];
#### marks[j*3] = marks[i+1];
#### marks[++j] = marks[i]%5;
#### marks[2*j] = marks[j-1];
```
 marks[0] = 12;
 marks[1] = 31;
 marks[0] = 372;
 marks[3] = 12;
 marks[2] = 2;
 marks[2] = 30;
```
### 4. Write the statements that display the number of occurrence of the word "the" (case sensitive) in a string array name sentence.
```

```
### 5. Write the statements that display the string array name sentence in reverse order. Each string element must be displayed in reverse order as well.
```
        System.out.println("Enter string to reverse:");
        
        Scanner scan = new Scanner(System.in);
        String word = scan.nextLine();
        String reverse = "";
        
        
        for(int i = word.length() - 1; i >= 0; i--)
        {
            reverse = reverse + word.charAt(i);
        }
        
        System.out.println("Reversed string is:");
        System.out.println(reverse);
```
### 6. Write the statements that generate 1 random integer within 0 – 255. Convert the number to binary and store the bit into an 8 bit array. Then, display the binary number.
```
        Random rand = new Random();
        int num = rand.nextInt(254);
        System.out.println("generate random number:"+num);
        int[] arr = new int[8]; 
        int i = 0; 
        while (n > 0) { 
            arr[i] = num % 2; 
            num = num / 2; 
            i++; 
        } 
        for (int j = i - 1; j >= 0; j--){ 
            System.out.print(arr[j]);
        }
```
