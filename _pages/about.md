---
layout: home
permalink: /
title: "Shashi B. Mishra"
excerpt: "Theoretical condensed matter physicist and computational materials scientist"
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<section class="home__header home__header--with-photo" aria-label="Identity">
  <figure class="home__portrait">
    <img src="{{ site.baseurl }}/images/profile.png" alt="Portrait of Shashi B. Mishra" />
  </figure>
  <div class="home__header-text">
    <h1 class="home__name">Shashi B. Mishra</h1>
    <p class="home__role">
      <em>Assistant Research Scientist</em>,
      Department of Electrical &amp; Computer Engineering,<br>
      University of Maryland, College Park
    </p>
    <ul class="home__links">
      <li><a href="mailto:shashi13@umd.edu">shashi13@umd.edu</a></li>
      <li><a href="https://scholar.google.com/citations?user=yLSyEkoAAAAJ&amp;hl=en" target="_blank" rel="noopener">Google&nbsp;Scholar</a></li>
      <li><a href="https://orcid.org/0000-0002-6361-3379" target="_blank" rel="noopener">ORCID</a></li>
      <li><a href="https://gitlab.com/Shashi-phy" target="_blank" rel="noopener">GitLab</a></li>
    </ul>
  </div>
</section>

<section class="home__about" aria-labelledby="about-heading">
  <h2 id="about-heading">About</h2>
  <p>
    I am a theoretical condensed matter physicist and computational materials scientist with expertise in first-principles simulations, many-body theory, and high-performance computing. My work focuses on understanding quantum materials through electron-phonon interactions, with particular interests in superconductivity beyond the Migdal approximation, transport in topological semimetals, and light-induced magnetic phenomena in metals. I am also a contributor to the open-source EPW code, where I have implemented electron-phonon vertex corrections and efficient two-level MPI parallelization strategies for superconductivity.
  </p>
</section>

