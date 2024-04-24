.. qnum::
   :prefix: 6-11-
   :start: 1

More Code Practice with Arrays
================================

.. activecode:: sum13_written
   :language: java
   :autograde: unittest

   Create a function ``sum13(nums)`` that takes an array of integers, ``nums`` and 
   returns the sum of the numbers in the array. However, the number 13 is 
   very unlucky, so do not add it or the number that comes immediately 
   after a 13 to the sum.    Return ``0`` if ``nums`` is an empty array. 
   
    .. table:: 
          :name: sum13-table
          :class: longtable
          :align: left
          :width: 80%

          +----------------------------------------------------+-----------------+
          | Example Input                                      | Expected Output |
          +====================================================+=================+
          | ``sum13({13, 1, 2})``                              | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({1,13})``                                  | ``1``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({4, 13, 8})``                              | ``4``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({13, 1, 13, 3, 2})``                       | ``2``           |
          +----------------------------------------------------+-----------------+
          | ``sum13({})``                                      | ``0``           |
          +----------------------------------------------------+-----------------+

   ~~~~
   public class Sum13 {
      public static int sum13(int[] nums) {
          // ADD CODE HERE //
      }

      public static void main(String[] args) {
         int[] nums1 = {13, 1, 2};
         System.out.println(sum13(nums1));

         int[] nums2 = {1, 13};
         System.out.println(sum13(nums2));
 
         int[] nums3 = {4, 13, 8};
         System.out.println(sum13(nums3));

         int[] nums4 = {13, 1, 13, 3, 2};
         System.out.println(sum13(nums4));

         int[] nums5 = {};
         System.out.println(sum13(nums5));
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
       public void testSum13() throws IOException {
            String output = getMethodOutput("main");
            String expect = "2\n1\n4\n2\n0\n";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
      }
   }

.. activecode:: has22_written
   :language: java
   :autograde: unittest

   Create a function ``has22(nums)`` that takes an array of integers, ``nums`` 
   and returns ``true`` if there are at least two items in the list that are 
   adjacent and both equal to ``2``, otherwise return ``false``. 

   .. table::
      :name:  has22-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``has22({1, 2, 2})``                               | ``true``        |
      +----------------------------------------------------+-----------------+
      | ``has22({2, 1, 2})``                               | ``false``       |
      +----------------------------------------------------+-----------------+
      | ``has22({2, 2, 8})``                               | ``true``        |
      +----------------------------------------------------+-----------------+
      | ``has22({3, 3, 5})``                               | ``false``       |
      +----------------------------------------------------+-----------------+
 
   ~~~~
   import java.util.Scanner;
   import java.util.Arrays;

   public class Has22{
      public static boolean has22(int[] nums){
          // ADD CODE HERE //

      }


      public static void main(String[] args) {

         int[] nums1 = {1, 2, 2};
         System.out.println(has22(nums1));

         int[] nums2 = {2, 1, 2};
         System.out.println(has22(nums2)); 
          
         int[] nums3 = {2, 2, 8};
         System.out.println(has22(nums3));
          
         int[] nums4 = {3, 3, 5};
         System.out.println(has22(nums4)); 
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
      public void testHas22() throws IOException {
         String output = getMethodOutput("main");
         String expect = "true\nfalse\ntrue\nfalse\n";
         boolean passed = getResults(expect, output, "Expected output from main");
         assertTrue(passed);
      }
   }

.. activecode:: total89_written
   :language: java
   :autograde: unittest

   Create the ``total89(nums)`` function below that takes an array of integers,
   ``nums``, and returns the total of the numbers in ``nums`` except for all numbers
   in the array between an 8 and a 9 (inclusive). 
   
   .. table:: 
      :name: total89-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``total89({1, 2})``               | ``3``                                 |
      +----------------------------------+---------------------------------------+
      |``total89({2, 8, 3, 9, 2})``      | ``4``                                 |
      +----------------------------------+---------------------------------------+
      |``total89({8, 3, 5, 9, 6})``      | ``6``                                 |
      +----------------------------------+---------------------------------------+

   ~~~~
   public class Total89 {
      public static int total89(int[] nums) {
          // ADD CODE HERE //
      }

      public static void main(String[] args) {
         int[] nums1 = {1, 2};
         System.out.println(total89(nums1));

         int[] nums2 = {2, 8, 3, 9, 2};
         System.out.println(total89(nums2));
 
         int[] nums3 = {8, 3, 5, 9, 6};
         System.out.println(total89(nums3));
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
       public void testTotal89() throws IOException {
            String output = getMethodOutput("main");
            String expect = "3\n4\n6\n";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
      }
   }

.. activecode:: twoSum_written
   :language: java
   :autograde: unittest

   Create a function ``twoSum(nums, target)`` that takes an array of integers
   ``nums`` and an integer ``target`` and returns an array with the indices of 
   two numbers such that they add up to ``target``. If no two numbers add up to
   ``target``, it returns an empty array. Assume that each input has exactly one
   solution, and you may not use the same element twice.

   .. table::
      :name: two-sum-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------+---------------------------------------+
      | Example Input                    | Expected Output                       |
      +==================================+=======================================+
      |``twoSum({2,7,11,15}, 9)``        | ``{0, 1}``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum({2,7,11,15}, 13)``       | ``{0, 2}``                            |
      +----------------------------------+---------------------------------------+
      |``twoSum({2,7,11,15}, 5)``        | ``{}``                                |
      +----------------------------------+---------------------------------------+
 
   ~~~~
   import java.util.Scanner;
   import java.util.Arrays;

   public class TwoSum {
      public static int[] twoSum(int[] nums, int target) {
          // ADD CODE HERE //
      }

      public static void main(String[] args) {
        int[] nums = {2, 7, 11, 15};
        int target = 9;
        System.out.println(Arrays.toString(twoSum(nums, target))); 
        target = 13;
        System.out.println(Arrays.toString(twoSum(nums, target))); 
        target = 5;
        System.out.println(Arrays.toString(twoSum(nums, target))); 
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
       public void testTwoSum() throws IOException {
            String output = getMethodOutput("main");
            String expect = "{0, 1}, {0, 2}, {}";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
     
       }
    }


