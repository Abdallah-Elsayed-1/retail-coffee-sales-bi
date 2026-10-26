<div align="center">

  <h1>☕ Coffee Shop Executive & Sales Analytics</h1>
  <p><b>An End-to-End Enterprise Power BI Dashboard featuring Page Navigation, Web.Contents ETL, Dynamic DAX, and Retail Sales Diagnostics.</b></p>

  <!-- Clean Tech Stack Badge Bar -->
  <p align="center">
    <code>🟡 Power BI Desktop</code> &bull; 
    <code>🔵 M-Code & Web.Contents ETL</code> &bull; 
    <code>🟢 Dynamic DAX & Time Intelligence</code> &bull; 
    <code>🟣 Dimensional Star Schema</code> &bull; 
    <code>☕ Retail Analytics</code>
  </p>

</div>

<hr />
<br />

<h2>📌 Project Overview</h2>
<p>
  This project delivers an interactive <b>Coffee Shop Sales & Operations Intelligence Solution</b> developed in Power BI. It is engineered for retail branch managers and commercial strategists to evaluate sales trajectory, examine unit movement across beverage and bakery categories, compare store performance across locations (Astoria, Lower Manhattan, Hell's Kitchen), and review line-item transactions.
</p>
<p>
  <b>Business Objective:</b> Enable retail leadership to identify top-performing product lines, monitor average order value, track Month-over-Month (MoM) revenue pace, and conduct transaction-level ledger audits.
</p>

<br />

<h2>📊 Executive Dashboard Preview</h2>
<p>The primary executive command center featuring multi-location sales distribution, revenue progression trends, and top product categories:</p>

<div align="center">
  <img src="https://i.postimg.cc/PJZZjwTB/excutive-over-View.png" alt="Coffee Shop Executive Overview" width="100%" />
</div>

<br />
<hr />
<br />

<h2>🔑 Key Performance Indicators (KPIs)</h2>
<ul>
  <li><b>Total Sales:</b> $698.81K gross retail sales generated across the network.</li>
  <li><b>Total Transactions & Volume:</b> 149K completed customer orders fulfilling 214K total units.</li>
  <li><b>Average Ticket Size (AOV):</b> $4.7 average spend per customer transaction.</li>
  <li><b>Basket Depth:</b> 1.44 average units purchased per transaction.</li>
  <li><b>MoM Growth Rate:</b> +31.28% revenue surge ($166.49K increase) compared to preceding period.</li>
  <li><b>Sales Per Store:</b> $232.9K average baseline revenue across active locations.</li>
</ul>

<br />
<hr />
<br />

<h2>🛠️ Analytics Architecture & Technical Stages</h2>

<h3>Stage 1: Automated Cloud ETL Pipeline & Dimension Modeling</h3>
<p>
  Data extraction was automated via <b>Power Query M-Code</b> using <code>Web.Contents</code> to ingest cloud-hosted data sources dynamically. Dimension engineering was implemented to generate standardized product categorizations and granular calendar matrices.
</p>

<div align="center">
  <table border="0" width="100%">
    <tr>
      <td width="33%" align="center" valign="top">
        <h4>Cloud Source Ingestion (M-Code)</h4>
        <img src="https://i.postimg.cc/tJPPjx9g/swrs.png" width="95%" alt="Power Query Web Contents" />
        <p align="left"><small>Dynamic web-based cloud ingestion pipeline.</small></p>
      </td>
      <td width="33%" align="center" valign="top">
        <h4>Product Dimension & Price Tiers</h4>
        <img src="https://i.postimg.cc/rsWWkrqF/brwdkt.png" width="95%" alt="Product Dimension Setup" />
        <p align="left"><small>Classification of products and price band tiers.</small></p>
      </td>
      <td width="33%" align="center" valign="top">
        <h4>Calendar Date Dimension</h4>
        <img src="https://i.postimg.cc/tJPPjx9n/kalndr-dyt.png" width="95%" alt="Calendar Dimension Table" />
        <p align="left"><small>Date hierarchy supporting Day, Month, and Quarter modeling.</small></p>
      </td>
    </tr>
  </table>
</div>

<br />

<h3>Stage 2: Relational Data Modeling (Star Schema)</h3>
<p>
  The data model separates operational transactions and revenue facts from descriptive dimensions through normalized 1-to-many (<code>1:*</code>) relationships, ensuring efficient filter propagation and DAX computation:
</p>

<div align="center">
  <img src="https://i.postimg.cc/Hn55gyTJ/mwdylynj.png" alt="Star Schema Relational Data Model" width="90%" />
</div>

<br />

<h3>Stage 3: Core Dynamic DAX Expressions</h3>
<p>Analytical calculations isolated in a dedicated measure table:</p>
<ul>
  <li><code>Total Revenue</code> = <code>SUM(Fact_sales[toal_sales])</code></li>
  <li><code>AVG Trans Value</code> = <code>DIVIDE([total revenu], [total transaction], 0)</code></li>
  <li><code>AVG Quantity Per Trans</code> = <code>DIVIDE([Total Quantity Sold], [total transaction], 0)</code></li>
  <li><code>MOM_change</code> = <code>[total revenu] - [Last month_Revenu]</code></li>
  <li><code>MOM_PCT %</code> = <code>DIVIDE([MOM_change], [Last month_Revenu], 0)</code></li>
</ul>

<br />
<hr />
<br />

<h2>🎯 Detailed Navigation & Analytical Modules</h2>

<h3>1. Report Navigation Portal & Scorecard Overview</h3>
<p>Intuitive page routing alongside a consolidated KPI matrix for operational reviews:</p>

<div align="center">
  <table border="0" width="100%">
    <tr>
      <td width="50%" align="center" valign="top">
        <h4>Landing Page Navigation Portal</h4>
        <img src="https://i.postimg.cc/MHRRSQzT/login.png" width="95%" alt="Navigation Landing Page" />
        <p align="left"><small>Custom UI buttons routing to core diagnostic views.</small></p>
      </td>
      <td width="50%" align="center" valign="top">
        <h4>Consolidated KPIs Matrix</h4>
        <img src="https://i.postimg.cc/sXbSqcCy/dax-measuers.png" width="95%" alt="KPIs Overview Matrix" />
        <p align="left"><small>Unified card board for store averages and growth rates.</small></p>
      </td>
    </tr>
  </table>
</div>

<br />

<h3>2. Sales Performance & Waterfall Diagnostics</h3>
<p>Visualizing revenue build-up across product categories and evaluating unit velocity:</p>

<div align="center">
  <img src="https://i.postimg.cc/2yvvDZCr/sales-performance.png" alt="Sales Performance and Waterfall Analysis" width="95%" />
</div>

<br />

<h3>3. Granular Transaction Audit & Multi-Level Filtering</h3>
<p>Detailed row-level audit trails and multi-attribute slicer interaction:</p>

<div align="center">
  <table border="0" width="100%">
    <tr>
      <td width="50%" align="center" valign="top">
        <h4>Multi-Category Cross Filtering</h4>
        <img src="https://i.postimg.cc/j2NNb7RC/fltr.png" width="95%" alt="Filtered Performance View" />
        <p align="left"><small>Dynamic filtering isolating Lower Manhattan coffee demand ($89K).</small></p>
      </td>
      <td width="50%" align="center" valign="top">
        <h4>Itemized Transaction Details</h4>
        <img src="https://i.postimg.cc/PJZZjwdj/details.png" width="95%" alt="Granular Details Ledger" />
        <p align="left"><small>Invoice-level grid detailing unit sales and timestamps.</small></p>
      </td>
    </tr>
  </table>
</div>

<br />
<hr />
<br />

<h2>💡 Strategic Recommendations & Insights</h2>
<ol>
  <li><b>Beverage Volume Dominance:</b> Coffee and Tea drive the vast majority of store turnover ($270K and $196K respectively). Bundling baked goods ($82K) with morning brews represents a high-conversion cross-selling opportunity.</li>
  <li><b>Even Branch Contribution:</b> Revenue is evenly distributed across Astoria (33.84%), Lower Manhattan (33.23%), and Hell's Kitchen (32.92%), proving brand equity is uniform across diverse commercial zones.</li>
  <li><b>Growth Momentum Capitalization:</b> Sales accelerated steadily from January ($62K) to peak in June ($166K), indicating strong seasonal summer demand that warrants proactive inventory ramp-up.</li>
</ol>

<br />
<hr />
<br />

<h2>📂 Repository Architecture</h2>
<pre>
├── Data/                        # Retail transaction and calendar datasets
├── Reports/                     # Coffee_Shop_Executive_Analytics.pbix
├── Screenshots/                 # Multi-page dashboard interface views
└── README.md                    # Project documentation
</pre>

<br />

<div align="center">
  <p>Developed with passion by <b>Abdallah Elsayed</b> | Data & Business Intelligence Analyst</p>
</div>
