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


    <img src="../_images/pretest-gym1.png" width="1000">

    <img src="../_images/pretest-gym2.png" width="1000">



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
    <img src="../_images/pretest-lucky-1.png" width="1000">

    <img src="../_images/pretest-lucky-2.png" width="1000">


    



.. activecode:: most-common-pretest-clean
   :language: java
   :autograde: unittest
   :nocodelens:

   .. raw:: html

      <b> Apartment Cleaning </b>

   You and your roommate are deciding whether to clean the apartment. The parameter ``yourMessiness`` represents how messy your side of the apartment is, and ``roommateMessiness`` represents how messy your roommate's side is, both in the range from 0 to 20. The result is an ``int`` value indicating whether it's time to clean. Return:
    * If either messiness is 5 or less (i.e., it's still relatively clean), return 0 (no need to clean);
    * With the exception that if either messiness is 18 or more (i.e. the apartment is very messy), return 2 (definitely needs to clean);
    * Otherwise, return 1 (maybe).

   .. table::
      :name: clean-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``shouldClean(4, 3)``                              | ``0``           |
      +----------------------------------------------------+-----------------+
      | ``shouldClean(4, 18)``                             | ``2``           |
      +----------------------------------------------------+-----------------+
      | ``shouldClean(6, 15)``                             | ``1``           |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class CleaningDecision 
   {
       public static int shouldClean(int yourMessiness, int roommateMessiness)
       {
           // Your Code Here //
       }

       public static void main(String[] args)
       {
           System.out.println(shouldClean(4, 3)); // Output: 0

           System.out.println(shouldClean(4, 18));  // Output: 2

           System.out.println(shouldClean(6, 15)); // Output: 1

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
           CleaningDecision c = new CleaningDecision();
           assertTrue(getResults(0, c.shouldClean(4, 3), "shouldClean(4, 3)"));
       }

       @Test
       public void testValue2() throws IOException {
           CleaningDecision c = new CleaningDecision();
           assertTrue(getResults(2, c.shouldClean(4, 18), "shouldClean(4, 18)"));
       }

       @Test
       public void testValue3() throws IOException {
           CleaningDecision c = new CleaningDecision();
           assertTrue(getResults(1, c.shouldClean(6, 15), "shouldClean(6, 15)"));
       }

       @Test
       public void testValue4() throws IOException {
           CleaningDecision c = new CleaningDecision();
           assertTrue(getResults(1, c.shouldClean(10, 15), "Hidden test"));
       }

       @Test
       public void testValue5() throws IOException {
           CleaningDecision c = new CleaningDecision();
           assertTrue(getResults(2, c.shouldClean(18, 3), "Hidden test"));
       }
   }
