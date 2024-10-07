# $roleInfo
Returns the role information.

## Usage
```py
$roleInfo[(Guild ID;Role ID);Param]
```

## Parameters
| Label | Description | Required |
| ----- | ----------- | -------- |
| Guild ID | Guild ID to return this information. | False |
| Role ID | Role ID to return this information. | False |
| Param | What param of information should be returned? | True |

### Supported inputs for `Param`
| Input | Description |
| ----- | ----------- |
| color | Returns color role. |
| created | Returns the time when the role was created. |
| emoji | Returns the emoji that is associated with the role. |
| guild | Returns the guild ID in which the role is located. |
| hoist | Returns information is shown separately from others. |
| managed | Returns information whether the role is linked to a platform. |
| mention | Returns information whether a role can be mentioned. |
| name | Return role name. |
| position | Return role position. |
| tags | Return tags role |