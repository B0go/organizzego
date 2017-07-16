# Organizzego [![Build Status](https://travis-ci.org/B0go/organizzego.svg?branch=master)](https://travis-ci.org/B0go/organizzego)

Go implementation of Organizze's API (https://www.organizze.com.br)

## Usage

Auth:

* User name: Your Organizze e-mail
* Api Token: The api token retrieved by Organizze at https://app.organizze.com.br/configuracoes/api-keys
* User agent: This will be used by Organizze to know who is behind the request. Follow the template "You (you@yourdomain.com)"

The OrganizzeApi struct centralize all API actions already implemented. After building it passing the auth data, simply call the desired method as shown:

```go
package main

import (
	"github.com/B0go/organizzego"
	"github.com/B0go/organizzego/model"
)

func main() {
	organizzeApi := organizzego.OrganizzeApi{"username", "api-token", "You (you@yourdomain.com)"}

        statement := model.Statement{"blah2", "2017-07-16", 10}

	organizzeApi.CreateStatement(statement)
}
```

## Actions already implemented

* Statement Creation


## Contributing
If you need to send more data to Organizze, feel free to open a pull request adding it on each struct.

Any other improvement are wellcome.
