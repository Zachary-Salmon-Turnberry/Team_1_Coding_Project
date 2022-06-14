---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
tags: [mermaid]
mermaid: true
---

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```

<div class="mermaid">
graph LR
    A --- B
    B-->C[Happy]
    B-->D(Sad);
</div>