What is the significance, and what are the benefits, of including `use strict` at the beginning of a JavaScript source file?

---

`use strict` is a way to voluntarily enforce stricter parsing and error handling. Code errors that would otherwise have been ignored or would have failed silently will now generate errors or throw exceptions.

One change (among others) is preventing the accidental creation of global variables. 