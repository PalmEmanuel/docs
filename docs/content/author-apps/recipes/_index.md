---
type: docs
title: "Radius Recipes"
linkTitle: "Recipes"
description: "Automate infrastructure deployment for your resources with Radius recipes"
weight: 300
---

## Overview

Recipes enable a **separation of concerns** between infrastructure teams and developers by **automating infrastructure deployment**. Developers select the resource they want in their app (_Mongo Database, Redis Cache, Dapr State Store, etc._), and infrastructure teams codify how these resources should be deployed and configured (_lightweight containers, Azure resources, AWS resources, etc._). When a developer deploys their application and its resources, Recipes deploy the backing infrastructure and bind it to the developer's resources.

## Recipe capabilities

### Select the Recipe that meets your needs

Recipes can be used in any environment, from dev to prod. Simply specify `mode: 'recipe'` in your [Link resource]({{< ref links >}}), and select the Recipe you want to run:

{{< rad file="snippets/recipe-link-example.bicep" embed=true marker="//BASIC" >}}

Use [**rad recipe list**]({{< ref rad_recipe_list >}}) to view the Recipes available to you in your environment.

### Customize Recipes with parameters

Recipes can be customized with parameters, allowing developers to fine-tune infrastructure to meet their specific needs:

{{< rad file="snippets/recipe-link-example.bicep" embed=true marker="//PARAMETERS" >}}

You can use [**rad recipe show**]({{< ref rad_recipe_show >}}) to view the parameters available to you in a Recipe.

## Supported resources

Recipes currently support the following resources. Support for additional resources is actively being worked on.

| Supported resources | 
|---------------------|
| `Applications.Link/redisCaches` | 
| `Applications.Link/mongoDatabases` |
| `Applications.Link/daprStateStores` |

## Further Reading

- [`rad recipe` CLI reference]({{< ref rad_recipe >}})
- [Author custom recipes]({{< ref custom-recipes >}})