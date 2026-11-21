<!-- ░░ HEADER ░░ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=210&color=0:0f2027,55:203a43,100:2c5364&text=Vivaan%20Sanghavi&fontColor=ffffff&fontSize=58&fontAlignY=36&desc=B.Tech%20IT%20%40%20VJTI%20Mumbai%20%20%E2%80%A2%20%20Systems%20%C2%B7%20Open%20Source%20%C2%B7%20ML&descSize=17&descAlignY=58&animation=fadeIn" width="100%" alt="Vivaan Sanghavi" />
</p>

<p align="center">
  <a href="https://github.com/vivs24307-maker">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=900&color=22D3EE&center=true&vCenter=true&width=620&lines=C%2B%2B+%C2%B7+parallel+runtimes+%C2%B7+databases;Merged+PRs+in+HPX+%E2%80%94+the+C%2B%2B+parallel+runtime;Contributing+to+MariaDB+Connector%2FC;Co-building+MemoraDB%3A+a+temporal+%2B+vector+DBMS;ML+for+floods%2C+oceans+and+oil+spills" alt="typing intro" />
  </a>
</p>

<p align="center">
  <a href="mailto:vivs24307@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/vivs24307-maker?tab=repositories"><img src="https://img.shields.io/badge/Repos-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
  <img src="https://komarev.com/ghpvc/?username=vivs24307-maker&style=for-the-badge&color=22d3ee&label=PROFILE+VIEWS" />
</p>

<br/>

<!-- ░░ ABOUT — written the way I like to think ░░ -->
```cpp
#include <future>

struct Vivaan {
    std::string_view studies   = "B.Tech Information Technology @ VJTI, Mumbai";
    std::string_view loves     = "systems code: runtimes, schedulers, storage engines";
    std::array<std::string_view, 3> stack = {"C / C++", "Machine Learning", "DBMS"};
    std::string_view open_src  = "HPX · MariaDB Connector/C · FOSSology";
    std::string_view looking   = "GSoC · open-source programs · SWE internships";
    std::string_view fun_fact  = "I hunt bugs in chunk sizes and in byte order";
};

int main() {
    auto next = std::async([] { /* next PR: HPX, MariaDB, FOSSology */ });
    next.get();   // ⏳ always in progress
}
```

---

## 🧬 Open-Source Contributions

> I like bugs that hide in release builds and in the byte order of other people's machines.

