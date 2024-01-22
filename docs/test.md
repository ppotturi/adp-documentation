---
title: Test
summary: A brief description of my document.
authors:
    - xxx
date: 2018-07-10
weight: 10
some_url: https://example.com
---
# test

# C#

```c#
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");  
    }
  }
}

```

JavaScript

```js
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

```mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

```mermaid
sequenceDiagram
  autonumber
  Alice->>John: Hello John, how are you?
  loop Healthcheck
      John->>John: Fight against hypochondria
  end
  Note right of John: Rational thoughts!
  John-->>Alice: Great!
  John->>Bob: How about you?
  Bob-->>John: Jolly good!
```

| Method     | Description                          |
| ---------- | ------------------------------------ |
| `GET`    | :material-check:     Fetch resource  |
| `PUT`    | :material-check-all: Update resource |
| `DELETE` | :material-close:     Delete resource |

<div class="grid cards" markdown>

- :fontawesome-brands-html5: __HTML__ for content and structure
- :fontawesome-brands-js: __JavaScript__ for interactivity
- :fontawesome-brands-css3: __CSS__ for text running out of boxes
- :fontawesome-brands-internet-explorer: __Internet Explorer__ ... huh?

</div>

![Image title](https://dummyimage.com/600x400/eee/aaa){ align=left } Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

<figure markdown>
  ![Image title](https://dummyimage.com/600x400/){ width="300" }
  <figcaption>Image caption</figcaption>
</figure>

[Subscribe to our newsletter](#){ .md-button }
[Send :fontawesome-solid-paper-plane:](#){ .md-button }

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
    
[^2]: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
       nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
       massa, nec semper lorem quam in massa.
