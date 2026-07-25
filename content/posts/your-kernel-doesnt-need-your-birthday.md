---
title: "Your Kernel Doesn’t Need Your Birthday"
date: 2026-03-19
description: "We are moving toward a reality where your local system is designed to interrogate you and report your status to any application that asks"
tags: ["security","privacy","linux"]
---

The recent activity in the systemd repository, specifically [Pull Request #40954: userdb: add birthDate field to JSON user records](https://github.com/systemd/systemd/pull/40954), has raised serious red flags for me. The proposal and the underlying intent is deeply concerning and not ok.

The code proposal explicitly mentions that this field is intended to facilitate age verification compliance for various regional laws. By integrating this into the core of the operating system's identity management, systemd is effectively transforming the OS into a mechanism for gatekeeping and surveillance.

The whole Linux ethos aligns to a user-first philosophy. When it begins to store and serve sensitive personal data like an exact birth date to satisfy legal requirements or third-party portals, it ceases to be a tool for the user and starts acting as an agent for external regulators.

WIt feels like we are rapidly moving toward a reality where your local system is designed to interrogate you and report your status to any application that asks. I'd expect that in Windows (and have done for years), but not Linux. Privacy and anonymity have always been central tenets of the Linux ecosystem; baking age-verification hooks into the heart of the system is a fundamental betrayal of those principles.

We should be very wary of any "feature" that makes it easier for software to demand our identity. Sigh.