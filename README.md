# Extraction_Function


![toolset2](https://user-images.githubusercontent.com/45528113/199018279-066288d4-5203-4760-9954-371946a72510.jpg)




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

First, the state space of the Timed Rebeca is mapped using <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">cast function</a>.
The mappped state space of the <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/state_transition_diagram.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile_exp2.aut">mapped state space (aut file)</a>


Second, the extraction function uses the maped state space (aut file) and a list of observable actions to generate tau transitions. 
A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions_exp2.txt">observable actions</a>

Output (tau transitions): 

status_[22_],sense_[22_],status_[21_],status_[23_],sense_[21_],sense_[23_],heating_[20_],status_[20_],sense_[20_],cooling_[24_],status_[24_],sense_[24_]
(This list shows tau transitions for reducing the casted_LTS based on equivalence relationships.)


![Screenshot 2022-10-31 at 10 11 53](https://user-images.githubusercontent.com/45528113/198972831-22fd55fc-ffb1-442d-b6e4-eca6a1a7b06c.png)


The output list above shows tau transitions.
The reduced model is generated based on tau transitions and tau_star equivalence relationship (i.e., weak trace equivalence) in <a href="https://github.com/fereidoun-moradi/mCRL2">mCRL2 tool</a>.

The reduced state space (<a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/OneRoomTemp_mode_casted_tau_star.lts">aut file</a>): <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/abstracted_LTS_exp2.png">abstracted_LTS_diagram</a>. (It contains 49 states and 71 transtions.)


# Example 3.
The diagram of the messages passing between actors defined in a model of a secure water treatment system.

![diagram_actors_messages_swat drawio](https://user-images.githubusercontent.com/45528113/199199300-2946742b-285a-46f4-b825-2d81adfcd6ee.png)

First, the state space of the Timed Rebeca is mapped using <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/OneRoomTemp_mode.rebeca">cast function</a>.
The mappped state space of the <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/SWaT_Time_WithoutAttacks.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/SWaT_Time_WithoutAttacks.pdf">state dransition diagram</a>, (The state space of the Timed Rebeca model includes 688 states and 1825 transtions)): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile_exp3.aut">mapped state space (aut file)</a>


![Screenshot 2022-11-01 at 10 31 59](https://user-images.githubusercontent.com/45528113/199203830-1efc2b37-976d-4a3d-8807-baec7d2ff869.png)


Second, the extraction function uses the maped state space (aut file) and a list of observable actions to generate tau transitions. 

A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions_exp3.txt">observable actions</a>

Output (tau transitions): 

sensor1_sense_[1_1_1_],sensor2_sense_[1_1_1_],sensor3_sense_[1_1_1_],tank1_status_[1_1_1_],tank2_status_[1_1_1_],tank3_status_[1_1_1_],sensor1_reportstatus_[1_1_1_],sensor2_reportstatus_[1_1_1_],sensor3_reportstatus_[1_1_1_],plc1_openreq_[1_1_1_],tank1_waterincrease_[1_1_1_],tank1_waterdecrease_[2_1_1_],tank1_status_[2_1_1_],tank2_waterincrease_[2_1_1_],sensor1_reportstatus_[2_1_1_],tank2_status_[2_1_1_],sensor2_reportstatus_[2_1_1_],tank1_waterdecrease_[2_2_1_],tank1_status_[2_2_1_],tank2_waterincrease_[2_2_1_],sensor1_reportstatus_[2_2_1_],tank2_status_[2_2_1_],tank3_waterincrease_[2_2_1_],sensor2_reportstatus_[2_2_1_],tank3_status_[2_2_1_],sensor3_reportstatus_[2_2_1_],plc1_closereq_[2_2_1_],plc3_onreq_[2_2_1_],tank1_status_[2_2_3_],sensor1_reportstatus_[2_2_3_],tank3_waterdecrease_[2_2_3_],tank2_waterincrease_[2_2_3_],tank3_status_[2_2_3_],cleanwater_[2_2_3_],tank2_status_[2_2_3_],sensor3_reportstatus_[2_2_3_],sensor2_reportstatus_[2_2_3_],tank1_status_[2_3_3_],tank2_waterdecrease_[2_3_3_],tank1_status_[2_3_1_],tank2_waterdecrease_[2_3_1_],sensor1_reportstatus_[2_3_3_],tank2_status_[2_3_3_],sensor1_reportstatus_[2_3_1_],tank2_status_[2_3_1_],sensor2_reportstatus_[2_3_3_],sensor2_reportstatus_[2_3_1_],plc1_openreq_[2_2_1_]
(This list shows tau transitions for reducing the casted_LTS based on equivalence relationships.)

The output list above shows tau transitions.
The reduced model is generated based on tau transitions and tau_star equivalence relationship (i.e., weak trace equivalence) in <a href="https://github.com/fereidoun-moradi/mCRL2">mCRL2 tool</a>.

The reduced state space (<a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/SWaT_Time_WithoutAttacks_casted_v2_tau_star.lts">aut file</a>): <a href="https://github.com/fereidoun-moradi/extraction_Function/blob/main/reduced_state_space_swat.png">abstracted_LTS_diagram</a>. (It contains 62 states and 90 transtions.)

