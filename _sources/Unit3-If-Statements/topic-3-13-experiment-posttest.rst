.. qnum::
   :prefix: exp-4-
   :start: 1

Posttest
==============================

.. poll:: most-common-posttest-park
    :option_1: A
    :option_2: B
    :option_3: C 
    :option_4: D 
    :results: instructor
    
    <b>Theme Park Discount</b>
    <br>
    A theme park offers discounts on ticket prices based on age and the number of visits per month. The parameter age is the person's age in years, and visitsPerMonth is the average number of visits per month. The result is the discount percentage encoded as an int. The conditions are:
    <ul>
    <li>If the person is 13 years old or younger and visits the theme park 3 or more times per month, they get a 20% discount.</li>
    <li>If the person is older than 13 years old and visits the theme park 5 or more times per month, they get a 10% discount.</li>
    <li>If neither condition is met, and the person is between 13 and 19 years old (inclusive), they get a 5% discount.</li>
    <li>Otherwise, there is no discount.</li>
    </ul>
    Select the correct code for this problem.
    <b>Only the highlighted lines are different in each option.</b>
    <br>

    <img src="../_images/posttest-theme1.png" width="1000">

    <img src="../_images/posttest-theme2.png" width="1000">



.. poll:: most-common-posttest-unlucky
    :option_1: A
    :option_2: B
    :option_3: C 
    :option_4: D 
    :results: instructor
    
    <b>Unlucky Number</b>
    <br>
    A local fortune teller claims that a person's unlucky number is determined based on the month and minute of their birth. The parameters are month and minute. The month is the month of birth (from 1 to 12), and the minute is the minute of birth (from 0 to 59). According to the fortune teller, the unlucky number is calculated as follows:
    <ul>
    <li> If the month is even and the minute is greater than 30, the unlucky number is the sum of the month and the minute.</li>
    <li>If the month is even and the minute is less than or equal to 30, the unlucky number is the product of the month and the minute.</li>
    <li>If the month is odd and the minute is greater than 20, the unlucky number is the minute minus the month.</li>
    <li>If the month is odd and the minute is less than or equal to 20, the unlucky number is the month minus the minute.</li>
    </ul>
    Select the correct code for this problem.
    <b>Only the highlighted lines are different in each option.</b>

    <br>
    <img src="../_images/posttest-unlucky-1.png" width="1000">

    <img src="../_images/posttest-unlucky-2.png" width="1000">

.. activecode:: most-common-posttest-work
   :language: java
   :autograde: unittest
   :nocodelens:

   .. raw:: html

      <b> Working Overtime </b>


   You and your project partner are deciding whether to work overtime based on your remaining workload. The parameter ``yourWorkload`` represents how much work you have left, and ``partnerWorkload`` represents how much work your project partner has left, both in the range from 0 to 20. The result is an ``int`` value indicating whether you both should work overtime. Return:
    * If either workload is 5 or less (i.e., there's little work left), return 0 (no need to work overtime);
    * With the exception that if eithr workload is 18 or more, return 2 (i.e., a large amount of work to complete);
    * Otherwise, return 1 (maybe).

   .. table::
      :name: work-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``needOvertime(4, 3)``                             | ``0``           |
      +----------------------------------------------------+-----------------+
      | ``needOvertime(4, 18)``                            | ``2``           |
      +----------------------------------------------------+-----------------+
      | ``needOvertime(6, 15)``                            | ``1``           |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class OvertimeDecision 
   {
       public static int needOvertime(int yourWorkload, int partnerWorkload)
       {
           // Your Code Here //
       }

       public static void main(String[] args)
       {
           System.out.println(needOvertime(4, 3)); // Output: 0

           System.out.println(needOvertime(4, 18));  // Output: 2

           System.out.println(needOvertime(6, 15)); // Output: 1

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
       public void testValue1() throws IOException {
           OvertimeDecision c = new OvertimeDecision();
           assertTrue(getResults(0, c.needOvertime(4, 3), "needOvertime(4, 3)"));
       }

       @Test
       public void testValue2() throws IOException {
           OvertimeDecision c = new OvertimeDecision();
           assertTrue(getResults(2, c.needOvertime(4, 18), "needOvertime(4, 18)"));
       }

       @Test
       public void testValue3() throws IOException {
           OvertimeDecision c = new OvertimeDecision();
           assertTrue(getResults(1, c.needOvertime(6, 15), "needOvertime(6, 15)"));
       }

       @Test
       public void testValue4() throws IOException {
           OvertimeDecision c = new OvertimeDecision();
           assertTrue(getResults(1, c.needOvertime(10, 15), "Hidden test"));
       }

       @Test
       public void testValue5() throws IOException {
           OvertimeDecision c = new OvertimeDecision();
           assertTrue(getResults(2, c.needOvertime(18, 3), "Hidden test"));
       }
   }


