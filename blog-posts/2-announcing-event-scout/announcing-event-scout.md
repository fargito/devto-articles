---
published: false
title: 'Introducing EventScout: Easy Integration Tests for Event-Driven AWS Architectures'
cover_image:
description: EventScout secures your event-driven applications!
tags: serverless, eventbridge, integration, tests, cdk, typescript
series:
canonical_url:
---

When building event-driven Serverless applications on AWS, EventBridge is a must-have. It's simple to use, scalable and inexpensive.

However, a challenge I often faced during my event-driven projects was testing. I could not find an easy way to validate that the events sent by my application were matching my expectations. The critical challenge was to list events sent through an event bus, which is not natively possible with EventBridge.

## TL;DR

I made a cool EventBridge integration testing library for Typescript, [check it out](https://github.com/fargito/event-scout)!
