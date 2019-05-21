---
layout: default
title: Overview
nav_order: 2
---

# [](#header-1)Overview

![](../img/analysis_overview.png)


The high-level overview of <span style="font-variant:small-caps;">GoalExplorer</span> is presented in the figure above. It obtains two inputs: the APK file of the app and the target functionality of interest, which can be provided as an app activity, an API call, or a code statement.


In the first step, <span style="font-variant:small-caps;">GoalExplorer</span> statically constructs the Screen Transition Graph (STG) of the app in the STG Extractor component. It then maps the target(s) to (possibly multiple) nodes of the graph in the Target Detector. Finally, it uses the graph to guide the dynamic exploration to a reachable target node, starting with the one that has the shortest path from the initial screen in the Dynamic Explorer.

## [](#header-2)API Methods

STG Extractor searches for specific API invocations when constructing the nodes and transitions.

- For complete lists of API methods collected from [Android Developers](https://developer.android.com/), see:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[API Methods](apis/apimethods.md){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 } 

### [](#header-3)Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### [](#header-4)Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### [](#header-5)Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### [](#header-6)Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Nesting an ol in ul in an ol

- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)
  1. level 2 item (ol)
  1. level 2 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
  1. level 4 item (ol)
  1. level 4 item (ol)
    - level 3 item (ul)
    - level 3 item (ul)
- level 1 item (ul)

### And a task list

- [ ] Hello, this is a TODO item
- [ ] Hello, this is another TODO item
- [x] Goodbye, this item is done

### Small image

![](https://assets-cdn.github.com/images/icons/emoji/octocat.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
