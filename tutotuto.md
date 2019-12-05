# WIX1002 Fundamentals of Programming
#####  MUHAMMAD AFIQ AIMAN BIN MOHD SHUHAIMI - WIC190026
#####  Tutorial 9 Inheritance
##  1. Write statements for each of the following

###  a. Write a static method compare that return true if two objects parameter (Student s, Teacher t) are belongs to the same class. Otherwise return false.
```
public class compare {

    public static void main(String[] args) {
    Teacher t = new Teacher();
    Student s = new Student();
    boolean result = s.getClass().equals( t.getClass());  
        System.out.println(result);
    }    
}
```
###  b. Write a static method isClass that return true if the object parameter (Students) is belong to any descendent class of Person. Otherwise return false.
```
```
##  2. Define a class Organism. The class contains the initial size of the organism and the growth rate. Create a constructor to initialize the instance variables. Then, define a class Animal. Animal is an organism that has extra instance variable which is the amount of eating need. Create a constructor to initialize the instance variable and a method to display the Animal instance variables.
```
public class Organism {
    private int size;
    private int growRate;
    
    public Organism() {
        size = 1;
        growRate = 5;
    }
    
    public Organism(int size, int growRate) {
        this.size = size;
        this.growRate = growRate;
    }

    public int getSize() {
        return size;
    }

    public void setSize(int size) {
        this.size = size;
    }

    public int getGrowRate() {
        return growRate;
    }

    public void setGrowRate(int growRate) {
        this.growRate = growRate;
    }   
}
*********************************************************************************************************
public class Animal extends Organism {
    private int eating;
    
    public Animal() {
        eating = 10;
    }

    public Animal(int eating) {
        this.eating = eating;
    }

    public int getEating() {
        return eating;
    }

    public void setEating(int eating) {
        this.eating = eating;
    }
    
    void print(){
        System.out.println("eating="+(this.eating));
        System.out.println("size="+(this.getSize()));
        System.out.println("Grow rate="+(this.getGrowRate()));
    }
    
}
```
##  3. Define a class PaySystem. The class consists of the payrate per hour and the number of hours. The class also contains a method to return the total pay for a given amount of hours and a method to display the total payment. Derive a class RegularPay from PaySystem that has a constructor and did not override any base methods. Derived a class SpecialPay from PaySystem that override the base method and return the total pay plus 30% commission.
```
public class PaySystem {
    protected double payRateHour;
    protected int numberHours;
    double total;

    public PaySystem() {
        payRateHour = 0.0;
        numberHours = 0;
        total = 0.0;
    }
    
    public PaySystem(double payRateHour, int numberHours) {
        this.payRateHour = payRateHour;
        this.numberHours = numberHours;
    }

    public double getPayRateHour() {
        return payRateHour;
    }

    public void setPayRateHour(double payRateHour) {
        this.payRateHour = payRateHour;
    }

    public int getNumberHours() {
        return numberHours;
    }

    public void setNumberHours(int numberHours) {
        this.numberHours = numberHours;
    }
    
    public void totalPay(){
        total = (this.numberHours)*(this.payRateHour);
    }
    
    public void totalPayment(int n){
        System.out.println("total payment = RM "+total);
    }
}
************************************************************************
public class RegularPay extends PaySystem{

    public RegularPay() {
    }

    public RegularPay(double payRateHour, int numberHours) {
        super(payRateHour, numberHours);
    }
    
}
***********************************************************************
public class SpecialPay extends PaySystem {

    public SpecialPay() {
    }

    public SpecialPay(double payRateHour, int numberHours) {
        super(payRateHour, numberHours);
    }
    
    @Override
    public void totalPay(){
        double total = 0.0;
        total = (payRateHour*numberHours)*1.3;
        System.out.println("total payment = "+total);
    }
}

```
##  4. Define a class PurchaseSystem. The class consists of product code, unit price, quantity and total price. Besides the class consists of a method to compute the total price and a display method. Derived a class SugarPurchase from PurchaseSystem. This new class add a sugar weight attributed and override the method to compute the total price as unit price*quantity*sugar weight. 
```
public class PurchaseSystem {
    private String code;
    protected int quantity;
    protected double price;
    protected double total;
    
    public PurchaseSystem() {
        code = "";
        quantity = 0;
        price = 0.0;
        total = 0.0;
    }

    public PurchaseSystem(String code, int quantity, double price, double total) {
        this.code = code;
        this.quantity = quantity;
        this.price = price;
        this.total = total;
    }

    public String getCode() {
        return code;
    }

    public void setCode(String code) {
        this.code = code;
    }

    public int getQuantity() {
        return quantity;
    }

    public void setQuantity(int quantity) {
        this.quantity = quantity;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public double getTotal() {
        return total;
    }

    public void setTotal(double total) {
        this.total = total;
    }
    

    public void totalPrice(){
        this.total=this.quantity*this.price;
    }
    public void display(){
        System.out.println("total price "+this.total); 
    }
}

********************************************************************************
public class SugarPurchase extends PurchaseSystem {
    private double weight;
            
    public SugarPurchase() {
        weight = 0.0;
    }
    public SugarPurchase(double weight) {
        this.weight = weight;
    }

    public double getWeight() {
        return weight;
    }

    public void setWeight(double weight) {
        this.weight = weight;
    }

    public SugarPurchase(double weight, String code, int quantity, double price, double total) {
        super(code, quantity, price, total);
        this.weight = weight;
    }
    
    public void totalPrice(){
        this.total = this.price*this.weight*this.quantity;
    }
    public void display(){
        System.out.println("total price : "+this.total);
    }
}

```
