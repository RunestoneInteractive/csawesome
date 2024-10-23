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
    <li>If the person is 13 years old or younger or visits the theme park 4 or more times per month, they get a 20% discount.</li>
    <li>If the person is older than 13 years old and visits the theme park 2 or more times per month, they get a 10% discount.</li>
    <li>If neither condition is met, and the person is between 13 and 19 years old (inclusive), they get a 5% discount.</li>
    <li>Otherwise, there is no discount.</li>
    </ul>
    Select the correct code for this problem.
    <b>Only the highlighted lines are different in each option.</b>
    <br>

    <img src="https://i.postimg.cc/P5WhF5V8/gym.png" width="1000">


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
    <img src="https://i.postimg.cc/SNWCVW4L/lucky.png" width="1000">

.. activecode:: most-common-posttest-course
   :language: java
   :autograde: unittest

   You are selecting a course based on interest level and your available study hours per week. The parameter interestLevel represents the average interest score (from 0 to 10, where 10 indicates high interest), and studyHours represents available study hours per week. The result is the course type encoded as an int value with 0=no course, 1=basic, 2=intermediate, 3=advanced. The conditions are:

   * If the interest level is 9 or more, and the study hours are 10 or more, the result is 3 (advanced).
   * If the interest level is between 6 and 8 (inclusive), and the study hours are 5 or more (inclusive), the result is 2 (intermediate).
   * If the interest level is between 3 and 5 (inclusive), and the study hours are 2 or more (inclusive), the result is 1 (basic).
   * Otherwise, you decide not to take the course, so the result is 0 (no course).

   .. table::
      :name: course-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``selectCourse(9, 10)``                            | ``3``           |
      +----------------------------------------------------+-----------------+
      | ``selectCourse(7, 6)``                             | ``2``           |
      +----------------------------------------------------+-----------------+
      | ``selectCourse(5, 2)``                             | ``1``           |
      +----------------------------------------------------+-----------------+
      | ``selectCourse(2, 5)``                             | ``0``           |
      +----------------------------------------------------+-----------------+
      | ``selectCourse(8, 0)``                             | ``0``           |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class CourseSelection 
   {
      public static int selectCourse(int interestLevel, int studyHours)
      {
         // Your Code Here //
      }

      public static void main(String[] args)
      {
         System.out.println(selectCourse(9, 10));  // 3
         System.out.println(selectCourse(7, 6));  // 2
         System.out.println(selectCourse(7, 2));  // 2
         System.out.println(selectCourse(5, 2));  // 1
         System.out.println(selectCourse(2, 5));  // 0
         System.out.println(selectCourse(8, 0));  // 0
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
