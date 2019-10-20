
An algorithm is procedure which upon taking some input returns an output. The main goal of an algorithm is to return specific output as a result to a problem, which is defined by its spefication how to achieve it.

"Instance" of a problem is the input to an algorithm, satisfying all the constraints.
The main goal of algorithm is to provide detail explanation and steps how to solve an imposed problem.

Exercises:

#### 1.1-1 

Sorting between students would be required to stand in line by height in PE class.

#### 1.1-2

Besides speed, in real world one could measure the number or operations required - maybe more operations cost more money. Also storage, meaning if you can do all the required operations without storing partial results somewhere.

#### 1.1-3 (Array)

Strenghts - the main strenght is the lookup time. You can take any element from it in O(1) if you know the concrete index where the information is stored. Also, depending on the type of the array, you can set the size of it as fixed or dynamic. If fixed the memory allocated is put near each other and it's faster to iterate than a linked list. [Contiguous Memory Blocks](https://stackoverflow.com/questions/4059363/what-is-a-contiguous-memory-block)

Weakness - the removal and addition of elements. If you want to add a new element in the 3'rd position, you would need to shift all the elements from index 3 one place to the right, which is an O(n) operation. Also if you allocate an array with size of 10 and put only 1 element, you will have 9 allocated, but not used memory addresses.

#### 1.1-4

The SP Problem is about two points A and B, to which a shortest distance is needed to be found. The TSP Problem is about finding an optimal path shortest distance by visiting each city and being able to return at the same place at the end of the day.

[Shortest Path Problem](https://en.wikipedia.org/wiki/Shortest_path_problem)

[Traveling Salesman Problem](https://en.wikipedia.org/wiki/Travelling_salesman_problem)

#### 1.1-5

Only the best: To determine the required amounts (in percentage) of medicide a person needs in a vital operation to recover or not to overdose depending on his height, body weight, gender and etc..

Approximate: Looking for a taxi by GPS, if you get the taxi which is closest or one extra minute away from you, it usually doesn't make a big difference.