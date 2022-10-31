# Extraction_Function
The <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/extraction_function">function</a> extracts a list of tau (silent) transtions 
from the mapped state space (aut file) based on a list of observable actions. The output list can be used in mCRL2 tool for reducing the transtion system based on difference equivalence relationships.


# Example 1.
A mappped state space of a <a href="https://github.com/fereidoun-moradi/Abstraction-tool/blob/main/RV-Example.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/RV_Example.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile.aut">mapped state space (aut file)</a>

A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions.txt">observable actions</a>

Output: heating_[20_true_false_]


![Screenshot 2022-08-28 at 16 34 01](https://user-images.githubusercontent.com/45528113/187079441-b0a7669a-6f8a-48f2-bb1d-fc9182e52985.png)

# Example 2.
The diagram of the messages passing between actors defined in a model of a room temperature control system.

![diagram_actors_messages](https://user-images.githubusercontent.com/45528113/198962230-89231591-082f-4591-b449-b58471ea3488.jpg)

A mappped state space of a <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/state_transition_diagram.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile_exp2.aut">mapped state space (aut file)</a>

A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions_exp2.txt">observable actions</a>

Output (tau transitions): 

status_[22_],sense_[22_],status_[21_],status_[23_],sense_[21_],sense_[23_],heating_[20_],status_[20_],sense_[20_],cooling_[24_],status_[24_],sense_[24_]
(This list shows tau actions for reducing the casted_LTS based on equivalence relationships.)


![Screenshot 2022-10-31 at 10 11 53](https://user-images.githubusercontent.com/45528113/198972831-22fd55fc-ffb1-442d-b6e4-eca6a1a7b06c.png)


