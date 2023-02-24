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
      For more information about LoAT, we refer to the <a href="https://loat-developers.github.io/LoAT/">general LoAT website</a>.
    </p>

    <h1>Getting LoAT</h1>

    We provide a <a href="https://github.com/LoAT-developers/LoAT/releases/tag/adcl-nt">pre-compiled binary of LoAT (Linux, 64 bit)</a>.
    Moreover, you can find the source code of LoAT at <a href="https://github.com/loat-developers/LoAT/tree/adcl-nt">GitHub</a>.

    <h1>Evaluation</h1>

    <h2>Examples</h2>

    <p>
      We evaluated our implementation on all 1222 examples from the category <i>Termination of Integer Transition Systems</i> and all 335 examples from the category <i>Termination of C Integer Programs</i> of the <i><a href="https://github.com/TermCOMP/TPDB">Termination Problems Data Base</a></i>.
    </p>

    <h2>Tools</h2>

    <p>
      We compared our implementation (<a href="https://github.com/LoAT-developers/LoAT/releases/tag/adcl-nt">LoAT ADCL</a>) with other leading termination analyzers: <a href="http://irankfinder.loopkiller.com:8081/">iRankFinder</a>, <a href="https://github.com/mmjb/T2">T2</a>, <a href="https://monteverdi.informatik.uni-freiburg.de/tomcat/Website/?ui=tool&tool=automizer">Ultimate</a>, <a href="https://www.cs.upc.edu/~albert/VeryMax.html">VeryMax</a>, and the previous version of LoAT (<a href="https://github.com/aprove-developers/LoAT/releases/tag/ijcar22">LoAT '22</a>).
    </p>

    <p>
      For T2, VeryMax, and Ultimate, we took the versions of their last participations at the <a href="https://termination-portal.org/wiki/Termination_Competition">Termination and Complexity Competition</a> (2015, 2019, and 2022).
      For iRankFinder, we used the configuration from the evaluation of our <a href="https://doi.org/10.1007/978-3-031-10769-6_41">IJCAR '22 paper</a>, which is tailored towards proving non-termination.
    </p>

    <p>
      We excluded <a href="https://aprove.informatik.rwth-aachen.de/">AProVE</a>, as it cannot prove non-termination of ITSs, and it uses LoAT and T2 as backends when analyzing C programs.
      Moreover, we excluded Ultimate from the evaluation on ITSs, as it cannot parse them.
      For the same reason, we excluded T2 and LoAT '22 from the evaluation on C integer programs.
    </p>

    <h2>StarExec Bundles</h2>

    We provide StarExec bundles for all tools used in our evaluation.

    <ul>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=d7af3eff-e61d-4d54-b895-86d8cf62c3cd">LoAT ADCL</a>, configuration <code>loat_nonterm_proofout</code> and <code>loat_c_nonterm_proofout</code>, respectively</li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?id=35581">LoAT '22</a>, configuration <code>loat_nonterm_proofout</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=a737357a-83c6-4d1e-b144-40e68d621037">T2</a>, configuration <code>default fixed</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=4798c8a9-e698-4029-a052-5ba641e2e0ea">VeryMax</a>, configuration <code>termcomp2019_ITS</code></li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=ca1897a6-b107-48ab-8c94-11f3e009bad4">iRankFinder</a>, configuration <code>competition_its</code> and <code>competition_c</code>, respectively</li>
      <li><a href="https://www.starexec.org/starexec/secure/details/solver.jsp?anonId=a6e85c65-6074-4ae3-9337-2bb9834554a6">Ultimate</a>, configuration <code>default</code></li>
    </ul>

    <h2>Results</h2>

    <p>
      The table below shows the results for our evaluation on ITSs.
      Here, avg, rt, and TO abberviate average, runtime, and Timeouts, respectively.
      Moreover, VB refers to the virtual best solver, i.e., the combination of all tools from our evaluation.
    </p>

    <table>
      <thead>
        <tr>
          <th></th>
          <th>NO</th>
          <th>unique NO</th>
          <th>Yes</th>
          <th>avg rt</th>
          <th>median rt</th>
          <th>TO</th>
          <th>avg rt NO</th>
          <th>median rt NO</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>LoAT ADCL</td>
          <td>521</td>
          <td>9</td>
          <td>0</td>
          <td>48.6s</td>
          <td>0.1s</td>
          <td>183</td>
          <td>2.9s</td>
          <td>0.1s</td>
        </tr>
        <tr>
          <td>LoAT '22</td>
          <td>494</td>
          <td>2</td>
          <td>0</td>
          <td>7.4s</td>
          <td>0.1s</td>
          <td>0</td>
          <td>6.2s</td>
          <td>0.1s</td>
        </tr>
        <tr>
          <td>T2</td>
          <td>442</td>
          <td>3</td>
          <td>615</td>
          <td>17.2s</td>
          <td>0.6s</td>
          <td>45</td>
          <td>7.4s</td>
          <td>0.6s</td>
        </tr>
        <tr>
          <td>VeryMax</td>
          <td>421</td>
          <td>6</td>
          <td>631</td>
          <td>28.3s</td>
          <td>0.5s</td>
          <td>30</td>
          <td>30.5s</td>
          <td>14.5s</td>
        </tr>
        <tr>
          <td>iRankFinder</td>
          <td>409</td>
          <td>0</td>
          <td>642</td>
          <td>32.0s</td>
          <td>2.0s</td>
          <td>93</td>
          <td>12.3s</td>
          <td>1.7s</td>
        </tr>
        <tr>
          <td>VB</td>
          <td>536</td>
          <td>--</td>
          <td>661</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
        </tr>
      </tbody>
    </table>

    <p>
      Impressively, the virtual best solver can solve all but 25 of the 1222 examples.
      As a reference, the participants of the first run of the category Termination of ITSs on the same set of examples in 2015 could solve all but 105 examples.
    </p>

    <p>
      The next table below shows the results for our evaluation on C Integer Programs.
    </p>

    <table>
      <thead>
        <tr>
          <th></th>
          <th>NO</th>
          <th>unique NO</th>
          <th>Yes</th>
          <th>average runtime</th>
          <th>median runtime</th>
          <th>timeouts</th>
          <th>average runtime NO</th>
          <th>median runtime NO</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>LoAT ADCL</td>
          <td>102</td>
          <td>2</td>
          <td>0</td>
          <td>24.7s</td>
          <td>0.1s</td>
          <td>26</td>
          <td>0.2s</td>
          <td>0.1s</td>
        </tr>
        <tr>
          <td>VeryMax</td>
          <td>103</td>
          <td>1</td>
          <td>213</td>
          <td>5.5s</td>
          <td>0.1s</td>
          <td>0</td>
          <td>12.0s</td>
          <td>8.3s</td>
        </tr>
        <tr>
          <td>Ultimate</td>
          <td>100</td>
          <td>0</td>
          <td>205</td>
          <td>14.8s</td>
          <td>4.6s</td>
          <td>9</td>
          <td>6.1s</td>
          <td>3.9s</td>
        </tr>
        <tr>
          <td>iRankFinder</td>
          <td>90</td>
          <td>1</td>
          <td>206</td>
          <td>9.9s</td>
          <td>1.7s</td>
          <td>2</td>
          <td>5.0s</td>
          <td>1.6s</td>
        </tr>
        <tr>
          <td>VB</td>
          <td>109</td>
          <td>--</td>
          <td>215</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
          <td>--</td>
        </tr>
      </tbody>
    </table>

    <p>
      Finally, we provide tables with the detailed results of our benchmarks.
    </p>
    <ul>
      <li>
        <a href="table.html">Integer Transition Systems</a>
      </li>
      <li>
        <a href="table_c.html">C Integer Programs</a>
      </li>
    </ul>

  </body>
</html>