<section class="home__featured" aria-labelledby="featured-heading">
  <h2 id="featured-heading">Featured research</h2>

  <div class="slider" aria-label="Research highlights carousel">
    <button type="button" class="slider__btn slider__btn--prev" data-slider-prev aria-label="Previous highlights">&lsaquo;</button>
    <div class="slider__track" data-slider-track role="list">

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/h3s-vertex-correction.png"
             alt="Vertex corrections to the electron-phonon interaction in H3S and Pb, from DFT." />
      </figure>
      <h3 class="highlights__title">Vertex corrections in H<sub>3</sub>S</h3>
      <p class="highlights__venue"><em>npj Comput. Mater.</em> <strong>11</strong>, 342 (2025)</p>
      <p class="highlights__summary">
        First-principles electron-phonon vertex corrections reduce the predicted T<sub>c</sub> of H<sub>3</sub>S by roughly a quarter, while leaving conventional superconductors like Pb essentially untouched — refining the Migdal framework for high-pressure hydrides.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1038/s41524-025-01818-9"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/topological-transport.png"
             alt="Electrical conductivity of the Weyl semimetal TaAs family from first principles." />
      </figure>
      <h3 class="highlights__title">Transport in topological materials</h3>
      <p class="highlights__venue"><em>Phys. Rev. B</em> <strong>113</strong>, 045202 (2026)</p>
      <p class="highlights__summary">
        Phonon-limited carrier transport across the TaAs family of Weyl semimetals, computed from first principles — resolving how Berry-curvature-rich bands and electron–phonon scattering jointly shape conductivity.
      </p>
      <a class="highlights__doi"
         href="https://journals.aps.org/prb/abstract/10.1103/d9np-11j1"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/na-graphite.png"
             alt="Emergent quantum phenomena in DFT-predicted Na-intercalated graphite compounds." />
      </figure>
      <h3 class="highlights__title">Na-intercalated graphite superconductors</h3>
      <p class="highlights__venue"><em>Phys. Rev. B</em> <strong>110</strong>, 174508 (2024)</p>
      <p class="highlights__summary">
        A stability–superconductivity map for compressed Na-intercalated graphite — charting the stoichiometries and pressures that maximize phonon-mediated T<sub>c</sub> within the Migdal regime to guide experimental synthesis.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1103/PhysRevB.110.174508"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/h3s-isotope.png"
             alt="Isotope effect and anharmonic phonons in H3S versus D3S superconductors." />
      </figure>
      <h3 class="highlights__title">Non-adiabatic &amp; anharmonic H<sub>3</sub>S / D<sub>3</sub>S</h3>
      <p class="highlights__venue"><em>Annalen der Physik</em> <strong>538</strong>, e00553 (2026)</p>
      <p class="highlights__summary">
        Full-bandwidth ab initio Eliashberg calculations that quantify how non-adiabatic electron-phonon coupling and phonon anharmonicity jointly reshape the isotope effect and T<sub>c</sub> in H<sub>3</sub>S and D<sub>3</sub>S.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1002/andp.202500553"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/ife-light-matter.png"
             alt="First-principles inverse Faraday response across the 3d, 4d, and 5d transition metal series." />
      </figure>
      <h3 class="highlights__title">Inverse Faraday effect in metals</h3>
      <p class="highlights__venue">
        <em>Phys. Rev. B</em> <strong>111</strong>, 174413 (2025) &middot;
        <a href="https://doi.org/10.1103/PhysRevB.107.214432" target="_blank" rel="noopener"><em>Phys. Rev. B</em> <strong>107</strong>, 214432 (2023)</a>
      </p>
      <p class="highlights__summary">
        A gauge-invariant first-principles theory of light-induced magnetization — formulated for non-magnetic metals using degenerate perturbation theory with Wannier interpolation (2023), and traced systematically across the 3<em>d</em>, 4<em>d</em>, and 5<em>d</em> series (2025) to reveal trends that enable ultrafast optical control of magnetism.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1103/PhysRevB.111.174413"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/energy-materials.png"
             alt="Two-dimensional framework materials for next-generation battery anodes and cathodes." />
      </figure>
      <h3 class="highlights__title">Energy materials by design</h3>
      <p class="highlights__venue"><em>ACS Appl. Energy Mater.</em> <strong>4</strong>, 7786 (2021)</p>
      <p class="highlights__summary">
        First-principles design of two-dimensional anodes and cathodes — Si<sub>2</sub>BN, graphyne, graphdiyne — for next-generation Al- and Mg-ion batteries, balancing capacity, diffusivity, and structural stability.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1021/acsaem.1c01164"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-fluorine-graphene.jpg"
             alt="Fluorine intercalation between graphene layers forming a dimerized spin lattice." />
      </figure>
      <h3 class="highlights__title">Suspended spin lattice in fluorine–graphene</h3>
      <p class="highlights__venue"><em>Phys. Rev. Mater.</em> <strong>4</strong>, 074411 (2020)</p>
      <p class="highlights__summary">
        Fluorine intercalated between graphene layers is pseudoatomized through bond stretching and charge transfer, stabilizing a spin-polarized ground state with long-range magnetic order — an artificial van der Waals spin lattice with the graphene host retaining its pristine bands.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1103/PhysRevMaterials.4.074411"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-ba2mnteo6.jpg"
             alt="Triangular lattice of Mn2+ spins in the double perovskite Ba2MnTeO6." />
      </figure>
      <h3 class="highlights__title">Magnetic order in Ba<sub>2</sub>MnTeO<sub>6</sub></h3>
      <p class="highlights__venue"><em>Sci. Rep.</em> <strong>11</strong>, 6959 (2021)</p>
      <p class="highlights__summary">
        Experiment and DFT+U together resolve competing intra- and inter-layer AFM exchanges on the Mn<sup>2+</sup> triangular lattice of Ba<sub>2</sub>MnTeO<sub>6</sub>, stabilizing a 3D long-range magnetic ordering that matches the measured Curie–Weiss temperature at <em>U</em> = 5.75 eV.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1038/s41598-021-84876-5"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-graphene-tio2.jpg"
             alt="Low-strain commensurate graphene/TiO2 interface with Dirac-cone preservation." />
      </figure>
      <h3 class="highlights__title">Graphene / TiO<sub>2</sub> interface</h3>
      <p class="highlights__venue"><em>Appl. Surf. Sci.</em> <strong>542</strong>, 148709 (2021)</p>
      <p class="highlights__summary">
        A low-strain commensurate graphene/TiO<sub>2</sub> interface preserves graphene's gapless Dirac bands under strain; in the AB-stacked bilayer, interfacial charge transfer opens a narrow bandgap — enabling visible-light-sensitized photocatalysis.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1016/j.apsusc.2020.148709"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-sp2deg.jpg"
             alt="Double-perovskite heterostructure hosting a spin-polarized two-dimensional electron gas." />
      </figure>
      <h3 class="highlights__title">Spin-polarized 2DEG in oxide heterostructures</h3>
      <p class="highlights__venue"><em>Phys. Rev. B</em> <strong>98</strong>, 115155 (2018)</p>
      <p class="highlights__summary">
        A non-polar oxide heterostructure Sr<sub>2</sub>FeMoO<sub>6</sub>/La<sub>2</sub>CoMnO<sub>6</sub> realizes a spin-polarized two-dimensional electron gas through quantum confinement and orbital manipulation — a route distinct from LaAlO<sub>3</sub>/SrTiO<sub>3</sub>-like polar interfaces.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1103/PhysRevB.98.115155"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-co2-tio2.jpg"
             alt="Three-state model for CO2 adsorption on anatase TiO2(001) surface." />
      </figure>
      <h3 class="highlights__title">Three-state model of CO<sub>2</sub> on TiO<sub>2</sub>(001)</h3>
      <p class="highlights__venue"><em>Phys. Rev. Mater.</em> <strong>2</strong>, 115801 (2018)</p>
      <p class="highlights__summary">
        A three-state model couples surface deformation, charge transfer, and molecular-orbital bonding to explain CO<sub>2</sub> adsorption on anatase TiO<sub>2</sub>(001) — predicting uniaxial, long-ranged interactions and strong binding-energy anisotropy confirmed by density-of-states analysis.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1103/PhysRevMaterials.2.115801"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-facet-tio2.jpg"
             alt="Reactivity order across anatase TiO2 facets for CO2 and H2O co-adsorption." />
      </figure>
      <h3 class="highlights__title">Facet-dependent CO<sub>2</sub> catalysis on TiO<sub>2</sub></h3>
      <p class="highlights__venue"><em>Appl. Surf. Sci.</em> <strong>531</strong>, 147330 (2020)</p>
      <p class="highlights__summary">
        Ranking CO<sub>2</sub>, H<sub>2</sub>O, and co-adsorption-driven bicarbonate formation across low-index anatase TiO<sub>2</sub> facets — including the reconstructed (1×4)-(001) — with the change in exchange–correlation energy serving as a quantitative bond-strength indicator.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1016/j.apsusc.2020.147330"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    <article class="highlights__card" role="listitem">
      <figure class="highlights__figure">
        <img src="{{ site.baseurl }}/images/featured/rs-no2-tio2.jpg"
             alt="Reaction pathway for NO2 dissociation on rutile TiO2(110) surface." />
      </figure>
      <h3 class="highlights__title">NO<sub>2</sub> dissociation on rutile TiO<sub>2</sub>(110)</h3>
      <p class="highlights__venue"><em>J. Phys. Chem. C</em> <strong>124</strong>, 8786 (2020)</p>
      <p class="highlights__summary">
        DFT reaction-pathway analysis for NO<sub>2</sub> on rutile TiO<sub>2</sub>(110): NO<sub>2</sub> dimerizes into a short-lived N<sub>2</sub>O<sub>4</sub> that dissociates to ionic species and, with H<sub>2</sub>O present, converts to HONO and HNO<sub>3</sub> — a roadmap for toxic-gas conversion on oxide surfaces.
      </p>
      <a class="highlights__doi"
         href="https://doi.org/10.1021/acs.jpcc.0c00525"
         target="_blank" rel="noopener">
        Read the paper &rarr;
      </a>
    </article>

    </div>
    <button type="button" class="slider__btn slider__btn--next" data-slider-next aria-label="Next highlights">&rsaquo;</button>
  </div>
  <script>
    (function(){
      var track = document.querySelector('[data-slider-track]');
      var prev  = document.querySelector('[data-slider-prev]');
      var next  = document.querySelector('[data-slider-next]');
      if (!track || !prev || !next) return;
      function step(){ return Math.max(200, track.clientWidth * 0.85); }
      prev.addEventListener('click', function(){ track.scrollBy({left: -step(), behavior: 'smooth'}); });
      next.addEventListener('click', function(){ track.scrollBy({left:  step(), behavior: 'smooth'}); });
    })();
  </script>
