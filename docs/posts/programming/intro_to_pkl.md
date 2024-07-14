---
date:
    created: 2024-07-14
categories:
    - Programming
---

# Pkl language

There are many configuration languages such as `json`, `yaml` and `toml`. They are perfect for simple tasks but quickly get out of hand when it is used for seting up complicated systems like docker or kubernetes. Then Pkl language from Apple came to rescue. Here is the link to [the home page](https://pkl-lang.org/index.html). (Don't confuse this with `Python`'s `pickle`.)

<!-- more -->

Biggest advantages of `Pkl` are
- validations
- import of other files
- lazy evaluation

## Quick example
```pkl
name = "Pkl: Configure your Systems in New Ways"
attendants = 100
isInteractive = true
amountLearned = 13.37
```
```bash
$ pkl eval -f json /Users/me/tutorial/intro.pkl
```
output:
```json
{
  "name": "Pkl: Configure your Systems in New Ways",
  "attendants": 100,
  "isInteractive": true,
  "amountLearned": 13.37
}
```

## Install

### For linux (amd64)
```BASH
curl -L -o pkl 'https://github.com/apple/pkl/releases/download/0.26.1/pkl-linux-amd64'
chmod +x pkl
./pkl --version
```

## Pkl-Python

I am a heavy user of Python and needed binding to `pkl`.
Since `pkl` is very new, I needed to make my own.
Here is the link to [the github page](https://github.com/jw-y/pkl-python)

### Quick Introduction

Install with `pip install pkl-python`

```python
import pkl
config = pkl.load("path/to/pkl/file.pkl")
```





