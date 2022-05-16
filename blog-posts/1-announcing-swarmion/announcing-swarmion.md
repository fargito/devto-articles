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

A great emphasis has been done on developer experience, since working with a Typescript monorepo can be a challenge. The swarmion template uses state of the art tools to ensure the best developer experience possible.

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

## ✨ Template features

The template comes with state of the art tooling for a typescript monorepo. The main philosophy is to allow easy customization of the different tools used in the packages, without having to write too many code; every tool can be configured at the root level and extended through composition at the package level.

### Yarn 3 with workspaces

Enables you to create a monorepo with multiple packages, each with their own dependencies. Every package in the monorepo is considered as a npm package inside the monorepo, with every modification to its source code being instantly available to the other packages.

### Nx

A powerful and extensible build system. It is used in the template to manage dependencies between packages, provide visualization of the monorepo dependencies through the [`yarn nx graph` command](https://nx.dev/cli/dep-graph) and gain access to powerful custom generators (at the time, our [nx plugin](https://www.swarmion.dev/docs/code-structure/nx-plugin) has two generators, for libraries and serverless services).

Another feature Nx lies in the computation caching system, which allows to avoid unnecessary computation when running commands inside the monorepo. For example, running `yarn package` at the root level of the monorepo will only run the command in packages which code has changed since the last time it was run.

Finally, through the [`affected` commands](https://nx.dev/using-nx/affected), run targets only against modified code, both in local development and in CI/CD.

### Typescript

A strict and strong Typescript configuration at the root level, extended throughout the packages using composition. Since every package inside the monorepo is using Typescript, every line of code can be statically checked.

### ESLint

A comprehensive set of formatting (through [`eslint-plugin-prettier`](https://github.com/prettier/eslint-plugin-prettier)) and linting rules, generated with [Clinter](https://github.com/theodo/clinter). Once again, each package can easily extend the root configuration.

### Shared Typescript libraries

Easily share any sort of code (`ts` or `tsx`) between two services by defining it in a shared library. Packages are transpiled in `cjs`, `esm` (thanks to [Babel](https://babeljs.io/)) and `.d.ts` Typescript declaration file, to enable any usage across the monorepo.

### Jest

Every package has testing configured through [`jest`](https://jestjs.io/), with a default configuration that can easily be extended, thanks to the `jest.config.ts` file at the package level.

### VS Code support

Each package in the monorepo is defined as a workspace in the multi-root workspaces. It enables easier browsing and searching features.

Using multi-root workspaces makes it possible to use the great [`vs-code` extension](https://github.com/jest-community/vscode-jest#how-to-use-the-extension-with-monorepo-projects), which makes it possible to run and debug tests directly inside VS Code.

## 🎁 Wrapping up

Be sure to check out https://www.swarmion.dev/ for docs about swarmion, the [template repo](https://github.com/swarmion/template) and the [main repo](https://github.com/swarmion/swarmion), any feedback is greatly welcomed !

### 🎄 Upcoming features

Swarmion is being maintained by a core team of several people, we are striving to deliver more and more features:

- a `create-swarmion-app` script to create an app even more easily
- contracts library to define between services
- frontend and frontend library generators

### 🤝 Acknowledgments

Thanks to the swarmion team: [Adrien Cacciaguerra](https://github.com/orgs/swarmion/people/adriencaccia), [François Farge](https://github.com/orgs/swarmion/people/fargito), [Guillaume Duboc](https://github.com/orgs/swarmion/people/guillaumeduboc), [Maxime Vivier](https://github.com/orgs/swarmion/people/MaximeVivier), [Axel Fournier](https://github.com/orgs/swarmion/people/Sc0ra) and [Stanislas Hannebelle](https://github.com/orgs/swarmion/people/StanHannebelle).

Thanks to all the contributors !

Thanks to [Theodo](https://www.theodo.fr/) for sponsoring the project !
