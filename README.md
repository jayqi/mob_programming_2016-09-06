# Mob Programming - Sept 6, 2016

At Chi Hack Night in Chicago, IL

Here is the Jupyter notebook from our mob programming session, with some annotations added after the fact, for clarity.

The object was to compare these two datasets of complaints against police officers in the [chicago-police-data repository](https://github.com/invinst/chicago-police-data):
* Older data on [Citizen's Police Data Project](https://cpdb.co) (in repo, [/cpdb_complaints-cpd/](https://github.com/invinst/chicago-police-data/tree/master/cpdb_complaints-cpd))
* Data obtained recently in June 2016 by FOIA (in repo, [/complaints-cpd-june2016/](https://github.com/invinst/chicago-police-data/tree/master/complaints-cpd-june2016))

These two datasets contained some of the same information but were obtained at different times from the police department. For complaint cases overlapping between the two sets, we wanted to identify if the incident categorization changed over time. (The police department might recategorize incidents.)

## Results

Number of CRIDs in CPDB:  39591
Number of CRIDs in June 2016:  16531
Number of overlapping CRIDs:  2729

Number of rows for overlapping CRIDs with both non-null cat codes:  5505

Number of overlapping CRIDs with both non-null cat codes:  2293
Number of mismatches:  67

It looks like we were still having some multiple rows because we kept the Accused_Name and there are multiple accused officers for each CRID. So there were 67 unique CRIDs between the two sets where the categories changed, out of 2729 overlapping cases. This doesn't include cases where categories were not set for one or the other. 
