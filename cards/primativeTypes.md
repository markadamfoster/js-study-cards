What are the 6 primitive types in JS? Also, what *is* a primitive type? Other than these 6 primitive types, what is everything else a version of?

---

The 6 primitive types in JS:

- null
- undefined
- boolean
- number
- string
- symbol

Primitive types are just values, and have no methods. However, JavaScript will readily coerce a primitive type to its corresponding object type. So if you have a primitive string value, and try to access the `.length` property, you won't get an error, you'll get the length. Behind the scenes, JavaScript is coercing it to a String, which does have that property.

Everything else extends from `Object`. (for example, an array is a type of object)