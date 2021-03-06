# Restaurant Pricing
So you're going to [Edibles](http://ediblesrochester.com) on University Avenue in the Neighborhood of the Arts. It's a casual dining spot with eclectic eats and a location with a history. The restaurant features tall tin ceilings, original hardwoods, and a unique location in the Flatiron building, built in 1850. The food pulls influences from Eastern Europe but blends it with typical New American fare. Complemented by delicious cocktails and a spread of appetizers, you're sure to have a great time!

![alt text](https://s3-media1.fl.yelpcdn.com/bphoto/6bk_Qe5vbkCl5VVjqcxHFA/o.jpg)

## Code Description
This script is a Monte-Carlo simulation to determine the probability distribution function for the price of a meal at Edibles, but tailored to your specific preferences and to Edibles selection of menu items. I've used this code to set the gift amount. The gift card amount is set based on the 50% confidence interval and the additional cash is set based on the 90% one-sided confidence interval. Meaning, if you go out to eat at Edibles every day of the year for the next 273 years (100,000 times), this gift card and cash would cover the meal, tip, and tax 90% of the time.

The script pulls in menu pricing information and will stochastically and iteratively formulate a meal. For example, one meal may have two appetizers and the most expensive dessert whereas the next may only have one appetizer and no dessert. All of these decisions are dictated by independent event probability distribution functions. These are all then aggregated into an overall meal price probability distribution function, from which the final gift price is set.

## Inputs
I took a stab at predicting your inputs and the final gift values are based on these values. The values in the image below are reflected in edibles.py as inputs. Remember, this is the general spectrum of expected probabilities but in no way should affect what you actually decide to order. The fractional values represent the probability that you will order 0, 1, or, 2 items in a course respectively. From these inputs, the script will identify how many items you ordered and at each iteration will randomly select a menu item from the list of available plates.

![alt text](./img/inputs.png)

## Results
I know, this is terrible practice. But for the purposes of this gift, I'm going to assume the results are static and summarize in the markdown file. Let's get started.

The meal price probability distribution function for (my interpretation of) your preferences is shown below. The price specified by the 50th percentile is given in the form of a gift card. To ensure you don't get stuck with unused gift card monies, the remaining balance to get you up to the 90th percentile will be given in the form of cash.

![alt text](./img/pdf_edibles_100000.png)

To summarize, here is the total value of the gift.

```
Total Value: $141.44
  Gift Card: $115.62
  Cash Value: $25.82
```

We hope you enjoy this date and use the time to grow your marriage and to reflect on what great of a brother and sister-in-law you have.
