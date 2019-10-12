# galaxy-provenance-capture
Retrospective provenance capturing from Galaxy workflow invocations


- The initial version of this tool starts from a workflow invocation id and extracts all information required to reproduce the analysis including the workflow definition and a capture of retrospective provenance.  

- The files from the workflow definition and its retrospective provenance trace are then organized using the ligthweight packaging format RO-crate (https://github.com/ResearchObject/ro-crate).

- With the aim of improving interoperability, the RO-crate object created is extended with a CWL-abstract representation obtained from the Galaxy workflow file (see https://github.com/ieguinoa/cwl-from-galaxy for methodology).

- In case the executed workflow was derived from a reference workflow (coming from an external workflow repository: e.g the ones in https://github.com/usegalaxy-be/workflow-repository) then the RO-crate can also be extended to point to that reference workflow object from which this specific enactment was derived. 

- This repo contains also the required scripts to reproduce the workflow execution in a different Galaxy instance, starting from an RO-crate object.

- More info and discussion of the plans about this repo can be found at: https://github.com/ResearchObject/ro-crate/issues/21 and https://github.com/ieguinoa/galaxy-provenance-capture/issues/1

