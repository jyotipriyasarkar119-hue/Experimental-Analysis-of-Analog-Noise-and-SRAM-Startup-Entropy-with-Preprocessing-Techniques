<h2>🔬 Experimental Observations</h2>
<h3>SRAM Startup + Floating Analog Noise + XOR Mixing + Von Neumann Debiasing</h3>

<hr>

<h3> Observation Table</h3>

<table border="1" cellpadding="8" cellspacing="0">
<tr>
<th>Run No</th>
<th>Total Bits</th>
<th>Ones</th>
<th>Zeros</th>
<th>P(1)</th>
<th>P(0)</th>
<th>Shannon Entropy (per bit)</th>
</tr>

<tr><td>1</td><td>512</td><td>248</td><td>264</td><td>0.484375</td><td>0.515625</td><td>0.999295</td></tr>
<tr><td>2</td><td>512</td><td>258</td><td>254</td><td>0.503906</td><td>0.496094</td><td>0.999956</td></tr>
<tr><td>3</td><td>512</td><td>244</td><td>268</td><td>0.476563</td><td>0.523437</td><td>0.998414</td></tr>
<tr><td>4</td><td>512</td><td>256</td><td>256</td><td>0.500000</td><td>0.500000</td><td>1.000000</td></tr>
<tr><td>5</td><td>512</td><td>256</td><td>256</td><td>0.500000</td><td>0.500000</td><td>1.000000</td></tr>
<tr><td>6</td><td>512</td><td>234</td><td>278</td><td>0.457031</td><td>0.542969</td><td>0.994666</td></tr>
<tr><td>7</td><td>512</td><td>260</td><td>252</td><td>0.507812</td><td>0.492188</td><td>0.999824</td></tr>
<tr><td>8</td><td>512</td><td>253</td><td>259</td><td>0.494141</td><td>0.505859</td><td>0.999901</td></tr>
<tr><td>9</td><td>512</td><td>251</td><td>261</td><td>0.490234</td><td>0.509766</td><td>0.999725</td></tr>
<tr><td>10</td><td>512</td><td>248</td><td>264</td><td>0.484375</td><td>0.515625</td><td>0.999295</td></tr>

</table>

<hr>

<h3> Statistical Summary</h3>

<ul>
<li><strong>Minimum Entropy:</strong> 0.994666</li>
<li><strong>Maximum Entropy:</strong> 1.000000</li>
<li><strong>Average Entropy:</strong> ≈ 0.9993</li>
<li><strong>Worst Bias Deviation:</strong> |P(1) − 0.5| = 0.042969</li>
<li><strong>Total Runs Conducted:</strong> 10</li>
</ul>

<hr>

<h3> Observations</h3>

<ul>
<li>All runs produced Shannon entropy greater than <strong>0.994</strong>.</li>
<li>Two runs achieved perfectly balanced output (256 ones / 256 zeros).</li>
<li>Probability of '1' remained consistently close to 0.5.</li>
<li>No catastrophic entropy collapse observed across runs.</li>
<li>Hybrid mixing effectively stabilizes randomness.</li>
</ul>

<hr>



<h3> Conclusion</h3>

<p>
The Hybrid TRNG architecture demonstrates strong statistical properties,
with entropy consistently approaching the theoretical maximum of 1 bit per output bit.
The combination of SRAM startup entropy and floating analog noise,
conditioned through XOR mixing and Von Neumann debiasing,
produces stable, near-uniform random output suitable for embedded cryptographic experimentation.
</p>

<hr>
