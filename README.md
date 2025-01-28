# CodingExercisesWk2
a group coding exercise

Do this in either Java or Python. Your choice.

Ground Rules
- NO GOOGLING or Internet access
- The person with the puzzle tries their best to write it out in Java/Python
- only after their best guess is exhausted, the team can make suggestions
- once you think you got it, ask for another for the next person

#### Code Exercises

1. For loop from 100 to 5 by 5. Print index var for each step. 
   public void Hundoto5by5() {
   for (int i = 100; i >= 5; i -= 5) {
   System.out.print(i);
   }

2. For loop from 5 to 75 by 10. Print index variable on each value.
   void Fiveto75by10() {
   for (int i = 5; i <= 75; i += 10) {
   System.out.println(i);
   }
   }

3. Sum Integers from 9 to 17, print sum of integers
   void SumOf9to17(){
    int sum = 0;
    for (int i = 9; i<=17; i++){
        sum += i;
    } System.out.println(sum);
    }

4. Find and print the smallest integer in an array a = [9, 5, 6, 3, 8, 2, 4]; and print it.
    void FindSmallestIntinArray(int[] a){
    Arrays.sort(a);
    System.out.println(a[0]);
    }
    
5. Find largest integer in an array a = [9, 5, 6, 3, 8, 2, 4]; and print it.
   void FindLargestIntinArray(int[] a){
   Arrays.sort(a);
   System.out.println(a[a.length - 1]);
   }

6. Find and print index of first true element in an array of booleans a = [false, false, false, true, false];
    void PrintIndexOfFirstTrue(boolean[] a){
    for (int i = 0; i<a.length; i++){
        if (a[i]){
        System.out.println(i);
        break;
   }

7. Find and print index of first true element in an array of booleans (must use a while loop) a = [false, false, false, true, false];
    void PrintFirstTrueWhile(boolean[] a){
    int i = 0;
    while (!a[i]){
    i++;
    } System.out.println(i);
    }

8. add 5 to every element of an array of integers a = [9, 5, 6, 3, 8, 2, 4]
    void Add5(int[] a){
    for (int i = 0; i<a.length; i++){
    a[i] += 5;
    }
    }

9. divide each element of an array by 1.3; a = [0.5, 1.4, 6.7, 123.4 -34.6]
    void DivideBy(double[] a){
    for (int i = 0; i < a.length; i++){
    a[i]  = a[i] / 1.3;
    }
   }

10. raise each element of a double array to it's 3rd power and subtract the original element's value by 
the value divided by 3.0 a = [1.3, 5.4, 6.1, 1.0, 9.2];
    void RaiseandSubtract(double[] a){
    for (int i = 0; i < a.length; i++){
    a[i] = Math.pow(a[i], 3) - a[i]/3.0;
    }
    }


11. zero out a 4 by 6 integer array12. multiply each element of a 5 by 5 array of integers by 7
    void ZeroOut(int[][] array12){
    for (int i = 0; i < array12.length; i++) {
        for (int j = 0; j < array12[i].length; j++) {
        array12[i][j] = 0;
    }
    }
    
    void MultiplyBy5(int[][] array){
    for (int i = 0; i < array.length; i++){;
        for (int j = 0; j <array[i].length; j++){
        array[i][j] *= 7;
    }
    }

12. create a method `evenFalse` that takes a 5 by 5 array and produces a 5 by 5 array of booleans.
each element in the result should be true if the value in the argument array is even, 
else it's false.

    boolean[][] evenFalse(int[][] array){
    boolean[][] boolarray = new boolean[5][5];  
    for (int i = 0; i<array.length; i++){
        for (int j = 0; j<array[i].length; j++){
        if (array[i][j] % 2 == 0){
        boolarray[i][j] = true;
        } else boolarray[i][j] = false;
        }
        } return boolarray;
        }

13. create a method that takes two doubles and returns the first parameter raised to the 
second parameter's value

    double raiseFirstToSecond(double a, double b){
    return Math.pow(a, b);
    }

14. create a method that returns a boolean if the Object passed to it is a Fish or not

    boolean isFish(Object object){
    return object instanceof Fish;
    }

15. There is an object x which has a method (double)Balance(). Build an IF statement 
that prints "Paid Off" if the result of the balance call is less than of equal to 1.0, 
else it prints the balance as a Dollar figure (2 decimal places)

    void printBalance(){
    if (x.Balance() <= 1.0){
    System.out.println("Paid Off");
    } else {
    System.out.printf(%.2f, x.Balance());
    }
    }

16. Build a WHILE loop that turns on the heat if the thermo.getTemp() is less than 72.0 
else it turns on the A/C if thermo.getTemp() is greater that 76.0.

    void changeTemp(Thermo thermo){
    while(true){
    if (thermo.getTemp() < 72.0){
    System.out.println("Heat on");
    } else if (thermo.getTemp() > 76.0){
    System.out.println("AC on");
    } else {
    System.out.println("Just right");
    break;
    }
    }
    
17. Find a number greater than Pi in a double array, print number and its index.
    void greaterPi(double[][] array){
    for (int i = 0; i<array.length; i++){
        for (int j = 0; j<array[i].length; j++){
           if (array[i][j] > Math.PI) {
           System.out.println("Value " + array[i][j] + " is at index " + i + " and " + j + ".");
           }
        }
    }
    }
    
18. Given an array of objects (of class Xaction) w/nulls, sum all the values of the 
objects in the array, using Xaction::getValue() to get the object's value. 
Print the sum after the loop.

    void printSum(Xaction[] objects){
    int sum = 0;
    for (Xaction obj : objects){
    if (obj != null){
    sum += obj.getValue();
    } 
    }
    } System.out.println(sum);
    }

19. reverse an array of objects of type Xaction

    void reverseArray(Xaction[] objects){
    int start = 0;
    int end = objects.length - 1; 
    Xaction temp;
    while (start < end) {
    temp = objects[start]
    objects[start] = objects[end]
    objects[end] = temp;
    start += 1;
    end -= 1;
    }
    }

20. Print a 5's times table

    
21. detemine the hypotenuse of a 9 by 7 right triangle, assign it to a double

### Class Use
Use groups of 2-4, each group at a whiteboard (or online using a shared google doc), sketching out the answers.

#### FOR STUDYING for Assessment 1, step thru each of these, typing out a solution into the Solution.java file.

Some of you are asking for an exercise to work with very simple, small, snippets. 
This repo is good as it lets you work in a group, where you try to generate the code without googling anything.
Set up this way, as a group.

Use your Crew members as the group.
All gather around a google doc over zoom or discord.
allow all crew to access the same document.

Each taking a turn, try to create the code without googling anything. 
Allow the crew member to get their best effort finished BEFORE anyone says anything.
Then, each crew can make comments.
The idea is for each of you to do your best in writing out a solution before anyone comments, and giving you the chance to discuss your solution when it's done.

Also, be sure the solution is right! You should, at this point, have within a crew the ability to look at a piece of code and decide whether it is right or not!
So everyone should agree, "yes, that's right, that will work."

