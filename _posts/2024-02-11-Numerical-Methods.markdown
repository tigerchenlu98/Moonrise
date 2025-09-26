---
layout: post
title:  "Numerical Methods"
date:   2025-09-23 00:49:03 +0300
thumbnail: /images/numerical_methods_sq.png
---
<i>I develop novel numerical tools to improve the speed and accuracy of N-body simulations.</i>

<img src="/images/numerical_methods.jpg" alt="Flowchart of logic for the TRACE algorithm, described on this page"
     style="display:block; margin:20px auto; width:80%; max-width:300px; height:auto; border-radius:8px;">

The complex topic of planetary dynamics can be elegantly distilled into the so-called <i>N</i>-body problem: given the initial positions of <i>N</i> number of particles interacting under the influence of gravity, can you tell me where they will be at some future point in time? It turns out you can't. Well, unless <i>you</i> can, in which case you may have a Nobel prize waiting for you. Jokes aside, try as we may an exact solution to the <i>N</i>-body problem have evaded us so far. Thus, in lieu of an exact analytic solution we must resort to simulations that approximately solve the <i>N</i>-body problem. Here lies the crux of the issue -- while analytic methods are exact and instant, numerical methods are both expensive (time-wise) and inexact. A great deal of my research has gone towards making these simulations less expensive and more accurate.

The most popular software used to simulate the dynamics of planetary system is [REBOUND](https://rebound.readthedocs.io/en/latest/), developed and maintained by [Hanno Rein](https://hanno-rein.de/). REBOUND is a publicly available open-source package and all of the tools I develop live in the REBOUND ecosystem. It is a fantastic package that I am very proud to have contributed to!

I say this a lot: there is <b>no one</b> in the world who wants you to use these tools more than I do. So I am always very happy to look over code or help debug if you have any questions at all about any of the tools I've made. Just shoot me an email! You get to use my code, my code gets used, everyone wins.

-----
<div class="feature-row">
  <img src="/images/TRACE_schematic.png"
       alt="Very simplified version of how TRACE works"
       style="width:150px; height:auto; border-radius:2px;">
  <div>
    <h1 id="trace">TRACE</h1>
    <p>
      is a code for <b>T</b>ime <b>R</b>eversible <b>A</b>strophysical <b>C</b>lose <b>E</b>ncounters. TRACE is a hybrid integrator, meaning it uses a <a href="https://ui.adsabs.harvard.edu/abs/1991AJ....102.1528W/abstract" style="color:black;">fast inflexible method</a> most of the time and switches to a highly accurate flexible method only when it has to. The tricky thing about constructing hybrid integrators is deciding when to make this switch. The novelty of TRACE is that we switch in a manner that respects the time-reversibility of the natural world, following an astonishingly elegant algorithm developed by my collaborator (and co-author on this work) <a href="https://www.davidmhernandez.com/" style="color:black;">David Hernandez</a>. TRACE is mostly applied to highly chaotic systems with many close encounters between planets, and in these applications we've found it to be over 10x faster than previous state-of-the-art hybrid integrators with no penalty to accuracy.
    </p>
    <p><strong>Relevant Papers:</strong></p>
    <ul>
      <li><a href="https://ui.adsabs.harvard.edu/abs/2024MNRAS.533.3708L/abstract" style="color:blue;"><i><b>Lu</b>, Hernandez & Rein (2024)</i></a></li>
      <li><a href="https://ui.adsabs.harvard.edu/abs/2025RNAAS...9..110L/abstract" style="color:blue;"><i><b>Lu</b>, Tajer, Rein, et al. (2025)</i></a></li>
      <li><a href="https://ui.adsabs.harvard.edu/abs/2023MNRAS.522.4639H/abstract" style="color:blue;"><i>Hernandez & Dehnen (2023)</i></a></li>
    </ul>
  </div>
</div>

----------

<div class="feature-row">
  <div>
    <h1 id="trace">tides_spin</h1>
    <p>
      is a module in the <a href="https://reboundx.readthedocs.io/en/latest/effects.html" style="color:black;">REBOUNDx</a> library of add-ons for REBOUND simulations, developed and maintained by <a href="https://dtamayo.github.io/" style="color:black;">Dan Tamayo</a>. REBOUND generally treats all planets as point particles. But planets are <b>not</b>: they are dynamic things that spin and distort in the presence of other bodies. <i>tides_spin</i> incorporates an elegant prescription of tides known as the equilibrium tide framework into a REBOUND simulation. It allows study of extremely important astrophysical processes such as tidal decay of orbits and planetary spin evolution. Detailed documentation and example code can be found <a href="https://reboundx.readthedocs.io/en/latest/effects.html#tides" style="color:black;">here</a>.
    </p>
    <p><strong>Relevant Papers:</strong></p>
    <ul>
      <li><a href="https://ui.adsabs.harvard.edu/abs/2023ApJ...948...41L/abstract" style="color:blue;"><i><b>Lu</b>, Rein, Tamayo, et al. (2023)</i></a></li>
      <li><a href="https://ui.adsabs.harvard.edu/abs/1998ApJ...499..853E/abstract" style="color:blue;"><i>Eggleton, Kiselava-Eggleton & Hut (1998)</i></a></li>
      <li><a href="https://ui.adsabs.harvard.edu/abs/2002ApJ...573..829M/abstract" style="color:blue;"><i>Mardling & Lin (2002)</i></a></li>
    </ul>
  </div>
  <img src="/images/tides_spin.png"
       alt="A tidal bulge"
       style="width:150px; height:auto; border-radius:2px;">
</div>
