---
outline: deep
head:
  - - meta
    - property: og:title
      content: TurnkeySigner • getAddress
  - - meta
    - name: description
      content: Overview of the getAddress method on TurnkeySigner
  - - meta
    - property: og:description
      content: Overview of the getAddress method on TurnkeySigner
---

# getAddress

`getAddress` returns the EOA address of the Signer.

This method must be called after [`authenticate`](/packages/aa-signers/turnkey/authenticate). Otherwise, this method will throw an error with the message `Not Authenticated`.

## Usage

::: code-group

```ts [example.ts]
import { createTurnkeySigner } from "./turnkey";
// [!code focus:99]
const turnkeySigner = await createTurnkeySigner();

const address = await turnkeySigner.getAddress();
```

<<< @/snippets/turnkey.ts
:::

## Returns

### `Promise<Address>`

A Promise containing the address of the Signer.
