# extraction_Function
The <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/extraction_function">function</a> extracts a list of tau (silent) transtions 
from the mapped state space (aut file) based on a list of observable actions. The output list can be used in mCRL2 tool for reducing the transtion system based on difference equivalence relationships.


# Example.
A mappped state space of a <a href="https://github.com/fereidoun-moradi/Abstraction-tool/blob/main/RV-Example.rebeca">Timed Rebeca</a> model (<a href="https://github.com/fereidoun-moradi/cast_function/blob/main/RV_Example.png">state dransition diagram</a>): <a href="https://github.com/fereidoun-moradi/cast_function/blob/main/castfile.aut">mapped state space (aut file)</a>

A list of observable actions:  <a href="https://github.com/fereidoun-moradi/Extraction_Function/blob/main/observable_actions.txt">observable actions</a>

Output: heating_[20_true_false_]


![Screenshot 2022-08-28 at 16 34 01](https://user-images.githubusercontent.com/45528113/187079441-b0a7669a-6f8a-48f2-bb1d-fc9182e52985.png)
