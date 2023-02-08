# Simple Calculator

```php
$simpleCalculatorController = $client->getSimpleCalculatorController();
```

## Class Name

`SimpleCalculatorController`


# Get Calculate

Calculates the expression using the specified operation.

```php
function getCalculate(array $options): float
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`string (OperationTypeEnum)`](../../doc/models/operation-type-enum.md) | Template, Required | The operator to apply on the variables |
| `x` | `float` | Query, Required | The LHS value |
| `y` | `float` | Query, Required | The RHS value |
| `z` | `string` | Query, Required | asad |

## Response Type

`float`

## Example Usage

```php
$collect = [];

$operation = Models\OperationTypeEnum::MULTIPLY;
$collect['operation'] = $operation;

$x = 222.14;
$collect['x'] = $x;

$y = 165.14;
$collect['y'] = $y;

$z = 'z4';
$collect['z'] = $z;

$result = $simpleCalculatorController->getCalculate($collect);
```

