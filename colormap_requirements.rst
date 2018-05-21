==========================
Requirements for Colormaps
==========================

General requirements
====================
Colormaps should all be perceptually uniform unless there is a very specific reason to create a break or discontinuity
(eg to highlight a particular value). The mapping from the full color spectrum color space onto the CVD colorspaces for
deuteranomaly and protanomaly should be one-to-one. If possible (and achievable if aiming for CVD compatibility) colormaps
should also be one-to-one to a gray-space colormap.

Radar reflectivity factor requirements
======================================
Equivalent radar reflectivity factor (henceforth reflectivity)  values, in dBZ have clear clusters corresponding to both
processes and resultant habits. Non precipitating
cloud returns, detected by the most sensitive of radars range from -80 to around -15dBZ, drizzle is occurs up to around 5dBZ
transitioning to rain up to values around 50dBZ where hail (or very high rainfall rates) cause elevated signals. Returns approaching
80dBZ have been observed, usually aloft and caused by massive hail in supercellular storms (or gross miscalibration).

Reflectivity enjoys the most frequent public consumption via weather.gov, apps like Radar Scope and on TV. In general
the higher the reflectivity the higher the chance of public impact (starting at around 45dBZ where, given the right
conditions local flooding can start to occur). Therefore higher values should be psychologically impactful. This is generally
achieved with hotter values like reds and purples.

Mean Doppler velocity requirements
==================================
Mean Doppler velocity (henceforth velocity) varies between minus nyuqist to positive nyquist unless a correcton has been
performed. There are three requirements for velocity. First the value at zero m/s (the zero isodope) has a special significance due to the
conical nature of sampling of the radar. Since the height of the radar pulse increases with range the curve of zero isodope
indicates the shear profile of the winds. Therefore there should be a special value of a change in hue, around the zero
isodope. Second, it is essential to be able to visually see the impact of Doppler velocity alaising. So the color at
positive nyquist should be highly contrasting with that at negative nyquist. Finally, viewers of velocity imagery need to
be able to quickly discern areas of incoming and outgoing velocities. Therefore the colors for negative and positive values
need to have distinctively different proporties like hue while maintaining CVD compatibility.

Differential reflectivity requirements
======================================
Differential reflectivity, the difference between vertical and horizontal returns to the radar, has values that generally
range from -2dB to 6dB for meteorological scatterers. Negative values mean either the radar is miscalibrated or the scattering medium
exhibits prolate anisotropy in the backscatter cross section. The only hydrometeors where this tends to happen is vertically
aligned ice but it can also happen with larger birds or clutter. High values of differential reflectivity are scientifically
 interesting so colors about around 3dB should be striking and there should be a clear break around 0dB. It is useful for
scientists, especially radar engineers, to quickly identify areas of 0dB as this is useful in determining the accuracy of
vertical to horizontal calibration when viewed next to reflectivity images (ie areas of low reflectivity should be near
0dB).

Correlation coefficient
=======================
The Correlation coefficient (cc) is a measure of how uniform the anisotropy is in a scattering volume. In areas of known high
 uniformity (eg stratiform rainfall) it can also provide an indication as to the cross polar coupling (and hence "quality"
of the radar system). CC can range from 0 to 1 and only a small part of the range, around 0.98 to 1, indicates fairly uniform
anisotropy. Therefore a colormap for CC needs reserve much of its contrast for the range from 0.98 to 1 while still, roughly,
communicating broad structure in lower values.



