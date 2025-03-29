# micrograd

## Definition of Derivative

## Definition of `Value` Class

use `children` to store previous operands

## Calculate Gradients

Calculate gradients by calculation graph and chain rule:

1. multiplication: d * f = L => d.grad = f, f.grad = d
2. addition: c + e = d => c.grad = e.grad = 1
3. chain rule: dL / dc = (dL / dd) * (dd / dc) = f
4. tanh: o = tanh(n), do / dn = 1 - o**2

`backward()`: call `_backward()` for each node in reversed topological order

`+= grad` rather than `= grad (reset)` to avoid overwriting issue

## Enhance `class Value`

Change `__add__`, `__mul__`, `__mul__` to add support for raw value (not `Value` class)