# Welcome to the template

This is a template for creating documentation driven repos

## Commands

- `poetry run task serve` - Start the live-reloading docs server.
- `poetry run task build` - Build the documentation site.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
    docs_src/
        sample.py

# Code samples

## Annotations

```python
# Code block content
print("hello world") # (1)
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, **formatted
    text**, images, ... basically anything that can be written in Markdown.

## Highlight lines

```py hl_lines="2 3" title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

```{.py3 hl_lines="1 3" linenums="2"}
"""Some file."""
import foo.bar
import boo.baz
import foo.bar.baz
```

## From sample file

it is possible to add an entire file

```py hl_lines="5 6" title=".sample.py"
--8<-- "docs_src/sample.py"
```

1.  :man_raising_hand: I'm a code annotation! I can contain `code`, **formatted
    text**, images, ... basically anything that can be written in Markdown.
2.  :man_raising_hand: I'm a code annotation! I can contain `code`, **formatted
    text**, images, ... basically anything that can be written in Markdown.

Also possible to add just a snippet, however annotations won't work properly here. Please note that numbering starts over

```{py hl_lines="2" linenums=8 title=".sample.py"}
--8<-- "docs_src/sample.py:8:9"
```

## Other cool stuff

???+ note "Open styled details"

    ??? danger "Nested details!"
        And more content again.

/// admonition | Some title
Some content
///

Task List

- [x] item 1
  - [x] item A
  - [ ] item B
        more text
    - [x] item a
    - [ ] item b
    - [x] item c
  - [x] item C
- [ ] item 2
- [ ] item 3

If needed we can add inline math $p(x|y) = \frac{p(y|x)p(x)}{p(y)}$

Or like this `#!math p(x|y) = \frac{p(y|x)p(x)}{p(y)}`

Then there is regular math inputs

???+ note "Regular Math inputs"

    $$
    E(\mathbf{v}, \mathbf{h}) = -\sum_{i,j}w_{ij}v_i h_j - \sum_i b_i v_i - \sum_j c_j h_j
    $$

    \[3 < 4\]

    \begin{align}
    p(v*i=1|\mathbf{h}) & = \sigma\left(\sum_j w*{ij}h*j + b_i\right) \\
    p(h_j=1|\mathbf{v}) & = \sigma\left(\sum_i w*{ij}v_i + c_j\right)
    \end{align}

or even as superfences block

???+ note "Superfences block"

    ```#!math
    \begin{align}
    p(v*i=1|\mathbf{h}) & = \sigma\left(\sum_j w*{ij}h*j + b_i\right) \\
    p(h_j=1|\mathbf{v}) & = \sigma\left(\sum_i w*{ij}v_i + c_j\right)
    \end{align}
    ```
