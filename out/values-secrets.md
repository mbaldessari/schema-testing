# Hybrid Cloud Patterns - values-secret.yaml V2 schema Schema

```txt
undefined
```

This schema defines the values-secret.yaml file as used by Validated Patterns at <https://hybrid-cloud-patterns.io>

| Abstract               | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                            |
| :--------------------- | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------ |
| Cannot be instantiated | Yes        | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [values-secrets.v2.schema.json](values-secrets.v2.schema.json "open original schema") |

## Hybrid Cloud Patterns - values-secret.yaml V2 schema Type

`object` ([Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets.md))

## Hybrid Cloud Patterns - values-secret.yaml V2 schema Examples

```json
"`http://github.com/hybrid-cloud-patterns/common/examples/secrets`"
```

# Hybrid Cloud Patterns - values-secret.yaml V2 schema Definitions

## Definitions group valuesSecretsV2

Reference this group by using

```json
{"$ref":"undefined#/definitions/valuesSecretsV2"}
```

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                              |
| :------------------------------ | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [version](#version)             | `string` | Required | can be null    | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-version.md "undefined#/definitions/valuesSecretsV2/properties/version")           |
| [backingStore](#backingstore)   | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-backingstore.md "undefined#/definitions/valuesSecretsV2/properties/backingStore") |
| [vaultPolicies](#vaultpolicies) | `object` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-vaultpolicies.md "undefined#/definitions/valuesSecretsV2/properties/vaultPolicies")                                   |
| [secrets](#secrets)             | `array`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secrets.md "undefined#/definitions/valuesSecretsV2/properties/secrets")                                               |

### version

Version of the secret specification

`version`

*   is required

*   Type: `string`

*   can be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-version.md "undefined#/definitions/valuesSecretsV2/properties/version")

#### version Type

`string`

#### version Default Value

The default value is:

```json
"1.0"
```

### backingStore

Secrets backing store type

`backingStore`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-backingstore.md "undefined#/definitions/valuesSecretsV2/properties/backingStore")

#### backingStore Type

`string`

#### backingStore Default Value

The default value is:

```json
"vault"
```

### vaultPolicies

A dictionary of {name}:{policy} of custom vault password policies

`vaultPolicies`

*   is optional

*   Type: `object` ([Details](values-secrets-definitions-vaultpolicies.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-vaultpolicies.md "undefined#/definitions/valuesSecretsV2/properties/vaultPolicies")

#### vaultPolicies Type

`object` ([Details](values-secrets-definitions-vaultpolicies.md))

### secrets

The list of secrets to be injected into the vault

`secrets`

*   is required

*   Type: `object[]` ([Details](values-secrets-definitions-secret.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secrets.md "undefined#/definitions/valuesSecretsV2/properties/secrets")

#### secrets Type

`object[]` ([Details](values-secrets-definitions-secret.md))

## Definitions group VaultPolicies

Reference this group by using

```json
{"$ref":"undefined#/definitions/VaultPolicies"}
```

| Property | Type | Required | Nullable | Defined by |
| :------- | :--- | :------- | :------- | :--------- |

## Definitions group VaultPolicy

Reference this group by using

```json
{"$ref":"undefined#/definitions/VaultPolicy"}
```

| Property | Type | Required | Nullable | Defined by |
| :------- | :--- | :------- | :------- | :--------- |

## Definitions group Secrets

Reference this group by using

```json
{"$ref":"undefined#/definitions/Secrets"}
```

| Property | Type | Required | Nullable | Defined by |
| :------- | :--- | :------- | :------- | :--------- |

## Definitions group Secret

Reference this group by using

```json
{"$ref":"undefined#/definitions/Secret"}
```

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                     |
| :------------------------------ | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                   | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-name.md "undefined#/definitions/Secret/properties/name")                   |
| [vaultMount](#vaultmount)       | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultmount.md "undefined#/definitions/Secret/properties/vaultMount")       |
| [vaultPrefixes](#vaultprefixes) | `array`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultprefixes.md "undefined#/definitions/Secret/properties/vaultPrefixes") |
| [fields](#fields)               | `array`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-fields.md "undefined#/definitions/Secret/properties/fields")               |

### name

This is the name of the top level key that will be created at the vaultMount point and that will contain one secret per field inside its attributes

`name`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-name.md "undefined#/definitions/Secret/properties/name")

#### name Type

`string`

### vaultMount

This is the vault -mount=<...> mount point used in vault commands

`vaultMount`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultmount.md "undefined#/definitions/Secret/properties/vaultMount")

#### vaultMount Type

`string`

#### vaultMount Default Value

The default value is:

```json
"secret"
```

### vaultPrefixes

This is the list of prefixes the secret will be uploaded to

`vaultPrefixes`

*   is optional

*   Type: `string[]`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-vaultprefixes.md "undefined#/definitions/Secret/properties/vaultPrefixes")

#### vaultPrefixes Type

`string[]`

### fields

This is the list of actual secret material that will be placed in a vault key's attributes

`fields`

*   is optional

*   Type: `object[]` ([Details](values-secrets-definitions-field.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secret-properties-fields.md "undefined#/definitions/Secret/properties/fields")

#### fields Type

`object[]` ([Details](values-secrets-definitions-field.md))

## Definitions group Field

Reference this group by using

```json
{"$ref":"undefined#/definitions/Field"}
```

| Property                          | Type      | Required | Nullable       | Defined by                                                                                                                                                                     |
| :-------------------------------- | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name-1)                   | `string`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-name.md "undefined#/definitions/Field/properties/name")                     |
| [onMissingValue](#onmissingvalue) | `string`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-onmissingvalue.md "undefined#/definitions/Field/properties/onMissingValue") |
| [prompt](#prompt)                 | `string`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-prompt.md "undefined#/definitions/Field/properties/prompt")                 |
| [value](#value)                   | `string`  | Optional | can be null    | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-value.md "undefined#/definitions/Field/properties/value")                   |
| [path](#path)                     | `string`  | Optional | can be null    | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-path.md "undefined#/definitions/Field/properties/path")                     |
| [vaultPolicy](#vaultpolicy)       | `string`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-vaultpolicy.md "undefined#/definitions/Field/properties/vaultPolicy")       |
| [base64](#base64)                 | `boolean` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-base64.md "undefined#/definitions/Field/properties/base64")                 |

### name

This is the name of the attribute inside vault

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-name.md "undefined#/definitions/Field/properties/name")

#### name Type

`string`

### onMissingValue

'error' will generate an error if the secret (via value or via path attributes) are not defined. 'generate' will create a secret using a defined vaultPolicy. 'prompt' will ask the user for input and it requires to set a value or a path depending if the user should input a secret or a path to a secret file. Non-null entries represent the default value when prompted.

`onMissingValue`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-onmissingvalue.md "undefined#/definitions/Field/properties/onMissingValue")

#### onMissingValue Type

`string`

#### onMissingValue Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value        | Explanation |
| :----------- | :---------- |
| `"error"`    |             |
| `"generate"` |             |
| `"prompt"`   |             |

### prompt

Represents the prompt used when onMissingValue is set to prompt

`prompt`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-prompt.md "undefined#/definitions/Field/properties/prompt")

#### prompt Type

`string`

### value

Is the value of a secret. Represents the default value when onMissingValue is set to prompt

`value`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-value.md "undefined#/definitions/Field/properties/value")

#### value Type

`string`

### path

Is the path to a secret file. Represents the default path when onMissingValue is set to prompt

`path`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-path.md "undefined#/definitions/Field/properties/path")

#### path Type

`string`

### vaultPolicy

When onMissingValue is set to 'generate', uses the policy to create the secret inside the vault directly

`vaultPolicy`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-vaultpolicy.md "undefined#/definitions/Field/properties/vaultPolicy")

#### vaultPolicy Type

`string`

### base64

Before uploading the secret the content is base-64 encoded. It is recommended to set this to true when dealing with files

`base64`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-base64.md "undefined#/definitions/Field/properties/base64")

#### base64 Type

`boolean`

#### base64 Default Value

The default value is:

```json
"false"
```
