---
layout: default
title: Menus/Drawers/Dialogs
parent: API Methods
nav_order: 2
---

# Menu/Drawer/Dialog Initiation Methods
{: .no_toc }

Menu/drawer/dialog initiation methods are Android system methods that show menu/drawer/dialog on the screen:
{: .fs-6 .fw-300 }


| Transition Type| APIs|
|:------------------|:-----------------------------------|
| Menu Open        | MenuInflater.inflate(int, Menu) |
| Drawer Open      | DawerLayout.openDrawer(View, boolean)<br>&nbsp; &nbsp; &nbsp; &nbsp; .openDrawer(View)<br> &nbsp; &nbsp; &nbsp; &nbsp; .openDrawer(int)<br>&nbsp; &nbsp; &nbsp; &nbsp; .openDrawer(int, boolean) |
| ShowDialog       | DialogFragment.show(FragmentTransaction, String)<br>&nbsp; &nbsp; &nbsp; &nbsp; .show(FragmentManager, String)<br>&nbsp; &nbsp; &nbsp; &nbsp; .showNow(FragmentManager,String)|