#Maths

# The Birthday Paradox
In a group of just 23 people, there is roughly a $50\%$ chance of a at least two people sharing a birthday. Sounds counterintuitive, right? 

>[!Note]
*Many people find this counterintuitive. This suggests that many people's instict on probability and risk assesment is* **WRONNG**.

## Intuition
Assume the [[Probability|probability]] of a person having her birthday on any given day to be [[Uniform Distribution|uniformally distributed]], i.e., every day of the year has a $\frac{1}{365}$ chance of being the birthday of a given person.

Say *Person 1* has their birthday on some day of the year. Then, the probability that *Person 2* does **not** share the same birthday is $\frac{364}{365}$.

The probability that *Person 3* **doesn't** share a birthdy with, either, *Person 1* or *Person 2* is $\frac{363}{365}$.

*Person 4* has a $\frac{362}{365}$ probability of not sharing a birthday with any of the previous people, and so on. 

Therefore, the probability that none of the aforementioned people share a birthday is the product of the individual probabilities that each person doesn't share a birthday with any of the others. I.e., $\frac{364}{365}\times\frac{363}{365}\times\frac{362}{365}$.

To generalize, in a group of $n$ people, the probability that no pair shares a birthday is
$$\frac{364!}{(365-n)!\times365^{(n-1)}}$$

Consequently, we can conclude that the probability of at least one pair sharing a birthday within a group of $n$ people is
$$1 - \left( \frac{364!}{(365-n)!\times365^{(n-1)}} \right)$$

The paradoxical nature of this deduction is that with a group of 23 people ($n=23$), there is $\approx50\%$ chance that at least two people were born on the same day. 
$$1 - \left( \frac{364!}{342!\times365^{(22)}} \right)\approx 0.507297$$

## Applications

#CompSci 
### Estimating [[Hash Collision|hash collisions]]
#Todo