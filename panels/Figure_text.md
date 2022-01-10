## Figure legend:
* Figure xx. Within and across synapse specificity in postsynaptic sites.\
Example synaptic sites wherein a Kenyon Cell (KC) in the presynaptic site connects to multiple neurons in the postsynaptic site: \
(a) Here only one type of Mushroom Body Output Neuron (MBON) is present in the postsynaptic site, thus indicating higher specificity and lower chance of cross-talk between different MBONs on the postsynaptic site.\
(b) Here multiple types of MBONs are present in the postsynaptic site, thus indicating lower specificity and higher chance of cross-talk between different MBONs on the postsynaptic site.\
(c) The proportion of postsynaptic sites (KCs on the presynaptic side) for each MBON wherein the corresponding MBON is present without any other MBON on the same postsynaptic site (only containing target MBON) is plotted against the proportion of postsynaptic sites wherein the corresponding MBON is present with other MBONs on the same postsynaptic site (with non-target MBON). Generally MBONs on the top left quadrant are highly specific within a postsynaptic site and those on the bottom right quadrant are not so specific within a postsynaptic site.\
(d) Different types of neurons present in the postsynaptic site along with a specific MBON. This provides information on what neurons on the postsynaptic site could the specific MBON be cross talking with. For example for MBON03 about 15% of the postsynapses are shared with KCa'b'-ap2.\
Across synapse specificity on the postsynaptic side (MBON) quantified by distance between synaptic sites: \
(e) Example synaptic sites wherein two different KCs in the presynaptic site connects to the same MBON on the postsynaptic site. The euclidean distance between the synaptic sites would be the run length of the MBON cable between them.\
(f) The closest KC distance pairings across different MBONs are plotted.


## Methods description:
For the below EM analysis we used the partial connectome of the female adult fly brain (hemibrain v1.2.1) [1] using the neuprint-python package (Python, https://github.com/connectome-neuprint/neuprintpython).
* Specificity within a synapse set\
The main goal of this analysis was to understand how within a single synapse (where presynapses are KCs), specificity can be 
acheived by MBONs residing on the postsynaptic site.\
First, we fetched KCs which are only connected to typed MBONs.
Second, for each specific MBON, we obtained the relevant KCs connected to it (a subset of the count in the previous step).
Third, for the KCs obtained in the previous step, we identified all the synaptic connections (x,y,z locations of synapses) residing on the postsynaptic side to them.
Fourth, for the specific MBON, we counted the number of postsynaptic connections that contain only them (only containing target MBON) and those that contain atleast one another type of MBON (with non-target MBON) and further divide both the counts by the count of the total postsynaptic locations (for normalisation (Fig xx (c)).
Fifth, for identifying the relevant composition of the non-target MBON types (identified in the previous step), we counted the different types of neurons that co-occur in for each postsynapse and divide by the overall number of co-occuring neurons (for normalisation)  (Fig xx (d)).

* Specificity across synapse set\
The aim here was to understand how across synapse sets (where presynapses are KCs and postsynapses are MBONs), specificity can be 
acheived by segregation of the synapses residing on the postsynaptic site.\
First, for each specific MBON, we obtained all the relevant upstream neurons including KCs.
Second, for the specific MBON, we obtained the synaptic connections residing on the MBON (postsynapses).
Third, for each postsynaptic location identify the locations wherein the KCs are on the presynaptic side.
Fourth, for each KC-MBON synaptic pair compute the euclidean distance to the nearest KC-MBON synaptic pair. To achieve specificity across the synaptic sites, such distances should be larger (thereby preventing cross-talk)  (Fig xx (e)).

## References:
[1] Scheffer, L. K. et al. A connectome and analysis of the adult Drosophila central brain. eLife 9, e57443 (2020).
