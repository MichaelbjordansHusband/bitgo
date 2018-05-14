# BitGo Golang SDK V2

The BitGo Platform and SDK makes it easy to build multi-signature Bitcoin applications today.

[![Build Status](https://travis-ci.com/jazzserve/bitgo.svg?branch=master)](https://travis-ci.com/jazzserve/bitgo)

# Installing
Use `go get` to install the latest version of the library. This command will install the `BitGo Golang SDK` executable along with the library and its dependencies:

    go get -u github.com/jazzserve/bitgo

Next, include library in your application:

```go
import "github.com/jazzserve/bitgo"
```
# Documentation

View [API Documentation](https://www.bitgo.com/api/v2).

# Example Usage

## List Wallets
```go
b := bitgo.New("prod", "{Access token}")

list, err := b.Coin("btc").ListWallets(nil)
if err != nil {
	log.Fatal(err.Error())
}

for _, w := range list.Wallets {
	log.Println(w.ID, w.Label)
}
```
