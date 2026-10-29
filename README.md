<!--
  Profile README for github.com/Lunarc-Seattle.
  The banners live in assets/. Project pictures load straight from each project's own repo.
-->

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" alt="Jie (Fia) Yin. LLM evaluation and backend engineering." width="100%">
</picture>

I build Python pipelines and tools that run unattended, check their own results and give the same output on every rerun: automated runs with retries and resume, regression tests in CI, versioned data and results.

I'm a master's student in Information Systems at Northeastern's Silicon Valley campus and a TA for INFO 7374, Advanced Techniques with Large Language Models. My first degree is in landscape architecture, so my projects deal with terrain, water and maps. Looking for SDE roles in simulation and data tooling, and LLM engineering roles.

### Current LLM research

**LLM failure mode discovery: flood reasoning from site maps**<br>
Research with Prof. Lai at Northeastern, since January 2026

* Found and validated a failure mode in multimodal LLMs reading site-analysis maps: they mark floodplain only where water is mapped (3/49 for DeepSeek, 0/49 for Gemini on dry floodplain cells, vs. 24/26 for a blind human baseline); built a leakage-safe 194-site dataset from FEMA, USGS and county GIS data.
* Built a Python data pipeline over ArcGIS REST services (FEMA, USGS, county GIS) with tiled downloads, caching, retries and completeness checks that caught silent data loss; generated datasets for 148 sites in one overnight run.
* Designed an atomic rubric and a single scalar RL reward with automated tests; calibration caught a reward hack (always-NO scored 0.97, above both models), fixed by centering the reward on balanced accuracy (now 0.58 vs. 1.06 for reference answers); SFT and GRPO on a small VLM in progress.

The repository is private on purpose. If the test sites and answer keys were public, future models could look them up or see them in training, and the benchmark would stop measuring anything. [Contact me](https://www.linkedin.com/in/jiefiayincodingirl/) for details or a walkthrough.

### Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://lunarc-seattle.github.io/breath-runner/"><img src="https://github.com/Lunarc-Seattle/breath-runner/raw/main/docs/media/breath-runner.gif" alt="Breath Runner gameplay: the runner jumps a gap on a long inhale and collects coins" width="100%"></a>
      <h4><a href="https://github.com/Lunarc-Seattle/breath-runner">Breath Runner</a></h4>
      <p>A breathing rehab game for people recovering from lung surgery at home: breathe into the microphone to jump and glide. I designed the trainer, the app and the illustrations, then built it in React and TypeScript, with unit and end-to-end tests gating every deploy. Two versions are playable: <a href="https://lunarc-seattle.github.io/breath-runner/v1/">v1</a>, the first release, and <a href="https://lunarc-seattle.github.io/breath-runner/v2/">v2</a>, with the redesigned app pages.</p>
      <sub>React, TypeScript, Playwright, illustration</sub>
    </td>
    <td width="50%" valign="top">
      <a href="https://lunarc-seattle.github.io/st-augustine-slr/"><img src="https://github.com/Lunarc-Seattle/st-augustine-slr/raw/main/docs/figures/fig0_cover.png" alt="St. Augustine at 1, 5 and 9 ft of sea level rise: 8.0%, 43.3% and 69.4% of city land newly inundated" width="100%"></a>
      <h4><a href="https://github.com/Lunarc-Seattle/st-augustine-slr">St. Augustine sea level rise</a></h4>
      <p>How much of St. Augustine, Florida floods at 1 to 9 ft of sea level rise, rebuilt as a one-command Python pipeline on NOAA, Census and OpenStreetMap data. Reruns give byte-identical results, each run records SHA-256 hashes of every input and output and checks its own invariants, and CI tests it on Linux, macOS and Windows.</p>
      <sub>Python, GeoPandas, pytest, GitHub Actions</sub>
    </td>
  </tr>
</table>

### Backend projects

[CloudBite Engine](https://github.com/Lunarc-Seattle/CloudBite-Engine) is a food delivery backend on Spring Boot, MyBatis, MySQL and Redis, with JWT auth and WebSocket order alerts. It includes 18 bilingual engineering notes where I question and verify the course material instead of copying it.

[Patient management microservices](https://github.com/Lunarc-Seattle/SpringBoot) is a patient management system split into five Spring Boot services that talk over gRPC and Kafka behind an API gateway, running locally on Docker and LocalStack.

### Tools

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=java,spring,py,ts,react,mysql,postgres,redis,kafka,docker,githubactions&theme=dark">
  <img src="https://skillicons.dev/icons?i=java,spring,py,ts,react,mysql,postgres,redis,kafka,docker,githubactions&theme=light" alt="Java, Spring, Python, TypeScript, React, MySQL, PostgreSQL, Redis, Kafka, Docker, GitHub Actions" height="40">
</picture>

Reach me on [LinkedIn](https://www.linkedin.com/in/jiefiayincodingirl/).
