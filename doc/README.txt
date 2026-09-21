COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	also try with a LinkedList - does it make any difference?

		tests still pass / program works as expected, since list management methods are provided by Collections.


TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			list.remove(5) removes the element at index 5 (whose value is 77 in this case)

		list.remove(Integer.valueOf(5)); // what does this one do?

			removes the element with value 5, which is at index 4 in this list.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			list.remove() removes the first occurrence of an object when it is provided.
            In this case, the first occurrence of 77 is removed but others are kept.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	SIZE 10
								 #1   #2   #3   #4   #5    	... (as many tests as you ran)
        testLinkedListAddRemove: 316  321  309  308  437   ... (fill these in in ms)
        testArrayListAddRemove:  3066 2320 3554 2995 2971
		testLinkedListAccess:    48   126  92   43   113
        testArrayListAccess:     25   75   60   27   37

	SIZE 100
								 #1   #2   #3   #4   #5    	... (as many tests as you ran)
        testLinkedListAddRemove: 261  377  342  354  346   ... (fill these in in ms)
        testArrayListAddRemove:  3320 3154 3344 3063 3240
		testLinkedListAccess:    209  192  195  420  196
        testArrayListAccess:     27   25   24   79   27

	SIZE 1000
								  #1   #2    #3   #4   #5    	... (as many tests as you ran)
        testLinkedListAddRemove:  383  312   342  460  299 ... (fill these in in ms)
        testArrayListAddRemove:   5994 4984  4790 5840 5830
		testLinkedListAccess:     3242 3235  3266 3683 3684
        testArrayListAccess:      23   23    22   27   22

	SIZE 10000
								  #1     #2     #3    #4    #5    	... (as many tests as you ran)
        testLinkedListAddRemove:  380    336    399   453   317   ... (fill these in in ms)
        testArrayListAddRemove:   19361  16899  1640  21162 15599
		testLinkedListAccess:     47596  57081  54783 49389 50456
        testArrayListAccess:      23     28     28    29    23

	listAccess - which type of List is better to use, and why?

		ArrayList scales much better than LinkedList for access
		operations, and this can be attributed to the O(1) element
		access given by ArrayList's indexed elements. LinkedList element
		access is O(n) since it requires traversing the list to find
		a particular element.

	listAddRemove - which type of List is better to use, and why?

		LinkedList is better than ArrayList for adding/removing - the LinkedList
		is not index-based, so elements don't need to be shifted to accommodate
		a change. The 'next' attribute of a node is the only thing
		that needs to be changed with each add/remove