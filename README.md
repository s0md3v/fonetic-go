<h1 align="center">
  <br>
  <a href="https://github.com/s0md3v/fonetic"><img src="https://i.ibb.co/KctQhzN/phonetic.png" alt="fonetic"></a>
  <br>
  fonetic-go
  <br>
</h1>

<h4 align="center">assess pronounciblity of text</h4>

<p align="center">
  <a href="https://github.com/s0md3v/fonetic-go/releases">
    <img src="https://img.shields.io/github/release/s0md3v/fonetic-go.svg">
  </a>
  <a href="https://github.com/s0md3v/fonetic/issues?q=is%3Aissue+is%3Aclosed">
      <img src="https://img.shields.io/github/issues-closed-raw/s0md3v/fonetic-go.svg">
  </a>
</p>


### Introduction
Fonetic is a library to assess pronounceablility of a given text. For more information, check out the original [python implementation](https://github.com/s0md3v/fonetic).

### Documentation

fonetic is minimal and can be implemented in just 2 lines of code as follows:

```golang
package main

import (
    "github.com/s0md3v/fonetic-go"
)

func main(){
  total, good, bad := fonetic.Count("your string here")
  // your logic here
}
```

Where,
- **total**: total number of bigrams
- **good**: number of pronounceable bigrams
- **total**: number of non-pronounceable bigrams