</section>

<section class="home__themes" aria-labelledby="themes-heading">
  <h2 id="themes-heading">Research themes</h2>
  <div class="themes">
    <div class="themes__tile">
      <h3>Superconductivity &amp; electron-phonon coupling</h3>
      <p>Phonon-mediated pairing beyond Migdal, vertex corrections, anharmonicity, and first-principles design of ambient-pressure superconductors.</p>
    </div>
    <div class="themes__tile">
      <h3>Topological transport &amp; Berry curvature</h3>
      <p>Phonon-limited carrier transport in Weyl and Dirac semimetals; Berry-curvature-driven anomalous responses from first principles.</p>
    </div>
    <div class="themes__tile">
      <h3>Light–matter interaction</h3>
      <p>Inverse Faraday effect across 3<em>d</em>–5<em>d</em> metals, non-thermal phase transitions, and ultrafast optical control of magnetism.</p>
    </div>
    <div class="themes__tile">
      <h3>Energy materials &amp; catalysis</h3>
      <p>Design of two-dimensional battery anodes (Si<sub>2</sub>BN, graphdiyne, graphyne) and catalytically active oxide surfaces and interfaces.</p>
    </div>
  </div>
</section>

<section class="home__pubs" aria-labelledby="pubs-heading">
  <h2 id="pubs-heading">Selected publications</h2>
  <ol class="pubs">
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, Z.&nbsp;Liu, S.&nbsp;Tiwari, F.&nbsp;Giustino, E.&nbsp;R.&nbsp;Margine.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/d9np-11j1" target="_blank" rel="noopener">Comparative study of phonon-limited carrier transport in the Weyl semimetal TaAs family.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>113</strong>, 045202 (2026).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, E.&nbsp;R.&nbsp;Margine.</span>
      <a class="pubs__title" href="https://doi.org/10.1002/andp.202500553" target="_blank" rel="noopener">Nonadiabatic and anharmonic effects in high-pressure H<sub>3</sub>S and D<sub>3</sub>S superconductors.</a>
      <span class="pubs__venue">Annalen der Physik <strong>538</strong>, e00553 (2026).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, H.&nbsp;Mori, E.&nbsp;R.&nbsp;Margine.</span>
      <a class="pubs__title" href="https://doi.org/10.1038/s41524-025-01818-9" target="_blank" rel="noopener">Electron-phonon vertex correction effect in superconducting H<sub>3</sub>S.</a>
      <span class="pubs__venue">npj Computational Materials <strong>11</strong>, 342 (2025).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/PhysRevB.111.174413" target="_blank" rel="noopener">Inverse Faraday effect in 3<em>d</em>, 4<em>d</em>, and 5<em>d</em> transition metals.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>111</strong>, 174413 (2025).</span>
    </li>
    <li>
      <span class="pubs__authors">Z.&nbsp;Liu, <strong>S.&nbsp;B.&nbsp;Mishra</strong>, J.-M.&nbsp;Lihm, S.&nbsp;Poncé, E.&nbsp;R.&nbsp;Margine.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/x8zl-w5x3" target="_blank" rel="noopener">Phonon-limited carrier transport in the Weyl semimetal TaAs.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>112</strong>, 104311 (2025).</span>
    </li>
    <li>
      <span class="pubs__authors">X.&nbsp;Zhang, <strong>S.&nbsp;B.&nbsp;Mishra</strong>, E.&nbsp;R.&nbsp;Margine, E.&nbsp;Kioupakis.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/wx8d-6trp" target="_blank" rel="noopener">Cubic BeB<sub>2</sub>: a metastable <em>p</em>-type conductive material from first principles.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>112</strong>, 155206 (2025).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, E.&nbsp;T.&nbsp;Marcial, S.&nbsp;Debata, A.&nbsp;N.&nbsp;Kolmogorov, E.&nbsp;R.&nbsp;Margine.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/PhysRevB.110.174508" target="_blank" rel="noopener">Stability–superconductivity map for compressed Na-intercalated graphite.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>110</strong>, 174508 (2024).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, S.&nbsp;Coh.</span>
      <a class="pubs__title" href="https://doi.org/10.1103/PhysRevB.107.214432" target="_blank" rel="noopener">Spin contribution to the inverse Faraday effect of nonmagnetic metals.</a>
      <span class="pubs__venue">Phys. Rev. B <strong>107</strong>, 214432 (2023).</span>
    </li>
    <li>
      <span class="pubs__authors"><strong>S.&nbsp;B.&nbsp;Mishra</strong>, Abhijitha V.&nbsp;G., S.&nbsp;Ramaprabhu, B.&nbsp;R.&nbsp;K.&nbsp;Nanda.</span>
      <a class="pubs__title" href="https://doi.org/10.1021/acsaem.1c01164" target="_blank" rel="noopener">Graphdiyne — a promising cathode material for aluminium dual-ion batteries.</a>
      <span class="pubs__venue">ACS Appl. Energy Mater. <strong>4</strong>, 7786 (2021).</span>
    </li>
    <li>
      <span class="pubs__authors">P.&nbsp;Panigrahi, <strong>S.&nbsp;B.&nbsp;Mishra</strong>, T.&nbsp;Hussain, B.&nbsp;R.&nbsp;K.&nbsp;Nanda, R.&nbsp;Ahuja.</span>
      <a class="pubs__title" href="https://doi.org/10.1021/acsanm.0c01747" target="_blank" rel="noopener">Si<sub>2</sub>BN nanosheets as anode materials for magnesium-ion batteries.</a>
      <span class="pubs__venue">ACS Appl. Nano Mater. <strong>3</strong>, 9055 (2020).</span>
    </li>
  </ol>
  <p style="margin-top:1.25rem;font-size:14px;color:#6b6b6b;">
    See the <a href="{{ site.baseurl }}/publications/">full publication list</a> for all work.
  </p>
</section>

<section class="home__cv" aria-labelledby="cv-heading">
  <h2 id="cv-heading">Curriculum vitae</h2>
  <p>
    <a class="cv-link"
       href="{{ site.baseurl }}/cv/">
      View full CV &rarr;
    </a>
  </p>
</section>

<section id="contact" class="home__contact contact" aria-labelledby="contact-heading">
  <h2 id="contact-heading">Contact</h2>
  <p><a href="mailto:shashi13@umd.edu">shashi13@umd.edu</a></p>
  <p>Department of Electrical &amp; Computer Engineering<br>
  University of Maryland, College Park, MD 20742</p>
</section>
