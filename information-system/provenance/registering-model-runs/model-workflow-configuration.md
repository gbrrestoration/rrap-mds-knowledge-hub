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

{% include warning.html content="From this point on, it is assumed that you know how to use the entity registry to create, update, find and share entities. If not, you should see our documentation <a href=\"../registry/index.html\">here</a> before proceeding." %}

## Dataset Template

### What is a dataset template?

Dataset templates are referred to in model run workflow templates. They describe an expected set of data resources for a model run.

Sometimes the resources that should be present in a [dataset](../../data-store/overview) are consistent and predictable. We refer to these resources as **defined resources**. A defined resource has a predictable file path which doesn't change between model runs.

Sometimes, we know that a dataset will contain some resources, but we don't know the specific path to that data until the model run is created. We refer to these resources as **deferred resources**. A deferred resource has an unpredictable or variable file path which changes between model runs.

In the same way that model runs satisfy model run workflow templates, datasets (in the data store) satisfy dataset templates. When you register a model run, you will need to provide for each dataset template:

-   a [data store](../../data-store/overview) dataset ID which refers to a registered dataset which conforms to the template
-   the file path of any deferred resources - the resource is identified by a unique key

Dataset templates are reusable and can (and should) be shared. If two models refer to a common input, they can reference a shared dataset template which describes the purpose and resources of that input.

It may be worth noting the following when deciding how to structure your dataset and workflow templates:

-   a dataset template must be satisfiable by a **single** dataset (you can't combine datasets together to satisfy a dataset template)
-   if your model uses a shared dataset which other modellers are likely to use (or already do), consider creating a distinct dataset template which refers to this dataset so that you can share your work with other modellers more easily
-   you don't always have to satisfy a dataset template with the same dataset in different model runs. For example - you may define a 'reef geometry file' dataset template which contains a 'reefs.json' GeoJSON file. Different model runs could use a different dataset which contains a different version of this file.
-   a single dataset may satisfy multiple dataset templates within a model run record. For example, you may have two dataset templates, one defines a configuration file with a deferred resource with key "config_file", another defines a parameter file with a defined resource "model_params.json". A model run could provide a single dataset which contains a "model_params.json" file and a config file with name "config_2012_2030.json" file, satisfying both templates.

### How do I register a dataset template?

If the dataset template you are creating refers to shared input data that multiple models likely reference, it is worth [exploring the registry](../registry/exploring_the_registry) to see if others have registered a dataset template you could reuse.

To begin registration, navigate to the new entity form (for help, see [registering an entity](../registry/registering_and_updating.html)). Select the "Dataset Template" entity type. Information on the various metadata fields has been provided below.

-   **Display Name**\*: A user friendly, brief name for this dataset template? E.g. "Connectivity Matrices Input Template"
-   **Description**\*: A description which helps you and other users understand the purpose, contents and resources of this dataset template.

**Defined Resources**

Each dataset template contains a list of defined resources - to add a new defined resource, use the "Add Item" button under "Defined Resources". Each defined resource (you can add as many as you need) includes the following information:

-   **Path**\*: What is the path of this resource within the dataset. All paths must use the unix path syntax, use "/" as a separator, and begin at the root of the dataset e.g. "data/connectivity/file.txt". If you need to refer to a numerous set of files, you can either refer to the folder and describe it's contents in the description (see "Is Folder" below), or use a blob style path e.g. "connectivity\_\*.nc". If the path of the resource changes between model runs, considering using a deferred resource instead!
-   **Description**\*: A description of the resource - this should help you and other users understand the purpose, contents and usage of this resource.
-   **Resource Usage Type**\*: Select a usage type from the drop down menu. This selection should describe how the resource/data is being used. If none of the options are suitable for your use case, consider getting in contact with us to expand the list of selections.
-   **Optional**: True or false - if checked, the resource is considered optional. Non optional resources **must** be present in the dataset. Optional resources are sometimes present in the dataset.
-   **Is Folder**: True or false - if checked, the path must refer to a folder. This option is useful if you would like to describe a collection of files in a folder, rather than listing out every individual file.
-   **Additional Metadata**: If you would like to add additional key, value annotations to this resource, you can do so by ticking "Add annotations?" and using the "+" and "-" buttons to add and remove them. Annotations must have a key and value provided, and the keys must be unique within the resource. These annotations will be searchable which can assist you and others in discovering this entity when [exploring the registry](../registry/exploring_the_registry).

**Deferred Resources**

The registration details for a deferred resource are the same as a defined resource (above), with one exception:

-   the **path** is unknown at dataset template registration time - instead, we define a **key** which is a unique (within the entity) identifier for the deferred resource. Choose a key that will help you remember which resource is which when using the template later in the provenance workflow.

Once you have completed your registration, you can view the record and take note of the identifier (noting that you can find your entity again at any time by [exploring the registry](../registry/exploring_the_registry.html)).

## Model Run Workflow Template

### What is a model run workflow template?

TODO definition

### How do I register a model run workflow template?

TODO process
