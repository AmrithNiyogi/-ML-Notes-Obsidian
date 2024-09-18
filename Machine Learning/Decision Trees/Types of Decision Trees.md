- ID3:
	- Categorical features that will yield the largest information gain for categorical targets
- C4.5:
	- Successor to ID3. 
	- Removes restriction that features must be categorical by dynamically defining a discrete attribute (based on numerical variables) that partitions the continuous attribute values into discrete intervals.
- CART:
	- Similar to C4.5, but it differs in that it supports numerical target variables(regression), uses the Gini Index measure.