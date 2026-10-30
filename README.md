# Donghyun Kim (김동현)

I study Computer Science and Engineering at Seoul National University (expected 2028) and served in the Republic of Korea Air Force from 2023 to 2025.

I build LLM agents and services where deterministic code makes the decisions and a person approves what code can't decide. The model searches, reads and explains, and the evidence behind a decision has to be something the program can check.

## Results

- **[KRAFTON AI R&D Autonomy Hackathon 2026](https://kraftonai-autonomy-hackathon.com/): winner** (solo, 4 weeks, Oct 2026), 1st of 108 overall. The code is private because the problem materials are for participants only.
  - Autonomous navigation (1st of 105): trajectory optimization with iLQR, and Hybrid A\* to get out of dead ends.
  - Sim-to-real (2nd of 96): simulator calibration by gray-box system identification, and training-data design.
  - Lightweight video world model (1st of 84): physics identified from recordings and integrated inside the model, instead of learned dynamics.
- **2026 OpenAI-Seoul National University AI Summer Camp (AI Hackathon): winner** (team of 3, Aug 2026) with [Figma Font License Agent](https://github.com/jsko0313-glitch/LetsgoOpenAI) (Korean README), a Figma plugin and server that checks fonts against the company's licenses and never labels one COVERED without evidence.
  - My part: the 14 spec documents, the initial monorepo, the server's verdict pipeline, and the plugin UI and its server connection. By default the plugin runs in simulation mode and makes no real license judgments.

## How I work

- I set the goals and acceptance criteria, approve plans and decide what ships. Claude Code and Codex write most of the code, and commits made through Claude Code carry Co-Authored-By trailers.
- In the KRAFTON hackathon, a coordinator session handed tasks to Codex workers, each in its own git worktree, and reproduced one key claim from each report before merging.
- In all three problems, local metrics did not rank my candidates the way the official scores did (one world-model candidate scored 83.65 on my local control proxy and 15.37 officially), so I used them only to screen out broken candidates. Each upload was registered in advance with an expected score and a decision rule, and had to pass the official validator (498 scored uploads).
- Each submission behind my final score has a script that rebuilds the uploaded file byte for byte. Upstream selection and some training runs are not repeated.

## Selected projects

- [redline](https://github.com/dnhynk/redline): a fact-checking agent for AI-written text, built solo at the 24-hour AGENT:24 hackathon (Aug 2026). The verdict tool accepts only evidence IDs the host issued for search and fetch results, so no verdict can cite a source the agent never retrieved.
- [home-compass](https://github.com/dnhynk/home-compass): a solo contest MVP that helps young renters in Korea weigh lease costs and housing-program eligibility. Rules the LLM drafts from policy documents take effect only after their quotes match the source verbatim and a rule manager approves them. Four of the seven stored drafts failed the automatic check.
- [dev-infra](https://github.com/dnhynk/dev-infra): Slack cards and buttons for supervising my Claude Code and Codex agents running in parallel in Orca. A decision made in Slack is recorded in Orca before the waiting coordinator is woken to read it.
- [ctf-agent](https://github.com/dnhynk/ctf-agent): a harness and evaluation contract for a CTF-solving agent in authorized environments. A checker judges each recorded attempt, and a candidate flag counts only if it can be traced to tool output. It has not solved a CTF challenge yet.
- [postfeel](https://github.com/dnhynk/postfeel): a web app for unsent letters, open to anyone or locked for one reader. A rule filter and an LLM classifier check each letter for details that identify a real person, and a letter the classifier could not judge stays hidden. Not launched.

## Stack

- Languages: Python, TypeScript, Rust, C
- ML: PyTorch, ONNX, NumPy, SciPy
- Backend and web: FastAPI, Next.js, SQLite, PostgreSQL, Docker
- LLM tooling: OpenAI Agents SDK, vLLM, Claude Code, Codex
- Infrastructure: Linux GPU server, AWS EC2, Oracle OCI

## Contact

donghyun9282@snu.ac.kr
