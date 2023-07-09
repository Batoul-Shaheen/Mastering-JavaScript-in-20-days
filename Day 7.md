# Day7: 

Modules & Debugging.

## Lesson Summary:

#### Modules
- `Modules` are a relatively new development in JS that essentially let us take a big long programe & split it up across multiple files.
- use import && export.
- IF `<script type = "text/javascript">`: they are still accessible to global scope.
-  IF `<script type = "module">`: not able to access any of these variables that declare in " local scope".
-  JS modules work differently from JS scripts -> One difference is that we can't use await outside of a function in a script

```
 <script>
    await fetch("https://dog.ceo/api/breed/hound/list");
 </script>
```
- one of the differences btw JS modules & regular JS is await, top level of await but another difference is scope.

#### Debugging
- `debugger` is a really handy feature built into most browsers like Firefox and Chrome.
- console.log() (or .warn() or .error()) is one way to understand what's happening when your program runs.



