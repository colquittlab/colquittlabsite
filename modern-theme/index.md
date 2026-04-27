---
title: Home
---

<div class="hero">
  <div class="container">
    <div class="hero-content">
      <span class="hero-tag animate-fade-in">Neuroscience Research at UC Santa Cruz</span>
      <h1 class="animate-fade-in animate-delay-1">
        Decoding the <span class="highlight">Neural Symphony</span> of Birdsong
      </h1>
      <p class="hero-subtitle animate-fade-in animate-delay-2">
        We study how complex motor skills develop and evolve by investigating the neural circuitry behind birdsong—one of nature's most spectacular behaviors. Through advanced molecular techniques, bioinformatics, and behavioral analysis, we uncover how gene regulatory networks build specialized brain circuits.
      </p>
      <div class="animate-fade-in animate-delay-3" style="display: flex; gap: 1rem; flex-wrap: wrap;">
        {% include button.html link="research" text="Explore Our Research" icon="fa-solid fa-arrow-right" style="primary" %}
        {% include button.html link="publications" text="Publications" style="outline" %}
      </div>
    </div>
  </div>
</div>

{% include section.html background="var(--background-alt)" %}

## Our Research Focus

<div class="grid grid-3">
  <div class="card">
    <div style="font-size: 3rem; margin-bottom: 1rem;">🧬</div>
    <h3 style="font-size: 1.5rem;">Gene Regulatory Networks</h3>
    <p class="text-muted">
      Investigating the molecular processes that coordinate the development of birdsong neural circuitry during early brain development.
    </p>
  </div>
  
  <div class="card">
    <div style="font-size: 3rem; margin-bottom: 1rem;">🎵</div>
    <h3 style="font-size: 1.5rem;">Sensorimotor Learning</h3>
    <p class="text-muted">
      Understanding how neural networks intersect with experience during the critical period of birdsong learning.
    </p>
  </div>
  
  <div class="card">
    <div style="font-size: 3rem; margin-bottom: 1rem;">🧠</div>
    <h3 style="font-size: 1.5rem;">Behavioral Evolution</h3>
    <p class="text-muted">
      Exploring how modifications to developmental networks contributed to the evolution of complex learned behaviors.
    </p>
  </div>
</div>

{% include section.html %}

## Why Birdsong?

{% capture text %}
Birdsong provides an exceptional model for understanding neural development and evolution:

- **Well-defined circuitry** dedicated to song production and learning
- **Shared across thousands of species** enabling comparative studies
- **Complex learned behavior** similar to human speech acquisition
- **Accessible for molecular and behavioral analysis**

Birdsong is controlled by dedicated brain regions that are highly distinct from nearby sensorimotor areas, making it an ideal system to understand how specialized neural circuits develop and evolve.

{% include button.html link="research" text="Learn More About Our Approach" icon="fa-solid fa-microscope" style="bare" %}

{% endcapture %}

{%
  include feature.html
  image="images/song-system.png"
  link="research"
  title="A Powerful Model System"
  text=text
%}

{% include section.html background="var(--background-alt)" %}

## Recent Highlights

<div class="grid grid-2">
  <div class="card">
    <h4>🔬 Advanced Techniques</h4>
    <p>
      We combine single-cell transcriptomics, spatial genomics, CRISPR gene editing, and computational analysis to understand neural circuit development at unprecedented resolution.
    </p>
  </div>
  
  <div class="card">
    <h4>📊 Big Data Approaches</h4>
    <p>
      Our bioinformatics pipelines integrate multi-omics datasets to map gene regulatory networks and evolutionary relationships across thousands of cells and species.
    </p>
  </div>
</div>

{% include section.html %}

## Join Our Team

{% capture text %}
The Colquitt Lab opened in August 2022 and we're building a diverse, collaborative team. We're located on the stunning UC Santa Cruz campus, embedded in a redwood forest overlooking the Monterey Bay.

**We're recruiting:**
- Postdoctoral researchers
- Graduate students (rotation students welcome)
- Undergraduate researchers

Interested in developmental neuroscience, molecular biology, or computational approaches to understanding neural circuits? Get in touch!

{% include button.html link="team" text="Meet Our Team" icon="fa-solid fa-users" %}
{% include button.html link="contact" text="Contact Us" icon="fa-solid fa-envelope" style="outline" %}

{% endcapture %}

{%
  include feature.html
  image="images/BF_pic.png"
  link="team"
  title="Stellar Researchers Wanted"
  flip=true
  text=text
%}

{% include section.html background="var(--primary-dark)" dark=true %}

<div class="text-center">
  <h2 style="color: white; margin-bottom: 2rem;">Latest Publications</h2>
  <p style="color: var(--gray-400); max-width: 600px; margin: 0 auto 3rem;">
    Our research has been published in leading journals including <em>Science</em>, <em>eLife</em>, <em>Neuron</em>, and <em>Cell</em>.
  </p>
  {% include button.html link="publications" text="View All Publications" icon="fa-solid fa-book-open" style="accent" %}
</div>

{% include section.html %}
