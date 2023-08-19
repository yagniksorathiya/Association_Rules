# Association_Rules

## Problem Statement

Prepare rules for the all the data sets 

1) Try different values of support and confidence. Observe the change in number of rules for different support,confidence values

2) Change the minimum length in apriori algorithm

3) Visulize the obtained rules using different plots

# ➳ Association Rules Mining via Apriori Algorithm in Python

**Association Rule learning** is a rule-based machine learning technique which is used to find interesting relationships and associations hidden in large data-sets. This rule shows how frequently an itemset occurs in a dataset or transaction.

Market Based Analysis is one of the important methods used by large relations to show associations between items. Given a set of transactions or dataset, we can find rules that will predict the occurrence of specific item based on the occurrences of other items in the dataset.

![Market-basket-analysis](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/ceaf467f-4591-4cb4-9104-805738ef2d81)

Association Rule Learning works on the concept of if/then statements. These statements expose the associations and relationships between independent data and relational or other data in the dataset. These rules are used to identify the relationships between the objects or items which are generally used together.

![Association Rules](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/dadb9c1c-b7aa-40d3-9998-acbcb1fedc1e)

The two basic patterns or functions used in Association rule Learning are Support and Confidence. The method identifies similarities and rules formed by decomposing data for frequently used if/then patterns. Association rules are usually used to satisfy a user-specified minimum support and a user- specified minimum resolution or determination simultaneously.

## Support

Support indicates how frequently an item or item-set appears in the dataset or transaction.

![Support](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/822e60f6-47b5-497e-a03d-4c1b48abd425)


## Confidence

Confidence indicates how frequently a rule is found to be true.

![Confidence](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/a597480e-66e8-4ed1-8917-6540c88b1659)

## Lift

Lift (X → Y) indicates the rise in probability of occurrence of Y when X has already occurred

![lift](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/a6677a1b-cf44-49da-bc6d-e0e0fe4ce8aa)

Support and confidence are computed to overcome the issue where some patterns in data can occur by chance without any association. Support is an important measure because a rule which has very low support may occur simply by chance. Moreover, a low support rule is also less valuable in business perspective as it may not be profitable to promote items which customers rarely buy together.

Confidence calculates the reliability of the inference or interpretation made by a rule.

## For a rule, if {X} →{Y} has high confidence, then it indicates that Y is more likely to occur with X.

For rule {X} →{Y}

By computing support, we know whether the rule is important or not.

By computing confidence, we can able to know that how likely X and Y will occur together.

Although these computations are important, they do not give us any idea on what extent the occurrence of one item (say X) or item-set increase the occurrence of the other item (say Y) or item-set.

So, we have to calculate lift, to know how the antecedent (independent item or data) and consequent (dependent data) are related to one another.

For a rule: {Antecedent} →{Consequent}

If lift = 1, then the possibility of occurrence of Antecedent and Consequent are not dependent on each other.

If lift < 1, then the occurrence of Antecedent has negative effect on occurrence on Consequent and Antecedent has positive effect on occurrence on Consequent.

If lift > 1, then that the two occurrences are dependent on each other, and these rules are very useful in identifying the consequent in final cases. It also helps us know that to what extent the occurrences are dependent on each other.

### There are different algorithms which are used to implement association rule learning technique.

## Apriori Algorithm

Apriori algorithm is a standard algorithm in Association Rule Learning in Data mining. It is used for drawing familiar item sets and their relevant association rules. It is designed to perform on a database.

It is very important for effective Market Basket Analysis and it helps in understanding the businessman that which items customers will buy together. It has also been used in healthcare field for the discovery of adverse drug reactions. It generates association rules that shows what are all combinations of medications and patient characteristics which will help in effective drug delivering.

![APriori](https://github.com/yagniksorathiya/Association_Rules/assets/129974278/7314efab-2e58-4e3e-ba3f-7015627eebd8)

## Eclat Algorithm

Eclat algorithm is a type of Association rule learning algorithm. It can be applied to achieve itemset mining. Itemset mining helps us to obtain periodic patterns in data. For example, if a consumer buys shoes, he would also buy socks. The main purpose of this algorithm is to use set intersections to calculate the support of a candidate itemset avoiding the generation of subsets that does not exist in the prefix tree.

Eclat algorithm performs a depth-first search to count the number of columns. Therefore, Eclat algorithm performs faster than the Apriori algorithm.

## F-P Growth Algorithm

The Full form of F-P Growth algorithm is Frequent Pattern growth Algorithm. The FP Growth classification is used only with databases but not with streams. Apriori algorithm needs n+1 number of scan if a database is utilized, here n is the length of the longest model. We can decrease number of scans of complete database by two by using F-P growth Algorithm.
