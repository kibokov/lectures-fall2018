# lectures-fall2018

Lectures will be held in **[KPTC 206](https://www.google.com/maps/place/Kersten+Physics+Teaching+Center/@41.7910228,-87.6037179,17z/data=!3m1!4b1!4m5!3m4!1s0x880e293e862a1b5f:0x3726b2d1e371c9b8!8m2!3d41.7910228!4d-87.6015292)** on **Wednesdays at 7pm** throughout the quarter.

**Please fill out [this short survey](https://goo.gl/forms/deUMrr7leHhrq0eo1)!**

This repository hosts materials for a lecture series aimed at undergraduates offered at the University of Chicago during the Fall quarter in 2018.
The modules contained herein are meant to aid students through a series of lectures describing technical computing techniques often used in gravitational wave analyses. 

## lecture notes

Some lecture notes can be found within [this repostitory](https://github.com/uchicago-gw/lectures-fall2018/tree/master/lecture_notes).
Others can be found in [Google Drive](https://drive.google.com/drive/folders/1xwmOKxjHyTkvSpeAOS_-NaUv-15uKVEA).

A great list of papers about GW measurements is available at [papers.ligo.org](https://www.ligo.caltech.edu/page/detection-companion-papers).

## syllabus and futher reading

  * Oct 17: Introduction
    * Lecturer: [Zoheyr Doctor](zdoctor@uchicago.edu)
    * lecture notes
      * [notebook](https://github.com/uchicago-gw/lectures-fall2018/blob/master/lecture_notes/MassRadiusGW150914Class.ipynb)
      * [google sheet for zero-crossing times](https://docs.google.com/spreadsheets/d/1-KZ8zCI0sLLdETamXjnFnUk6ODnxpDhkcZ6ssXGQuc4/edit?usp=sharing)
    * further reading
        * [GW150914 detection PRL](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.116.061102)
        * [The basic physics of the binary black hole merger GW150914](https://arxiv.org/abs/1608.01940)

  * Oct 24: Stellar Structure and Neutron Stars
    * Lecturer: [Phil Landry](landryp@uchicago.edu)
    * lecture notes: ...
    * further reading
        * ...

  * Oct 31: Fourier Analysis
    * Lecturer: [Reed Essick](reedessick@uchicago.edu)
    * [lecture notes](https://github.com/uchicago-gw/lectures-fall2018/blob/master/lecture_notes/fourier_analysis.md)
    * further reading
        * ...

  * Nov 7: Machine Learning
    * Lecturer: [Zoheyr Doctor](zdoctor@uchicago.edu)
    * lecture notes: ...
    * further reading
        * ...

  * Nov 14: Cosmology
    * Lecturer: [Maya Fishbach](mfishbach@uchicago.edu)
    * lecture notes: ...
    * further reading
        * ...

  * Nov 21: Tolman-Oppenheimer-Volkoff Equations
    * Lecturer: [Phil Landry](landryp@uchicago.edu)
    * lecture notes: ...
    * further reading
        * ...

  * Nov 28: Time-series Analysis and Basci Parameter Estimation
    * Lecturer: [Reed Essick](reedessick@uchicago.edu)
    * [lecture notes](https://github.com/uchicago-gw/lectures-fall2018/blob/master/lecture_notes/stationary_gaussian_timeseries.md)
    * further reading
        * ...

  * Dec 5: Monte-Carlo Methods and the Hubble Constant
    * Lecturer: [Maya Fishbach](mfishbach@uchicago.edu)
    * lecture notes: ...
    * further reading
        * ...

## final projects

As part of this lecture series, you will be expected to complete a small project.
You must tell us what you plan to do for a final project by **Friday Nov 30, 2018** and final reports will be due on **Wednesday Dec 19, 2018**.
Please check with one of the lecturers if you have a specific idea you'd like to pursue.
Below, we've listed a few possibilities along with suggested steps

  * a few-parameter search for Gravitational Waves in stationary colored Gaussian noise
    * estimate the power spectral density of a timeseries (see [lecture 3](https://github.com/uchicago-gw/lectures-fall2018/tree/master/lecture3))
    * perform a matched-filter search: either convolution in the time domain or multiplication in the frequency domain
    * identify the time and rough parameters of the best-fit template for real data
  * sampling from a few-parameter posterior distribution for a real GW signal using [public data](https://www.gw-openscience.org/events/)
    * estimate the power spectral density (PSD) of a timeseries (see [lecture 3](https://github.com/uchicago-gw/lectures-fall2018/tree/master/lecture3))
    * compute the likelihood for observed data given the PSD and waveform parameters
    * use [emcee](http://dfm.io/emcee/current/) or another stochastic sampler or sampling method to generate the posterior distribution
  * inferring Hubble's constant using real, publicly available [GW170817 data](https://www.gw-openscience.org/events/GW170817/)
    * extract the 3-dimensional source localization for GW170817
    * estimate the redshift and redshift uncertainty of the host galaxy
    * marginalize away nuisance parameters to estimate the posterior distribution for the hubble constant
  * using real [GW170817 tidal deformability data](https://dcc.ligo.org/LIGO-P1800115/public) to rank a few [candidate neutron star equations of state](http://xtreme.as.arizona.edu/NeutronStars/) (EOS) by relative likelihood
    * estimate the likelihood from the publicly available data (a kernel density estimate is a good idea!)
    * integrate each EOS to obtain mass-tidal deformability curves
    * numerically estiamte the bayesian evidence for each EOS using the likelihood
  * anything else you can think of; just run it by us first!
  
Projects should be relativley short and take you no more than 10 hours to complete.
Reports should be 2-3 pages written in the style of a short research paper (a.k.a., a [letter](https://journals.aps.org/prl/authors)).
Please include a brief introduction a paragraph or two of background material describing your project before presenting your results.
You should include citations where appropriate (i.e., cite [losc.ligo.org](https://losc.ligo.org/) if you use real GW data) and include a bibliography, although the bibliography will not count toward the length of your  report.

In addition to describing your results with at least one figure, please submit the source code you develop during the project.
Code can be in whatever format is easiest for you as long as it can be read without undue effort (i.e., no compiled code).

Projects are meant to give you the chance to "get your hands dirty" with real data or real applications.
Be sure to show your work with comments in your code and describe whatever conclusions you draw.
If you're not sure about something, describe how you tested your hypotheses and explored.
Your approach and thought process count more than the final numbers you produce!

## installation

We highly recommend you use Python notebooks with standard anaconda installations.
However, if you are comfortable with other IDEs, all our modules should work with relatively standard dependencies (numpy, scipy, etc).

### anaconda

(Ana)conda installation instructions are available [here](https://conda.io/docs/user-guide/install/index.html).
There are separate instructions for various OSs

  * [Windows](https://conda.io/docs/user-guide/install/windows.html)
  * [MacOS](https://conda.io/docs/user-guide/install/macos.html) (ask Zoheyr or Maya for help if needed)
  * [Linux](https://conda.io/docs/user-guide/install/linux.html) (ask Reed or Phil for help if needed)

### this repository

This repository can be installed via standard tools

```
    git clone https://github.com/uchicago-gw/lectures-fall2018.git
    cd lectures-fall2018
    python setup.py install --prefix /path/to/install
```

don't forget to update your `PYTHONPATH` accordingly. For example,

```
    python setup.py install --prefix /home/albert.einstein/opt
    export PYTHONPATH=/home/albert.einstein/opt/lib/python2.7/site-packages:$PYTHONPATH
```
