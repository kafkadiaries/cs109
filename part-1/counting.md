# Counting

Counting is the foundation of probability.

## Counting with Steps

> [!NOTE]
> **Step/Product Rule of Counting**  
> If an experiment has two parts, *m* and *n*, and n is not affected by the results of *m* then:  
> Number of outcomes = *m* x *n*  
> **|A||B| = *m* x *n***

### Examples  

1. **Hash Tables**
   * Store two arbitrary strings into a hash table with 100 buckets. **How many possible ways to store the two strings?**
   * 100 * 100 because the placement of the first string does not impact the second.
   * |A| = 100; |B| = 100; |A||B| = 100 x 100 = 10,000 ways for two strings to be stored in a hash table.
     
2. **True Color Model**
   * According to the True Color Model, each pixel can be one of 2<sup>24</sup> colors approx. 17 million distinct colors.
   * **How many pictures can you generate from just 12 pixels?**
   * Since each pixel can be one of 17,000,000 then 17,000,000<sup>12</sup> which is approx. 10<sup>86</sup>, a million times more pictures than the number of atoms in the universe (10<sup>80</sup>).
      
3. **Go Board**
   * A Go Board has 19 x 19 positions for a user to place no stone, a black stone, or a white stone. **Compute the number of unique board configurations.**
   * Options = {no stone, black stone, white stone} then 3<sup>19 x 19</sup> approx. 10<sup>172</sup>.
     
4. **Rolling Two Dice**
   * **How many outcomes are there when rolling two six-sided dice?**
   * 6 x 6 = 36
   * {(1,1), (1,2), (1,3), (1,4),...(6,5),(6,6)}

## Counting with Or


## Overcounting and Correcting
