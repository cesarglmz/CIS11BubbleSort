# CIS11BubbleSort
Bubble Sort final project for CIS 11 

This program is a bubble sort written in LC-3 assembly language.

 This program takes as its input 8 user inputted numbers and uses a bubble sort
 to sort them in ascending order. This bubble sort works by comparing adjacent
 numbers and swapping them if the left value is less than the right value, until
 all numbers are in ascending order. It then outputs the sorted list of numbers.

 INPUT: ARRAY (8 numbers between 0-100)
 OUTPUT: ARRAY (8 numbers sorted in ascending order)

 Variables: \n   
        PNTR: sorting pointer (left value)
        TEMP: temporary hold for values
        COMP: comparing pointer (right value)
        FIRST: hold for left value in comparison
        SECOND: hold for right value in comparison
        ARRAY: array for 8 numbers

 Subroutines:    
        LOOP: user inputs 8 numbers for sorting
        ZERO: clears registers, sets pointers to first address in array,
              sets counters
        SORT: sets sorting pointer to address in R3, decrements counter
              until reaching zero, then calls on ISSORT
        COMPARE: increments address in R3 to set comparing pointer,
             sets left and right values into FIRST & SECOND,
             compares by checking if left value is greater
        SWAP: if left value was greater, swap is called to swap values
              from respective addresses, increments swap counter;
              ISSORT: is called after SORT has gone through all 8 comparisons,
            if swap counter is positive then it loops back to SORT,
            if zero then it moves on to outputting results
        CONSOL: outputs sorted list
