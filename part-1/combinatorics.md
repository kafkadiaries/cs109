# Combinatorics

Helpful set of common counting paradigms.  
**Unique == distinct**  
**indistinct != unique**   
Permutations = ordered  
Combinations = unordered  

## Permutations of Distinct Objects

> [!NOTE]  
> **Permutation of distinct objects**  
> An ordered arrangement of *n* distinct objects, which can be permuted in
> ```math
> n · (n-1) · (n-2) ...2 · 1 = n!
> ```

### Examples

1. **How many unique orderings are possible for the word "BAYES?"**
   
   * Since each letter is distinct: 5! = 120 different ways
     

## Permutations of Indistinct Objects

> [!NOTE]  
> **Permutation of indistinct objects**  
> *n* objects where *n<sub>1</sub>*, *n<sub>2</sub>*, up to *n<sub>r</sub>* are indistinguishable, then:
> ```math
> n!/n_1!n_2!...n_r!
> ```

### Examples

1. **How many distinct orderings are possible for the word 'MISSISSIPPI'?**
   ```math
     11!/4! 4! 2! = 34,650
   ```
   * 4 I's, 4 S's, and 2 P's

## Combinations with Distinct Objects



## Bucketing with Distinct Objects


## Bucketing with Indistinct Objects


## Bucketing with Fixed Sized Containers
