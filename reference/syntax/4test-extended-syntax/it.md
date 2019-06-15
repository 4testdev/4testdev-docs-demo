---
description: >-
  If a category is to be used several times in the same GIVEN-WHEN-THEN
  expression, IT can also be used to refer to the last category used.
---

# IT

## Example

The following expressions are the same:

```text
T_Smoke:
THEN user DOES #exist AND user IS "myUser"
```

```text
T_Smoke:
THEN user DOES #exist AND IT IS "myUser"
```



