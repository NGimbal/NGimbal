# AGENTS.md

- constantly interrogate how we can do less while achieving stated goals
- when modifying a function, research it's callsites, context around callsites
  and callers's callers and see if return values are truly needed
- a perfect commit reduces the number of non test LOC while increasing test
  coverage, regardless of whether tests have been added
- do not commit unused code or code that anticipates future features without
  present day use

- each change should strive to reduce entropy, this means:
  - reduce overall amount of code
  - increase legibility code (too many comments is also not legible)
  - reduce file size
  - reduce number of files
  - reduce levels of indentation
  - increase type safety
  - increase number of tested branches
  - return early where possible

- each change should meaningfully drive business goals, some common goals
  include:
  - reliability
  - ease of use
  - short "time to value"

- we strive for Buildplus to be easy and joyful for users, this means:
  - cached queries
  - optimistic mutations
  - descriptive errors
  - meaningful empty states with a path forward (i.e. new project, clear
    filters)
  - functionality is inline, not hidden behind drawers / modals
  - progressive disclosure enables self learning of product
  - keyboard navigation works as expected
  - notifications are useful and concise
  - features need to compose with one another, there should be many valuable ways to use Buildplus
  
- an ideal function is small, implements one feature, and can compose
- functions that implement mutation queries must enable transaction
  participation, in some cases they should require it

- testing documentation must be rigorously followed in ./docs/testing.md
