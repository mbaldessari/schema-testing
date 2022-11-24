# Untitled object in Hybrid Cloud Patterns - values-secret.yaml V2 schema Schema

```txt
undefined#/definitions/Field
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [values-secrets.v2.schema.json\*](values-secrets.v2.schema.json "open original schema") |

## Field Type

`object` ([Details](values-secrets-definitions-field.md))

# Field Properties

| Property                          | Type      | Required | Nullable       | Defined by                                                                                                                                                                     |
| :-------------------------------- | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                     | `string`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-name.md "undefined#/definitions/Field/properties/name")                     |
| [onMissingValue](#onmissingvalue) | `string`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-onmissingvalue.md "undefined#/definitions/Field/properties/onMissingValue") |
| [prompt](#prompt)                 | `string`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-prompt.md "undefined#/definitions/Field/properties/prompt")                 |
| [value](#value)                   | `string`  | Optional | can be null    | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-value.md "undefined#/definitions/Field/properties/value")                   |
| [path](#path)                     | `string`  | Optional | can be null    | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-path.md "undefined#/definitions/Field/properties/path")                     |
| [vaultPolicy](#vaultpolicy)       | `string`  | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-vaultpolicy.md "undefined#/definitions/Field/properties/vaultPolicy")       |
| [base64](#base64)                 | `boolean` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-base64.md "undefined#/definitions/Field/properties/base64")                 |

## name

This is the name of the attribute inside vault

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-name.md "undefined#/definitions/Field/properties/name")

### name Type

`string`

## onMissingValue

'error' will generate an error if the secret (via value or via path attributes) are not defined. 'generate' will create a secret using a defined vaultPolicy. 'prompt' will ask the user for input and it requires to set a value or a path depending if the user should input a secret or a path to a secret file. Non-null entries represent the default value when prompted.

`onMissingValue`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-onmissingvalue.md "undefined#/definitions/Field/properties/onMissingValue")

### onMissingValue Type

`string`

### onMissingValue Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value        | Explanation |
| :----------- | :---------- |
| `"error"`    |             |
| `"generate"` |             |
| `"prompt"`   |             |

## prompt

Represents the prompt used when onMissingValue is set to prompt

`prompt`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-prompt.md "undefined#/definitions/Field/properties/prompt")

### prompt Type

`string`

## value

Is the value of a secret. Represents the default value when onMissingValue is set to prompt

`value`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-value.md "undefined#/definitions/Field/properties/value")

### value Type

`string`

## path

Is the path to a secret file. Represents the default path when onMissingValue is set to prompt

`path`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-path.md "undefined#/definitions/Field/properties/path")

### path Type

`string`

## vaultPolicy

When onMissingValue is set to 'generate', uses the policy to create the secret inside the vault directly

`vaultPolicy`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-vaultpolicy.md "undefined#/definitions/Field/properties/vaultPolicy")

### vaultPolicy Type

`string`

## base64

Before uploading the secret the content is base-64 encoded. It is recommended to set this to true when dealing with files

`base64`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-field-properties-base64.md "undefined#/definitions/Field/properties/base64")

### base64 Type

`boolean`

### base64 Default Value

The default value is:

```json
"false"
```
