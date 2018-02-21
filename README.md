## `aes256`

AES256 for personal use.

### Usage

```go
text := []byte("Some string to encrypt")
key, err := GenerateRandomBytes(32)

fmt.Println("key: ", key)

ciphertext, err := Encrypt(text, key)
if err != nil {
  log.Fatal(err)
}
fmt.Printf("%s => %x\n", text, ciphertext)

plaintext, err := Decrypt(ciphertext, key)
if err != nil {
  log.Fatal(err)
}
fmt.Printf("%x => %s\n", ciphertext, plaintext)
```