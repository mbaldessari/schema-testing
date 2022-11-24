# Untitled object in Hybrid Cloud Patterns - values-secret.yaml V2 schema Schema

```txt
undefined#/definitions/Secret
```

The single secret to be injected into the vault

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [values-secrets.v2.schema.json\*](values-secrets.v2.schema.json "open original schema") |

## Secret Type

`object` ([Details](values-secrets-definitions-secret.md))

# Secret Properties

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                     |
| :------------------------------ | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                   | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-name.md "undefined#/definitions/Secret/properties/name")                   |
| [vaultMount](#vaultmount)       | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultmount.md "undefined#/definitions/Secret/properties/vaultMount")       |
| [vaultPrefixes](#vaultprefixes) | `array`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultprefixes.md "undefined#/definitions/Secret/properties/vaultPrefixes") |
| [fields](#fields)               | `array`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-fields.md "undefined#/definitions/Secret/properties/fields")               |

## name

This is the name of the top level key that will be created at the vaultMount point and that will contain one secret per field inside its attributes

`name`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-name.md "undefined#/definitions/Secret/properties/name")

### name Type

`string`

## vaultMount

This is the vault -mount=<...> mount point used in vault commands

`vaultMount`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultmount.md "undefined#/definitions/Secret/properties/vaultMount")

### vaultMount Type

`string`

### vaultMount Default Value

The default value is:

```json
"secret"
```

## vaultPrefixes

This is the list of prefixes the secret will be uploaded to

`vaultPrefixes`

*   is optional

*   Type: `string[]`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultprefixes.md "undefined#/definitions/Secret/properties/vaultPrefixes")

### vaultPrefixes Type

`string[]`

## fields

This is the list of actual secret material that will be placed in a vault key's attributes

`fields`

*   is optional

*   Type: `object[]` ([Details](values-secrets-definitions-field.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-fields.md "undefined#/definitions/Secret/properties/fields")

### fields Type

`object[]` ([Details](values-secrets-definitions-field.md))
