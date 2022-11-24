# Untitled string in Hybrid Cloud Patterns - values-secret.yaml V2 schema Schema

```txt
undefined#/definitions/Field/properties/onMissingValue
```

'error' will generate an error if the secret (via value or via path attributes) are not defined. 'generate' will create a secret using a defined vaultPolicy. 'prompt' will ask the user for input and it requires to set a value or a path depending if the user should input a secret or a path to a secret file. Non-null entries represent the default value when prompted.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [values-secrets.v2.schema.json\*](values-secrets.v2.schema.json "open original schema") |

## onMissingValue Type

`string`

## onMissingValue Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value        | Explanation |
| :----------- | :---------- |
| `"error"`    |             |
| `"generate"` |             |
| `"prompt"`   |             |
