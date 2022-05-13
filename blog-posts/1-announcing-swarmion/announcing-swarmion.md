---
published: false
title: 'Introducing Swarmion, a framework for shipping type-safe Serverless microservices at scale'
cover_image:
description: 'Description of the article'
tags: serverless, typescript, monorepo, microservices
series:
canonical_url:
---

The serverless computing paradigm introduced a lots of opportunities to create more scalable and cost-efficient software, but it also came with its lot of challenges, some of which we harshly experienced.

## What is Swarmion?[](https://www.swarmion.dev/docs#what-is-swarmion)

Swarmion is an open-source Framework for building Type-safe Serverless microservices at scale. It takes full advantage of the **Serverless Framework** to handle deployment and provisioning of resources, while adding support for microservices and end-to-end type-safety.

It contains the knowledge of more than two years building multiple real world applications, ranging from small startups to large groups.

## TL:DR, create an app using the swarmion template

_Demo of the tool, using the [https://github.com/swarmion/template](https://www.github.com/swarmion/template) template button_

## Our core beliefs[](https://www.swarmion.dev/docs#our-core-beliefs)

### Your codebase should adapt to your team organization[](https://www.swarmion.dev/docs#your-codebase-should-adapt-to-your-team-organization)

Changes in the way you organize your teams should not have an impact on the speed at which you can develop and deploy new features. Therefore, Swarmion uses a flexible microservices approach in a monorepo.

### DRY (Don't Repeat Yourself)[](https://www.swarmion.dev/docs#dry-dont-repeat-yourself)

Having several teams working in the same environment requires efficient collaboration. Swarmion allows to clearly separate the shared logic and interfaces from the service-specific logic for better decoupling.

### Developer experience is key for code quality[](https://www.swarmion.dev/docs#developer-experience-is-key-for-code-quality)

As your codebase grows, testing and deployment times are likely to skyrocket. Swarmion uses optimized low-level software (esbuild, vitejs) to reduce testing and building times and a smart monorepo management tool ([Nx](https://nx.dev/)) to provide a top-level developer experience and reduce CI/CD delays.

### Trust your deployments (beta)[](https://www.swarmion.dev/docs#trust-your-deployments-beta)

As the number of moving parts in your organization increases, it is paramount to secure the deployment process. At each deployment, Swarmion validates requested changes against all impacted services to prevent breaking changes.

## Template structure

_Schema of generated services and packages, with a quick explanation of each of them_

_Show what commands to run_

## Template features

_Add descriptions of each feature_

- Yarn 3 with workspaces
- Nx
- Eslint configuration
- Prettier configuration
- Jest configuration
- End-to-end Typescript
- Shared Typescript libraries built with babel, with a watch mode
- Selective tests, package and deploy to remove the need to run all the tests and deploy at every commit.

## Articles to come

- create-swarmion-app script and package generators
- contracts between services
