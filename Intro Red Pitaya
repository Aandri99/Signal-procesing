Using the Red Pitaya for measuring properties of periodic waveforms
============================================================================

Goals of this Lab
-------------------

1. Demonstrate ability to use Oscilloscope, Signal Generator, and Spectrum Analyzer capabilities of Red Pitaya through GUI.

2. Configure Red pitaya to receive external inputs.

3. Perform measurements on a multitude of periodic waveforms

Tasks / Measurements

--------------------
Configure the Red Pitaya for a Loopback configuration (SMA cables tied between the outputs and inputs to the Red Pitaya) as shown in Fig. 1.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image1.jpeg
   :alt: A picture containing text, electronics Description
   automatically generated
   :width: 4.1149in
   :height: 1.5in

Fig. 1: Red Pitaya in Loopback Configuration

Measure the Period of a waveform – Time Domain
-----------------------
Open the Oscilloscope & function Generator Application.

Configure the output of the red pitaya for a 1500Hz Sinusoid as shown in Fig. 2.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image2.png
   :width: 1.23547in
   :height: 2in

Fig. 2: OUT1 Configuration for measuring period/frequency

Configure the trigger for a negative edge trigger with zero level and normal trigger mode as shown in Fig. 3.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image3.png
   :width: 1.11555in
   :height: 2in

Fig. 3: Trigger Configuration

Enable OUT1. You should now see a figure close to the following

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image4.png
   :width: 3.69297in
   :height: 2.75in

Fig. 4: Target output for 1500 Hz Sinusoid with negative edge triggering

To measure the period,

1. Select the “Cursor” box, and enable “X1”, “X2” options.

2. Drag each cursor to a common feature of the waveform (peak to peak, trough to trough)

3. Read off spacing between cursors. This is an approximate measure of the period

Period can also be measured by the red pitaya itself, under the meas command by selecting “Period” and “IN2”, and finally selecting “Done”.
This is shown in Fig. 5.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image5.png
   :width: 3.51721in
   :height: 2.5in

Fig. 5: Measured waveform vs Cursor measurement

Measure the Fundamental Frequency of a waveform – Time Domain
-------------------------------------------------------------

To measure the fundamental frequency of a waveform, bring up the X1,X2 cursors, and select a single period of the waveform. From there one can
use the relation:

.. math::

   \begin{matrix}
   f = \frac{1}{T}\ \#(1) \\
   \end{matrix}

to estimate the frequency of the waveform.

Once again, the Red pitaya can also calculate this by selecting the “FREQ” measurement option in the “Meas” options as shown below.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image6.png
   :width: 3.86893in
   :height: 2.75in

Fig. 6: Frequency Measurement added

Measure the Phase between two waveforms – Time Domain
-----------------------------------------------------

Select output 2, and select the second output to be a 1500 Hz sine wave with a 45 degree phase shift

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image7.png
   :width: 1.19879in
   :height: 2in

Fig. 7: Second channel configuration

Configure the trigger for a single shot acquisition as shown in Fig. 8.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image8.png
   :width: 1.12857in
   :height: 2in

Fig. 8: Trigger configuration

Acquire a single capture, and measure the frequency and period of each waveform as previously described. Note that for the second channel, you
may want to specify your cursors to track channel 2 in the cursor menu. To measure the Phase between waveforms, simply calculate the difference
in time between two corresponding peaks between waveforms, and convert this to their corresponding difference in angular frequency. This can be
calculated for signals of equal frequency with the relation

.. math::

   \begin{matrix}
   \phi = 2\pi f\Delta t\ \ \ (rad)\ \#(2) \\
   \end{matrix}

1. Analytically calculate the period of either waveform, and the time delay expected for the configured 45 degree phase shift between waveforms.

2. Set the output frequency of a OUT1 to 1000 Hz and trigger to normal or auto. What is the behavior that is observed? Comment as to the origin 
   of the behavior, and a potential fix for the behavior. (hint,consider the greatest common divisor between the two frequencies)

3. (Take home) Repeat part 2, but for the frequency values of 3000Hz, and 1531Hz. What behavior is displayed here for each frequency? What are 
   some potential ways to work around this problem? (hint, consider the greatest common divisor between the two frequencies, and
   alternative trigger modes)

Measure the Spectrum of the waveform - Frequency Domain
-------------------------------------------------------

Open the DFT Spectrum Analyzer Application.

Recreate the waveform employed in ‎2.1. For convenience, this is reprinted below:

1. Configure the output of the red pitaya for a 1500Hz Sinusoid as shown
   in Fig. 2.

Set the Span of the spectrum analyzer to 6.5 kHz.

Observe the location of the peak(s), and infer what this implies about the sinusoid’s fundamental frequency and its purity (harmonic content). Mention 
the relative strength between the various peaks in dB and in linear scales, knowing the relation between dB and linear scales in dBm is given by:

.. math::

   \begin{matrix}
   P_{dBm} = 10\log_{10}\frac{P_{lin}}{1mW}\ \#(3) \\
   \end{matrix}

