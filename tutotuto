# WIX1002 Fundamentals of Programming
###### MUHAMMAD AFIQ AIMAN BIN MOHD SHUHAIMI (WIC190026)
## Tutorial 4 Flow of Control (Repetition)
### 1. Write statements for each of the following
#### a. Find the largest integer n so that n^3 is less than 2000.
```
int n,total=0;
for(n=0;(n*n*n)<2000;n++){
total=n*n*n;
System.out.printf("number:%d\t%d*%d*%d=%d\n",n,n,n,n,total);
}
System.out.printf("largest n is %d which is %d*%d*%d=%d",n,n,n,n,total);
```
#### b. Display the square number of the first twelve integers starting from 1.
```
int i,square=0;
for(i=1;i<=12;i++){
square=i*i;
System.out.printf("number:%d\t%d*%d=%d",i,i,i,square);
}
```
#### c. Display a 4-by-5 matrix using random number within 0 to 100.
```
int v,h,number;
Random rand = new Random ();
for(v=0;v<5;v++){
  for(h=0;h<4;h++){
    number = rand.nextInt(101);
    System.out.printf("%d\t",number);
  }  
System.out.println("\n");
}
```
#### d. Compute the sum of numbers from 1 to a given number.
```
int n,number,total=0;
System.out.println("Enter a number:");
Scanner scan = new Scanner(System.in);
number = scan.nextInt();                
for(n=1;n<=number;n++){
  total=total+n;
}
System.out.printf("the sum of numbers from 1 to %d is %d",number,total);
```
#### e. Compute the sum of the series: 1/25+2/24+3/23 … + 25/1 in two decimal places.
```
```
### 2. Correct the error for the following statements.
#### a.
#### for (x = 10; x > 0; x++)
#### sum += x;
```
for (x = 0; x < 10; x++){
sum += x;
}
```
#### b.
#### do
#### x += 2;
#### y += x;
#### System.out.println(x + " and " + y);
#### while (x < 100)
```

```
#### c.
#### for ( x==1, y==20; x < y, x++, y-=2);
#### System.out.println(x & " " & y);
```
for ( x=1, y=20; x < y; x++, y-=2){
System.out.printf("x=%d & y=%d\n",x,y);
}
```
#### d.
#### i =1;
#### while(i<10) {
#### if (i==10)
#### System.out.println("Program End");
#### }
```
int i=1;
while(i<10) {  
 i++;
 if (i==10){
 System.out.println("Program End");
 }
```
### 3. Write the statements that display the first ten values of the Fibonacci sequence. Given the formula f1 = 1, f2 =1, fn = fn-1 + fn-2.
```
int b=1,s=1,total=0,counter,number=0;
for(counter=3;counter<13;counter++){
    total=s+b;
    number++;
    System.out.printf("no%d\tf%d\t%d+%d=%d\n",number,counter,s,b,total);
    b=s;
    s=total;              
}
```
### 4. Write the statements that display the string in reverse order. (use String.length() to get the length of the string)
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
