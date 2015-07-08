# comcast
# comcast code challenge/Question 3 

public class Taxperson
{
  public double itemcost(String item ,String itemtype, double cost)
  {
     double totalcost;  
     if (itemtype = "necessaryitem")
     {
      totalcost = cost+ (.01 *cost);
     }
     else if (itemtype = "luxuryitem")
    {
       totalcost = cost+(.09*cost);
    }
     
     return totalcost;   
        
  }
}

/*
Calling the above function in main  method
*/

import java.io.*;
import java.util.Scanner;

public static void main (String[] args){
Scanner  UserInput = new Scanner(System.in);
String Item;
String Itemtype;
Double cost,totalcost;
System.out.print("Enter the item");
Item = UserInput.next();
System.out.print("Enter the itemtype");
Itemtype = UserInput.next();
System.out.print("Enter the cost");
cost = UserInput.nextDouble();


Taxperson Calculate = new Taxperson();
Totalcost = Calculate.itemcost(Item,Itemtype,cost);
System.out.println("Total cost after tax is $" + Double.toString(Totalcost);
}

/*
Unit Test Method for testing above TaxPerson
*/

@Test
Public Void testTaxpersonfornecessaryitem()
{
String item,itemtype;
Double cost;
item = "apple";
itemtype = "necessaryitem";
cost = 1;
Taxperson Calculate = new Taxperson();
assertequals(1.01 = Calculate.itemcost(item,itemtype,cost));
}

@Test
Public Void testTaxpersonforluxuryitem()
{
String item,itemtype;
Double cost;
item = "Luxury Car";
itemtype = "luxuryitem";
cost = 20000;
Taxperson Calculate = new Taxperson();
assertequals(21800 = Calculate.itemcost(item,itemtype,cost));
}

@Test
Public Void testnegativeTaxpersonfornecessaryitem()
{
String item,itemtype;
Double cost;
item = "apple";
itemtype = "necessaryitem";
cost = 1;
Taxperson Calculate = new Taxperson();
assertfalse(1.07 = Calculate.itemcost(item,itemtype,cost));
}
