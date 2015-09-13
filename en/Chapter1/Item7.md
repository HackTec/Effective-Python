##Item 7: Use List Comprehensions Instead of map and filter

Python provides compact syntax for deriving one list from another. These expressions are called list comprehensions. For example, say you want to compute the square of each number in a list. You can do this by providing the expression for your computation and the input sequence to loop over.

```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
squares = [x**2 for x in a] 
print(squares)

>>>

[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

Unless you’re applying a single-argument function, list comprehensions are clearer than the map built-in function for simple cases. map requires creating a lambda function for the computation, which is visually noisy.

```python
squares = map(lambda x: x ** 2, a)
```

Unlike map, list comprehensions let you easily filter items from the input list, removing corresponding outputs from the result. For example, say you only want to compute the squares of the numbers that are divisible by 2. Here, I do this by adding a conditional expression to the list comprehension after the loop:

```python
even_squares = [x**2 for x in a if x % 2 == 0] 
print(even_squares)

>>>

[4, 16, 36, 64, 100]
```

The filter built-in function can be used along with map to achieve the same outcome, but it is much harder to read.

```python
alt = map(lambda x: x**2, filter(lambda x: x % 2 == 0, a)) 
assert even_squares == list(alt)
```

Dictionaries and sets have their own equivalents of list comprehensions. These make it easy to create derivative data structures when writing algorithms.

```python
chile_ranks = {‘ghost’: 1, ‘habanero’: 2, ‘cayenne’: 3} 
rank_dict = {rank: name for name, rank in chile_ranks.items()} 
chile_len_set = {len(name) for name in rank_dict.values()} 
print(rank_dict)
print(chile_len_set)


>>>

{1: ‘ghost’, 2: ‘habanero’, 3: ‘cayenne’} {8, 5, 7}
```

##Things to Remember

* List comprehensions are clearer than the map and filter built-in functions because they don’t require extra lambda expressions.

* List comprehensions allow you to easily skip items from the input list, a behavior map doesn’t support without help from filter.

* Dictionaries and sets also support comprehension expressions.