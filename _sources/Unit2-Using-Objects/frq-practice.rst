
Unit 2 Free Response Question (FRQ) Practice
=============================================

.. index::
    single: free response questions
    single: FRQ

The AP CSA exam has 4 free response questions (FRQs) where you have to write Java code in 1.5 hours. The first FRQ is about Methods and Control Structures using expressions, methods, loops, and ``if`` statements. One part of this question usually involves expressions with math operators and calling methods of a given class. Although we have not yet covered enough to complete an FRQ, the following is an adaptation of the 2022 FRQ #1 part a about the points earned in a video game with 3 levels using the class ``Level``. You will try the simplified version of the FRQ in this lesson using just expressions and method calls, and then you will do the complete FRQ part a in the next unit after you learn about ``if`` statements.

FRQ Description of Level Class
----------------------------------

This question involves simulation of a single-player video game. In the game, a player attempts to complete three levels. A level in the game is represented by the ``Level`` class which keeps track of their points in a level and whether they have reached the end or goal of that level.

.. code-block:: java

    public class Level
    {
        /* The number of points the user has in this level */
        private int points;
        /* Whether the goal of the level has been reached */
        private boolean goal;

        /** Constructor for the Level class */
        public Level(int p, boolean g)
        {
            points = p;
            goal = g;
        }

        /** Returns the number of points (a positive integer) recorded for this level */
        public int getPoints()
        { /* implementation not shown */ }

        /** Returns true if the player reached the goal on this level and returns false otherwise */
        public boolean goalReached()
        { /* implementation not shown */ } 
        
        // There may be instance variables, constructors, and methods that are not shown.
    }

FRQ Practice
--------------

In this simplified version of this FRQ, you will declare 3 ``Level`` objects for the 3 levels of the game and then call their ``getPoints()`` methods to calculate the score for the game. The score is calculated by adding the points from each level, but in this version, level 2 points are doubled and level 3 points are tripled.

.. activecode:: frq-simple-game-score
    :language: java
    :autograde: unittest

    In the main method, declare 3 objects of the ``Level`` class called ``level1``, ``level2``, and ``level3`` with the following points and goals: 100 points and true, 100 points and true, and 200 points and true. Then, calculate the score for the game by adding the points from each level using their ``getPoints()`` method, but double the level 2 points and triple the level 3 points.
    ~~~~
    public class Game
    {	
        public static void main(String[] args) 
        {   
            // 1. Declare 3 objects of the Level class called level1, level2, and level3 
            // with the following points and goals: 100 points and true, 
            // 100 points and true, 
            // and 200 points and true

            int score = 0;

            // 2. Calculate the score for the game by adding the points 
            // from each level using their getPoints() method
            // but double the level 2 points and triple the level 3 points   



            System.out.println("Score is " + score);   
        }
    }

    /* The Level class: do not change */
    class Level
    {
        private int points;
        private boolean goal;

        /** Constructor for the Level class */
        public Level(int p, boolean g)
        {
            points = p;
            goal = g;
        }

        /** Returns true if the player reached the goal on this level and returns false otherwise */
        public boolean goalReached()
        { return goal; } 

        /** Returns the number of points recorded for this level */
        public int getPoints()
        { return points; }
    }
    ====
    import static org.junit.Assert.*;
    import org.junit.*;
    import java.io.*;
    
    public class RunestoneTests extends CodeTestHelper
    {
       public RunestoneTests()
       {
           super("Game");
       }
       @Test
       public void testMain() throws IOException
       {
           String output = getMethodOutput("main");
           String expect = "900";

           boolean passed = getResults(expect, output, "Output from main");
           assertTrue(passed);
       }
       @Test
       public void checkCodeContains0()
       {
           boolean passed = checkCodeContains(
            "call to constructor new Level(100,true)", "new Level(100,true)");
           assertTrue(passed);
       }
       @Test
       public void checkCodeContains1()
       {
           boolean passed = checkCodeContains(
            "call to level3.getPoints()", "level3.getPoints()");
           assertTrue(passed);
       }
        @Test
       public void checkCodeContains2()
       {
           boolean passed = checkCodeContains(
              "3* to triple the level 3 points", "3*");
           assertTrue(passed);
       }
       
       }



