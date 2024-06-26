# Calculation of sCO2 properties for the Brayton cycle

The program is based on the liquid properties library `pyfluids`.

### Units
- temperature - degree Celsius _(°C)_;
- absolute pressure _(Pa)_

Parameter values ​​are specified as a tuple. For secondary parameters, the calculated range is determined in the tuple.

## Dependence of specific heat on pressure

```python
from sCO2turboProp import PropSCO2
temperature = (32, 40, 50, 60, 600)
ts = PropSCO2()
ts.diagramm_pressure(pressure=(1e6, 20e6), temperature=temperature)
```

## Temperature dependence of specific heat

```python
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.diagramm_temperature(pressure=(7.4e6, 10e6, 15e6, 20e6), temperature=(20, 200))
```

## Compressibility factor

```python
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.compressibility(pressure=(5e6, 10e6), temperature=(32, 40, 60, 100, 300, 500))
```

## Theoretical useful work in the Brayton cycle

```python
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.work(pressure=(5e6, 10e6), pressure_rate=2., temperature=(32, 600))
```

## About the author
Sergey Besedin,
dr. of sc., prof.
