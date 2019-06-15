# Application Handling

## StartApp\( AN \)

### \#started

```text
CATEGORIES
Chrome(A): #started
url (I): "https://4test.io:20443/login"

CONSTRAINTS
Login User:
WHEN Chrome IS #started AND
     url IS "https://4test.io:20443/login"
```

The generated result is

```text
// Chrome(A) = #started
EN.StartApp("Chrome");
// url(I) = "https://4test.io:20443/login"
EN.SetValue("url", "https://4test.io:20443/login");
```



