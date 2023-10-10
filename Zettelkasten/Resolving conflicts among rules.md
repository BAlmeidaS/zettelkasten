It is common in [[Rule-based system - Expert system]] that we end up in a conflict resolution, which means, with the same input we have more than one possible outcome.

![[Pasted image 20231010020840.png|300]]

In order to solve this three methods are suggested:

1. *Fire the rule with the highest priority*. Rules have priority (can be the order that they are listed) and the first one to match is the one to be fired.

2. *Fire the most specific rule.* Also known as the longest matching strategy. More specific rules should have priority over more general ones
 ![[Pasted image 20231010021109.png|250]]

3. *Fire the rule that uses the data most recently entered.* It basically relies on time tags attached to each fact inputted by the user


Another possibility to very complexity, and not wanted solutions, is the creation of a "metaknowledge" with "metarules". metaknowledge is the knowledge about the knowledge, through meta rules that define how to use the rules.