# Setting a default value(?=)

?= is used for soft assignment for a variable

## What's the benefit?

Allows you to define a variable if it is undefined when the statement is parsed,

If the variable has a value, then the soft assignment is lost

Eg:

MACHINE ?= "qemuarm"

If MACHINE is already set before this statement is parsed, the above value is not assigned

If MACHINE is not set, then the above value is assigned

Note: Assignment is immediate

## What happens if we have multiple ?=

If multiple "?=" assignments to a single variable exist, the first of those ends up getting used
