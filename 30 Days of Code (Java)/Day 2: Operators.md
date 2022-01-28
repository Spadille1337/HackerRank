**Objective**

In this challenge, you will work with arithmetic operators. Check out the Tutorial tab for learning materials and an instructional video.

**Task**

Given the meal price (base cost of a meal), tip percent (the percentage of the meal price being added as tip), and tax percent (the percentage of the meal price being added as tax) for a meal, find and print the meal's total cost. Round the result to the nearest integer.

**Example**

meal_cost = 100

tip_percent = 15

tax_percent = 8

A tip of 15% * 100 = 15, and the taxes are 8% * 100 = 8. Print the value 123 and return from the function.

**Function Description**
Complete the solve function in the editor below.

solve has the following parameters:

- int meal_cost: the cost of food before tip and tax

- int tip_percent: the tip percentage

- int tax_percent: the tax percentage

Returns The function returns nothing. Print the calculated value, rounded to the nearest integer.

Note: Be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result.

**Input Format**

There are 3 lines of numeric input: 

The first line has a double, meal_cost (the cost of the meal before tax and tip). 

The second line has an integer, tip_percent (the percentage of meal_cost being added as tip).

The third line has an integer, tax_percent (the percentage of meal_cost being added as tax).

**Sample Input**
```
12.00
20
8
```
**Sample Output**
```
15
```
**Explanation**

Given:

meal_cost = 12

tip_percent = 20

tax_percent = 8

Calculations:

tip = 12 and (12/100)*20 = 2.4

tax = 8 and (8/100)*20 = 0.96

total_cost = meal_cost + tip + tax = 12+2.4+0.96 = 15.36

round(total_cost) = 15

We round total_cost to the nearest integer and print the result, 15.

```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

    public static void solve(double meal_cost, int tip_percent, int tax_percent) {
     System.out.println(Math.round(meal_cost + (tip_percent*meal_cost)/100 + (tax_percent*meal_cost)/100));
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        double meal_cost = Double.parseDouble(bufferedReader.readLine().trim());

        int tip_percent = Integer.parseInt(bufferedReader.readLine().trim());

        int tax_percent = Integer.parseInt(bufferedReader.readLine().trim());

        Result.solve(meal_cost, tip_percent, tax_percent);

        bufferedReader.close();
    }
}
```
