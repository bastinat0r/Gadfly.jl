---
title: Geom.vline
author: Daniel Jones
part: Geometry
order: 15
...

Draw vertical lines across the plot canvas.

# Aesthetics

  * `xintercept`: X-axis intercept

# Arguments

  * `color`: Color of the lines.
  * `size`: Width of the lines.

# Examples

```{.julia hide="true" results="none"}
using RDatasets
using Gadfly

Gadfly.prepare_display()
Gadfly.set_default_plot_size(14cm, 8cm)
```

```julia
plot(data("datasets", "iris"), x="Sepal.Length", y="Sepal.Width",
	 xintercept=[5.0, 7.0], Geom.point, Geom.vline)
```

```julia
# Colors and widths of lines can be changed. This works separately from the
# `color` and `size` aesthetics.
plot(data("datasets", "iris"), x="Sepal.Length", y="Sepal.Width",
	 xintercept=[5.0, 7.0], Geom.point,
	 Geom.vline(color="orange", size=2mm))
```
