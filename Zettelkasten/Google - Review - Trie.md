*Trie* type of [[Google - Review - Trees|tree]] that stores the values based on the position of the sequence.

*Nodes have an identifier* showing that are a sequence that existed in the original data!

**Usually it is used to keep strings**

![[Pasted image 20250212183251.png]]
*blue circles have the identifier. Thus, are valid words.

Nodes might have a value, instead just an identifier. In the example, we could attach to ear a number 1, and to eat a number 10.

### Hybrid structures
Instead of creating nodes for each reamining word, an hybrid algorithm might be created, you only create nodes when the leaf *get a number of items*.

>[!example]
suppose that we are doing a trie of words, and the maximum words is 3. 
> It starts receiving "ear", "earl", and "egg". All of this go to the first node as a list.
![[Pasted image 20250212185221.png|400]]
>
>Then a fourth word arrives, "erase".
>Because of the limit of 3 words, it _explodes_ this leaf. 
>Creating the letter "e" and from there another three nodes "a", "g",  and "r"
>![[Pasted image 20250212185240.png|600]]