<table>
  <tr>
    <th align="left">Project</th>
    <th align="left">Contribution</th>
    <th align="center">Status</th>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/HPX-C%2B%2B%20parallel%20runtime-1f6feb?style=flat-square" /></td>
    <td><a href="https://github.com/TheHPXProject/hpx/pull/8065"><b>#8065</b></a> · Parallel <code>set_union / intersection / difference / symmetric_difference</code> silently dropped results whenever the execution policy used a chunk size &gt; 1 (the guarding assert vanished in release builds). Fixed chunk handling in both the compute and copy steps and added a regression test that checks all four ops against the STL across static &amp; dynamic chunk sizes.</td>
    <td align="center"><img src="https://img.shields.io/badge/merged-8250df?style=flat-square&logo=git-merge&logoColor=white" /></td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/HPX-parallel%20algorithms-1f6feb?style=flat-square" /></td>
    <td><a href="https://github.com/TheHPXProject/hpx/issues/8115"><b>Issue #8115</b></a> → <a href="https://github.com/TheHPXProject/hpx/pull/8123"><b>#8123</b></a> · Found that <code>all_of</code>, <code>any_of</code>, <code>equal</code>, <code>is_sorted</code>, <code>transform_reduce</code> and other parallel algorithms didn't compile with <code>guided_chunk_size</code>: the static partitioner handed the reduction a future instead of the chunk results. Reported it, fixed the reduce step and added a regression test.</td>
    <td align="center"><img src="https://img.shields.io/badge/merged-8250df?style=flat-square&logo=git-merge&logoColor=white" /></td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/HPX-parallel%20algorithms-1f6feb?style=flat-square" /></td>
    <td><a href="https://github.com/TheHPXProject/hpx/pull/8178"><b>#8178</b></a> · Follow-up to #8115: <code>copy_if</code>, <code>unique_copy</code>, <code>partition_copy</code>, the four scans and <code>merge</code> also failed to compile with <code>guided_chunk_size</code>. Fixed the scan and for_each partitioners and added a regression test against the standard library.</td>
    <td align="center"><img src="https://img.shields.io/badge/in%20review-2da44e?style=flat-square&logo=git-pull-request&logoColor=white" /></td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/MariaDB-Connector%2FC-003545?style=flat-square&logo=mariadb&logoColor=white" /></td>
    <td><a href="https://github.com/mariadb-corporation/mariadb-connector-c/pull/334"><b>#334 · CONC-867</b></a> · <code>MYSQL_TYPE_VECTOR</code> values were copied raw into prepared-statement buffers, so big-endian hosts got byte-swapped floats. Each element is now unpacked in host byte order (incl. partial fetches at any offset), with updated unit tests.</td>
    <td align="center"><img src="https://img.shields.io/badge/in%20review-2da44e?style=flat-square&logo=git-pull-request&logoColor=white" /></td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/FOSSology-license%20compliance-0b7a75?style=flat-square" /></td>
    <td><a href="https://github.com/fossology/fossology/pull/4012"><b>#4012</b></a> · Search page now falls back to a sane default limit when the parameter is missing.</td>
    <td align="center"><img src="https://img.shields.io/badge/merged-8250df?style=flat-square&logo=git-merge&logoColor=white" /></td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/MariaDB-Server-003545?style=flat-square&logo=mariadb&logoColor=white" /></td>
    <td><a href="https://github.com/MariaDB/server/pull/6168"><b>#6168 · MDEV-41356</b></a> · <code>CREATE TABLE … SELECT</code> turned <code>VECTOR</code> results of window functions and scalar subqueries into <code>VARBINARY</code>, because the vector type handler inherited VARCHAR's temp-table handler. It now keeps the <code>VECTOR</code> type, with a new mtr test.</td>
    <td align="center"><img src="https://img.shields.io/badge/approved-1a7f37?style=flat-square&logo=github&logoColor=white" /></td>
  </tr>
</table>

---

