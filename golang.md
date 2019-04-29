# Go


## go mod

* `set GO111MODULE=on`
* `go mod init`
* `go build`


## Linter

* `gometalinter`
  * `$FileDir$ --fast --disable=dupl`
  

## Debugger error

1. this message occured.
```
could not launch process: decoding dwarf section info at offset 0x0: too short

Debugger finished with exit code 1
```
2. action: `go get -u github.com/derekparker/delve/cmd/dlv`
  * [decoding dwarf section info at offset 0x0: too short
](https://stackoverflow.com/questions/52230503/decoding-dwarf-section-info-at-offset-0x0-too-short)

