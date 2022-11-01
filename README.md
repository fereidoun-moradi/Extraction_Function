# Extraction_Function


![toolset (2)](https://user-images.githubusercontent.com/45528113/199217821-f1f13995-c50d-4d2a-8b61-2e1594b15981.jpg)




The <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/extraction_function">function</a> extracts a list of tau (silent) transtions 
from the mapped state space (aut file) based on a list of observable actions. The output list can be used in mCRL2 tool for reducing the transtion system based on difference equivalence relationships.


# Example 1.
A mappped state space of a <a href="https://github.com/fereidoun-moradi/Abstraction-tool/blob/main/RV-Example.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/RV_Example.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile.aut">mapped state space (aut file)</a>


A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions.txt">observable actions</a>

Output (i.e., tau transtions): heating_[20_true_false_]


![Screenshot 2022-08-28 at 16 34 01](https://user-images.githubusercontent.com/45528113/187079441-b0a7669a-6f8a-48f2-bb1d-fc9182e52985.png)

# Example 2.
The diagram of the messages passing between actors defined in a <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">Timed Rebeca</a>  model of a room temperature control system.

![diagram_actors_messages](https://user-images.githubusercontent.com/45528113/198962230-89231591-082f-4591-b449-b58471ea3488.jpg)

First, the state space of the Timed Rebeca is mapped using <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">cast function</a>.
The mappped state space of the Timed Rebeca model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/state_transition_diagram.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile_exp2.aut">mapped state space (aut file)</a>

(The state space includes 76 states and 103 transtions.)

(the maped state space (aut file) contains 103 states and 129 transtions.)

Second, the extraction function uses the maped state space (aut file) and a list of observable actions to generate tau transitions. 
A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions_exp2.txt">observable actions</a>

Output: <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/tau_transitions_exp2.txt">tau transitions</a>

(This list shows tau transitions for reducing the casted_LTS based on equivalence relationships.)


![Screenshot 2022-10-31 at 10 11 53](https://user-images.githubusercontent.com/45528113/198972831-22fd55fc-ffb1-442d-b6e4-eca6a1a7b06c.png)


The output list above shows tau transitions.
The reduced model is generated based on tau transitions and tau_star equivalence relationship (i.e., weak trace equivalence) in <a href="https://github.com/fereidoun-moradi/mCRL2">mCRL2 tool</a>.

The reduced state space (<a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/OneRoomTemp_mode_casted_tau_star.lts">aut file</a>): <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/abstracted_LTS_exp2.png">abstracted_LTS_diagram</a>. (It contains 49 states and 71 transtions.)


# Example 3.
The diagram of the messages passing between actors defined in a <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/SWaT_Time_WithoutAttacks.rebeca">Timed Rebeca</a> model of a secure water treatment system.

![diagram_actors_messages_swat drawio](https://user-images.githubusercontent.com/45528113/199199300-2946742b-285a-46f4-b825-2d81adfcd6ee.png)

First, the state space of the Timed Rebeca is mapped using <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">cast function</a>.
The mappped state space of the Timed Rebeca model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/SWaT_Time_WithoutAttacks.pdf">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile_exp3.aut">mapped state space (aut file)</a>

(The state space of the Timed Rebeca model includes 688 states and 1825 transtions)

(The mapped state space (aut file) contains 760 states and 1896 transtions)
![Screenshot 2022-11-01 at 10 31 59](https://user-images.githubusercontent.com/45528113/199203830-1efc2b37-976d-4a3d-8807-baec7d2ff869.png)


Second, the extraction function uses the maped state space (aut file) and a list of observable actions to generate tau transitions. 

A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions_exp3.txt">observable actions</a>

Output: <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/tau_transitions_exp3.txt">tau transitions</a>

(This list shows tau transitions for reducing the casted_LTS based on equivalence relationships.)

The output list above shows tau transitions.
The reduced model is generated based on tau transitions and tau_star equivalence relationship (i.e., weak trace equivalence) in <a href="https://github.com/fereidoun-moradi/mCRL2">mCRL2 tool</a>.

The reduced state space (<a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/SWaT_Time_WithoutAttacks_casted_v2_tau_star.lts">aut file</a>): <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/reduced_state_space_swat.png">abstracted_LTS_diagram</a>. (It contains 62 states and 90 transtions.)

