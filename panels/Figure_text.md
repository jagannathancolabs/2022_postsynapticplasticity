## Supplementary figure legend:
* Supplementary Figure 9. \
(a) Example MBON with pre,postsynapses overlaid on alpha, gamma lobes of the mushroom body. \
(b) Example synapses wherein two different KCs in the presynaptic side connects to the same MBON on the postsynaptic side. \
(c) In this example synapse, a KC in the presynaptic site is connected to only one type of MBON, while the rest of the neurons on the postsynaptic site are KCs. \
(d) In this example synapse, a KC in the presynaptic site is connected to multiple types of MBONs on the postsynaptic site.\
(e) The proportion of number of neurons per postsynaptic site (KCs on the presynaptic site) for MBON-M4.\
(f) The proportion of number of neurons per postsynaptic site (KCs on the presynaptic site) for MBON-M6.\
(g) The proportion of number of neurons per postsynaptic site (KCs on the presynaptic site) for MBON-α′3.\
(h) Percentage of different types of neurons present in the postsynaptic site along with a specific MBON. This provides information on what neurons on the postsynaptic site could the specific MBON be cross talking with. For example for MBON-M4 about 15% of the postsynapses are shared with KCa'b'-ap2.


## Methods description:
For the below EM analysis we used the partial connectome of the female adult fly brain (hemibrain v1.2.1) [1] using the neuprint-python package (Python, https://github.com/connectome-neuprint/neuprintpython).\
The main goal of this analysis was to understand how within a single synapse (where presynapses are KCs), different types of neurons (along with MBONs) can be residing on the postsynaptic site.\
First, we fetched KCs which have status as 'Traced' in the connectome.\
Second, for each specific MBON, we obtained the relevant KCs connected to it (a subset of the count in the previous step).\
Third, for the KCs obtained in the previous step, we identified all the synaptic connections (x,y,z locations of synapses) residing on the postsynaptic side to them.\
Fourth, for the specific MBON, we counted the number of postsynaptic connections per presynapse(that also contain the specific MBON) (Fig Suppl 9(d,e,f)).\
Fifth, we identified the relevant composition of the co-occuring neurons (identified in the postsynapses in the previous step)(Fig Suppl 9(g)).

## References:
[1] Scheffer, L. K. et al. A connectome and analysis of the adult Drosophila central brain. eLife 9, e57443 (2020).
