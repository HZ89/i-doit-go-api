# i-doit-go-api/goidoit 

is an [I-doit](https://www.i-doit.com/) API client implementation written in [GOLANG](https://golang.org).

Its focused on simplicity to create easy writable code for your projects.

the package supports:
- Login
- Requests
- Searching
- Getting object information by id, id slice, string or custom field
- creating, altering, deleting, archiving, quickpurging objects
- reports
- categories (only parts implemented) (wip)
- object\_type\_categories

Other types of requests like
- object\_types (comming soon)
- object\_type\_groups (comming soon)
- objects\_by\_relation (comming soon)
- categories (category, category\_info) (wip)
- location\_tree
- workstation\_components
- logbook
- impact

are not implemented yet (and maybe never will) but can easily be implemented using the goidoit.Request function
there are some [advanced](https://github.com/cseeger-epages/i-doit-go-api/blob/master/examples/advanced.go) [examples](https://github.com/cseeger-epages/i-doit-go-api/blob/master/examples/advanced2.go) of how to do this.

There is also a second repo [i-doit-go-tools](https://github.com/cseeger-epages/i-doit-go-tools) where you can find some more scripts for special use-cases that can be used as an
even more advanced example :P.

## Installation

If you already installed GO on your system and configured it properly than its simply:

```
go get github.com/cseeger-epages/i-doit-go-api
```

If not follow [these instructions](https://nats.io/documentation/tutorials/go-install/).

## Usage 

### Simple example

```
package main

import (
	"fmt"
	"github.com/cseeger-epages/i-doit-go-api"
)

func main() {
  // create api object
  a, _ := goidoit.NewApi("https://example.com/src/jsonrpc.php", "yourapikey")

  // or login using X-RPC-Auth
  // a, _ := goidoit.NewLogin("https://example.com/src/jsonrpc.php", "yourapikey", "username", "password")

  // search for sth like test
  s, _ := a.Search("test")

  // thats it
  fmt.Println(s)
}
```

### Advanced examples

There are more advanced [examples](https://github.com/cseeger-epages/i-doit-go-api/tree/master/examples) documented in the repo for common use cases.

## Code Documentation

You find the full [code documentation here](https://godoc.org/github.com/cseeger-epages/i-doit-go-api)

## Additional Informations

- [i-doit API documentation](https://kb.i-doit.com/pages/viewpage.action?pageId=37355644)
- [golang](https://golang.org/)
- [godoc](https://godoc.org/)
- [golang playground](https://play.golang.org/)

## Other great client implementations

- Benjamin Heisigs [i-doit-api-client-php](https://github.com/bheisig/i-doit-api-client-php/)
- Dennis Stückens [i-doit-api-clients](https://bitbucket.org/dstuecken/i-doit-api-clients/)

Thanks for your code inspirations!
