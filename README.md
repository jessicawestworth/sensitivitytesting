
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Sensitivity Testing

<!-- badges: start -->
<!-- badges: end -->

The goal of this sensitivity testing is to make logical changes to the
mizer model outlined in the [mizer
course](https://mizer.course.nov22.sizespectrum.org), and evaluate how
flexible the current model creation process and the final model are to
simple parameter changes.

Documentation of the changes made, and their resulting effects on the
steady state of the model, as well as its outputs, can be found in the
PDF documents in this repository. The final models created after each
change are also included.

## Summary of Changes

Below is a summary of the changes documented in each file:

### [`sensitivitytesting.pdf`](https://github.com/jessicawestworth/sensitivitytesting/blob/main/sensitivitytesting.pdf)

This document replicates the methodology shown in the [mizer course
model](https://github.com/gustavdelius/mizerCourse), with one key
difference:

1.  When the course model calls for loading species data from FishBase,
    **updated FishBase data** is used instead of the original FishBase
    data used upon creation of the course and course model.

- As a result, the final size spectrum model differs from the course
  version.

- We then attempt to **fit the parameters** of the new model to those of
  the course model and observe how similar the final models become.

### [`usingalternativemaxsizes.pdf`](https://github.com/jessicawestworth/sensitivitytesting/blob/main/usingalternativemaxsizes.pdf)

This document replicates the methodology shown in the [Mizer course
model](https://github.com/gustavdelius/mizerCourse), with two key
differences:

1.  The use of **updated FishBase data** when the course model creation
    methodology calls for loading species data from FishBase.

2.  The use of the median l_max and w_max parameters for all species
    from FishBase rather than those utilized in [Spence et
    al. (2021)](https://onlinelibrary.wiley.com/doi/10.1111/faf.12543).

- We then attempt to run the model to a steady state.

### [`adjustingw_maxofthefinalcoursemodel.pdf`](https://github.com/jessicawestworth/sensitivitytesting/blob/main/adjustingw_maxofthefinalcoursemodel.pdf)

This document uses the [final model
course](https://github.com/gustavdelius/mizerCourse/blob/master/build/cel_model_landings.rds),
with one key change made:

1.  The models species params l_max and w_max of the course model
    species params object are replaced with the updated FishBase l_max
    and w_maxvalues.

- We then attempt to run the model to a steady state.

### [`adjustingcatchcurves.pdf`](https://github.com/jessicawestworth/sensitivitytesting/blob/main/adjustingcatchcurves.pdf)

This document uses the [final course
model](https://github.com/gustavdelius/mizerCourse/blob/master/build/cel_model_landings.rds),
with one key change made:

1.  Small adjustments to catchability, L50, L50-L25, w_mat, and
    w_mat25/w_mat, are made to fit the catch curves slightly differently
    than those provided in the final course model.

- Model is run to a steady state and its resulting outputs are observed.

------------------------------------------------------------------------
