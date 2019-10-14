# galaxy-provenance-capture
Retrospective provenance capturing from Galaxy workflow invocations.

This project focus on producing a workflow-centric executable RO-crate from a workflow execution performed using a Galaxy instance. 	
This approach enables the complete sharing of a computational analysis performed using Galaxy in a format that allows re-running the analysis using any other Galaxy instance.

- The initial version of this tool starts from a workflow invocation id and extracts all information required to reproduce the analysis including the workflow definition, inputs, outputs and a capture of the retrospective provenance.  

- The files from the workflow definition and its retrospective provenance trace are then organized using the ligthweight packaging format RO-crate (https://github.com/ResearchObject/ro-crate).

- With the aim of improving interoperability, the RO-crate object created is extended with a CWL-abstract representation obtained from the Galaxy workflow file (see https://github.com/ieguinoa/cwl-from-galaxy for methodology).

- In case the executed workflow was derived from a reference workflow (coming from an external workflow repository: e.g the ones in https://github.com/usegalaxy-be/workflow-repository) then the RO-crate can also be extended to point to that reference workflow object from which this specific enactment was derived. 

- This repo contains also the required scripts to reproduce the workflow execution in a different Galaxy instance, starting from an RO-crate object.

- More info and discussion of the plans about this repo can be found at: https://github.com/ResearchObject/ro-crate/issues/21 and https://github.com/ieguinoa/galaxy-provenance-capture/issues/1



# Tests/examples

- Under the dir examples there is a set of directories, each corresponding to a reference workflow. Under each of these there are directories containing:
	- Directories named ro-crate-reference-workflow: Contain the RO-crate package associated with the reference workflow.
	- Directories named ro-crate-runX: These directories contain RO-crate packages derived from indepedent executions of the workflow and contain: input and output files, reference data, provenance trace, etc.

- RO-create folder structures
