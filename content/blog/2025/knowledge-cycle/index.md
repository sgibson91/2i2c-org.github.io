---
date: 2025-02-15
title: Where we hope to improve our service for creating and sharing knowledge.
draft: true
categories:
  - service
tags:
  - brainstorm
authors:
  - Chris Holdgraf
---

<style>
  figure iframe {
    margin-left: auto;
    margin-right: auto;
  }
  figure {
    display: flex;
    flex-direction: column;
    margin-left: auto;
    margin-right: auto;
    max-width: 500px;
  }
</style>

Over the years, 2i2c has managed infrastructure for more than 100 communities in research and education. During this time, we've seen patterns emerge in how communities attract new members, collaborate with them, and create new knowledge. This post is a reflection on this process, where 2i2c has supported it historically, and where we think we can enhance our service to better-support this workflow.
## Elements of data-driven discovery

For any individual to create and share knowledge with data, they need access to a few key resources[^1]:

- **Data** is the raw material that drives computational ideas.
- **Computation** provides the mechanism for manipulating data with code.
- **Tools** comprise of domain-specific software that leverage data and computation for specific outcomes.

Users leverage these resources by creating two types of content:

[^1]: For a more in-depth discussion of the relationship between tools, ideas, data, and computation, [Granger & Perez, 2021](https://ieeexplore.ieee.org/document/9387490).

- **Code** consumes these resources in order to run analyses, generate visualizations and reports, etc.
- **Narratives** contextualize the work of code to tell a story.
- **Computational Narratives** are a special-case of code and narratives that recognize the unique interplay between computation and scientific ideas for data-driven discovery.

Finally, **interfaces** allow users to manage all of the above to facilitate workflows in data-driven discovery and sharing.

{{< figure src="images/elements.png" title="Key elements needed for data-driven discovery include data, computation, tools, code, narratives, and interfaces that bring them all together." >}}

**Jupyter**'s goal is to build an ecosystem of tools and services that are modular, flexible, and interoperable, with a focus on interactive, dynamic, human-in-the-loop workflows. **2i2c**'s [hub platform](/platform) provides communities with their own community hub in the cloud to customize for their own workflows and to make them accessible to whomever they wish in order to create and share knowledge.

## The knowledge creation cycle requires building connections inside and outside of communities

Patterns emerge when you work with many different communities. Some grow and generate ideas more readily, while others do not. Why is this?

One consistent theme is that **successful communities make it easy to discover, co-create, and share both inside and outside of a community.**. When done well, this forms a cycle where new community members can quickly discover a community's ideas, learn its workflows, access its infrastructure, create their own knowledge, and share it with others.

{{< figure src="images/lifecycle.png" title="The community knowledge creation lifecycle involves a cycle of learning and community growth, followed by a cycle of knowledge creation and sharing that is then discovered by new community members." >}}

This isn't a complete or universal truth for how communities create and share knowledge, but we find it to be useful in thinking about how organizations like 2i2c can support communities along the way. There are some ways that 2i2c already facilitates this cycle, and others where we'd like to get better. The rest of this post explores each stage and where we think we can be more valuable.

### Discover: Making community impact accessible and interesting

The first step for most users is to learn about a community's big ideas and thematic areas. This is a crucial part of a community's ability to communicate the impact it is trying to have, and to share what it has accomplished so far.

{{< figure src="images/discover.png" title="Landing pages are a key way that communities signal the kinds of work they do and why it is valuable." >}}

2i2c's communities have facilitated the discovery of their work in a few ways:

1. **Landing pages**. Usually the first thing that newcomers see when they are trying to understand what a community does. For example, [here's the Cryocloud landing page](https://cryointhecloud.com/).
2. **Galleries**. Provide a way for community members to share their analyses in a discoverable way, with frictionless connections to their hub to allow others to quickly explore and iterate on their work. For example, [the Pangeo gallery](https://gallery.pangeo.io/) allowed users to submit notebooks that would be automatically executed and built into a page on the Pangeo website.
3. **Blogs**. Allow communities to informally share their ideas and updates. We'll discuss this in the "Share" section below.

**How we'd like to improve discovery**. Historically, communities have used a variety of tools for each of these workflows. For example, [Hugo](https://gohugo.io/) for landing pages and custom community code for galleries. We'd like to unify each of these workflows natively with [Jupyter Book 2](https://next.jupyterbook.org), which is built on the [MyST Document Engine](https://mystmd.org). This will require adding more functionality to [the MyST engine](https://mystmd.org) to allow for expressive (but still lightweight) interfaces like you'd find on an organization's webpage.

## Learn: Showing the core tools and practices behind a community's work

The next step in a newcomer's journey is to learn about the tools, practices, and workflows that a community hub enables. This is crucial for learning what kinds of skills and resources are needed to ask the questions that are of interest to a community, and how to learn them. For example, the [Project Pythia cookbooks](https://cookbooks.projectpythia.org/) provide an overview of core workflows in geospatial anlaytics, and are powered by the Pythia hub infrastructure.

{{< figure src="images/learn.png" title="Community documentation provides an accessible way for newcomers to learn what kinds of questions the community asks, how to ask them with code, and how to learn more." >}}

This is usually managed through **examples and tutorials** in the form of **computational narratives**. The two most common frameworks for documenting with computational narratives are [Jupyter Book](https://jupyterbook.org/) or [Quarto](https://quarto.org/).

**How we'd like to improve learning**. Our priorites over the past several months have been to [prepare Jupyter Book 2 for launch](https://next.jupyterbook.org) so that communities can leverage the [new MyST Document Engine](https://mystmd.org) to build their documentation. Here's the [Jupyter Book 2 priorities board](https://github.com/orgs/jupyter-book/projects/1), which is both our priorities for Jupyter Book 2, and the community's priorities in case you'd like to contribute. Our hope is to **unify landing pages, galleries, blogs, and documentation with a single community site powered by Jupyter Book 2**.

## Interact: Giving users all the tools they need to perform community workflows

Once a new member learns about community workflows, they need a space to dig more deeply into problems, sharpen their skills, and answer new questions with data. To do so, they need access to key data, computation, and tools that help them get started. Communities use [a community hub](https://jupyterhub.readthedocs.io) to provide all of these resources, and community administrators can give access to a hub to let a newcomer learn more deeply.

{{< figure src="images/interact.png" title="Allowing readers to directly interact with a community's resources removes the friction to learning these workflows, building on top of them, and growing their connection with a community." >}}

We encourage communities to configure their Jupyter Books to _directly point users to their JupyterHub_, allowing them to pull book content into their own interactive session running in the cloud. This provides a frictionless way to turn _readers_ into _creators_ that can start to generate their own knowledge on a hub.

**Where we'd like to improve the transition from learning to interactivity**. Historically, 2i2c hubs and community documentation have not been strictly connected. Some communities have done so on their own (e.g., by using JupyterHub launch buttons to point provide links to their community JupyterHub in a Jupyter Book), but we'd like to standardize and scale this practice by providing out-of-the-box configuration for new community hubs. We'd also like to make it easier for communities to define environments for their members so that they have fast access to the right tools to get started.

### Join: Converting community learners into community practitioners

Once a community member has participated in the community for long enough, they pass some threshold for "membership" and are given access to a more complete set of resources needed for community workflows. This might mean allowing them to spin up complex computing resources like GPUs or [Dask Gateway clusters](https://gateway.dask.org/), or giving them data resources like more local storage or [cloud scratch buckets](https://infrastructure.2i2c.org/howto/features/buckets/). At this point, a newcomer has been converted into a "member".

{{< figure src="images/join.png" title="Community hubs can extend access to new users as they wish, transforming learnings into community members. All community members get access to the same tools, data, and computation to create and share community knowledge." >}}

**How we'd like to improve membership**. Historically, 2i2c has provided a single set of hub resources to all of its users. We'd like to enable workflows that allow community leaders to define different tiers of access that map onto community member archetypes (e.g., newcomer, early member, member, expert, etc). This would allow communities to match the right resources to the level of trust they have in a given user to avoid misuse or runaway costs.

### Create: Providing community members the tools needed to ask new questions

Members of a community must build on top of the standardized workflows that are described in community documentation, and leverage a combination of data, computation, and tooling to answer new questions in their domain. 2i2c's hubs are designed to provide community members all of the resources needed to do so.

{{< figure src="images/create.png" title="By having access to all the tools needed for community workflows, members can ask their own questions and create new ideas and insights." >}}

**How we'd like to improve knowledge creation with a community hub**. Many of 2i2c's communities spend most of their time in this stage of knowledge creation, and the tools and workflows they use here are driven by communities themselves. The main areas we'd like to improve here are with service integrations for organizations and services that align with the values of open science. For instance, [data management services like Source Cooperative](https://source.coop/).

### Share: Allowing community members to easily share computational narratives

When a community member discovers something new, they want to share it with others in their community. This is an ongoing process where community members are giving and receiving information to iteratively drive their exploration and development.

These ideas are driven by data and computation, and so it is critical to **share the resources needed to reproduce the computation**. This has three benefits:

1. It allows others to **validate the core claims** by inspecting code and reproducing the results.
2. It allows others to **learn more effectively** by providing a more rich, interactive space to engage with the ideas.
3. It allows others to **build on top of work more easily** by providing an interactive starting point that lets readers get further with new ideas.

Community hubs leverage cloud infrastructure to facilitate this process. They standardize the environment so that content produced in one user's session can be easily reproduced by another user. [nbgitpuller](https://nbgitpuller.readthedocs.io/en/latest/) is the most common tool for distributing content within a JupyterHub. As long as the content was made on a JupyterHub, and shared with another user on the same hub, they'll be able to get their own copy and interact with it.

{{< figure src="images/share.png" title="The simplest sharing workflow uses nbgitpuller to distribute content via links that community members click. Doing so will give them their own copy of the content running in the hub's environment.">}}

{{< figure src="images/share.png" title="Because all community members have access to the same resources, it is easy to share the computational narratives." >}}

**Where we'd like to improve sharing**. We'd like to streamline a user's ability to share content with services like nbgitpuller, and unify the experience with more complex content sharing services like [Binder](https://mybinder.org). For example, we'd like to build [blogging functionality into Jupyter Book 2](https://github.com/jupyter-book/mystmd/issues/840), and make it easy to generate sharable links directly from within a JupyterHub.

### Reproduce: Bundling an environment with a sharable computational narrative

As an author's ideas are refined, it often comes with more specific needs for the environment and resources needed to reproduce their idea. For example, they might need a _specific version_ of a software package, or they may need a non-standard library that isn't available on their community hub's base environment. How can they share their computational narratives in a way that _bundles the environment_ with the content?

This is what [**the Binder Project**](https://mybinder.org) was built for. It provides a tool called [BinderHub](https://binderhub.readthedocs.io/en/latest/), which is an **engine for sharable, reproducible computational environments**. It allows an author to package up their computational narratives and code, and share access to a cloud environment that allows readers to reproduce and interact with the computation.
In 2024 our team prototyped how to [connect BinderHub services with a JupyterHub](../../2024/jupyterhub-binderhub-gesis/) and how to [deploy BinderHub services alongside each of our community hubs](../../2024/nasa-ephemeral-hubs/).
Doing so would allow community members to **build an environment needed to reproduce their computation and share it via their hub**.

{{< figure src="images/reproduce.png" title="BinderHub allows an author to package narrative, code, computational resources, and a software environment into a link that others can use to access a fully reproducible environment for their ideas.">}}

**Where we'd like to improve reproducibility**. We'd like to build on last year's work to make streamline the experience of generating sharable Binder links for a user's work so that others in a community can reproduce their results with custom environments rather than the standardized community environments. We'd also like to make it possible for members to **share external Binder links** so that non-members can reproduce and interact with their ideas, in a way that minimizes the risk of abuse or runaway cloud costs.

