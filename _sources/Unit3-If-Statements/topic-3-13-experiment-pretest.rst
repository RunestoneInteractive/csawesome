.. qnum::
   :prefix: exp-1-
   :start: 1

Pretest
==============================

.. poll:: most-common-pretest-gym
    :option_1: A
    :option_2: B
    :option_3: C 
    :option_4: D 
    :results: instructor
    
    <b>Gym Membership Discount</b>
    <br>
    A gym offers discounts on membership fees based on age and frequency of visits per week. The parameter <code>age</code> is the person's age in years, and <code>visitsPerWeek</code> is the average number of visits per week. The result is the discount percentage encoded as an int. The conditions are:
    <ul>
    <li>If the person is 60 years old or older and visits the gym 3 times or more per week, they get a 30% discount.</li>
    <li>If the person is less than 60 years old and visits the gym 5 times or more per week, they get a 15% discount.</li>
    <li>If neither condition is met, and the person is between 18 and 25 years old (inclusive), they get a 5% discount.</li>
    <li>Otherwise, there is no discount.</li>
    </ul>
    Select the correct code for this problem.
    <b>Only the highlighted lines are different in each option.</b>
    <br>

    <img src="https://i.postimg.cc/P5WhF5V8/gym.png" width="1000">


.. poll:: most-common-pretest-lucky
    :option_1: A
    :option_2: B
    :option_3: C 
    :option_4: D 
    :results: instructor
    
    <b>Lucky Number</b>
    <br>
    An old witch told us a person's lucky number is determined based on the date and time of their birth. The parameters are <code>day</code> and <code>hour</code>. The <code>day</code> is the day of birth (from 1 to 31), and the <code>hour</code> is the hour of birth (from 0 to 23). According to her, the lucky number is calculated as follows:
    <ul>
    <li>If the day is even and the hour is greater than 12, the lucky number is the sum of the day and the hour.</li>
    <li>If the day is even and the hour is less or equal than 12, the lucky number is the product of the day and the hour.</li>
    <li>If the day is odd and the hour is greater than 10, the lucky number is the hour minus the day.</li>
    <li>If the day is odd and the hour is less or equal than 10, the lucky number is the day minus the hour.</li>
    </ul>
    Select the correct code for this problem.
    <b>Only the highlighted lines are different in each option.</b>

    <br>
    <img src="https://i.postimg.cc/SNWCVW4L/lucky.png" width="1000">

.. activecode:: most-common-pretest-vacation
   :language: java
   :autograde: unittest

   You are selecting a vacation package based on weather and budget. The parameter weather represents average weather score (from 0 to 10, where 10 is perfect weather), and budget represents available budget in thousands of dollars. The result is the package type encoded as an int value with 0=no package, 1=standard, 2=premium, 3=luxury. The conditions are:

   * If the weather score is 9 or more, and the budget is 5 or more, the result is 3 (luxury).
   * If the weather score is between 6 and 8 (inclusive), and the budget is 3 or more (inclusive), the result is 2 (premium).
   * If the weather score is between 3 and 5 (inclusive), and the budget is 1 or more (inclusive), the result is 1 (standard).
   * Otherwise, you decide not to go on vacation, so the result is 0 (no package).

   .. table::
      :name: vacation-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``selectPackage(9, 5)``                            | ``3``           |
      +----------------------------------------------------+-----------------+
      | ``selectPackage(7, 3)``                            | ``2``           |
      +----------------------------------------------------+-----------------+
      | ``selectPackage(4, 1)``                            | ``1``           |
      +----------------------------------------------------+-----------------+
      | ``selectPackage(2, 5)``                            | ``0``           |
      +----------------------------------------------------+-----------------+
      | ``selectPackage(8, 0)``                            | ``0``           |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class VacationPackageSelection 
   {
      public static int selectPackage(int weather, int budget)
      {
         // Your Code Here //
      }

      public static void main(String[] args)
      {
         System.out.println(selectPackage(9, 5));  // 3
         System.out.println(selectPackage(7, 3));  // 2
         System.out.println(selectPackage(8, 6));  // 2
         System.out.println(selectPackage(4, 1));  // 1
         System.out.println(selectPackage(2, 5));  // 0
         System.out.println(selectPackage(8, 0));  // 0
     }
   }

   ====
   import static org.junit.Assert.*;
   import org.junit.Test;
   import java.io.IOException;
   import java.util.Arrays;

   public class RunestoneTests extends CodeTestHelper {
       public RunestoneTests() {
           super();
       }

       @Test
       public void testBoundarySum() throws IOException {
            String output = getMethodOutput("main");
            String expect = "3\n2\n2\n1\n0\n0\n";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
      }
   }
