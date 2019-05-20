# Chapter 3 - Commit Conventions

We enncourage a commit convention style utilized by the Linux kernel. Unlike semantic commit messages, we only focus on the scope and summary of the change instead of formatting it with the commit type, scope and summary. 

## The Format

Our format is as follows


```

Basic layout

[game/HitWindow] Fix windows not accounting for the input lag
   ^             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |                                    |
   |                                    |
 Scope                               Summary


Example Message:

[game/HitWindow] Fix windows not accounting for input lag

* Window was only accounting on hit presses but not really
* tracking how accurate it was. We should use input lag for
* this

Closes GH-1929
```

 - Scope determines the part of the codebase that was changed. Regardless if its one-file changes, it should count as a whole scope.
 
 - Summmary is a detailed but short description of the change, which should be continued if needed on additional lines.
 
 ## Allowed Scopes
 
 Scope of the change should be the area of a code or a subsystem. Say if you're editing `file.foo` from `game/Sample`, your scope is `game/Sample` and not `game/Sample/file.foo` or `file.foo`.
 
 ## Allowed Summary format
 
 Summaries should explain the commit in detail as stated previously, however, committer must detail what kind of change they have to perform, examples may be:
 
 - `` [game/Subsystem/OpenGL] refactor declaration Foo -> FooBar``
 
 - `` [game/Window] Fix openGL context not being drawn correctly to window``
 
 What we don't encourage is
 
 - ``[game/XY] Update file``
 - `` [game/XY] delete unnnecessary JSON file``
 
 
 As they don't explain what was edited, although scope was proper. This does not tell immediately what was changed.
