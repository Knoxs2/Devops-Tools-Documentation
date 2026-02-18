# CodePipeline Notes

Documentation reference: https://docs.aws.amazon.com/codepipeline/

## Useful information

* Integrates better with AWS resources
* There is nothing different than other CI/CD tools available on the market


## Components of CodePipeline

### Pipeline

Same as jenkins, a Workflow on Actions, Same as Azure Devops pipelines


### Stages

Each pipeline has a number of stages, which a logical unit where changes can be made to the artifact

### Transitions

Consist in an action that is called after a Stage is finished, can be disabled, can run multiple in series where the last one executes only when all of the previous defined finish

### Actions
Set of operations that are pre-defined by providers, they can facilitate Stage execution as quick option to do a pre-defined list of "processes"
Examples: source, build, test, deploy, approval, invoke

### Pipeline Executions
Basically status of each Pipeline

### Artifacts
Every collection of data that is treated inside a pipeline, could be source code, definition files, templates

### Triggers

Events that are used to change status of a Pipeline, usually start it can  be integrated with AWS resources via Cloud Watch events, or third-parties

### Variables

hold values and can be declared on the Pipeline Level or Stage level

### Conditions
Can dictate how a Stage starts, or do an action when it fails or create specific conditions