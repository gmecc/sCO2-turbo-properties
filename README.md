# Программа расчета свойств sCO2

Программа основана на библиотеке свойств жидкостей `pyfluids`.


### Зависимость теплоемкости от давления

```
from sCO2turboProp import PropSCO2
temperature = [32, 40, 50, 60, 600]
ts = PropSCO2()
ts.diagramm_pressure(pressure=(1e6, 20e6), temperature=temperature)
```

### Температурная зависимость теплоемкости

```
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.diagramm_temperature(pressure=[7.4e6, 10e6, 15e6, 20e6], temperature=(20, 200))
```

### Сжимаемость

```
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.compressibility(pressure=(5e6, 10e6), temperature=(32, 40, 60, 100, 300, 500))
```

### Теоретическая полезная работа цикла

```
from sCO2turboProp import PropSCO2
ts = PropSCO2()
ts.work(pressure=(5e6, 10e6), pressure_rate=2., temperature=(32, 600))
```
