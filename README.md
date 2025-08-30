# IdealSampling
# Aim
Write a simple Python program for the construction and reconstruction of ideal sampling.
# Tools required
# Program
 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.signal import resample
 fs = 100
 t = np.arange(0, 1, 1/fs) 
 f = 5
 signal = np.sin(2 * np.pi * f * t)
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal')
 plt.title('Continuous Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()
 t_sampled = np.arange(0, 1, 1/fs)
 signal_sampled = np.sin(2 * np.pi * f * t_sampled)
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
 plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()
 reconstructed_signal = resample(signal_sampled, len(t))
 plt.figure(figsize=(10, 4))
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
 plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show()

# Output Waveform
<img width="1920" height="1020" alt="Screenshot 2025-08-30 152733" src="https://github.com/user-attachments/assets/3d8911eb-5e43-45bc-b748-af0d93417a32" />
<img width="1920" height="1020" alt="Screenshot 2025-08-30 152742" src="https://github.com/user-attachments/assets/1a44fa73-dbac-4cc8-87c5-9a002c50c5ac" />
<img width="1920" height="1020" alt="Screenshot 2025-08-30 152746" src="https://github.com/user-attachments/assets/0b47e56e-5549-443d-b6f1-ff9943e1d412" />
Results

Hence Wrote a simple Python program for the construction and reconstruction of idealsampling.

