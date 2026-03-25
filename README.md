# Spectral Analysis of Deterministic Signals

This project implements spectral analysis of various types of signals using the Fast Fourier Transform (FFT) and its inverse (IFFT). 
The work was developed as part of a course on Numerical Modeling in Acoustics.

## This work includes
- Generation of different signal types:
  - Harmonic signals (sine, cosine)
  - Pulse signals (triangle, rectangular, Gaussian)
  - Periodic pulse sequences
  - Modulated versions of the above signals
- Signal operations:
  - Summation of multiple signals
  - Amplitude modulation
- Spectral analysis:
  - Fast Fourier Transform (FFT)
  - Inverse Fast Fourier Transform (IFFT)
- Visualization:
  - Time-domain signals
  - Frequency-domain spectra
  - Reconstructed signals

## Project Structure

The implementation follows an object-oriented approach and consists of three main classes:

### Signal

Responsible for generating signals and combining them.

#### Capabilities:

- Create sine and cosine waves
- Generate pulse signals:
  - Triangle
  - Rectangular (meander)
  - Gaussian
- Sum multiple signals into one

### Wave

Represents a signal in the time domain.

#### Attributes:

- Time axis (ts)
- Signal values (ys)
- Frequency, amplitude, duration
- Modulation parameters

#### Methods:

- modulate_wave() — amplitude modulation of harmonic signals
- modulate_pulse() — modulation of pulse signals

### Spectrum

Handles frequency-domain representation.

#### Methods:

- FFT(signal) — computes spectrum of a signal
- IFFT(spectrum) — reconstructs signal from spectrum

### Notes:

- Only the first two periods are shown in time-domain plots
- Irrelevant near-zero amplitudes are omitted in spectra