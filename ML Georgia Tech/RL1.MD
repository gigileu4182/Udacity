# RL1. MARKOV

%% categories:
- Supervised learning: function approximation.. given (x,y), to learn f.
- unsup..... learning: description/clustering
- Rein...... learning: given (x,z), find f to generate y.

%% state, actions.
- implicit: when I can observe the **state**.
- implicit: I can update at each state, instead of obeying what I planned at the beginning.

%% MDP
- **s**: state 
  - ^^ (implicit. time. coordinates.)
- **model**: T(state,action,state') ~ Pr(state'|state,action)
  - ^^ transition of state. given s, do a, then given s, a(s), Pr(s')?
  - ^^ markovian!
  - ^^ _the function T does not depend on time!!!_ == stationary
- **actions**: A(s) or A 
  - ^^(dependent on state, current state? all the past?)
- **reward**: R(s), R(s,a), R(s,a,s')
  - ^^ the usefulness of entering into the state/utility?
- **policy**: a solution to the MDP problem.
  - ^^ important!!!! 
  - SL is like <s,a>, <s,a>, <s,a>...
  - RL is like <s,a,r>, <s,a,r>, <s,a,r>...!!! 

%% Policies

- Reward is the immediate reward, utility is the long term accumulate
- maximize the cumulative reward, given initial state and action
-> the recursive version

%% finding policies.

- That is non linear because of max..

- start with an arbitrary utility (or estimated utility?)
- update utility based on **neighbors**
- repeat till convergence

The key is that the wrongs are being discounted, 
and R(s) is the truth I add, and I am adding more and more truth!

the order, instead of the absolute value, matters!


# RL2

- planner
  - inputs: model ( transition matrix, instance reward)
  - outputs: policies (mapping from state to action)
- learner
  - 


- stimulus, action, reward: (s,a,r)
  - choose action to maximize reward as a function of state

with an ex post reward,
red lights stregthens the repsonse to the stimulus.

modeler or simulator, (自上而下，自下而上). the latter is more expensive
- transitions -> model
- model -> transitions

