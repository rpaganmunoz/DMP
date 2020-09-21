# Introduction

A Data Management Plan (DMP) is a formal document that outlines how data are to be handled both during a research project, and after the project is completed. 
It is the essential reference to assure the Findability, Accessibility, Interoperability, and Reuse [(FAIR)](https://www.go-fair.org/fair-principles/) of digital assets, 
stablishing the format of data and metadata, how they is generated, stored and accessed, among other issues.  
Currently, DMPs are mandatory for data-science and e-science founded grants, and indispensable for the sutentability of any long-term project.

DMPs will be living documents that will be amended, improved and detailed along the project timeline. Therefore, DMPs should have a clear version number and include a
timetable for updates. The DMPs should been defined according to the template of the [DMP Online tool](https://dmponline.dcc.ac.uk/), 
but they could derivate into structured documents, as long as maintain a unity.

# The LAGO Data Management Plan (DPM)

Published in EU Deliverable EOSC-SYNERGY-D4.1 "Best Practices Elicitation including Data Management Plans" (EOSC-SYNERGY – H2020 RIA 857647)

|Version|Date|Contributors|
|-------|----|------------|
|1.0|17/2/2020|Antonio Juan Rubio Montero (CIEMAT), Rafael Mayo (CIEMAT)|

## A. Data summary

Provide a summary of the data addressing the following issues:

● **State the purpose of the data collection/generation**. The Latin American Giant Observatory
(LAGO) is an extended cosmic ray observatory composed of a network water-Cherenkov
detectors (WCD) spanning over different sites located at significantly different altitudes and
latitudes. The measurements collected from these detectors are posteriorly processed and
analysed. Additionally, scientists continuously generate simulated data. The final purpose is to
enable the long-term curation and re-use of data within and outside the LAGO Collaboration
through a Virtual Observatory.

● **Explain the relation to the objectives of the project**. European Commision requires open access
to the results obtained from their funded projects, meanwhile EOSC-Synergy is a H2020 project
that encourages the implementation of FAIR policies as another standard in research. Since the
LAGO computation is included in the EOSC-Synergy as one of their Thematic Services, generated
or stored data in its resources must observe these guidelines, being also beneficial for the
success of both initiatives.

● **Specify the types and formats of data generated/collected**. CORSIKA outputs described in the
official documentation [D. Heck and T. Piero, "Extensive Air Shower Simulation with CORSIKA: A
User’s Guide". Version 7.7100 from December 17, 2019], section 10, page 121. Available at
https://web.ikp.kit.edu/corsika/usersguide/usersguide.pdf

● **Specify if existing data is being re-used (if any)**. Measurements from WCDs gathered in previous
years.

● **Specify the origin of the data**.
○ Raw data (L0) from WCDs.

○ Preliminary data (L1) obtained cleaning raw data (L0).

○ Quality data (L2, L3) obtained analysing and fixing preliminary data (L1).

○ Simulated from standalone CORSIKA runs by researchers.

● **State the expected size of the data (if known)**. Minimal data-set is one hour of measurement or
simulation:
○ Raw data (L0): ~200MB
○ Preliminary data (L1): ~100MB
○ Quality data (L2, L3): ~ 30 MB
○ Simulated (background): ~ 10GB
○ Simulated (event): ~ 100GB

● **Outline the data utility: to whom will it be useful**. Data are of interest for the Astrophysics
community but also for other scientific or industrial areas such as High Energy Physics, Life
Sciences, Weather Forecasting, Aerospatial security or Computer Science, among others,
because the effects of cosmic radiation on natural life, materials, or climate change.

## B. FAIR data

### Making data findable, including provisions for metadata:

● **Outline the discoverability of data (metadata provision)**. Specific LAGO wrappers execute the
processing or simulation and posteriorly check the data-sets and will store them in EGI DataHub
always with their metadata to allow gathering by services such as B2FIND.

● **Outline the identifiability of data and refer to standard identification mechanism**. Do you
make use of persistent and unique identifiers such as Digital Object Identifiers? Data-sets will
be referenced by PIDs automatically requested through EOSC B2Handle service.

● **Outline naming conventions used**. It should be based in the metadata values but an approach
for clear versioning is being discussed.

● **Outline the approach towards search keywords**. Searching should be based on any metadata
value.

● **Outline the approach for clear versioning**. It should be based on the metadata An approach for
clear versioning is being discussed.

● **Specify standards for metadata creation (if any)**. If there are no standards in your discipline
describe what metadata will be created and how

### Making data openly accessible:

● **Specify which data will be made openly available? If some data is kept closed provide
rationale for doing so**. Data will be made publicly available after a variable waiting (embargo)
period similar to the established ones for other large experiments.

● **Specify how the data will be made available**. Consolidated data-sets that are stored in EGI
DataHub will be exposed together with their metadata to be gathered by services such as
B2FIND.

● **Specify what methods or software tools are needed to access the data? Is documentation
about the software needed to access the data included?** Is it possible to include the relevant
software (e.g. in open source code)? . To take advantage of the data published, researchers
should use the CORSIKA tools included in the source code and described in the official
documentation in section 10, page 121 at
https://web.ikp.kit.edu/corsika/usersguide/usersguide.pdf

● **Specify where the data and associated metadata, documentation and code are deposited**.

○ Data and metadata will be stored in EGI DataHub service (OneData technology)

○ CORSIKA documentation and source code https://web.ikp.kit.edu/corsika/

● **Specify how access will be provided in case there are any restrictions**. Data will be only
accessible by the author and/or the Collaboration making during embargo period use of EGI AAI.

### Making data interoperable:

● **Assess the interoperability of your data**. Specify what data and metadata vocabularies,
standards or methodologies you will follow to facilitate interoperability. Metadata follows the
Dublin Core schema ( http://dublincore.org ), extending the vocabulary with the elements the
described in [H. Asorey et al. The LAGO: A Successful Collaboration in Latin America Based on
Cosmic Rays and Computer Science Domains, in Proc. 16th IEEE/ACM CCGrid, 2016,
https://doi.org/10.1109/CCGrid.2016.110 ].

○ Common for all metadata: site contains the name, latitude, longitude and height of the
WCD or the simulated ground point.

○ WCD metadata scheme adds: data corresponds to the version/type of the Digit/Analog
electronic board; voltage, level and sensor.

○ Simulation metadata adds: primary described by the CORSIKA input file DATXXXX.dbase;
libraries indicating which are the included CORSIKA libraries; computation describing the
computational environment by unix command: uname -a , lsb_release -a , free and gcc -v .

● **Specify whether you will be using standard vocabulary for all data types present in your data
set, to allow inter-disciplinary interoperability? If not, will you provide mapping to more
commonly used ontologies?** In principle, only support CORSIKA outputs as described in the
official documentation, but we can consider translating files to standardised formats in the
future.

### Increase data re-use (through clarifying licenses):

● **Specify how the data will be licenced to permit the widest reuse possible**. They will be
published under BSD-3 or CC license.

● **Specify when the data will be made available for reuse. If applicable, specify why and for what
period a data embargo is needed**. LAGO Collaboration requires a waiting period similar to the
established ones for other large experiments. Such a period should be set not only to properly
exploit results by the Consortium prior to their availability, but because raw data measured
must be pre-processed by the Consortium to make them 'understandable’. Simulations will be
available too, but it would be valuable that the waiting period could be set by the user, because
he is the owner of the data. The embargo period is set for a year in general, but depends of the
data type, specifically:

○ L0, L1: private while analysed data are not publicly available.

○ L2, L3: a year.

○ Simulated data: a year maximum, the owner can decide to open the data before the end
of this period.

● **Specify whether the data produced and/or used in the project is usable by third parties, in
particular after the end of the project? If the re-use of some data is restricted, explain why**.
There is no restriction after the embargo period.

● **Describe data quality assurance processes**. Only the data measured by WCDs or generated
using software versions officially released by LAGO will be stored and exposed in repositories.
Previously to the publication, a robot of the Virtual Organization will check the minimal accuracy
of data.

● **Specify the length of time for which the data will remain re-usable**. Indefinitely after the
waiting period.

## C. Allocation of resources

Explain the allocation of resources, addressing the following issues:
● **Estimate the costs for making your data FAIR. Describe how you intend to cover these costs**.
The process of making the data FAIR will be supported by the EOSC-Synergy project. The human
cost of the management will be supported by LAGO Collaboration.

● **Clearly identify responsibilities for data management in your project**. Computing as data
management will be structured as a Virtual Organization with specific roles for data acquisition
and processing.

● **Describe costs and potential value of long term preservation**. Preservation of data-sets is
essential for the sustainability of LAGO. Every active WCD should generate 300GB/month of
L0-L3 data. Currently, due to the number of active WCDs, the Collaboration will generate up to
27 TB of L0-L3 data, plus 12-120 TB of simulated data throughout the year. Data should be
replicated, at least, in two locations of a distributed repository (in this case OneData).
Considering an average generation of 60TB/year, the costs of long-term preservation for 4 years
are the hardware (two generic RAID servers ~240TB = ~30k€, prices in 2019), the consumption
(3.68KW max. power for 2 servers, ~ 0.1 €/kWh industrial price average in 2019 = max. 13k€)
and human resources (technician: 1 person/month, scientific: 2 p/m, ~10k€).

## D. Data security

Address data recovery as well as secure storage and transfer of sensitive data. There is no sensitive
data, thus anonymization and encryption of the data is not required. Data recovery should be
guaranteed by means of replication, at least, in two locations of a distributed repository or filesystem (in
this case OneData).

## E. Ethical aspects

Data do not contain protected records that could present ethical or security issues. The only personal
data included is the required by FAIR policies in metadata, this is, the name and identifier of the author
of the data-set. On the other hand, there are no issues with reusing previous raw data generated in
LAGO, as well as the data belonging to the Collaboration.


