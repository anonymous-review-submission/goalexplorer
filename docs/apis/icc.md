---
layout: default
title: ICC Methods
parent: API Methods
nav_order: 4
---

# Inter-Component Communication Methods
{: .no_toc }

Inter-component communication (ICC) methods are Android system methods that launches another Android component, e.g. another activity or service.
ICC methods use either Intents or Unified Resource Identifiers (URIs) to identify the target component.
{: .fs-6 .fw-300 }

| Transition Type| APIs of Context class|
|:------------------|:-----------------------------------|
| Launch activity  | startActivity(Intent)<br>startActivity(Intent, Bundle)<br> startActivityForResult(Intent, int)<br> startActivityForResult(Intent, int, Bundle)<br> startActivityFromChild(Activity, Intent, int, Bundle)<br> startActivityFromChild(Activity, Intent, int)<br>startActivityFromFragment(Fragment, Intent, int)<br> startActivityFromFragment(Fragment, Intent, int, Bundle)<br> startActivityIfNeeded(Intent,int)<br> startActivityIfNeeded(Intent, int, Bundle)<br> startActivities(Intent[])<br>startActivities(Intent[], Bundle)|
| Launch service   | startService(Intent)<br>startForegroundService(Intent)|
| Send broadcast   | sendBroadcast(Intent)<br>sendBroadcast(Intent, String)<br>sendBroadcastAsUser(Intent,UserHandle)<br>sendBroadcastAsUser(Intent, UserHandle,String) |