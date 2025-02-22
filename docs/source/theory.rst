Theory of Operation
===================

The Output module accepts line signals (10Vpp) at the inputs. With :math:`R=100\mathrm{k}\Omega`, the input impedance ranges from :math:`R||R_i` to :math:`R`. The gain of the input stage is :math:`A_i = -\frac{R_f}{R_i}`. Gain options include 2.2 (:math:`R_i = 100k\Omega`, :math:`R_f=220k\Omega`), 4.5 (:math:`R_i=47k\Omega`, :math:`R_f=220k\Omega`) or 10 (:math:`R_i=47k\Omega`, :math:`R_f=470k\Omega` per MFOS).

.. image:: _static/images/mixer_input.png
    :width: 400
    :alt: Mixer input

At the output of the input gain stage, the panning network sends the signal to the line out buffers and stereo out amplifiers on the left and right channels. Here, the lower fixed :math:`R` also acts as the input resistance for the inverting summing amplifier (line out buffering), and :math:`V_{o(l|r)} = -\frac{R_{fo}}{R}\left(V_{i(l|r)1} + V_{i(l|r)2}\right)`. With the variable resistor :math:`R` for panning, the voltages :math:`V_{ir}` and :math:`V_{il}` will be in the range :math:`0 \leq V_{i(r|l)} \leq \frac{V_i}{3}`, so an output stage gain of 3 will restore the signal level.   

.. image:: _static/images/panning_network.png
    :width: 400
    :alt: Panning network

