%% reference %%
https://www.stat.ubc.ca/~jenny/STAT545A/topic13_make-browsing-GitHub-repo-more-rewarding.html


# Classifications learning #
### Important notions which are embedded in every classification problem.
%% instances:: (input,vector or attributes that define your input.)

%% concept:: (funciton, maps input to output)..
             (objects in the world -> members in the set)
             (what a thing is..conformable to the 'concept'? true or false)

%% target concept:: **(t.c. is the actual answer.)**

%% hypothesis (class): **all the functions that we are willing to think about.**

%% sample (training set, (input,output))

%% candidate (concept):: going to be tested..

%% testing set.
*the important lesson is .. teacher wants to make sure the students understand..
== they want to make sure they know how to generalize, not by memorizing, but by
applying the concept/the model in mind!!* 

###### example of ceteri paripas? 
*I want to go to an occupied resterant, but not at 2:00 in the morning.*

###### `<undefined>`
a decicition tree == a specific representation \\ 

and an algorithm == how to build the trees

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
%% and, or, xor,...
- n-or == any: size of decision tree is linear. 
- n-xor == odd/parity: O(2^N)
- ^^ Remark:AI is about finding the best representation.

###### `<table representation>` 
- %% n attributes .. O(n!) for building the nodes of the tree.
- %% output (if boolean).. another 2^n

so table representation!!!: the attributes | the ouputs!

with attributes and the outputs, that is **"the function"**!

the total number is 2^(2^n)... so we need to trim??

###### id3
- best attribute? -> information gain == gain(s,action)
  - but information gain is composed of entropy:
    - entropy: more randomness? 
    - amount of information to be released
    - entropy == expost - exante

###### id3 bias!!
- restriction bias!
- preference bias! 


