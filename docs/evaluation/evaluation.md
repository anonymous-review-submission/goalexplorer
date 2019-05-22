---
layout: default
title: Evaluation
nav_order: 4
has_children: true
permalink: docs/evaluation
---

# Evaluation
{: .no_toc }

The empirical evaluation of <span style="font-variant:small-caps;">GoalExplorer</span> is performed on 93 benchmark apps and 95 the most popular GooglePlay apps.

Both <cite>[Sapienz][1]</cite> and <cite>[Stoat][2]</cite> were evaluated on the benchmark of 68 F-Droid apps and the Stoat authors further extended the benchmark with additional 25 F-Droid apps, producing a benchmark with 93 F-Droid apps in total. <span style="font-variant:small-caps;">GoalExplorer</span> is evaluated on the same 93 benchmark apps.
In addition, we downloaded the 100 most popular apps on the Google Play store as of July 31, 2018. This dataset allows us to evaluate our approach on real apps commonly used in practice. Of the 100 Google Play apps, five failed to run on the emulator. We excluded these five applications from further analysis, arriving at the set of 93 benchmark and 95 Google Play apps.

The page contains the details of our empirical evaluation on 93 benchmark applications and 95 the most popular GooglePlay applications, with app version, category, and size.

### Google Play Apps

|Mean(MB)          | Min(MB) | Max(MB) |
|:----------------:|---------|---------|
|25.03             | 1.32    | 86.72   |

### Benchmark Apps

| Mean(MB)         | Min(MB)  | Max(MB) |
|:----------------:|----------|---------|
| 0.71             | 0.02     | 20.59   |

[1]:https://dl.acm.org/citation.cfm?id=2931054
[2]:https://dl.acm.org/citation.cfm?id=3106298
