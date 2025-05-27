#core/appliedneuroscience

Spectral analysis in EEG is the **examination of the signal’s frequency content and involves techniques like Fast Fourier Transform (FFT) and Wavelet Transform.** These methods decompose the EEG signal into its constituent frequencies, revealing insights into the rhythmic and transient aspects of brain activity.

## Fast Fourier Transform (FFT)

![[fft.jpg]]

- **Mathematical Basis:** Efficiently computes the Discrete Fourier Transform (DFT) and its inverse. DFT decomposes a sequence of values into components of different frequencies.
- **Operation:** Transforms a signal from its original domain into a frequency domain representation. FFT reduces the number of computations from O(N^2) to O(N log N) through a divide-and-conquer strategy.
- **Application in EEG:** Used for power spectral density estimation, identifying dominant frequencies and their contributions, crucial for understanding rhythmic brain activity.

---

## Wavelet Transform

![[wavelet.png]]

- **Mathematical Basis:** Involves convolution of the EEG signal with wavelets. Wavelets are localised waves characterised by scale and position.
- **Types:** Continuous Wavelet Transform (CWT) for detailed analysis and Discrete Wavelet Transform (DWT) for fast computation.
- **Operation:** Offers a time-frequency representation of the EEG signal, adjusting time and frequency resolution for detailed transient analysis.
- **Application in EEG:** Ideal for non-stationary signal analysis, such as EEG, for detecting transient phenomena and characterising signal changes over time.

## [[Talairach atlas and MNI-ICBM AVG152#Comparative Insights|Comparative]] Note

- **Resolution:** FFT is preferred for its frequency resolution in stationary signals, while wavelet transform balances time and frequency resolution for non-stationary signals.
- **Application Suitability:** FFT is applied for stable frequency content analysis, and wavelet transform is preferred for signals with notable frequency and temporal dynamics.
