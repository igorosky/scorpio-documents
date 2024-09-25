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

Every section with some rover submodule - eg. `autonomy` which is inside `core` should also contain `README.md` which looks as follows:
```
# <Submodule name>
<Explanation what is inside and what it does>

## Defined Node class list
|                 Name                 |    Description     |
|                  ---                 |        ---         |
| [`<Node name>`](<URL to node class>) | <Node description> |

## Launch files
|                    Name                    |      Decryption      |
|                     ---                    |         ---          |
| [`<launch file name>.launch`](<url to it>) | <Launch description> |

## Node graph
`'`mermaid
graph <TD/LR>
    %% Internal nodes %%
    <list of internal nodes>

    %% External nodes %%
    <list of external nodes>
    
    external((External-sources))

    <connections for each node>
`'`

## List of advertised topics
|       Name     |              Publisher             |                 Published data type                  |     Description     |
|       ---      |                 ---                |                         ---                          |         ---         |
| `<Topic name>` | [`<Publishing node>`](<URL to it>) | [`<Data type that is being published>`](<URL to it>) | <Topic description> |

## List of served served
|                  Name                 |                 Published data type                  |     Description     |
|                  ---                  |                         ---                          |         ---         |
| [`<Service name>`](<URL to node class>) | [`<Data type that is being published>`](<URL to it>) | <Topic description> |

```

> **Note:** mermaid graph should only contain topics and services used by internal nodes

