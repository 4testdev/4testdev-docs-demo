# StartApp\( AN \)

```typescript
CATEGORIES
Chrome(A): #started
url (I): "https://4test.io:20443/login"​CONSTRAINTS

Start Chrome:
WHEN Chrome IS #started AND
     url IS "https://4test.io:20443/login"
```

The generated result is

```java
// Chrome(A) = #started
EN.StartApp("Chrome");
// url(I) = "https://4test.io:20443/login"
EN.SetValue("url", "https://4test.io:20443/login");
```

​[  
](https://4test.gitbook.io/4test-manual/~/drafts/-LUnMc5pP8rNIcswbK0U/primary/reference/okw-integration/implicit-okw)

