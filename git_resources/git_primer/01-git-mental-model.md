# The Git Mental Model

Most Git confusion comes from a bad mental model, or understanding of how things work. Understanding this is going to be far more important than understanding individual commands. 

## Git is a snapshot database
Each commit is:
- A snapshot of *all tracked files*
- Linked to its parent commit(s)
- Identified by a hash

Git does **not** store diffs, or comparisons between different file versions, internally.

## Three main areas
You work in three places:

1. **Working Directory**
   - Your actual files
2. **Staging Area (Index)**
   - What will go into the next commit
3. **Repository (History)**
   - Committed snapshots

