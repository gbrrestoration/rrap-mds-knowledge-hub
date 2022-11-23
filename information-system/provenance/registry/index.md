---
layout: default
title: Registry
nav_order: 5
has_children: true
grand_parent: Information System
parent: Provenance
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

# Registry

Click [here](https://registry.rrap-is.com){:target="\_blank"} to visit the RRAP M&DS IS Registry.

# What's on this page?

This guide will focus on providing information about the registry and it's purpose, while offering general guidance about registering, updating, exploring and sharing resources.

For detailed information about the types of entities and their metadata, see the relevant sections in the provenance documentation.

TODO - links here.

# What is the Registry?

The RRAP Information System Registry is a centralised location to register, update, explore and share [persistently identified](../../digital-object-identifiers.html) resources.

The Registry is a critical part of the [RRAP Provenance Store](../index.html) as it facilitates the creation of and linking between persistently identified artefacts of provenance, such as people, organisations, models and model runs.

# Accessing the registry

## Navigating to the registry

The Registry is hosted at [https://registry.rrap-is.com](https://registry.rrap-is.com).

## Logging in

Your user session is shared between all RRAP M&DS Components - you may already be logged in. If you are logged in, you will see a profile icon and email address in the upper right hand corner:

|                                      Logged in                                       |
| :----------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/logged_in.png" alt="drawing" width="800"/> |

If you are not logged in, you will see a "Click to Login" button in the upper right hand corner:

|                                      Not Logged in                                       |
| :--------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/not_logged_in.png" alt="drawing" width="800"/> |

The login process for the registry is the same as other components, see [logging in](../../getting-started-is/logging-in.html) for more information.

## Requesting access

The process of requesting access for the Registry is the same as other components. See [requesting access](../../getting-started-is/requesting-access-is.html) for more information.

# Registering an entity

**Link**: [https://registry.rrap-is.com/registerentity](https://registry.rrap-is.com/registerentity)

## Required Permissions

-   Registry Read
-   Registry Write

## Process

### Navigating to the Register Entity page

From the home page of the Registry, click the "Register a new entity" button, as shown below:

|                                   Register a new entity                                   |
| :---------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/register_start.png" alt="drawing" width="800"/> |

### Selecting an Entity Type

At the top of the page, you can select the entity type from the dropdown. Simply click on the dropdown and click on the desired type:

|                                   Select an entity type                                    |
| :----------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/register_select.png" alt="drawing" width="800"/> |

### Filling out the form

Once you have selected your entity type, the updated form will load.

Form fields will provide guidance on what is expected underneath the input field, for example:

|                                      Form caption                                       |
| :-------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/form_caption.png" alt="drawing" width="800"/> |

Form fields can be of various types:

-   **Text**: Text fields are either single or multi line input boxes. Simply click inside the box and type the desired text.
-   **Selection**: Some fields allow selection from a predefined list of inputs - click the dropdown and select the desired item from the list.
-   **Yes or No**: Yes or no (boolean) fields are displayed as a check-box. To indicate "yes" or "true", tick the box. Otherwise, leave the box unticked.
-   **List**: Some fields contain a list of items. To add an item to the list, use the "+ Add Item" button. To remove the item, use the "-" button on the right hand side. Both buttons are shown below.

|                                      Add item                                       |
| :---------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/add_item.png" alt="drawing" width="800"/> |

|                                      Remove item                                       |
| :------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/remove_item.png" alt="drawing" width="800"/> |

-   **Other Entities**: Some entity types require references to other registered entities. To help this process, the form allows you to search for resources of a specific type based on their properties. You can search by name, ID, or other fields. For example, when registering a "Model Run Workflow Template" you can select a model by typing a search query into the input field, selecting your desired result, and clicking it in the list. To clear your selection, use the "Clear Selection" button that appears after selection.

|                                      Selecting other entities                                       |
| :-------------------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/selecting_other_entities.png" alt="drawing" width="800"/> |

### Submitting the entity and handling errors

Once you have completed the form, use the "Submit" button at the bottom of the page to register the entity.

If there were no validation errors in the form, you will receive a success alert:

|                                      Form success                                       |
| :-------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/form_success.png" alt="drawing" width="800"/> |

If there were form validation errors, or another issue occurred, you will see an error indication either on the field itself (such as when a field is not completed), or at the top of the page (when more detailed validation catches an error after submission). In this case, the format of the URL did not include the required "https" component, so an error appeared on the field:

|                                      Form error                                       |
| :-----------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/form_error.png" alt="drawing" width="800"/> |

After correcting the issue, the submit button can be pressed again - it is safe to repeat this process until the form is accepted.

# Updating an entity

## Required Permissions

-   Registry Read
-   Registry Write

## Process

Updating an entity is a very similar process to registering an entity, except that the existing form details are pre-filled from the record.

Start by navigating to the entity (see [exploring the registry](#exploring-the-registry) for more information). From the entity detailed view, you can select "Edit Entity" on the right hand side:

|                                          Edit                                          |
| :------------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/edit_button.png" alt="drawing" width="800"/> |

Then make the desired changes to the record on the resulting form, clicking submit when you are ready to publish the updates. For help completing these forms, see [registering an entity](#registering-an-entity) above.

# Exploring the registry

## Required Permissions

-   Registry Read

## Listing, sorting and filtering entities

**Link**: [https://registry.rrap-is.com/records](https://registry.rrap-is.com/records)

This method of exploration is ideal for when you want to browse or filter a list of all the registered entities. Various filtering and sorting options means you can narrow the list to find relevant entities or get an idea of system activity.

Start by navigating to the above link. Once the registry list loads, you will see a scrollable list of entities.

Entities are distinguished in three ways. Their colour (1), icon (2) and type (3).

|                                  Record Display                                   |
| :-------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/record.png" alt="drawing" width="300"/> |

You can refine the list of entities by using the sorting and filtering options. Shown below:

1. Sorting - click the dropdown and select an order this includes:
    - Oldest first
    - Newest first
    - Name
    - Entity ID
2. Filtering by type - click the dropdown and select the entity type
3. Filtering by text - click in the input box and type your query - this filters the record list for resources which contain your specified substring. You do not need to submit or confirm the search query, it will automatically search as you type.

|                                 Sorting and filtering                                 |
| :-----------------------------------------------------------------------------------: |
| <img src="../../../assets/images/registry/filter_bar.png" alt="drawing" width="800"/> |

## Searching the registry

**Link**: [https://registry.rrap-is.com/search](https://registry.rrap-is.com/search)

# Sharing an entity

## Required Permissions

-   Registry Read
