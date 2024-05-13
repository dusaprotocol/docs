---
sidebar_position: 4
sidebar_label: Bin Id From Price
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Get Bin Id From Price

As mentioned previously, it is possible to link a `bin` to a price. It is also possible to perform the conversion in the other direction and thus link a price to a `bin`. We provide examples to get the `binId` from a price.

### Conversion Functions

As the previous example, it is necessary to know the `binStep` of the underlying pair. Here is the conversion logic.
<Tabs>
<TabItem value="typescript" label="Typescript">

```typescript
function getIdFromPrice(price: number, binStep: number): number {
  /**
   * Convert a price to the underlying binId.
   *
   * @param price - Price of the bin.
   * @param binStep - BinStep of the pair.
   * @return BinId of the underlying bin.
   */

  return Math.trunc(Math.log(price) / Math.log(1 + binStep / 10_000)) + 8388608;
}
```

</TabItem>
<TabItem value="python" label="Python" default>

```python
import math

def getIdFromPrice(price: float, binStep: int) -> int:
    """
    Convert a price to the underlying binId.

    :param price: Price of the bin.
    :param binStep: BinStep of the pair.
    :return: Id of the underlying bin.
    """

    return (
      math.trunc(math.log(price) / math.log(1 + binStep / 10_000)) + 8388608
    )
```

</TabItem>
</Tabs>

### Example

Here is an example to illustrate the conversion function with the [`USDC`/`DAI`](https://beta.dusa.io/pools/AS1217cAveD2H5rkuytUoiMEL1sg8BXwp966daPRoaoxmV8zv7Bdv/AS1sKBEGsqtm8vQhQzi7KJ4YhyaKTSkhJrLkRc7mQtPqme3VcFHm/2) pair which has a `binStep` of 2. We choose here a price equal to 1.0020019, as both tokens have 6 decimals.

```python
getIdFromPrice(1.0020019, 2)
>>> 8388618
```

For second example, let's take [`MAS`/`USDC`](https://beta.dusa.io/pools/AS12Emra1SrLsFgYdFRQXBjsksWummAs8zG14iFytS73bZBjbVY5v/AS1sKBEGsqtm8vQhQzi7KJ4YhyaKTSkhJrLkRc7mQtPqme3VcFHm/20) pair which has a `binStep` of 20. To choose price equal to 5.008 USDC / MAS we need to adjust it

$$
priceAdjusted = price\cdot 10^{(\text{decimalsY} - \text{decimalsX})}
$$

$$
priceAdjusted = 5 \cdot 10^{(\text{6} - \text{9})} = 0.005008
$$

```python
getIdFromPrice(0.005008, 20)
>>> 8385957
```
