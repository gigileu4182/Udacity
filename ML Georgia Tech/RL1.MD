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
