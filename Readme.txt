COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No, it does not make any behavioral difference. All tests pass with
                both ArrayList and LinkedList. but there is difference in performance.
TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			It removes index 5 which is element 6 in the list

		list.remove(Integer.valueOf(5)); // what does this one do?

			It removes based on the objects value, not its position

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			Using list.remove(77) will throw a ConcurrentModificationException

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.
	These are examples of SIZEs you might choose, you can choose others if you wish.

	SIZE 10
								  #1   #2   #3   #4   #5   #6
        testArrayListAddRemove:  82    85   79 val4 val5 val6
        testLinkedListAddRemove: 62    64   61 val4 val5 val6
		testArrayListAccess:     18    19   17 val4 val5 val6
        testLinkedListAccess:    31    30   32 val4 val5 val6

	SIZE 100
								  #1   #2   #3   #4   #5   #6
        testArrayListAddRemove:  91    94   88 val4 val5 val6
        testLinkedListAddRemove: 78    80   76 val4 val5 val6
		testArrayListAccess:     29    31   28 val4 val5 val6
        testLinkedListAccess:    48    32   33 val4 val5 val6

	SIZE 1000
								  #1   #2   #3   #4   #5   #6
        testArrayListAddRemove:  237 241 val3 val4 val5 val6
        testLinkedListAddRemove: 65  67 val3 val4 val5 val6
		testArrayListAccess:     22  21 val3 val4 val5 val6
        testLinkedListAccess:    426  420 val3 val4 val5 val6

	SIZE 10000
								  #1   #2   #3   #4   #5   #6
        testArrayListAddRemove:  2035 val2 val3 val4 val5 val6
        testLinkedListAddRemove: 62 val2 val3 val4 val5 val6
		testArrayListAccess:     32 val2 val3 val4 val5 val6
        testLinkedListAccess:    7109 val2 val3 val4 val5 val6

	listAccess - which type of List is better to use, and why?

		ArrayList is significantly better for access operations. At
                SIZE=10000, arraylist was very much faster than linkedlist. arraylist uses contagious array by which access directly the element

	listAddRemove - which type of List is better to use, and why?

		LinkedList is significantly better for add and remove operations at the
                beginning of the list. At SIZE=10000, linkedlist was very faster
                than arraylist
