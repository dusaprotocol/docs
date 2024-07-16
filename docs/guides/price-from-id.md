---
sidebar_position: 3
sidebar_label: Price From Bin Id
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Get Price From Bin Id

In v2.1 each `bin` holds the liquidity of the pair for a specific price range. Thus, it is possible to link a certain `bin` to a price by using the `id` of the underlying `bin`. We provide examples to get the price from a `binId`.

### Conversion Functions

In order to link a `binId` to a price it is necessary to know the `binStep` of the underlying pair. Here is the conversion logic.
<Tabs>
<TabItem value="typescript" label="Typescript">

```typescript
function getPriceFromId(binId: number, binStep: number): number {
  /**
   * Convert a binId to the underlying price.
   *
   * @param binId - Bin Id.
   * @param binStep - binStep of the pair.
   * @return Price of the bin.
   */

  return (1 + binStep / 10_000) ** (binId - 8388608);
}
```

</TabItem>
<TabItem value="python" label="Python" default>

```python
def getPriceFromId(binId: int, binStep: int) -> float:
    """
    Convert a binId to the underlying price.

    :param binId: Bin Id.
    :param binStep: BinStep of the pair.
    :return: Price of the bin.
    """

    return (1 + binStep / 10_000) ** (binId - 8388608)
```

</TabItem>
</Tabs>

### Example

Here is an example to illustrate the conversion function with the [`USDC`/`DAI`](https://beta.dusa.io/pools/AS1217cAveD2H5rkuytUoiMEL1sg8BXwp966daPRoaoxmV8zv7Bdv/AS1sKBEGsqtm8vQhQzi7KJ4YhyaKTSkhJrLkRc7mQtPqme3VcFHm/2) pair which has a `binStep` of 2. We choose here a `binId` equal to 8388618. Price returned doesn't need to be adjusted, as both tokens have 6 decimals.

```python
getPriceFromId(8388618, 2)
>>> 1.0020018009603358

```

For second example, let's take [`MAS`/`USDC`](https://beta.dusa.io/pools/AS12Emra1SrLsFgYdFRQXBjsksWummAs8zG14iFytS73bZBjbVY5v/AS1sKBEGsqtm8vQhQzi7KJ4YhyaKTSkhJrLkRc7mQtPqme3VcFHm/20) pair which has a `binStep` of 20. We choose `binId` equal to 8385957.

```python
getPriceFromId(8385957, 20)
>>> 0.00500806804134404

```

$$
priceAdjusted = price\cdot 10^{(\text{decimalsX} - \text{decimalsY})}
$$

$$
priceAdjusted = 0.00500806804134404 \cdot 10^{(\text{9} - \text{6})} = 5.00806804134404
$$
