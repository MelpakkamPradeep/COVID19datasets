# COVID19datasets (Source: WHO COVID Data)

v1 dataset contains the cases for each country, along with whether the day is part of a "wave" (1) or not (0).
v2 dataset contains the cases for each country over a week, with "wave" corresponding to T7 case data.
v1.5 dataset contains the case data for each stretch of "wave" and "non-wave".

# Wave Classification
Since waves can be thought as deviations from the level of the data, we first mean normalize the data for each country. This gives us a natural definition of when a wave occurs. If the case on a day is greater than the total mean, the day is part of a wave (Wave = 1) else nor (Wave = 0). To remove fluctuations in the data, before the labelling the normalized data is double smoothed (Simple Exp Smoothing + LOESS Smoothing). These methods preserve the underlying shape of the data. To make the labelling more accurate, a correction factor 'k' is used to retroactively label more of the data by dividing the length of a labelled wave by 'k' and including this in the label. k = 6 is used here.

As better wave definitions/'k' value comes up, the dataset labels will be updates.