## 🚀 Featured Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🗄️ <a href="https://github.com/v1haan24/MemoraDB">MemoraDB</a></h3>
      A from-scratch <b>C++17 relational DBMS</b> with append-only binary storage, immutable <b>time-travel queries</b> (<code>AS OF</code>, <code>BETWEEN</code>, <code>EVOLUTION</code>) and in-process <b>semantic search</b> via ONNX Runtime + MiniLM. I built the SQL parser/executor and vector compaction.
      <br/><br/>
      <img src="https://img.shields.io/badge/C%2B%2B17-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
      <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" />
      <img src="https://img.shields.io/badge/ONNX%20Runtime-005CED?style=flat-square&logo=onnx&logoColor=white" />
    </td>
    <td width="50%" valign="top">
      <h3>🛢️ <a href="https://github.com/shaurya212121/OceanGuard">OceanGuard AI</a></h3>
      <b>SIH 2026</b> · Detects marine oil spills in <b>SAR satellite imagery</b>, hindcasts drift with ocean currents to find the origin, then cross-references <b>AIS ship data</b> to score and attribute suspect vessels.
      <br/><br/>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
      <img src="https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🌊 <a href="https://github.com/vivs24307-maker/FloodOracle">FloodOracle</a></h3>
      Flood forecasting for the Hoovinahole catchment: <b>XGBoost</b> on 25 years of gauge data + <b>NASA POWER</b> satellite meteorology, with a soil-saturation "sponge effect" feature and a <b>Folium</b> spatial risk map.
      <br/><br/>
      <img src="https://img.shields.io/badge/XGBoost-EB5E28?style=flat-square" />
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
      <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
    </td>
    <td width="50%" valign="top">
      <h3>🎬 <a href="https://github.com/vivs24307-maker/dti_grp24">CineVerse</a></h3>
      Full-stack movie booking platform: <b>10-min seat locking</b> so no seat sells twice, QR M-tickets, refunds, coupons and an admin dashboard with revenue analytics. API-tested with Supertest.
      <br/><br/>
      <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
      <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
      <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" />
      <img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🗓️ <a href="https://github.com/shaurya212121/PDL_lab_project">ClashAudit</a></h3>
      Catches timetable clashes (faculty, room, section), enforces <b>AICTE/UGC workload limits</b>, suggests one-click fixes and finds substitutes when faculty are on leave. Excel/CSV import &amp; reports.
      <br/><br/>
      <img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white" />
      <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
      <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" />
    </td>
    <td width="50%" valign="top">
      <h3>⚙️ <a href="https://github.com/vivs24307-maker/CPUSim">CPUSim</a></h3>
      Simulates a CPU scheduling tasks with <b>Round Robin</b> while fetching through an <b>L1 → L2 → L3 → RAM</b> hierarchy with <b>LRU</b> eviction, reporting hits, misses and access cost.
      <br/><br/>
      <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
      <img src="https://img.shields.io/badge/Computer%20Architecture-444?style=flat-square" />
    </td>
  </tr>
</table>

---

## 🏆 Highlights

<p>
  <img src="https://img.shields.io/badge/Smart%20India%20Hackathon-2026%20Participant-C1622B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Hacktoberfest-2026%20Contributor-6f2da8?style=for-the-badge&logo=hacktoberfest&logoColor=white" />
  <img src="https://img.shields.io/badge/HPX-2%20merged%20PRs-1f6feb?style=for-the-badge" />
</p>

- 🛢️ **SIH 2026:** built [OceanGuard AI](https://github.com/shaurya212121/OceanGuard), [Well-Whisperer](https://github.com/shaurya212121/Well-Whisperer) (offset-well risk intelligence for Oil India) and [BlueByte AI](https://github.com/shaurya212121/Bluebyte) (ocean & biodiversity data platform) with my team
- 🎃 **Hacktoberfest 2026:** PRs to HPX and FOSSology
- 🔬 Currently working on `MYSQL_TYPE_VECTOR` handling in MariaDB Connector/C and digging into HPX's work-requesting schedulers

---

## 🛠️ Toolbox

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,cmake,python,sklearn,linux,git,github&theme=dark" /><br/>
  <img src="https://skillicons.dev/icons?i=mysql,sqlite,flask,fastapi,react,nodejs,express,vscode&theme=dark" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Parallel%20Computing-HPX-1f6feb?style=flat-square" />
  <img src="https://img.shields.io/badge/Databases-MariaDB%20%C2%B7%20SQLite%20%C2%B7%20DB%20internals-003545?style=flat-square&logo=mariadb&logoColor=white" />
  <img src="https://img.shields.io/badge/ML-XGBoost%20%C2%B7%20scikit--learn%20%C2%B7%20ONNX-EB5E28?style=flat-square" />
</p>

---

## 📊 GitHub Pulse

<p align="center">
  <img src="https://streak-stats.demolab.com?user=vivs24307-maker&hide_border=true&background=0d1117&ring=22d3ee&fire=22d3ee&currStreakLabel=22d3ee&sideLabels=c9d1d9&currStreakNum=ffffff&sideNums=ffffff&dates=8b949e&stroke=30363d" />
</p>

<!-- ░░ FOOTER ░░ -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=110&section=footer&color=0:0f2027,55:203a43,100:2c5364" width="100%" />
</p>
