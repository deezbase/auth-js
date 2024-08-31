# `auth-js`

An isomorphic JavaScript client library for the [Deezbase Auth](https://github.com/deezbase/auth) API.

## Docs

- Using `auth-js`: https://deezbase.com/docs/reference/javascript/auth-signup
- TypeDoc: https://deezbase.github.io/auth-js/v2

## Quick start

Install

```bash
npm install --save @deezbase/auth-js
```

Usage

```js
import { AuthClient } from '@deezbase/auth-js'

const GOTRUE_URL = 'http://localhost:9999'

const auth = new AuthClient({ url: GOTRUE_URL })
```

- `signUp()`: https://deezbase.io/docs/reference/javascript/auth-signup
- `signIn()`: https://deezbase.io/docs/reference/javascript/auth-signin
- `signOut()`: https://deezbase.io/docs/reference/javascript/auth-signout

### Custom `fetch` implementation

`auth-js` uses the [`cross-fetch`](https://www.npmjs.com/package/cross-fetch) library to make HTTP requests, but an alternative `fetch` implementation can be provided as an option. This is most useful in environments where `cross-fetch` is not compatible, for instance Cloudflare Workers:

```js
import { AuthClient } from '@deezbase/auth-js'

const AUTH_URL = 'http://localhost:9999'

const auth = new AuthClient({ url: AUTH_URL, fetch: fetch })
```

## Sponsors

We are building the features of Firebase using enterprise-grade, open source products. We support existing communities wherever possible, and if the products don’t exist we build them and open source them ourselves.

[![New Sponsor](https://user-images.githubusercontent.com/10214025/90518111-e74bbb00-e198-11ea-8f88-c9e3c1aa4b5b.png)](https://github.com/sponsors/deezbase)

