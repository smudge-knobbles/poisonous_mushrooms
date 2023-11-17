# poisonous_mushrooms

data source: https://www.openml.org/search?type=data&sort=runs&status=active&id=24

For this project, I used the above data set in which there are ~8100 hypothetical samples corresponding to 23 species of gilled mushrooms in the Agaricus and Lepiota Family as described by The Audubon Society Field Guide to North American Mushrooms (1981).

There are 23 features described, one of which is whether the specimen is poisonous or not.

My goal was to use machine learning to establish a small number of rules that could be easily remembered that a person hiking in the woods could use to distinguish between edible or poisonous mushrooms.

In the categorical_binning notebook, I dropped some columns and binned some values to be more realistic.

I then used a Decision Tree model to find the least number of rules that would be able to classify mushrooms as poisonous with very high accuracy:

1. If a mushroom has any smell and it bruises when touched, consider it poisonous
2. If a mushroom doesn't bruise, but smells foul or pungent, consider it poisonous

These two rules taken together correctly identifies 98.5% of poisonous mushrooms.