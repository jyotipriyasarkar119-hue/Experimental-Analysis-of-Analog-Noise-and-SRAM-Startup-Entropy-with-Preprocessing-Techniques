<h2> Comparative Statistical Observation Report</h2>

<p><strong>Platform:</strong> Arduino Uno (ATmega328P)</p>

<hr>

<h3> Average Entropy Comparison</h3>

<table>
<thead>
<tr>
<th>Process</th>
<th>Output Bits</th>
<th>Avg Entropy</th>
<th>Min</th>
<th>Max</th>
<th>Observation</th>
</tr>
</thead>
<tbody>
<tr>
<td>Floating Analog Only</td>
<td>1000</td>
<td><strong>0.9867</strong></td>
<td>0.9544</td>
<td>0.9999</td>
<td>High bias variation</td>
</tr>

<tr>
<td>SRAM + Floating (Raw XOR)</td>
<td>1024</td>
<td><strong>0.99934</strong></td>
<td>0.9975</td>
<td>0.99996</td>
<td>Very stable hybrid source</td>
</tr>

<tr>
<td>Half-Split XOR</td>
<td>512</td>
<td><strong>0.9969</strong></td>
<td>0.9901</td>
<td>0.9999</td>
<td>Lightweight mixing</td>
</tr>

<tr>
<td>2-bit Folding</td>
<td>512</td>
<td><strong>0.99876</strong></td>
<td>0.99365</td>
<td>0.99999</td>
<td>Efficient compression</td>
</tr>

<tr>
<td>XOR + Von Neumann</td>
<td>512</td>
<td><strong>0.99967</strong></td>
<td>0.99841</td>
<td>1.00000</td>
<td>Best statistical uniformity</td>
</tr>

<tr>
<td>8-Fold XOR + VN</td>
<td>512</td>
<td><strong>0.99767</strong></td>
<td>0.99417</td>
<td>0.99930</td>
<td>Over-mixing effect observed</td>
</tr>

<tr>
<td>XOR + 8-bit Folding</td>
<td>128</td>
<td><strong>0.99589</strong></td>
<td>0.98870</td>
<td>1.00000</td>
<td>High compression trade-off</td>
</tr>

</tbody>
</table>

<hr>

<h3> Key Observations</h3>

<ul>
<li>Hybrid entropy sources significantly outperform single-source analog noise.</li>
<li>XOR mixing effectively reduces bias.</li>
<li>Von Neumann debiasing provides the cleanest statistical output.</li>
<li>Aggressive folding slightly reduces entropy due to compression.</li>
<li>Best overall balance: <strong>SRAM + Floating + XOR + Von Neumann</strong>.</li>
</ul>

<hr>

<h3> Conclusion</h3>

<p>
Experimental results demonstrate that multi-source entropy fusion combined with lightweight 
post-processing achieves near-ideal Shannon entropy (~0.9996 per bit) 
on a resource-constrained microcontroller (ATmega328P).
</p>

<p>
This validates the feasibility of secure hardware-based TRNG design 
for embedded cryptographic applications.
</p>
