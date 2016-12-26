---
title: "Flat Belt Drive Design"
output:
  html_document:
    toc: true
    toc_float: true
    theme: sandstone
    highlight: default
    fig_width: 7
    fig_height: 6
    fig_caption: true
---

# Calculations
## Velocity Ratio

$$ \frac{N_{i}}{N_{o}} = \frac{d_{o}}{d_{i}} = \text{Speed ratio} $$

Standard pulley diameters

> 40, 45, 50, 56, 63, 71, 80, 90, 100, 112, 125, 140, 160, 180, 200, 224, 250, 280, 315, 355, 400, 450, 500, 560, 630, 710, 800, 900, 1000, 1120, 1250, 1400,1600, 1800, 2000

[Source](http://mechteacher.com/flat-belt-design/#ixzz4Txx4FaWZ)

## Design Power

$$ \text{Design power} = \frac{\text{Rated power} * \text{Load correction factor}}{\text{Contact factor} * \text{Smaller pulley diameter factor}}, $$

where the rated power is a project parameter and the correction factors may be determined by the following equations and attached tables.

$$ \text{Contact factor} = 180° - \frac{D-d}{C} * 60° $$

After finding the arc of contact, it must be changed to the nearest standardized value, as shown in Table 2.

The number of plies may be chosen by using reference tables, e.g. Shigley's or PSG Machine Design Handbook's.

## Belt and Pulley Width

$$ b = \frac{\text{Design power}}{\text{No. of plies} * \text{Load rating at operating speed}} mm $$

The value calculated with the formula above must be substituted by the nearest standardized value, which can be consulted in catalogues.

Additional width in the pulley is needed in order to accomodate properly the belt. As we are working with relatively low torques, an additional width of 15 mm is enough.

## Belt Length

For an open flat belt drive, it is given by:

$$ L = 2*C + \frac{\pi}{2} * (d_{0} + d_{i}) + \frac{(d_{0} - d_{i})^{2}}{4} * C $$


# List of Variables

Variable      | Description
------------- | -------------
$N_{i}$       | Speed of the driving pulley in rpm (input)
$N_{o}$       | Speed of the driven pulley in rpm (output)
$d_{i}$       | Diameter of the driving pulley in mm
$d_{o}$       | Diameter of the driven pulley in mm
C             | Centre distance between pulleys


# Auxiliar Tables
## Table 1: Load correction factor

Type of load      | Applications      | Correction factor
----------------- | ----------------- | -----------------
Normal | Known maximum load | 1.0
Steady | Light duty rotating machines, printing machinery, centrifugal pumps, evaporators and light machinery | 1.2
Intermittent | Heavy machine tools, heavy duty fans, compressors, reciprocating pumps, elevators, mill machinery, paper and saw machinery | 1.3
Shock | Hammers, grinders, crushing machines, vacuum pumps, tube mills, stamp presses and automated machinery | 1.5

## Table 2: Arc of contact factor
Arc of Contact      |	Arc of Contact Factor
-----------------   | -----------------
90° | 1.68
120°  | 1.33
130°  | 1.26
140°  | 1.19
150°  | 1.13
160°  | 1.08
170°  | 1.04
180°  | 1.00
190°  | 0.97
200°  | 0.94
210°  | 0.91
220°  | 0.88
230°  | 0.86
240°  | 0.84
250°  | 0.82

## Table 3: Smaller pulley diameter factor
Smaller Pulley Diameter (in mm) | Smaller Pulley Diameter Factor
----------------- | -----------------
 <= 100 | 0.5
 100-200  | 0.6
 200-300  | 0.7
 300-400  | 0.8
 400-750  | 0.9
 > 750  | 1.0
