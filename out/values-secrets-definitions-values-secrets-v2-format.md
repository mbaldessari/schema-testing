# Values Secrets V2 Format Schema

```txt
undefined#/definitions/valuesSecretsV2
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                              |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [values-secrets.v2.schema.json\*](values-secrets.v2.schema.json "open original schema") |

## valuesSecretsV2 Type

`object` ([Values Secrets V2 Format](values-secrets-definitions-values-secrets-v2-format.md))

# valuesSecretsV2 Properties

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                              |
| :------------------------------ | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [version](#version)             | Multiple | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-version.md "undefined#/definitions/valuesSecretsV2/properties/version")           |
| [backingStore](#backingstore)   | `string` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-backingstore.md "undefined#/definitions/valuesSecretsV2/properties/backingStore") |
| [vaultPolicies](#vaultpolicies) | `object` | Optional | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-vaultpolicies.md "undefined#/definitions/valuesSecretsV2/properties/vaultPolicies")                                   |
| [secrets](#secrets)             | `array`  | Required | cannot be null | [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secrets.md "undefined#/definitions/valuesSecretsV2/properties/secrets")                                               |

## version

Version of the secret specification

`version`

*   is required

*   Type: any of the folllowing: `number` or `string` ([Details](values-secrets-definitions-values-secrets-v2-format-properties-version.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-version.md "undefined#/definitions/valuesSecretsV2/properties/version")

### version Type

any of the folllowing: `number` or `string` ([Details](values-secrets-definitions-values-secrets-v2-format-properties-version.md))

## backingStore

Secrets backing store type

`backingStore`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-values-secrets-v2-format-properties-backingstore.md "undefined#/definitions/valuesSecretsV2/properties/backingStore")

### backingStore Type

`string`

### backingStore Default Value

The default value is:

```json
"vault"
```

## vaultPolicies

A dictionary of {name}:{policy} of custom vault password policies

`vaultPolicies`

*   is optional

*   Type: `object` ([Details](values-secrets-definitions-vaultpolicies.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-vaultpolicies.md "undefined#/definitions/valuesSecretsV2/properties/vaultPolicies")

### vaultPolicies Type

`object` ([Details](values-secrets-definitions-vaultpolicies.md))

## secrets

The list of secrets to be injected into the vault

`secrets`

*   is required

*   Type: `object[]` ([Details](values-secrets-definitions-secret.md))

*   cannot be null

*   defined in: [Hybrid Cloud Patterns - values-secret.yaml V2 schema](values-secrets-definitions-secrets.md "undefined#/definitions/valuesSecretsV2/properties/secrets")

### secrets Type

`object[]` ([Details](values-secrets-definitions-secret.md))
