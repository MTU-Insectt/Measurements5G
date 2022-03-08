# Measurements5G
This repository contains CSV files of 5G NSA measurements recorded in the scope of the InSecTT project

Data5G_151221.csv contains data recorded on 15 December 2021 in and around Cork city centre

Data5G_171221.csv contains data recorded on 17 December 2021, travelling on a route MTU -> CUH -> UCC -> MTU

Data5G_static4Gonly_110122.csv contains data recorded on 11 January 2022, in a static location on MTU campus where only 4G coverage was available.
It is included here to represent a situation where the 5G modem has no access to 5G.

Data5G_static5G_070322.csv contains data recorded on 07 March 2022, in a static location in Cork City where 5G coverage was available.
Note that the data rates in this measurement are relatively low, which can be explained by the 5G channel parameters also being low, indicating borderline coverage in this static location.

The folder "cleaned" contains the same recordings, but with three kinds of entries removed:
- The first few samples before traffic generation started
- Any lines where no channel parameters were obtained (i.e. all parameters are zeros)
- Any lines where the sent bytes parameter could not be obtained from the modem, and the next line in each of those cases (missing sent bytes parameter leads to miscalculated data rates)
