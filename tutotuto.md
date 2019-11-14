# WIX1002 Fundamentals of Programming
MUHAMMAD AFIQ AIMAN BIN MOHD SHUHAIMI
## Tutorial 7 File Input and Output
### 1. Write statements for each of the following
#### a. Store ten random integers within 0 to 1000 to a text file name integer.txt.
```
        try {
            PrintWriter p = new PrintWriter(new FileOutputStream("integer.txt"));
            int j=0;
            for(int i=0; i<=10; i++){
                Random rand = new Random();
                j =  rand.nextInt(1001);
                p.println(j);
            }
            p.close();
        }catch (IOException e){
            System.out.println("problem file with output");
        }
```
#### b. Read from the text file generated in a. Display all the integer and the largest integer.
```
try{
            Scanner s = new Scanner (new FileInputStream("integer.txt"));
            int input = s.nextInt();
            int max = 0;
            while(s.hasNextInt())
                System.out.println(s.nextInt());
                if (input>max){
                max=r;
                }
            }
            out.println("max number = "+max)
            s.close();
        }catch(FileNotFoundException e){
            System.out.println("file does not found");
        }
```
#### c. Store ten random integers within 0 to 1000 to a binary file name integer.dat.
```
        try {
            ObjectOutputStream out = new ObjectOutputStream (new FileOutputStream("integer.dat"));
            int max = 0;
            for(int i=1;i<=10;i++){
                Random rand = new Random();
                int r = rand.nextInt(1001);
                out.writeInt(r);
            }
            out.close();
        }catch (IOException e){
            System.out.println("problem file with output");
        }
```
#### d. Read from the binary file generated in a c. Display the all the integer and the average.
```
```
### 2. Correct the error for the following statements.
#### a. PrintWriter out = new PrintWriter(new FileOutputStream
#### ("d:\data\matrix.txt"));
```
a. PrintWriter out = new PrintWriter(new FileOutputStream
("d:/data/matrix.txt"));
```
#### b.
#### try {
####  PrintWriter out = new PrintWriter(new FileOutputStream("data.txt"));
#### out.close();
#### } catch (FileNotFoundException e) {
####  System.out.println("Problem with file output");
#### }
```
try {
PrintWriter out = new PrintWriter(new FileOutputStream("data.txt"));
out.close();
} catch (IOException e) {
System.out.println("Problem with file output");
}
```
#### c.
#### int num;
#### Scanner a = new Scanner(new FileInputStream("data.dat"));
#### num = a.readInt();
#### a.close();
```
int num;
Scanner a = new Scanner(new FileInputStream("data.dat"));
num = a.nextInt();
a.close();
```
#### d.
#### ObjectOutputStream o = new ObjectOutputStream (new
#### FileOutputStream("data.dat"));
#### o.print('A');
#### o.close();
```
ObjectOutputStream o = new ObjectOutputStream (new
FileOutputStream("data.dat"));
o.write('A');
o.close();
```
### 3. Write a program that convert a sentence into binary number (ASCII code 8 bit) and store it in a text file named data.txt. Then, read from the text file and display the sentence.
```
```
