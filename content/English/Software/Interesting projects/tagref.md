---
page:
  headHtml: |
    <snippet var="js.highlightjs" />

---
# Tagref

[Tagref](https://github.com/stepchowfun/tagref) is a tool for managing labeled notes in comments and references to these notes. It ensures the references are valid:

1. References actually point to tags. A tag cannot be deleted or renamed without updating the references that point to it.
2. Tags are unique. There is never any ambiguity about which tag is being referenced.

Written in Rust.

Inspired by [GHC notes convention](https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/coding-style#2-using-notes) ([archived](https://web.archive.org/web/20221212203306/https://gitlab.haskell.org/ghc/ghc/-/wikis/commentary/coding-style)). See http://www.aosabook.org/en/ghc.html ([archived](https://web.archive.org/web/20221022104412/https://www.aosabook.org/en/ghc.html)).

## Example

We hava a tag like:

```python
# [tag:cities_nonempty] This function always returns a non-empty list.
def get_cities():
  return ['San Francisco', 'Tokyo']
```

Elsewhere we use the above assumption and make it clear with a comment:

```python
cities = get_cities()

first_city = cities[0] # This is safe due to [ref:cities_nonempty].
```

#interesting-software
#developer-tooling