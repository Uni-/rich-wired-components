Rich Wired Components: the RWLength module
==========================================

Introduction
------------

RWLength is a module for representing arbitrary physical length.

Expression
----------

An RWLength expression is anything parsed into:
* a RWNumber value, and
* a length metric (optional).

The metric is translated by the following steps.
* If the metric is a reserved keyword or a valid functional expression, use it as evaluated.
* If the metric is in a form of an optional SI prefix and a SI length unit, use it as is.
    * A metric can be written in the full name with no space; e.g. both 'nm' and 'nanometer' is allowed. 'nanom' or 'nmeter' is not allowed.
    * Prefix 'μ'(micro) can be substituted by 'u'.
* If no metric is specified, it can be presumed by the default designated by the parent module agent.
* If the metric contains no length unit itself and never presumed, assume the unit is meter(m).
    * e.g. '460u' matches this rule, so it is equivalent to '460um'.

Keywords
--------

* `lights`, equiv. to '2.99792458e+8m'.
* `planck`, equiv. to '1.616199e-35m'.

Functions
---------

* `radio` translates an RWChemical expression into an RWLength value.
