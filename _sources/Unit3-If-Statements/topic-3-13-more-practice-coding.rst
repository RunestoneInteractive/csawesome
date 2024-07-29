.. qnum::
   :prefix: 3-13-
   :start: 1

FRQ Style Coding Practice
==============================

In the following exercises which are similar to the Free Response Questions (FRQs) in the AP exam, you will write code inside a method with parameters and return values. Make sure that you use the parameter variables given in the method header and return a value.

.. code-block:: java

   public static return-type method-name(param-type param-var1, param-type param-var2, ...)
   {
       // ADD CODE HERE using the param-variables //
       return result; 
   }
 

.. activecode:: front_back_written
   :language: java
   :autograde: unittest

   Create the method ``front_back(str, start, end)`` that takes three strings and returns 
   a string based on the following conditions.

   * If ``str`` contains ``start`` at the beginning and ``end`` at the end then return  ``"s_e"``.  
   * If ``str`` contains ``start`` at the beginning of the string return ``"s"``.
   * if ``str`` contains ``end`` at the end of the string return ``"e"``.
   * Otherwise return ``"n"``.
  
   .. table:: 
      :name: front-back-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      | ``front_back("Open at noon", "Open", "noon")``     | ``"s_e"``       |
      +----------------------------------------------------+-----------------+
      | ``front_back("Opening time", "Open", "noon")``     | ``"s"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Afternoon", "Open", "noon")``        | ``"e"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("Closed", "Open", "noon")``           | ``"n"``         |
      +----------------------------------------------------+-----------------+
      | ``front_back("It is noon now", "open", "noon")``   | ``"n"``         |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class FrontBack 
   {
      public static String front_back(String str, String start, String end) 
      {
          // ADD CODE HERE //
      }

      public static void main(String[] args) 
      {
         String str1 = "Opening time";
         String start1 = "Open";
         String end1 = "noon";
         System.out.println(front_back(str1, start1, end1));

         String str2 = "Afternoon";
         String start2 = "Open";
         String end2 = "noon";
         System.out.println(front_back(str2, start2, end2));

         String str3 = "Open at noon";
         String start3 = "Open";
         String end3 = "noon";
         System.out.println(front_back(str3, start3, end3));
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
            String expect = "s\ne\ns_e\n";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
      }
   }


.. activecode:: squirrelPlay_written
   :language: java
   :autograde: unittest

   The squirrels in Palo Alto spend most of the day playing. In particular, they play if the temperature is between 60 and 90 (inclusive). Unless it is summer, then the upper limit is 100 instead of 90. Given an ``int temperature`` and a ``boolean isSummer``, return ``true`` if the squirrels play and ``false`` otherwise.

   .. table:: 
      :name: squirrelPlay-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      |  ``squirrelPlay(70, false)``                       | ``true``        |
      +----------------------------------------------------+-----------------+
      |  ``squirrelPlay(95, false)``                       | ``false``       |
      +----------------------------------------------------+-----------------+
      |  ``squirrelPlay(95, true)``                        | ``true``        |
      +----------------------------------------------------+-----------------+
 
   ~~~~

   public class SquirrelParty
   {
      public static boolean squirrelPlay(int temp, boolean isSummer) 
      {
          // ADD CODE HERE //
      }

      public static void main(String[] args) 
      {
         System.out.println(squirrelPlay(70, false));
         System.out.println(squirrelPlay(95, false));
         System.out.println(squirrelPlay(95, true));
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
            String expect = "true, false, true";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
     
       }

   
    }

.. activecode:: alarmClock_written
   :language: java
   :autograde: unittest

   Given a ``day`` of the week encoded as 0=Sun, 1=Mon, 2=Tue, ...6=Sat, and a ``boolean`` indicating if we are on ``vacation``, return a string of the form ``"7:00"`` indicating when the alarm clock should ring. Weekdays, the alarm should be ``"7:00"`` and on the weekend it should be ``"10:00"``. Unless we are on vacation -- then on weekdays it should be ``"10:00"`` and weekends it should be ``"off"``.

   .. table:: 
      :name: alarmClock-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      |      ``alarmClock(1, false)``                      | ``7:00``        |
      +----------------------------------------------------+-----------------+
      |      ``alarmClock(5, false)``                      | ``7:00``        |
      +----------------------------------------------------+-----------------+
      |      ``alarmClock(0, false)``                      | ``10:00``       |
      +----------------------------------------------------+-----------------+

   ~~~~
   public class VacayAlarmClock
   {
      public static String alarmClock(int day, boolean vacation) 
      {
              // ADD CODE HERE //
      }

      public static void main(String[] args) 
      {
         System.out.println(alarmClock(1, false));
         System.out.println(alarmClock(5, false));
         System.out.println(alarmClock(0, false));
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
            String expect = "7:00, 7:00, 10:00";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
     
       }

   
    }


.. activecode:: dateFashion_written
   :language: java
   :autograde: unittest

   You and your date are trying to get a table at a restaurant. The parameter ``you`` is the stylishness of your clothes, in the range 0..10, and ``date`` is the stylishness of your date's clothes. The result getting the table is encoded as an int value with 0=no, 1=maybe, 2=yes. If either of you is very stylish, 8 or more, then the result is ``2`` (yes). With the exception that if either of you has style of 2 or less, then the result is ``0`` (no). Otherwise the result is ``1`` (maybe).

   .. table:: 
      :name: datFashion-table
      :class: longtable
      :align: left
      :width: 80%

      +----------------------------------------------------+-----------------+
      | Example Input                                      | Expected Output |
      +====================================================+=================+
      |      ``dateFashion(5, 10)``                        |     ``2``       |
      +----------------------------------------------------+-----------------+
      |      ``dateFashion(8, 2)``                         |     ``0``       |
      +----------------------------------------------------+-----------------+
      |      ``dateFashion(5, 5)``                         |     ``1``       |
      +----------------------------------------------------+-----------------+
   
   ~~~~
   public class DateStylishness
   {
      public static int dateFashion(int you, int date) 
      {
          // ADD CODE HERE //
      }

      public static void main(String[] args) 
      {
         System.out.println(dateFashion(5, 10));
         System.out.println(dateFashion(8, 2));
         System.out.println(dateFashion(5, 5));
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
            String expect = "2, 0, 1";
           boolean passed = getResults(expect, output, "Expected output from main");
           assertTrue(passed);
     
       }

   
    }
