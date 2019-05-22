---
layout: default
title: Home
nav_order: 1
description: "GoalExplorer is a tool that performs goal-driven exploration to trigger functionality of interest for Android apps."
permalink: /
---

<!-- <img src="../img/logo.png" width="262> -->
![](../img/logo.png){:height="50%"}

Goal-driven Exploration for Android Apps.
{: .fs-6 .fw-300 }

<!-- [Overview](docs/overview.md){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } [Download](https://drive.google.com/open?id=1w6MXs5gPbX-lpl2SE1jYz_Xo1A40rY13){: .btn .fs-5 .mb-4 .mb-md-0 } -->

---

<span style="font-variant:small-caps;">GoalExplorer</span> automatically generates an executable test script that directly triggers the functionality of interest. The core idea behind <span style="font-variant:small-caps;">GoalExplorer</span> is to first statically model the application UI screens and transitions between these screens, producing a Screen Transition Graph (STG). Then, <span style="font-variant:small-caps;">GoalExplorer</span> uses the STG to guide the dynamic exploration of the application to the particular target of interest: an Android activity, API call, or a program statement. The results of our empirical evaluation on 93 benchmark applications and 95 the most popular GooglePlay applications show that the STG is substantially more accurate than other Android UI models and that <span style="font-variant:small-caps;">GoalExplorer</span> is able to trigger a target functionality much faster than existing application exploration.

This repo contains the API calls, collected from [Android Developers](https://developer.android.com/), that are used to identify fragments transaction, menu/drawer/dialog creation, and inter-component transitions.
The repo also contains the details of our empirical evaluation on 93 benchmark applications and 95 the most popular GooglePlay applications, with app version, category, and size.

### <span style="font-variant:small-caps;">GoalExplorer</span> overview

- [See overview]({{ site.baseurl }}{% link docs/overview.md %})

### Evaluation

- [See evaluation]({{ site.baseurl }}{% link docs/evaluation/evaluation.md %})

### Configure <span style="font-variant:small-caps;">GoalExplorer</span>

- [See instructions]({{ site.baseurl }}{% link docs/instruction.md %})