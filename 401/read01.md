# Pain vs. Suffering
![pain vs suff](https://i.pinimg.com/originals/db/3d/f1/db3df1e503d98939361caba6c7c5e200.jpg)
* pain in the service of growth is a good thing, as long as that pain is what’s necessary to achieve the growth that you’re aiming for. And even better than that, this pain is only temporary. It’s what will launch you forward into the next phase of your life.



* Suffering is pain without purpose. Pain with no higher goal. Pain with no dreams, no ambition, no aspiration.

#  Big O Notation

## What is Big O Notation?
Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

## below are some common orders of growth along with descriptions and examples where possible.


![notation o](https://www.sahinarslan.tech/static/b14f0f927757ce111e7338d849f219a5/17bda/big-o-table.jpg)
### O(1)

O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

### O(N)
O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set.


## O(N²)
O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N³), O(N⁴) etc.

## O(2^N)
O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set. The growth curve of an O(2^N) function is exponential — starting off very shallow, then rising meteorically. An example of an O(2^N) function is the recursive calculation of Fibonacci numbers:

![o](https://sauanla.com/wp-content/uploads/2020/05/12-28-10-341-d633585c-1a04-4b97-9276-7812ae96a6d7.png)

A grasp of Big O is an important tool when dealing with algorithms that need to operate at scale, allowing you to make the correct choices and acknowledge trade-offs when working with different data sets.