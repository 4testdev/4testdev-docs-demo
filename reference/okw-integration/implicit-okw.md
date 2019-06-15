# Implicit OKW

## Input Categories

If an input-category `myCat` is used with the choice e.g. `myChoice`, 4Test generates a`SetValue( "myCat", "myChoice")` automatically.

```text
CATGORIES
Login(I): #opened
user (I): Kermit
passwd(I): secret1
ok(A): #clicked

CONSTRAINTS
T_Login:
WHEN Login IS #opened AND
      user IS Kermit AND
    passwd IS secret1 AND
        ok IS #clicked
```

## Output Categories

Similar is the use of an output-category: In this case 4Test generates a `VerifyValue( "myCat", "myChoice")` automatically.

```text
CATGORIES
Login(I): #opened
user (I): Empty

CONSTRAINTS
T_Login:
WHEN Login IS #opened
  THEN user IS Empty
```



