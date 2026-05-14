---
title: "Programmable Control and Optimization of the Quantum Noise of Light"
layout: gridlay
sitemap: false
permalink: /research/programmable-quantum-noise/
---

<p><a href="{{ site.url }}{{ site.baseurl }}/research/">Back to research</a></p>

## Programmable control and optimization of the quantum noise of light

<div class="research-detail-figure">
<img src="{{ site.url }}{{ site.baseurl }}/images/research/programmable-quantum-noise.png" alt="Programmable control and optimization of the quantum noise of light">
<p>By reflecting light off of a spatial light modulator before being sent into an optical fiber, the correlations generated between different modes can be controlled, allowing for control over the noise. In the bottom panel, optimizing over the phases between modes strongly removes noise from the center of the beam, giving a shot-noise limited region of light despite strong excess noise.</p>
</div>

Many light sources, especially intense ones, have noise well above the shot noise level associated with coherent states of light. For example, high-power laser sources often carry excess noise from spontaneous emission, among other sources. This limits sensitivity, image contrast, and penetration depth, and necessitates longer acquisition times in optical coherence tomography. Despite the importance of noise, it is not known how to bring the excess noise of bright light sources down to shot noise levels while maintaining useful classical properties: reducing the excess noise by linear attenuation sacrifices too much power, and active stabilization only gets to 1.5 dB above the shot noise level and is limited by the power-handling capacity of photodetectors.

In recent work, we developed a new approach to controlling the noise of intense beams of light. It relies on the fact that when an intense beam of light propagates through a nonlinear medium, the nonlinearity generates correlations between different modes. Certain subsets of modes can develop anticorrelated response to input fluctuations, allowing the noise to be much lower than one would naively suspect. These correlations can be actively controlled by changing the relative phases between modes at the input of the nonlinear medium using, for example, a spatial light modulator.

The ability to do this enables an experimental optimization in which the cost function is the noise of some part of the beam and the optimization parameters are the relative phases of input modes. We showed that this form of laser stabilization can reduce the relative intensity noise of a part of a light beam by over 12 dB. Unlike conventional forms of laser stabilization, it is ultra-broadband, does not struggle near the quantum shot-noise level, and can in principle lead to noise below it.

Important to this work was the development of an adjoint model of the multimode generalized nonlinear Schrodinger equation describing the evolution of multimode ultrafast pulses in nonlinear optical waveguides. This adjoint model, common in machine learning and optimization applications, allows us to efficiently and accurately predict a wide range of quantum noise effects.

Related links: [arXiv](https://arxiv.org/pdf/2509.03482), [MultiModeNoise.jl](https://github.com/michaelhorodynski/MultiModeNoise.jl)
