---
layout: default
---

## Weight Calculations - Encounters, Target Rate and more

#### By [Andar](https://forums.rpgmakerweb.com/index.php?members/andar.11882/), 27 Jul 2015

Everyone knows what percentages are when calculating probability, but in a lot of places the computer does not give percentage value, but something called "weight". You can see that directly in the random encounter tables of a map, but there are other places where this principle is used as well - for example with the target rate or the attack patterns (but a bit more hidden in both of those cases).

But what exactly is "weight", and how it is used in calculating probability?

Let's take a step back and begin by looking at percentages. What is a "percent"?
Translated that word basically means "of hundred". When we say "eleven percent" we are basically saying "eleven out of hundred (parts)"
It could also be written as 11/100 - you probably have seen that form of writing percentages one or two times before.

Now compare that to an example from the encounter tables.
Let's say we have three random enemies A, B and C. We'll give them a few weight values, resulting in:
A - 10
B - 15
C - 25

So now we have a total weight of 10+15+25 = 50. With that we can see the probability of each enemy appearing:
Enemy A will be selected 10/50 times
Enemy B will be selected 15/50 times
Enemy C will be selected 25/50 times

Do you recognise that form of writing from above?
Yes, percentages are a very special form of weight where the total weight is always set to be 100.

You could easily write 10/50 as 20/100 or 20% as that is all the same probability. So why don't we do that?

Let's assume the fictional game gets further into development, and at some time you decide that on this map, you want an additional but rarer enemy. You add Enemy D with a weight of 5.
What happens? The table now reads
A - 10
B - 15
C - 25
D - 5
with a total weight of 55.

The probabilities now are
Enemy A will be selected 10/55 times (don't bother calculating, it's now 18,2%)
Enemy B will be selected 15/55 times (27,3%)
Enemy C will be selected 25/55 times (45,5%)
Enemy D will be selected 5/55 times (9,1%)

What numbers do you think are better to work with? 10/55 weight or 18,2%? Especially if there is the possibility that the encounter table will be changed again and again during game development?

Percentages are better readable because they are based on the total weight of 100, but that is also their greatest disadvantage when the total numbers start to change. For percentage numbers to work, you'll always have to recalculate for a total of 100, and that can cause a lot of ridicilous numbers when the totals change.
And that recalculation also has to be done in the engine, costing some processing time. Because the computer can also better calculate with the direct weight numbers, he doesn't need to conform to a special weight number of 100 for readability.

Additionally, the RELATIVE weight is even better to read than percentages:
Enemy A has a weight of 10, Enemy D has a weight of 5. Because 10 is double of 5, the enemy A will appear (in average) two times for each time enemy D appears. And since enemy C has a weight of 25, it will be encountered five times as often as enemy D.
That form is even easier to read than understanding that 18,2% is two times 9,1% and 45,5% is five times 9,1% - and it holds even true if you decide for example to delete enemy B from the table - 10/40 is still double of 5/40, no matter how often the percentage numbers would change.

If you understand that, you should be able to do your balancing work a lot easier with weights than with percentages for probability...

[back](./)
