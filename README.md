<h2>Introduction</h2>

<p>
Random number generation is a fundamental requirement in modern cryptographic systems, secure communications, authentication protocols, and hardware security primitives. The security of encryption algorithms, digital signatures, and key generation mechanisms heavily depends on the quality of randomness. While pseudo-random number generators (PRNGs) rely on deterministic algorithms, True Random Number Generators (TRNGs) extract entropy from physical phenomena, making them significantly more secure against prediction and reverse engineering.
</p>

<p>
This project presents an experimental investigation of two hardware-based entropy sources: <strong>analog noise</strong> and <strong>SRAM startup behavior</strong>. Analog noise arises from inherent electrical fluctuations such as thermal and electronic noise, while SRAM startup entropy originates from unpredictable memory cell initialization states caused by microscopic manufacturing variations. Both sources provide physical randomness but often contain bias and structural dependencies that must be carefully analyzed and conditioned.
</p>

<p>
The primary goal of this work is to evaluate the raw entropy characteristics of these sources and examine how preprocessing techniques influence randomness quality. Techniques such as XOR folding, half-split XOR, and Von Neumann debiasing are applied to improve statistical balance and entropy strength. The effectiveness of each method is assessed using Shannon entropy measurements, probability bias analysis, and output bit count comparison.
</p>

<p>
By combining experimental data collection, statistical evaluation, and graphical analysis, this repository provides a systematic comparison of entropy improvement techniques and highlights the trade-off between randomness quality and throughput. The results contribute to a deeper understanding of hardware-based entropy extraction and its relevance to secure system design.
</p>

<h2>Objectives</h2>

<ul>
  <li><strong>Measure and compare</strong> the raw entropy characteristics of analog noise and SRAM startup values.</li>
  <li><strong>Apply preprocessing techniques</strong> such as XOR folding, half-split XOR, and Von Neumann extraction to improve randomness quality.</li>
  <li><strong>Quantitatively analyze</strong> bias, entropy values, and randomness metrics for each method.</li>
  <li><strong>Visualize the results</strong> through clear graphs and comparisons to highlight the effect of preprocessing on entropy quality.</li>
  <li><strong>Assess trade-offs</strong> between randomness quality and output throughput for each conditioning technique.</li>
  <li><strong>Provide reproducible code and data</strong> for future research or extension.</li>
</ul>
<h2>Concept</h2>

<p>
  True Random Number Generators (TRNGs) are essential for secure systems because pseudorandom number generators (PRNGs) can be predictable. This project focuses on two physical entropy sources:
</p>

<ol>
  <li>
    <strong>Analog Noise Entropy Source</strong><br>
    Random fluctuations in analog circuits (e.g., thermal noise, amplifier noise) can provide high entropy. However, raw analog noise often contains bias and structural patterns that reduce randomness quality unless conditioned.
  </li>
  <li>
    <strong>SRAM Startup Startup Entropy</strong><br>
    SRAM memory cells initialize to unpredictable states at power-up due to manufacturing variation and environmental noise. This makes SRAM a good candidate for entropy extraction, but raw startup bits are often biased and require preprocessing.
  </li>
</ol>

<p>
  To improve randomness, we explore preprocessing and debiasing techniques:
</p>

<ul>
  <li><strong>XOR Folding (Block-based)</strong> — Combines multiple bits via XOR to reduce bias but may reduce entropy throughput.</li>
  <li><strong>Half-Split XOR</strong> — Splits the bit sequence and XORs halves to reduce spatial bias.</li>
  <li><strong>Von Neumann Extraction</strong> — Classic debiaser that removes bias by pairing bits and discarding certain patterns.</li>
  <li><strong>Combined Methods</strong> — Mixing preprocessing with Von Neumann to investigate synergy.</li>
</ul>

<p>
  For each method, we evaluate key metrics such as Shannon entropy, probability bias, and output bit count, and compare them across all techniques. The results are visualized through graphs and supported by statistical observations to show how preprocessing affects randomness quality and output efficiency.
</p>

---

<p align="center">
  <strong>Explore the data, run the scripts,</strong> and feel free to extend the work for hardware security or cryptographic research.
</p>
