# IdentityCreateTransitionWASM

This class allows to create instance of IdentityCreateTransition struct

`IdentityCreateTransitionWASM` can be created via constructor, `default()`, bytes and state transition

Constructor params:

- `publicKeys -> [IdentityPublicKeyInCreationWASM]`
- `assetLock -> AssetLockProofWASM`
- `userFeeIncrease -> Number`
- `signature -> ?ArrayLike`
- `identityId -> IdentifierWASM | String | ArrayLike`

___

## Navigation

- [Example](#Example)
- [Fields](#fields)
    - [userFeeIncrease](#userfeeincrease)
    - [assetLock](#assetlock)
- [Getters](#getters)
    - [getSignableBytes](#getsignablebytes)
    - [toBytes](#tobytes)
    - [toStateTransition](#tostatetransition)

___

### Example

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)
// or
const bytes = [0, 0, 0, 162, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 60, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 255, 255, 255, 255, 0, 255, 255, 255, 255, 1, 255, 255, 255, 255, 255, 255, 255, 255, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
const transition = wasm.IdentityCreateTransitionWASM.fromBytes(bytes)
```

___

## Fields

All fields are readable and writable.

### `userFeeIncrease`

Contains userFeeIncrease in `Number`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

transition.userFeeIncrease = 99

transition.userFeeIncrease // -> Number
```

___

### `assetLock`

Contains asset lock proof in `AssetLockProofWASM`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

const anotherAssetLockProof = wasm.AssetLockProofWASM.createInstantAssetLockProof(
  // instant lock
  [1, 1, 193, 219, 244, 102, 77, 20, 251, 187, 201, 109, 168, 125, 7, 244, 118, 119, 210, 53, 238, 105, 138, 31, 7, 73, 30, 128, 131, 175, 114, 76, 187, 37, 0, 0, 0, 0, 177, 215, 65, 96, 204, 228, 86, 13, 14, 185, 46, 65, 241, 38, 226, 172, 59, 96, 158, 15, 126, 90, 225, 3, 140, 221, 96, 131, 254, 12, 236, 26, 48, 124, 31, 23, 184, 202, 122, 231, 123, 59, 43, 118, 27, 214, 225, 58, 44, 191, 232, 10, 33, 35, 8, 113, 145, 159, 158, 88, 80, 0, 0, 0, 173, 103, 128, 160, 29, 226, 161, 219, 167, 194, 158, 38, 19, 51, 143, 248, 161, 87, 126, 32, 143, 209, 152, 44, 174, 6, 25, 210, 101, 127, 131, 65, 202, 241, 47, 166, 132, 10, 199, 15, 187, 136, 11, 217, 237, 13, 173, 64, 11, 6, 112, 188, 234, 239, 204, 29, 3, 6, 35, 154, 44, 106, 44, 183, 171, 126, 146, 240, 153, 210, 187, 56, 133, 161, 11, 4, 151, 63, 89, 20, 44, 66, 153, 242, 97, 207, 44, 110, 208, 51, 198, 113, 104, 79, 154, 19],
  // transaction
  [3, 0, 8, 0, 1, 193, 219, 244, 102, 77, 20, 251, 187, 201, 109, 168, 125, 7, 244, 118, 119, 210, 53, 238, 105, 138, 31, 7, 73, 30, 128, 131, 175, 114, 76, 187, 37, 0, 0, 0, 0, 106, 71, 48, 68, 2, 32, 2, 146, 73, 163, 223, 124, 140, 225, 109, 126, 239, 87, 105, 184, 118, 87, 182, 100, 182, 6, 15, 200, 26, 44, 33, 215, 165, 110, 211, 232, 245, 233, 2, 32, 69, 161, 168, 128, 101, 26, 171, 20, 63, 30, 219, 87, 23, 4, 142, 115, 73, 73, 170, 203, 46, 187, 149, 32, 210, 171, 46, 136, 253, 188, 36, 12, 1, 33, 2, 144, 231, 28, 153, 30, 92, 52, 10, 111, 47, 107, 74, 225, 237, 151, 33, 188, 184, 247, 121, 70, 135, 174, 31, 160, 16, 216, 239, 225, 103, 88, 112, 255, 255, 255, 255, 2, 64, 66, 15, 0, 0, 0, 0, 0, 2, 106, 0, 216, 154, 230, 5, 0, 0, 0, 0, 25, 118, 169, 20, 229, 154, 45, 140, 145, 114, 18, 52, 205, 13, 179, 84, 94, 174, 149, 207, 101, 115, 51, 240, 136, 172, 0, 0, 0, 0, 36, 1, 1, 64, 66, 15, 0, 0, 0, 0, 0, 25, 118, 169, 20, 176, 213, 107, 82, 203, 147, 209, 128, 255, 63, 69, 219, 41, 250, 232, 254, 185, 168, 85, 184, 136, 172],
  // output index
  0
)

transition.assetLockProof = anotherAssetLockProof

transition.assetLockProof // -> AssetLockProofWASM
```

___

### `publicKeys`

Contains public keys in `[IdentityPublicKeyInCreationWASM]`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

const publicKeyInCreation = new wasm.IdentityPublicKeyInCreationWASM(
  0,
  'AUTHENTICATION',
  'master',
  'ECDSA_SECP256K1',
  false,
  Buffer.from('0333d5cf3674001d2f64c55617b7b11a2e8fc62aab09708b49355e30c7205bdb2e', 'hex'),
  []
)

transition.publicKeys = [publicKeyInCreation]

transition.publicKeys // -> [IdentityPublicKeyInCreationWASM]
```

___

## Getters

### `getSignableBytes`

Returns bytes for sign in `Uint8Array`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

transition.getSignableBytes() // -> Uint8Array

```

___

### `toBytes`

Returns transition in `Uint8Array`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

transition.toBytes() // -> Uint8Array

```

___

### `toStateTransition`

Returns `StateTransitionWASM`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

transition.toStateTransition() // -> StateTransitionWASM

```

___

### `getIdentifier`

Allows to get identity Identifier in `IdentifierWASM`

```js
const transition = wasm.IdentityCreateTransitionWASM.default(0)

transition.getIdentifier() // -> IdentifierWASM
```