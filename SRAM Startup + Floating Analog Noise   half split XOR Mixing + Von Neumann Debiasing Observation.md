<h2>Experimental Observations</h2>
<h3>Hybrid TRNG: SRAM + Floating Analog + Half-Split XOR + Von Neumann</h3>

<hr>

<h3>Observation Table</h3>

<table border="1" cellpadding="8" cellspacing="0">
<tr>
<th>Run</th>
<th>Total Bits</th>
<th>Ones</th>
<th>Zeros</th>
<th>P(1)</th>
<th>Shannon Entropy</th>
</tr>

<tr><td>1</td><td>512</td><td>263</td><td>249</td><td>0.513672</td><td>0.999461</td></tr>
<tr><td>2</td><td>512</td><td>252</td><td>260</td><td>0.492188</td><td>0.999824</td></tr>
<tr><td>3</td><td>512</td><td>272</td><td>240</td><td>0.531250</td><td>0.997180</td></tr>
<tr><td>4</td><td>512</td><td>268</td><td>227</td><td>0.523437</td><td>0.998414</td></tr>
<tr><td>5</td><td>512</td><td>265</td><td>247</td><td>0.517578</td><td>0.999108</td></tr>
<tr><td>6</td><td>512</td><td>265</td><td>247</td><td>0.517578</td><td>0.999108</td></tr>
<tr><td>7</td><td>512</td><td>260</td><td>240</td><td>0.507812</td><td>0.999824</td></tr>
<tr><td>8</td><td>512</td><td>254</td><td>258</td><td>0.496094</td><td>0.999956</td></tr>
<tr><td>9</td><td>512</td><td>241</td><td>263</td><td>0.470703</td><td>0.997522</td></tr>
<tr><td>10</td><td>512</td><td>280</td><td>232</td><td>0.546875</td><td>0.993651</td></tr>

</table>

<hr>

<h3>Statistical Summary</h3>

<ul>
<li><strong>Minimum Entropy:</strong> 0.993651</li>
<li><strong>Maximum Entropy:</strong> 0.999956</li>
<li><strong>Average Entropy:</strong> ≈ 0.9980</li>
<li><strong>Total Runs:</strong> 10</li>
</ul>

<hr>

<h3>Interpretation</h3>

<p>
Half-split XOR mixing reduces spatial SRAM bias by folding the first and second halves
of the bitstream before applying Von Neumann debiasing. Across 10 experimental runs,
Shannon entropy consistently remains above 0.993 bits per output bit, confirming
stable hybrid entropy generation behavior.
</p>

<hr>
