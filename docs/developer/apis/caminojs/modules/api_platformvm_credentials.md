# Module: API-PlatformVM-Credentials

## Index

### Classes

- [SECPCredential](../classes/api_platformvm_credentials.secpcredential)

### Functions

- [SelectCredentialClass](api_platformvm_credentials#const-selectcredentialclass)

## Functions

### `Const` SelectCredentialClass

▸ **SelectCredentialClass**(`credid`: number, ...`args`: any[]): _[Credential](../classes/common_signature.credential)_

_Defined in [src/apis/platformvm/credentials.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/credentials.ts#L17)_

Takes a buffer representing the credential and returns the proper [Credential](../classes/common_signature.credential) instance.

**Parameters:**

| Name      | Type   | Description                                                                 |
| --------- | ------ | --------------------------------------------------------------------------- |
| `credid`  | number | A number representing the credential ID parsed prior to the bytes passed in |
| `...args` | any[]  | -                                                                           |

**Returns:** _[Credential](../classes/common_signature.credential)_

An instance of an [Credential](../classes/common_signature.credential)-extended class.
