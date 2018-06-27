%% reference %%
https://www.stat.ubc.ca/~jenny/STAT545A/topic13_make-browsing-GitHub-repo-more-rewarding.html

# Instance based learning 
- POINTS
  - good
    - remembers, fast, simple
  - bad
    - no generalization, 
    - overfittings.. 
      1. (believing the data too much )
      2. some data appear too often!
      3. I can not get which is not in the data.
- EXAMPLE: I look at my **nearest neighbor**! but what if I have a lot of ambiguours neighbor**s**?
  - I enlarge my neigbor region (but this comes with a **cost**!)
  - K nearest neighbor**s**
  - depending on where I am on the map, I may have different structures of the neighbors.
- *KNN*,
  - given training data, distance metric `d(q,x)`, number of neighbors
  - return
    - classification: (`weighted`) vote
    - regression: (`weighted`) mean/median
  - KNN problems
    1. locality
    2. smoothness
    3. all features matter equally.





# Classifications learning #
### Important notions which are embedded in every classification problem.
- instances:: (input,vector or attributes that define your input.)

- concept:: (funciton, maps input to output)..
             (objects in the world -> members in the set)
             (what a thing is..conformable to the 'concept'? true or false)

- target concept:: **(t.c. is the actual answer.)**

- hypothesis (class): **all the functions that we are willing to think about.**

- sample (training set, (input,output))

- candidate (concept):: going to be tested..

- testing set.
  - *the important lesson is .. teacher wants to make sure the students understand..
  - == they want to make sure they know how to generalize, not by memorizing, but by
applying the concept/the model in mind!!* 

###### example of ceteri paripas? 
- *I want to go to an occupied resterant, but not at 2:00 in the morning.*

###### `<undefined>`
- a decicition tree == a specific representation \\ 

- and an algorithm == how to build the trees

#### Decision tree #### \\ order matters! \\
- nodes: attributes
- edges: value of attributes
- leaves: output/decisions

#### Decision tree learning####
1. Pick best attribute (best: splits the data)
2. ased question
3. follow the answer path
4. go to 1.. until got an answer..

#### D.T expressiveness ####
- and, or, xor,...
  - n-or == any: size of decision tree is linear. 
  - n-xor == odd/parity: O(2^N)
  - ^^ Remark:AI is about finding the best representation.

###### `<table representation>` 
- n attributes .. O(n!) for building the nodes of the tree.
- output (if boolean).. another 2^n

so table representation!!!: the attributes // the ouputs!

with attributes and the outputs, that is **"the function"**!

the total number is 2^(2^n)... so we need to trim??

###### id3
- best attribute? -> information gain == gain(s,action)
  - but information gain is composed of entropy:
    - entropy: more randomness? close the eyes or not.
    - amount of information to be released
    - entropy == expost - exante

###### id3 bias!! (top down. -> good split near the top.)
- restriction bias: (the boundary of the set?)
  - hypothesis sets I care about. e.g.
  there are an infinite number.
- preference bias! (the choice from the set.)
  - given two trees, it prefers better splits near the top!!!
  - prefer correct (model data better) ones to incorrect ones (model data worse).
    - good splits near the top but wrong.. bad splits near the top but correct. CHOOSE THE LATTER.
    - shorter is preferred to longer???
- repeat the choice
  - not for the discrete
  - a further narrow down for the continuous.
- When do we stop? Problem.. overfitting..
  - can we trust data completely? **add noise.**
    - USE CV!
    - PRUNNING (bottom top..)


