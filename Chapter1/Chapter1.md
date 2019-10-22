
### 1.1

An algorithm is procedure which upon taking some input returns an output. The main goal of an algorithm is to return specific output as a result to a problem, which is defined by its spefication how to achieve it.

"Instance" of a problem is the input to an algorithm, satisfying all the constraints.
The main goal of algorithm is to provide detail explanation and steps how to solve an imposed problem.

*Exercises*

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

---

### 1.2

In algorithms one of the main things to have in mind is how fast the running time grows. For example if you two algorithms for sorting, where ones complexity is `n^2` and the others `n * n log n`, it's maybe hard at first to see the difference, but when you start taking bigger numbers like `10 000`.

For example, if a computer is able to perform `1 000 000 000` operations per second, `10^9`
One will see that for the insertion sort `O(n^2)`, the required operation time will be:

`n = 1 000 000`

```
        (10^6)^2 ops          10^12 ops       
    ------------------- = ---------------- = 1000s = 16 minutes
        10^9 ops / s         10^9 ops / s
```

For merge sort, which has a complexity of `O(n * n log n)`, the required operation time will be:

```
      10^6 * (10^6 log 10^6)        10^6 ops       
    ------------------------- = ---------------- = 1s
          10^9 ops / s             10^9 ops / s
```

*Exercises*

#### 1.2-1 
Uber requires various algorithms to determine which driver should be picked for you. In a simple manner, it would be a shortest path algorithm, but there might be various different criteria's included. Filtering would be required to pick only the required types of cars. Maybe we would like to give some priority according to how many travels you already have, for example - 4.95 if it's your first trip.

#### 1.2-2

`8n^2 vs 64n log n`

```
8n^2 < 64nlogn
8n^2 - 64nlogn < 0
n^2 - 8 * n * logn < 0
n - 8 * logn < 0

n - 8logn = 0 
n = 44
```

#### 1.2-2

`100n^2 > 2^n`

```
100n^2 > 2^n
n = 14
```

*Problems*

```
1s = 10^6 microseconds

|        |     1s    |          1m        |         1h      | 
|--------|-----------|--------------------|-----------------|
| lgn    |  2.7^10^6 |    8 * 10^2605788  |                 |
| root(n)|  10^12    |    3.6 * 10^14     |  1.296 * 10^17  |
| n      |  10^6     |     3.6 * 10^7     |   3.6 * 10^9    |
| nlgn   |  87847    |      3.9 * 10^6    |    1.8 * 10^6   |
| n^2    |  1000     |        7749        |      60 000     |
| n^3    |   100     |         391        |      1532       |
| 2^n    |    20     |          25        |        31       |
| n!     |    9      |          11        |        12       |

lg(n) < 10^6 = 2.7^10000
root(n) < 10^6 = 10^12
nlg(n) < 10^6 = ...
```