Comparing Waveforms in the Time domain
--------------------------------------

Configure the Red Pitaya for a Loopback configuration (SMA cables tied between the outputs and inputs to the Red Pitaya) as shown in Fig. 1.

Reference Case: Sine and Cosine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Set OUT1 and OUT2 to be sines of the same frequency of 1000Hz, with equal amplitude. Set OUT2 to have a phase of 90 degrees.

|Graphical user interface Description automatically generated|\ |A screenshot of a phone Description automatically generated with medium
confidence|

Fig. 9: Reference waveforms

1. Capture a screen shot of the resulting waveforms. Comment on any visible similarities or differences.

2. Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in the
   time domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each.

3. (Take Home) Drop the amplitude of OUT2 to 0.45 V (0.5x amplitude). How much does the waveform’s Peak-to-Peak value change by?

Sine and Square
~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a SQUARE, as shown in Fig. 10.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image11.png
   :alt: Graphical user interface Description automatically generated
   with medium confidence
   :width: 1.18395in
   :height: 2in

Fig. 10: OUT1 Configured for SQUARE output

1. Capture a screen shot of the resulting waveforms. Comment on and visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed 
   in the time domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between 
   each channel. For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:

Sine and Sawtooth
~~~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a SAWU, as shown in Fig. 11.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image12.png
   :alt: Graphical user interface Description automatically generated
   :width: 1.18812in
   :height: 2in

Fig. 11: OUT1 Configured for SAWU output

1. Capture a screen shot of the resulting waveforms. Comment on any visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed 
   in the time domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each channel. 
   For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:

(Take Home) Sine and Pulse Width Modulated (PWM) output
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a PWM with a 10% duty cycle, as shown in Fig. 12.

.. image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image13.png
   :alt: Graphical user interface Description automatically generated
   with low confidence
   :width: 1.18367in
   :height: 2in

Fig. 12: OUT 1 configured for PWM output

1. Capture a screen shot of the resulting waveforms. Comment on any visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in the
   frequency domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each channel. 
   For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:

   d. Duty Cycle:

Comparing Waveforms in Frequency Domain
---------------------------------------

Configure the Red Pitaya for a Loopback configuration (SMA cables tied between the outputs and inputs to the Red Pitaya) as shown in Fig. 1. 
Open the DFT Spectrum Analyzer application. **This portion is equivalent to viewing all the waveforms in part ‎2.5 in the Frequency Domain.**

Reference Case: Sine and Cosine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Set OUT1 and OUT2 to be sines of the same frequency of 1000Hz, with equal amplitude. Set OUT2 to have a phase of 90 degrees, as shown in Fig. 9.

1. Capture a screen shot of the resulting spectrums/spectrograms. Comment on any visible similarities or differences.

2. Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in the frequency
   domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each.

3. (Take Home) Drop the amplitude of OUT2 to 0.45 V (0.5x amplitude). How much do the peaks corresponding to this waveform shift by in dBm?


Sine and Square
~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a SQUARE, as shown in Fig. 10.

1. Capture a screen shot of the resulting spectrums/spectrograms. Comment on any visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in 
   the frequency domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each channel.
   For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:

Sine and Sawtooth
~~~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a SAWU, as shown in Fig. 11.

1. Capture a screen shot of the resulting spectrums/spectrograms. Comment on any visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in the
   frequency domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each channel. 
   For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:


(Take Home) Sine and Pulse Width Modulated (PWM) output
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

With the same setup as ‎‎2.5.1, change OUT1 to produce a PWM, as shown in Fig. 12.

1. Capture a screen shot of the resulting spectrums/spectrograms. Comment on any visible similarities or differences.

2. (Take Home) Try varying amplitudes/frequencies/phases of both channels and comment on the overall effects each variable does as observed in the 
   frequency domain. Capture a screen capture that demonstrates each observable change, and clearly label what change was done between each channel.
   For any parameters that do not produce visible changes, comment on why you believe this is so.

   a. Amplitude:

   b. Frequency:

   c. Phase:

   d. Duty Cycle:

Inferences to be made / Questions
=================================

1. From the previous sets of measurements what instrument(s) would you use to measure each of the following quantities:

A. Amplitude:

B. Frequency:

C. Phase:

Reference text
==============

For more in-depth documentation, view the official documentation at:

Oscilloscope:
https://redpitaya.readthedocs.io/en/latest/appsFeatures/apps-featured/oscSigGen/osc.html

Spectrum Analyzer:
https://redpitaya.readthedocs.io/en/latest/appsFeatures/apps-featured/spectrum/spectrum.html

dB scale: 
https://en.wikipedia.org/wiki/Decibel

.. |Graphical user interface Description automatically generated| image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image9.png
   :width: 1.22517in
   :height: 2in
.. |A screenshot of a phone Description automatically generated with medium confidence| image:: vertopal_731800f41f7745ee952b5f4e35d32883/media/image10.png
   :width: 1.17608in
   :height: 2in
