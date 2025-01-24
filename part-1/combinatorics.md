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

> [!NOTE]  
> **Combination of distinct objects**  
> An unordered selection of *r* objects from a set of *n* objects. An object is not replaced once selected.  
> ```math
> n!/r!(n-r)! = {n \choose r}
> ```

### Examples

1. **How many ways to choose three items from a selection of 5 items?**
   ```math
   {5 \choose 3} = 5! / 3! (5-3)! = 10
   ```

## Bucketing with Distinct Objects

Bucketing = group assignment or the many different ways we can stuff elements into containers  

> [!NOTE]
> Place *n* distinguisable items in *r* containers.
> ```math
> r^n
> ```
> You have *n* steps (one step for each item) and for each element you have *r* choices

### Examples

1. **Place 10 different colored balls into 5 urns.**
   * 5<sup>10</sup>

## Bucketing with Indistinct Objects

> [!NOTE]
> Place *n* indistinguisable objects in *r* distinct groups.  
> Use stars and banners technique (fence post problem)  
> *n* = stars, *r - 1* = banners/dividers  
> ```math
> (n + r - 1)! / n!(r-1)! = {n+r-1 \choose n} = {n+r-1 \choose r-1}
> ```

### Examples

1. **How many ways to invest $10 million dollars in 4 companies (in $1 million increments)?**
   * Consider this as 10 balls in 4 containers.
   * *n* = 10, *r* = 4  
```math
   {10+4-1 \choose 10} = {13 \choose 10} = 286
```

## Bucketing with Fixed Sized Containers

Same formula as "Permutations with indistinct objects"

### Examples

1. Company Camazon has 13 distinct new servers and would like to divy them up to 3 data centers where data center A, B, and C have 6, 4, and 3 empty racks. **How many different divisions of servers are possible?**
```math
{13 \choose 6,4,3} = 13!/6!4!3! = 60,060
