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

```golang
package main

import (
  "github.com/s0md3v/fonetic-go"
)

 /*
 This is just an example, don't copy-paste this. Use fonetic.Count's output according to your needs.
 */

func main(){
  total, good, bad := fonetic.Count("your string here")
  if (good/total) > 70 || (bad == 0 && total < 2)) {
    fmt.Println("TEXT")
  } else {
    fmt.Println("RANDOM")
  }
}
```

Where,
- **total**: total number of bigrams
- **good**: number of pronounceable bigrams
- **bad**: number of non-pronounceable bigrams

> Note: Non-alphabetic characters do not count as `good` or `bad`, but they do count in `total`. It means the output for `aa1323423634` would be `total=11,good=1,bad=0`.
