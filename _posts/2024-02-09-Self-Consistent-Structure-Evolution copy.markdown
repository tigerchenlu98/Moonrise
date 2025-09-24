---
layout: post
title:  "Self-Consistent Structure and Dynanical Evolution"
date:   2025-09-23 00:49:03 +0300
thumbnail: /images/hatp11.png
---
<i>Recently I've been thinking a lot about how a planet's changing interior structure can affect its motion, and vice versa.</i>

It behooves us to remember that planets are not points. Planets are dynamic -- they shrink as the heat of their formation fades away. Their spins evolve as they accrete gas from the circumplanetary disk. And most importantly, if you heat up a planet, whether that be through tides or some other mechanism, the planet puffs up like a hot air balloon.

<img src="/images/hatp11.png" alt="HAT-P-11"
     style="display:block; margin:20px auto; width:80%; max-width:300px; height:auto; border-radius:8px;">

This is HAT-P-11, my favorite exoplanet system (it's actually tattooed on my right shoulder)! The 3D architecture of the HAT-P-11 system was measured by Qier An, a co-author on this work. And it is fascinating: both planets in the system are eccentric and misaligned, in contrast to the circular aligned orbits one would expect. In other words, every aspect of this system is a dynamical puzzle. To a dynamicist like me, systems like HAT-P-11 scream an obvious origin -- the so-called <i>von Zeipel-Lidov-Kozai (ZLK)</i> effect. Fun fact: the ZLK effect was first discovered when satellite orbits started going haywire due to the influence of the Moon. In multi-planet systems the ZLK effect causes the inner planet to undergo massive eccentricity and inclination oscillations. Tidal evolution does the rest, and ZLK evolution tends to form these extremely strange systems that we've seen.

The goal of this project was initially pretty simple: to reproduce the dynamical history of HAT-P-11 through the ZLK effect. The problem was it didn't work. In every simulation we tried, HAT-P-11b passed so close to the central star that it was ripped apart. HAT-P-11c was too close, its effect too strong, and it invariably forced HAT-P-11b onto an orbit so eccentric it could not avoid destruction.

It turns out the key was to account for, you guessed it, structure evolution. When HAT-P-11b gets very eccentric, it is blasted by tons of tidal heating, puffing the planet up. This introduces a small competing force that stops HAT-P-11b from getting so close to the star. Not enough to prevent the formation of the system, but <i>just</i> enough to prevent the planet's destruction.

I am <b>very</b> excited about right now. The slight puffing up of a planet as it ages may seem a small effect, and it is. But even the smallest person can change the course of the future. And in this case, this change is as profound as the different between a planet orbiting its star happily on a close-in orbit, and its desiccated remains floating through space after its been ripped apart.

<p><strong>Relevant Papers:</strong></p>
<ul>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2025ApJ...979..218L/abstract" style="color:blue;"><i><b>Lu</b>, An, Li, et al. (2025)</i></a></li>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2025AJ....169...22A/abstract" style="color:blue;"><i>An, <b>Lu</b>, Brandt, et al. (2025)</i></a></li>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2016ARA%26A..54..441N/abstract" style="color:blue;"><i>Naoz (2016)</i></a></li>
</ul>
