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

The total number of unique outcomes derived from source A or B depends on whether or not they are mutually exclusive (i.e. they don't don't share any outcomes).

> [!NOTE]
> **Mutually Exclusive Counting**  
> If the outcome of an experiment can be drawn from set A or set B, and none of the outcomes in set A are in set B then:  
> **|A or B| = |A| + |B|**

### Examples

1. **Sum of Routes**
   * **Find the total number of routes from Nairobi to Dar Es Salaam that pass through Mt. Kilimanjaro or Mombasa.**
   * There are 20 routes that pass through the former, 15 through the latter, and 0 paths through both.
   * 20 + 15 = 35 

> [!NOTE]
> **Inclusion Exclusion Counting**  
> If the outcome can be drawn from set A or B, and sets A and B may potentially overlap, then:  
> **|A or B| = |A| + |B| - |A and B|**  

### Examples

1. **An 8 bit string sent over a network**
   * A valid string must either start with '01' or end with '10'. **How many such strings are there?**
   * |A| = '01' + 2<sup>6</sup>
   * |B| = 2<sup>6</sup> + '10'
   * |A and B| = '01' + 2<sup>4</sup> + '10'
   * Total outcomes = |A| + |B| - |A and B|
   * Total outcomes = 64 + 64 - 16 = 112
   
## Overcounting and Correcting

One handy strategy for counting is to overcount and correct for duplicates, especially if it's easy to generate all outcomes. Then, correct with subtraction if the exact duplicate amount is known or division if it produces multiples. 

#### Examples

1. Consider an image with 4 pixels (2x2) with reduced color options wherein each pixel can be either blue or white.
   * **First, how many total images can be generated?** 2^<sup>4</sup> = 16 images
   * Now, let's introduce a constraint: we only want images with odd number of blue and white pixels (1 or 3 pixels)
   * Using mutual exclusion where |A| = 1 white pixel, 3 blue and |B| = 1 blue pixel, 3 white:
   * **|A or B| = 4 + 4 = 8 images with odd number of blue or white**
   * Finally, let's add one more constraint: mirror indistinction - if you can flip an image horizontally and it creates another image, then it is not considered unique.
   * As a result, this again reduces the number of outcomes by half: 4.
