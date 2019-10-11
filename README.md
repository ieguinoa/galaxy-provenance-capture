# galaxy-provenance-capture
Retrospective provenance capturing from Galaxy workflow invocations


- The initial version of this tool starts from a workflow invocation id and extracts all information required to reproduce the analysis. 

- The provenance information is then wrapped in the ligthweight packaging format ro-crate (https://github.com/ResearchObject/ro-crate).

- The ro-crate object is extended with metadata obtained from the Galaxy workflow file (see https://github.com/ieguinoa/cwl-from-galaxy) and the input data.

- In case the executed workflow was derived from a reference workflow (e.g the ones in https://github.com/usegalaxy-be/workflow-repository) then the ro-crate can also be extended to point to that reference workflow object from which this specific enactment was derived 

- This repo contains also the required scripts to reproduce the workflow execution in a different Galaxy instance, starting from an ro-crate object. 

