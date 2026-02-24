<h2>Floating Analog + SRAM + XOR + 2-bit Folding Observation</h2>

<p><strong>Platform:</strong> Arduino Uno (ATmega328P)</p>
<p><strong>Method:</strong> SRAM Startup + Floating Analog Noise + XOR + 2-bit Folding</p>
<p><strong>Raw Bits:</strong> 1024 &nbsp; | &nbsp; <strong>Output Bits per Trial:</strong> 512</p>

<hr>
<h3>Observation Table</h3>
<table>
  <thead>
    <tr>
      <th>Trial</th>
      <th>Total Bits</th>
      <th>Ones</th>
      <th>Zeros</th>
      <th>P(1)</th>
      <th>P(0)</th>
      <th>Shannon Entropy (per bit)</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>512</td><td>255</td><td>257</td><td>0.498047</td><td>0.501953</td><td>0.999989</td></tr>
    <tr><td>2</td><td>512</td><td>254</td><td>258</td><td>0.496094</td><td>0.503906</td><td>0.999956</td></tr>
    <tr><td>3</td><td>512</td><td>239</td><td>273</td><td>0.466797</td><td>0.533203</td><td>0.996817</td></tr>
    <tr><td>4</td><td>512</td><td>251</td><td>261</td><td>0.490234</td><td>0.509766</td><td>0.999725</td></tr>
    <tr><td>5</td><td>512</td><td>241</td><td>271</td><td>0.470703</td><td>0.529297</td><td>0.997522</td></tr>
    <tr><td>6</td><td>512</td><td>267</td><td>245</td><td>0.521484</td><td>0.478516</td><td>0.998668</td></tr>
    <tr><td>7</td><td>512</td><td>268</td><td>244</td><td>0.523437</td><td>0.476563</td><td>0.998414</td></tr>
    <tr><td>8</td><td>512</td><td>232</td><td>280</td><td>0.453125</td><td>0.546875</td><td>0.993651</td></tr>
    <tr><td>9</td><td>512</td><td>248</td><td>264</td><td>0.484375</td><td>0.515625</td><td>0.999295</td></tr>
    <tr><td>10</td><td>512</td><td>262</td><td>250</td><td>0.511719</td><td>0.488281</td><td>0.999604</td></tr>
  </tbody>
</table>

<br>

<hr>

<h3>Statistical Summary</h3>

<ul>
  <li>Entropy Range: <strong>0.9936 – 0.99999 bits per bit</strong></li>
  <li>Average Entropy: <strong>≈ 0.9986 bits per bit</strong></li>
  <li>Probability P(1) remains close to 0.5 across power cycles</li>
  <li>No fixed bias or deterministic pattern observed</li>
</ul>

<hr>

<h3>Conclusion</h3>

<p>
The hybrid entropy extraction technique using SRAM startup variability combined 
with floating analog noise and 2-bit folding demonstrates near-ideal Shannon entropy 
performance. The probability distribution remains statistically balanced across 
multiple power cycles, validating effective bias reduction and source mixing.
</p></h2>

