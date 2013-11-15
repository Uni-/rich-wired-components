Rich Wired Componenets: the RWNumber module
===========================================

Introduction
------------

RWNumber is a module for representing arbitrary number.

Format
------

No other base is supported than decimal.

* natural: `0 | \[1-9\]\[0-9\]\*`
* real, fixed point: `\[0-9\]+ | \[0-9\]\* . \[0-9\]+`
* real, floating point: `(fixed-point) (e|E) (\+|\-)* \[0-9\]+`
