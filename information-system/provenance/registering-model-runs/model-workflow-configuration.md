---
layout: default
title: Model workflow configuration
nav_order: 2
has_children: false
grand_parent: Provenance
parent: Registering model runs
---

{: .no_toc }

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

# Model workflow configuration

## Overview

Registering a model run record requires referring to configuration entities which describe:

-   the model being run
-   the expected inputs of the model run
-   the expected outputs of the model run

This configuration is contained in two critical entities.

The [model run workflow template](#model-run-workflow-template) provides a blueprint or template for a modelling activity which consumes inputs, and produces outputs using a particular [model](./establishing-required-entities#model) at a particular point in time (version). Model run workflow templates point to input and output dataset templates.

The [dataset template](#dataset-template) provides a blueprint for a dataset which is _instantiated_ or _satisfied_ at model run registration time. Dataset templates usually specify a set of _resources_ (files and/or folders) which must be provided in the conforming dataset.

{% include notes.html content="It may be useful to consider templates as <i>containers</i> of a particular shape, which provide a structure to the data which is <i>instantiated</i> in a model run record. Templates (dataset and workflow) are reusable (see <a href=\"./establishing-required-entities#when-to-create-and-when-to-reuse\">occurants vs continuants</a> for more discussion about entity reusability), while model run records are not.
" %}

Before proceeding, an understanding about the inputs and outputs of your model will be required, consider:

-   what data/inputs are required to run the model?
-   what parameters/configuration are required to run the model?
-   what is consistent between model runs, and what changes?
-   what outputs are produced by the model, is this consistent?

More information about [dataset templates](#dataset-template) and [model run workflow templates](#model-run-workflow-template) are provided below.

## Prerequisites

Please ensure that you have registered and/or identified the [required entities](./establishing-required-entities) before proceeding. This includes:

-   [Model](./establishing-required-entities#model)
-   [Organisation](./establishing-required-entities#organisation)
-   [Person](./establishing-required-entities#person)

You will also require permission to **write** into the provenance store and registry.

For more information about how to access the system, see [requesting access](../../getting-started-is/requesting-access-is) and [logging in](../../getting-started-is/logging-in).

## Dataset Template

### What is a dataset template?

Dataset templates are referred to in model run workflow templates. They describe an expected set of data resources for a model run.

Sometimes the resources that should be present in a [dataset](../../data-store/overview) are consistent and predictable. We refer to these resources as **defined resources**. A defined resource has a predictable file path which doesn't change between model runs.

Sometimes, we know that a dataset will contain some resources, but we don't know the specific path to that data until the model run is created. We refer to these resources as **deferred resources**. A deferred resource has an unpredictable or variable file path which changes between model runs.



Dataset templates are reusable and can (should) be shared. If two models refer to a common input, they can reference a shared dataset template which describes the purpose and resources of that input.

### How do I register a dataset template?

TODO registration process

## Model Run Workflow Template

### What is a model run workflow template?

TODO definition

### How do I register a model run workflow template?

TODO process
