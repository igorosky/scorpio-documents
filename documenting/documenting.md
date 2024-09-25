# Documenting

## In code documentation
Code should be documented using comments and functions should be described as follows:
```C++
/**
 * Function that divides `a` over `b`
 * \param a number to divide
 * \param b number that divides
 * \returns `a / b`
 * \exception if `b` is `0` an exception is thrown
*/
float divide(const float a, const float b) {
    return a / b;
}
```

> **Note:** short self describing functions without non-obvious behaviors does not have to be described.


## In repo documentation
Every repository should contain `README.md` explaining what it contains.
> **Note:** Documentation should be written in english

Every section with some rover submodule - eg. `autonomy` which is inside `core` should also contain `README.md` which looks like [this](submodule_readme_example.md)

> **Note:** mermaid graph should only contain topics and services used by internal nodes

