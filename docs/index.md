<html>
  <head>
    <meta http-equiv="Content-Type" content="text/html;charset=utf-8" >
    <title>Proving Non-Termination via Acceleration Driven Clause Learning</title>
    <style>
      table, th, td {border: 1px solid black;}
      td {text-align: center;}
      p {text-align: justify;}
    </style>
  </head>
  <body>

    <p>
      This is the empirical evaluation of the paper <a href="???"><i>Proving Non-Termination via Acceleration Driven Clause Learning</i></a>.
    </p>

    <p>
      We implemented our contributions in our tool LoAT.
      For more information about LoAT, we refer to the <a href="https://loat-developers.github.io/LoAT/">general LoAT website</a>.</p>

    <h1>Getting LoAT</h1>

    We provide a <a href="https://github.com/loat-developers/LoAT/releases/tag/adcl-term">pre-compiled binary of LoAT (Linux, 64 bit)</a>.
    Moreover, you can find the source code of LoAT at <a href="https://github.com/loat-developers/LoAT/tree/adcl-term">GitHub</a>.

    <h1>Evaluation</h1>

    <h2>Examples</h2>

    <p>
      We evaluated our implementation on all 1222 examples from the category <i>Termination of Integer Transition Systems</i> of the <i><a href="https://github.com/TermCOMP/TPDB">Termination Problems Data Base</a></i>.
    </p>

    <h2>StarExec Bundles</h2>

    We provide StarExec bundles for all tools used in our evaluation.

    <ul>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?id=???">LoAT ADCL</a>, configuration <code>loat_nonterm_proofout</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?id=35581">LoAT '22</a>, configuration <code>loat_nonterm_proofout</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=a737357a-83c6-4d1e-b144-40e68d621037">T2</a>, configuration <code>default fixed</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=4798c8a9-e698-4029-a052-5ba641e2e0ea">VeryMax</a>, configuration <code>termcomp2019_ITS</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=788f0245-548d-4148-b840-50df112c3f8f">iRankFinder</a>, configuration <code>competition</code></li>
    </ul>

    <h2>Results</h2>

    <a href="table.html">Here</a> we provide a table with the detailed results of our benchmarks.

  </body>
</html>
