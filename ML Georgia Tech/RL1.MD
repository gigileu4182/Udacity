# RL1. MARKOV

- categories:
  - Supervised learning: function approximation.. given (x,y), to learn f.
  - unsup..... learning: description/clustering
  - Rein...... learning: given (x,z), find f to generate y.

- the example:
  - given my decision U U R R R.
  - **the resulting move**  may be different from my decision.

- state, actions.
  - implicit: when I can observe the **state**.
  - implicit: I can update at each state, instead of obeying what I planned at the beginning.

- MDP
  - **`S`**: state (*example*: coordinates)
    - ^^ (implicit. time. coordinates.)
  - **model / transition function**: T(state,action,state') ~ Pr(state'|state,action)
    - ^^ transition of state. given `s` (at the beginning of the phase), do `a`, `s'` is the state we end up with, then given s, a(s), Pr(s'|s,a)?
    - ^^ markovian!
    - ^^ the function T does not depend on time!!!_ == stationary
  - **space of actions for each state may be different**: A(s) or A 
    - ^^(dependent on state, current state? all the past?)
  - **reward/the FEEDBACK!**: R(s), R(s,a), R(s,a,s')
    - ^^ the usefulness of entering into the state/utility?
  - **policy/the command: THE OPTIMAL ACTION TO TAKE**: a solution to the MDP problem.
    - ^^ 
    - SL is like <s,a>, <s,a>, <s,a>...
    - RL is like <s,a,r>, <s,a,r>, <s,a,r>...!!! HERE, the `r` is the *feedback!*

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

