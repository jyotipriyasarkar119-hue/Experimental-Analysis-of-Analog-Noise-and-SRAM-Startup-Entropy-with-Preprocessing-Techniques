<h1>SRAM + Floating Pin Analog Noise Experimental Observations</h1>

<p><strong>Experiment:</strong> Hybrid Entropy Source (SRAM + Floating Analog)</p>
<p><strong>Microcontroller:</strong> Arduino Uno (ATmega328P)</p>
<p><strong>Bit Count per Run:</strong> 1024 bits</p>
<p><strong>Fusion Method:</strong> Bitwise XOR (SRAM ⊕ Analog)</p>

<hr>

<h2>Observed Results</h2>

<table>
<tr>
<th>Run</th>
<th>Ones</th>
<th>Zeros</th>
<th>P(1)</th>
<th>Shannon Entropy</th>
</tr>

<tr><td>1</td><td>495</td><td>529</td><td>0.483</td><td>0.999205</td></tr>
<tr><td>2</td><td>493</td><td>531</td><td>0.481</td><td>0.999006</td></tr>
<tr><td>3</td><td>542</td><td>482</td><td>0.529</td><td>0.997522</td></tr>
<tr><td>4</td><td>504</td><td>520</td><td>0.492</td><td>0.999824</td></tr>
<tr><td>5</td><td>501</td><td>523</td><td>0.489</td><td>0.999667</td></tr>
<tr><td>6</td><td>508</td><td>516</td><td>0.496</td><td>0.999956</td></tr>
<tr><td>7</td><td>502</td><td>522</td><td>0.490</td><td>0.999725</td></tr>
<tr><td>8</td><td>526</td><td>498</td><td>0.513</td><td>0.999461</td></tr>
<tr><td>9</td><td>500</td><td>524</td><td>0.488</td><td>0.999604</td></tr>
<tr class="highlight"><td>10</td><td>497</td><td>527</td><td>0.485</td><td>0.999381</td></tr>

</table>

<hr>

<h2>Statistical Summary</h2>

<ul>
<li><strong>Entropy Range:</strong> 0.9975 – 0.9999</li>
<li><strong>Average Entropy (approx.):</strong> ~0.9992</li>
<li><strong>P(1) Range:</strong> 0.481 – 0.529</li>
<li><strong>Bias Observation:</strong> Minimal deviation from ideal 0.5</li>
<li><strong>Bit Count Stability:</strong> Fixed 1024 bits per run</li>
</ul>

<hr>

<h2>Graphs</h2>

![Entropy vs Run](/hybrid_entropy_vs_run.png)


![Probability vs Run](/hybrid_probability_vs_run.png)


![Ones vs Zeros](/hybrid_ones_zeros_bar.png)


![Entropy Histogram](/hybrid_entropy_histogram.png)


![Bias Deviation](/hybrid_bias_deviation.png)

![Bias Deviation](/Bit_Rate_vs_Shanon_Entropy.png)

<hr>

<h2>Observations</h2>

<ul>
<li>The hybrid entropy source demonstrates extremely high Shannon entropy across all runs.</li>
<li>Probability of ones remains tightly clustered around 0.5, indicating strong balance.</li>
<li>Entropy fluctuation is significantly lower compared to standalone analog entropy.</li>
<li>XOR fusion of SRAM startup randomness and floating analog noise stabilizes randomness.</li>
<li>No severe bias or deterministic pattern was observed in any run.</li>
</ul>

<hr>

<h2>Conclusion</h2>

<p>
The hybrid entropy system (SRAM ⊕ Floating Analog) exhibits highly stable and near-ideal Shannon entropy performance across multiple independent measurements. 
Compared to standalone entropy sources, the hybrid approach reduces probability variance and enhances statistical robustness. 
These results indicate that multi-source entropy fusion is effective for embedded True Random Number Generator (TRNG) design.
</p>
