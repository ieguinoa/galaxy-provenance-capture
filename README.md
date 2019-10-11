# galaxy-provenance-capture
Retrospective provenance capturing from Galaxy workflow invocations


- The initial version of this tool starts from a workflow invocation id and extracts all information required to reproduce the analysis. 

-The provenance information is then wrapped in a ligthweight packaging format ro-crate (https://github.com/ResearchObject/ro-crate) including also metadata obtained from the Galaxy workflow file (https://github.com/ieguinoa/cwl-from-galaxy) and the input data.



