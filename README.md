# PhysiologicalSignalsAI-Udacity
This is the forth project in fulfilment of the **AI for Healthcare** *Udacity Nanodegree*. The goal of this project is to develop an algorithm that estimate the pulse rate by reading PPG and accelerometer signals. The following Background are adopted from [*Udacity* project repository](https://github.com/udacity/nd320-c4-wearable-data-project-starter).

## Background
The following description of PPG principal is taken from [here](https://github.com/udacity/nd320-c4-wearable-data-project-starter#physiological-mechanics-of-pulse-rate-estimation).

Pulse rate is typically estimated by using the PPG sensor. When the ventricles contract, the capilaries in the wrist fill with blood. The (typically green) light emitted by the PPG sensor is absorbed by red blood cells in these capilaries and the photodetector will see the drop in reflected light. When the blood returns to the heart, fewer red blood cells in the wrist absorb the light and the photodetector sees an increase in reflected light. The period of this oscillating waveform is the pulse rate.
However, the heart beating is not the only phenomenon that modulates the PPG signal. Blood in the wrist is fluid, and arm movement will cause the blood to move correspondingly. During exercise, like walking or running, we see another periodic signal in the PPG due to this arm motion. Our pulse rate estimator has to be careful not to confuse this periodic signal with the pulse rate.
We can use the accelerometer signal of our wearable device to help us keep track of which periodic signal is caused by motion. Because the accelerometer is only sensing arm motion, any periodic signal in the accelerometer is likely not due to the heart beating, and only due to the arm motion. If our pulse rate estimator is picking a frequency that's strong in the accelerometer, it may be making a mistake.
All estimators will have some amount of error. How much error is tolerable depends on the application. If we were using these pulse rate estimates to compute long term trends over months, then we may be more robust to higher error variance. However, if we wanted to give information back to the user about a specific workout or night of sleep, we would require a much lower error.

<figure>
  <p align="center">
  <img
  src="ppg_mechanics.png"
  alt="PPG"></p>
  <figcaption><p align="center">PPG signal & Blood Flow </p></figcaption>
</figure>
