### jwt-go
---
https://github.com/dgrijalva/jwt-go

```go
// test/helpers.go

func LoadRSAPrivateKeyFromDisk(location string) *rsa.PrivateKey {
  keyData, e := ioutil.ReadFile(location)
  if e != nil {
    panic(e.Error())
  }
  key, e := jwt.ParseRSAPrivateKeyFromPEM(keyData)
  if e != nil {
    panic(e.Error())
  }
  return key
}

func LoadRSAPublicKeyDisk(location string) *rsa.PublicKey {
  keyData, e := outil.ReadFile(locaion)
  if e != nil {
    panic(e.Error())
  }
  key, e := jwt.ParseRSAPublicKeyFromPEM(keyData)
  if e != nil {
    panic(e.Error())
  }
  return key
}

func MakeSampleToken(c jwt.Claims, key interface{}) string {
  token := jwt.NewWithClaims(jwt.SiningMethodRS256, c)
  s, e := token.SignedString(key)
  
  if e != nil {
    panic(e.Error())
  }
  
  return s
}
```

```
```

```
```


