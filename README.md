# PulseMF [![DOI](https://zenodo.org/badge/151828731.svg)](https://zenodo.org/badge/latestdoi/151828731)

##### Pulsating Membership Functions
A special case of the [M-Fuzzy-Membership Function](https://github.com/somefunAgba/MFuzzyMF)

#### Usage
###### PULSEMF(X, PARAMS, OPTION) returns a matrix which is the  low or high triggered pulse-shaped membership function evaluated at X,

OPTION = 0, 1

###### 0 -> Low-Triggered Pulse, output = 1010

###### 1 -> High-Triggered Pulse, output = 0101 [Default]

###### PARAMS = [X0,X1,..,X5] is an 5-element vector that determines the break points of this membership function.

##### Example:

![url](pulse_view.svg)

```Matlab
x = 0:0.1:10;
subplot(421); ax11 = plot(x, pulsemf(x, [2.5 3 4 4.5 5.5], 0), '--.b');
ax11.LineWidth = 1.5;ax11.MarkerSize = 10;
grid on; grid minor;
subplot(423); ax21 = plot(x, pulsemf(x, [2 3.5 5 5.5 6], 0), '--.b');
ax21.LineWidth = 1.5;ax21.MarkerSize = 10;
grid on; grid minor;
subplot(425); ax31 = plot(x, pulsemf(x, [4 4.2 4.6 5 5.8 ], 0), '--.b');
ax31.LineWidth = 1.5;ax31.MarkerSize = 10;
grid on; grid minor;
subplot(427); ax41 = plot(x, pulsemf(x, [1 3.2 5.2 5.8 6], 0), '--.b');
ax41.LineWidth = 1.5;ax41.MarkerSize = 10;
grid on; grid minor;
subplot(422); ax12 = plot(x, pulsemf(x, [2.5 3 4 4.5 5.5]), '--r.');
ax12.LineWidth = 1.5; ax12.MarkerSize = 10;
grid on; grid minor;
subplot(424); ax22 = plot(x, pulsemf(x, [2 3.5 5 5.5 6]), '--r.');
ax22.LineWidth = 1.5;ax22.MarkerSize = 10;
grid on; grid minor;
subplot(426); ax32 = plot(x, pulsemf(x, [4 4.2 4.6 5 5.8 ]), '--r.');
ax32.LineWidth = 1.5;ax32.MarkerSize = 10;
grid on; grid minor;
subplot(428); ax42 = plot(x, pulsemf(x, [1 3.2 5.2 5.8 6]), '--r.');
ax42.LineWidth = 1.5;ax42.MarkerSize = 10;
grid on; grid minor;
set(gcf, 'name', 'pulsemf', 'numbertitle', 'off');
```
