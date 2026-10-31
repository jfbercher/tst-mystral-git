---
title: A title
subtitle: A subtitle
authors:
  - author names, one per line
date: 2026-09-19
license: GPL-3.0-or-later
github: https://github.com/jfbercher/Mystral-Editor
bibliography: references.bib
citation-style: author-year # or numeric
citation-template: "{authors} ({year}). *{title}*. {container}{volume}{pages}.{doilink}"
settings:
    myst_to_tex:
        code_style: listings
    output_stderr: remove
    output_matplotlib_strings: remove
exports:
  - format: tex
  - format: docx
  - format: pdf
    template: arxiv_nips
    article_type: article
    chapters: []
numbering:
  headings: true # activate headings numbering
  equations: true 
  figure: true
    #template: Fig. %s # Define the prefix
math:
  '\sha': 'ш'
  '\dr': '\mathrm{d}#1'
  '\wb': '\mathbf{w}' 
---


:::{toc} Contents
::: 

## First section

See [issue #1234](https://example.com/issue/1234) for details
[|date|](https://example.com)
[bad #1234]((url))

## Mermaid diagrams

Mermaid diagrams are rendered with [Pele](https://github.com/obsidianmd/pele), enabling you to add diagrams and flowcharts to your documents.
An overview of the Mermaid syntax is available [here](https://mermaid.js.org/intro/).

### Graphs

~~~mermaid
graph TD;
    A-->B;
    A-->C;
    B-->C;
    C-->Z;
~~~


### Sequence diagrams

~~~mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop HealthCheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
~~~

### Git graphs

~~~mermaid
gitGraph
   commit
   commit
   branch develop
   commit
   commit
   commit
   checkout main
   commit
   commit
~~~