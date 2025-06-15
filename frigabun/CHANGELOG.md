## 3.1.2

- 96bc815 build(deps): bump github.com/labstack/echo/v4 from 4.13.3 to 4.13.4
- 405b7af build(deps): bump github.com/rs/zerolog from 1.33.0 to 1.34.0
- bae1fbb build(deps): bump github.com/spf13/viper from 1.19.0 to 1.20.0
- a07c3e2 build(deps): bump github.com/spf13/viper from 1.20.0 to 1.20.1
- de17053 build(deps): bump golang.org/x/net from 0.33.0 to 0.36.0
- 77e926e build(deps): bump golang.org/x/net from 0.36.0 to 0.38.0
- aa79064 chore: add changelog
- 98e9e62 chore: go mod tidy
- 2c367ce chore: go mod tidy
- 880bfd5 ci: bump mockery

## 3.1.1

- ff03ab4 build(deps): bump github.com/labstack/echo/v4 from 4.12.0 to 4.13.0
- 065a0c1 build(deps): bump github.com/labstack/echo/v4 from 4.13.0 to 4.13.1
- d9d439f build(deps): bump github.com/labstack/echo/v4 from 4.13.1 to 4.13.2
- 448c8b8 build(deps): bump github.com/labstack/echo/v4 from 4.13.2 to 4.13.3
- f1856ac build(deps): bump golang.org/x/crypto from 0.22.0 to 0.31.0

## 3.1.0

- 370e89c build(deps): bump github.com/stretchr/testify from 1.9.0 to 1.10.0
- 037c4b8 chore: change required coverage
- a9ee623 feat: allow omitting subdomain
  - thanks to [@katidiot](https://github.com/katidiot) for the suggestion!

## 3.0.2

- 84eda73 Update Dockerfile to use multi-stage build
- 1a98f49 Update porkbun API host in sample config
- 659dc51 build(deps): bump github.com/labstack/echo/v4 from 4.11.4 to 4.12.0
- 420ccbc build(deps): bump github.com/rs/zerolog from 1.32.0 to 1.33.0
- 88043a3 build(deps): bump github.com/spf13/viper from 1.18.2 to 1.19.0
- 578113a build(deps): bump github.com/stretchr/testify from 1.8.4 to 1.9.0
- b82efb7 doc: add ha repo instructions

## 3.0.1

- 7c10c37 doc: update readme
- 76ad359 feat: add support for config via homeassistant addon
- 21cc812 feat: make logging configurable

## 3.0.0

- c77dd4f doc: add api key instructions to readme
- 1327858 doc: add cloudflare to readme, update API doc
- d927232 ci: add test coverage check
- 936001c feat: add cloudflare support
- b3d1395 feat: add more params to logger
- 4c282dc feat: use viper for config
- f05318c fix: param naming for porkbun secret api key,
  [#12](https://github.com/davidramiro/frigabun/issues/12)
- 87be43d fix: prevent porkbun rate limit
- accb5d3 Merge pull request
  [#20](https://github.com/davidramiro/frigabun/issues/20) from
  davidramiro/feat/cloudflare
- bdf45fa Merge pull request
  [#21](https://github.com/davidramiro/frigabun/issues/21) from
  davidramiro/refactor/v3
- 382cb0f build(deps): bump github.com/go-faker/faker/v4 from 4.0.0 to 4.1.0
- aa3b85f build(deps): bump github.com/labstack/echo/v4 from 4.10.1 to 4.10.2
- 8fcbdcf build(deps): bump github.com/rs/zerolog from 1.29.0 to 1.29.1
- 3549a9f build(deps): bump github.com/stretchr/testify from 1.8.1 to 1.8.2
- 9acabfa build(deps): bump github.com/stretchr/testify from 1.8.2 to 1.8.4
- 51e7c51 chore: code style, update deps
- fa9ed00 refactor: add service interface and factory
- 32d4980 refactor: implement service interface
- 21ad5d5 refactor: move service factory
- 9701368 refactor: query porkbun record before create
- 618b449 refactor: refine error handling, add registered services to status
  endpoint
- a677a49 refactor: simplify logging
- 11cde81 refactor: use methods for dns structs
- b80ea4c refactor: use service factory in api handler

## 2.0.1

- f769357 fix: hide api secret in logs on porkbun requests
- f3b0ec3 feat: handle invalid registrar param

## 2.0.0

- a005486 feat: add support for porkbun
- 9e4caa8 build(deps): bump github.com/labstack/echo/v4 from 4.10.0 to 4.10.1
- 2ba8b75 refactor: restructure project, add tests
- da1a5ed tests: add test for porkbun

## 1.0.2

- caab0b0 feat: add config toggle for status request logging
- fd9fc11 feat: add option to hide api key from request log

## 1.0.1

- fe97f59 feat: add health check endpoint

## 1.0.0

- 782729a initial commit: rewrite fritzgandi
