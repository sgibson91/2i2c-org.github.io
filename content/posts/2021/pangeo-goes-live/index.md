---
title: "2i2c begins operating Pangeo's hub infrastructure!"
subtitle: ""
summary: "2i2c are pleased to announce that the first Pangeo JupyterHub is now live on 2i2c-operated infrastructure! :tada: "
authors: ["Sarah Gibson"]
tags: [2i2c, pangeo]
categories: [updates]
date: 2021-11-08
featured: false
draft: false
---

We have recently finished re-creating the Pangeo community JupyterHub hosted on GCP in the [2i2c-org/infrastructure](https://github.com/2i2c-org/infrastructure) repository.
This is a huge milestone in our partnership with Pangeo to provide expertise and operations of cloud-based, vendor-agnostic Jupyter infrastructure and workflows.
Read on for more information about this partnership, and a bit about its history.

## What does this mean?

In short: moving forward, 2i2c will manage Pangeo's JupyterHub-based cloud infrastructure, and will collaborate with the Pangeo community to develop new features in partnership with open source communities.

For users of Pangeo's infrastructure, the switch should be a smooth one!
The new hub will behave nearly identically to the old one - it will simply be managed by 2i2c engineers moving forward.
The hub will be available at the same URL (https://dus-central1-b.gcp.pangeo.io) and user directories will be updated to the state they were in a few days before the migration took place.

Under the hood, the Pangeo Hubs will still be configured via [Zero to JupyterHub](https://z2jh.jupyter.org/) configuration, and follow best-practices in hub deployment from the JupyterHub community.
The workflows and tools that power user workflows in Pangeo will not change.

Development and operations on this hub will all be done in the open via [the 2i2c `infrastructure` repository](https://github.com/2i2c-org/infrastructure), and [we invite participation and feedback from others](https://discourse.pangeo.io/t/migration-of-us-central1-b-gcp-pangeo-io-to-2i2c-infrastructure/1890) in our infrastructure work.

On **22nd November 2021**, the old Pangeo GCP JupyterHub will be shut down, and the project will move forward on the new Pangeo Hub managed by 2i2c.
Moving forward, we plan to collaborate together in order to find new pathways for development in the Jupyter ecosystem - we will share more ideas of things we will work on soon!

## History of Pangeo Cloud Hubs

Pangeo has pioneered a new model in using open source and cloud-agnostic infrastructure to support scientific research in the cloud, and we aim to build on this legacy to support the Pangeo project moving forward.

The first Pangeo cloud JupyterHub (`pangeo.pydata.org`; now defuct) was deployed for the [2017 American Meteorological Society Meeting](https://annual.ametsoc.org/2017/); since then, the Pangeo community has iterated through several different prototypes of cloud-based hubs.
This allowed for many new workflows that enabled a more open and collaborative pathway to doing world class research, and included access to datasets and computational resources that were previously unattainable.
Pangeo achieved this by working in partnership with open source communities and building technology that leveraged modular open source components for their platform.

In the last several years, Pangeo have built a thriving community of practice around this infrastructure.
As the community has grown, so has the need for more reliable and dedicated operational and developmental support.
Until now, Pangeo community members have maintained their cloud infrastructure in an ad-hoc fashion, which has required significant resources from the project.
Pangeo is now a service that many rely upon for their scientific and educational workflows, and deploying modern cloud infrastructure to support the community requires dedicated cloud expertise and support.
This is the basis of our partnership.

## The Pangeo-2i2c Partnership

[2i2c](https://2i2c.org) is a non-profit team that develops and operates cloud infrastructure for interactive computing workflows.
We have extensive experience in managing Jupyter workflows in the cloud and a long history of contributions to projects in this ecosystem.
2i2c utilizes [a cloud deployment management system](https://github.com/2i2c-org/infrastructure) to centralise and configure the deployment of many independent JupyterHubs, empowering communities to leverage the same infrastructure (and team!) for JupyterHubs running in the cloud.

All of 2i2c's core infrastructure [is cloud- and vendor-agnostic](https://2i2c.org/right-to-replicate/), and follows a model of building open source tools and giving back to those communities.
Moreover, our JupyterHub deployments deploy a technical stack that closely mirrors the Pangeo deployments.
Our partnership with Pangeo began through 2i2c's core competency in these areas and the similarity between the two project's technical stacks.

## What's next?

We believe that this approach allows each community to focus on it's core strengths: Pangeo will continue to grow an open community and scientific software ecosystem around geospatial analytics, and 2i2c will oversee the development and operations of the core cloud infrastructure stack that powers Pangeo's workflows.

We have many ideas for improving workflows in this ecosystem (you can see a few ideas [from our kickoff meeting notes a few months ago](https://discourse.pangeo.io/t/notes-from-the-pangeo-2i2c-kick-off-meeting/1587)).
By working closely with members of the Pangeo community as we operate its infrastructure, we will be able to identify new ways to improve cloud technology and the Pangeo stack.

We are extremely grateful to the Pangeo project for giving us the opportunity to serve their community, and we look forward to a long partnership ahead! :rocket:
