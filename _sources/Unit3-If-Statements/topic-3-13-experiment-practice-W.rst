.. qnum::
   :prefix: exp-3-
   :start: 1

Practice Problems (Write Code)
==============================

.. activecode:: most-common-practice-alarmclock-written
   :language: java
   :autograde: unittest
   :nocodelens:

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


.. activecode:: most-common-practice-datefashion-written
   :language: java
   :autograde: unittest
   :nocodelens:

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

.. activecode:: most-common-practice-frontback-written
   :language: java
   :autograde: unittest
   :nocodelens:

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


.. raw:: html

    <p>click on the following link to proceed to the posttest: <b><a id="next-link"><font size="+2">posttest</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("next-link")
        a.href = "topic-3-13-experiment-posttest.html"

      };

    </script>