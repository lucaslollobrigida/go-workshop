# Go Workshop

## Installation

Download the last release from: [https://golang.org/dl/](Golang)

Or use a language distribution versioning tool: [https://github.com/asdf-vm/asdf](asdf)

## Tooling

```bash

go get -u golang.org/x/tools/...

```

## Agenda

### Modules

```go
package account
```

### Functions

```go
func myFunc() {
    return "Hello, world!"
}
```

### Types

```go
bool

string

int  int8  int16  int32  int64
uint uint8 uint16 uint32 uint64 uintptr

byte // alias for uint8

rune // alias for int32
     // represents a Unicode code point

float32 float64

complex64 complex128
```

You can see more details:

```go
fmt.Printf("Type: %T Value: %v\n", x, x)
```

### Tests

Create a file ending with `_test.go`, like this:

```sh

touch account_test.go

```

Now, let's write some tests.

```go
package account

import "testing"

func TestAbc(t *testing.T) {}
    t.Error() // to indicate test failed
}
```
### Structs

```go
type Account struct {
	ID int64
	PersonName string
	Cards []*Card
}
```

### Interfaces

```go
type Logger interface {
	String() string
	Print(interface{})
}
```

### Advanced

#### Builtin Concurrency

+ Goroutines
+ Wait Groups
+ Mutexes

## Next Steps

Real world projects ideas:

+ A CLI that automates a process done by the development team.
+ A Rest API that gets the weather for my location.
+ A memory cache system, Redis alike.
