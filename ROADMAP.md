# My DevOps Learning Journey: Roadmap

My plan and my progress for going from complete beginner to DevOps engineer, at my own pace.

It's based on [The Complete DevOps Engineer Roadmap](https://codewithmosh.com) by Mosh Hamedani. The PDF itself stays private: it's listed in `.gitignore`.

- **Part 1, the plan:** how I study, track my progress and make decisions. Agreed on 2026-11-09.
- **Part 2, the phases:** every topic in every phase, as checkboxes. This is where my progress is tracked.

## Contents

**Part 1: The plan**

1. [Guiding principle](#1-guiding-principle)
2. [Schedule](#2-schedule)
3. [Setup and safety](#3-setup-and-safety)
4. [Money and resources](#4-money-and-resources)
5. [Repo structure](#5-repo-structure)
6. [What done means](#6-what-done-means)
7. [Journal](#7-journal)
8. [Capstone project](#8-capstone-project)
9. [The learn script](#9-the-learn-script)
10. [Git habits](#10-git-habits)
11. [Revisit when I get there](#11-revisit-when-i-get-there)

**[Part 2: The phases](#part-2-the-phases)**

---

## Part 1: The plan

### 1. Guiding principle

**Structure with flexibility.** Structure creates discipline and consistency. Flexibility prevents discouragement and stops me from quitting when I miss the mark.

Every rule in this plan has a clear default (the structure) and a way to bend it when life gets in the way (the flexibility).

**Hands-on first.** I learn by doing: I type every command myself and write my own code, notes, labs and journal.

### 2. Schedule

I have a full-time job, so my study days and times change from week to week.

| | Structure | Flexibility |
|---|---|---|
| **Week** | Aim for 12–15 hours over 4–5 days | Any days, any times |
| **Streak** | A week (Monday to Sunday) counts if I study on at least 3 days | 3 is the minimum for hard weeks, not the target |
| **Study day** | At least 30 minutes of focused study, plus a journal entry | Short days still count |
| **Session** | Start by re-reading the "Next time" section of my last journal entry. End with notes, the journal entry and a commit | What happens in between depends on the topic |
| **Hands-on** | At least half of each phase's hours, checked in the retro | Some sessions are all reading and some are all labs. It evens out over a phase |
| **Breaks** | If I'm sick, busy at work or on holiday, I log a break week | The streak pauses instead of resetting |
| **Timeline** | About 1,035 hours: roughly 17–18 months at 13.5 hours a week | An estimate, not a deadline. It's recalculated from my real pace |

- My dashboard shows totals that only go up (hours, study days, topics done) and my longest streak, so a bad month never wipes out my progress.
- Break weeks appear on the dashboard too, which keeps them honest without needing a hard limit.

**Hour budgets.** The roadmap assumes 3–5 hours of study *every day*. Each phase's budget is the roadmap's upper estimate in weeks × 21 hours (3 hours a day, 7 days a week). I finish a phase when its topics are done, not when its hours run out.

| Phase | Roadmap estimate | Hour budget | Weeks at my pace (about) |
|---|---|---|---|
| 0 Setup | — | 6 | 0.5 |
| 1 Linux | 2–3 weeks | 63 | 5 |
| 2 Networking | 2 weeks | 42 | 3 |
| 3 Git | 1–2 weeks | 42 | 3 |
| 4 Python | 4–6 weeks | 126 | 9 |
| 5 AWS | 4–6 weeks* | 126 | 9 |
| 6 Docker | 3–4 weeks | 84 | 6 |
| 7 CI/CD (Jenkins) | 3–4 weeks | 84 | 6 |
| 8 Kubernetes | 4–6 weeks | 126 | 9 |
| 9 Nginx | 3–4 weeks | 84 | 6 |
| 10 Ansible | 3–4 weeks | 84 | 6 |
| 11 Terraform | 3–4 weeks | 84 | 6 |
| 12 Monitoring | 3–4 weeks | 84 | 6 |
| **Total** | 10–14 months | **about 1,035** | **about 75 weeks (17–18 months)** |

\*The PDF gives AWS 4–6 weeks in its overview table but 3–4 weeks on the AWS page. This plan uses the larger number.

### 3. Setup and safety

**My machine (at planning time, November 2026):**
- Dell Latitude 7390 with a 4-core Intel i5, 8 GB of RAM and Ubuntu 26.04 LTS. Virtual machines are supported.
- **Already installed:** git, Python 3.14, VS Code, VirtualBox, curl, ssh and nano.
- **Docker:** installed but not fully set up. Compose is missing, and it needs `sudo`. Finishing the setup is a Phase 6 lesson.
- **Memory:** 8 GB is enough for the whole roadmap, but tight in Phase 8 (Kubernetes), Phase 10 (Ansible) and the ELK part of Phase 12. In those phases I'll use lightweight options and close the browser while labs run.
- **Possible upgrade:** the RAM is a single removable stick, and the laptop reports support for up to 32 GB, so a 16 GB stick is an option. I'll decide around Phase 8.

**I install each tool when its phase starts.** Installing tools myself is part of the learning: Phase 1 covers package management.

| Phase | What I'll set up | Cost |
|---|---|---|
| 0 Setup | An SSH key to connect to GitHub | Free |
| 1 Linux | A throwaway Ubuntu VM in VirtualBox, and basic vim (only nano is installed) | Free |
| 2 Networking | Wireshark, traceroute and other network tools | Free |
| 3 Git | Nothing new | Free |
| 4 Python | pip and virtual environments | Free |
| 5 AWS | An AWS account and the AWS CLI | Free plan (see below) |
| 6 Docker | The rest of the Docker setup: Compose, and running it without sudo | Free |
| 7 CI/CD | Jenkins, running inside Docker | Free |
| 8 Kubernetes | A small local cluster (kind or minikube), kubectl and Helm | Free |
| 9 Nginx | Nginx, HAProxy and Redis, in containers | Free |
| 10 Ansible | Ansible, plus 2–3 practice servers (containers or small VMs) | Free |
| 11 Terraform | Terraform | Maybe a few dollars (see below) |
| 12 Monitoring | Prometheus, Grafana and ELK, in containers | Free |

**Accounts:**

| Account | When | Why |
|---|---|---|
| GitHub | Phase 0 (I already have one) | This repo lives there |
| AWS | The day I start Phase 5, not before | The free plan's clock starts when I sign up |
| Docker Hub | Phase 6, optional | For sharing container images. GitHub can do this too |

**The AWS free plan** (checked November 2026; check again at Phase 5):
- New accounts get $100–200 in credits.
- The free plan ends 6 months after sign-up, or sooner if the credits run out, and then AWS closes the account. On the free plan I can't be charged unless I choose to upgrade.
- At my pace, Phase 5 starts around month 5, so the free plan would end around month 11, during Kubernetes.
- Terraform (around month 14) uses AWS again. I'll either:
  - upgrade to pay-as-you-go with a billing alert, which costs a few dollars if I delete everything after each session, or
  - practise Terraform locally and keep the AWS part short.
- AWS has started rolling out spending limits for new accounts. If one is available when I sign up, I'll set it.
- Details: [AWS Free Tier](https://aws.amazon.com/free/).

**Safety rules, from day one:**
1. **Break things in a VM, not on my laptop.** Firewall rules, permission changes and deleting system files all happen in the throwaway VM. If it breaks, I delete it and make a new one.
2. **Nothing secret goes in the repo.** It's public, and bots scan GitHub for leaked keys and abuse them within minutes.
3. **AWS, from my first day in Phase 5:** two-step login (MFA) on the root account, a budget alert, and deleting everything I created at the end of each session.
4. **Git:** if a command contains `--force` or `reset --hard`, I stop and check before running it.

**Connecting to GitHub:**
- I use an SSH key instead of the `gh` tool. That way I learn SSH, which I'll also use to log into servers in Phase 5 and with Ansible in Phase 10.
- I create the empty repo on the GitHub website.
- For this repo only, I set my full name and GitHub's private (noreply) email address. My global git identity stays as it is.

### 4. Money and resources

**Money:** $0 until the month-4 checkpoint. After that, I'm willing to spend some.

**The month-4 checkpoint:**
- **When:** 4 months after I start, around the middle of Phase 4 and just before AWS.
- **What I look at:** hours logged, how many weeks my streak held, topics done, and how I feel about it.
- **What I decide:** keep going for free, or start spending, and on what: a course, AWS after the free plan, or more memory.
- **It's a check-in, not a test.** Missing a target means I adjust the plan, not that I stop.

**How I choose each phase's resources:**
1. **One main resource**, a course or a book, as the backbone. I stick with it, and only switch if it still isn't working after a week of honest effort. If I switch, I note why in my journal.
2. **One hands-on practice source**, such as exercises, games or labs.
3. **The official documentation.**

I learn best from **videos and hands-on practice**, so video-led resources come first.

| Phase | Main resource | Practice | Docs |
|---|---|---|---|
| 0 Setup | The Phase 0 steps in Part 2 | This repo | GitHub's [Markdown guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) and [SSH guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) |
| 1 Linux | [Introduction to Linux (LFS101)](https://training.linuxfoundation.org/training/introduction-to-linux/), free from the Linux Foundation. It mixes reading, short videos and labs. I can skim the desktop and printing chapters. Backup: [The Linux Command Line](https://linuxcommand.org/tlcl.php), a free book | [OverTheWire Bandit](https://overthewire.org/wargames/bandit/), plus my throwaway VM | `man` pages |
| 2 Networking | [Professor Messer](https://www.professormesser.com)'s free Network+ videos, only the sections that cover the roadmap's topics | Wireshark on my own traffic, plus `ping`, `traceroute`, `dig` and UFW in my VM | `man` pages |
| 3 Git | Mosh's free Git tutorial on [YouTube](https://www.youtube.com/c/programmingwithmosh), then [Pro Git](https://git-scm.com/book), a free book | [Learn Git Branching](https://learngitbranching.js.org), plus this repo | Pro Git |
| 4 Python | [CS50P](https://cs50.harvard.edu/python/), Harvard's free Python course | [Automate the Boring Stuff with Python](https://automatetheboringstuff.com) (free online), plus capstone v0.4 | The [Python tutorial](https://docs.python.org/3/tutorial/) |

**Phases 5–12:**
- I choose resources at the start of each phase, using the same three parts, video first.
- Paid options are allowed after the checkpoint. If I pay for something, I'll save it for the harder phases like AWS or Kubernetes, where a structured course saves the most time.
- Every tool in these phases has free official tutorials, so $0 stays possible the whole way.

### 5. Repo structure

Repo name: **`my-devops-learning-journey`** (public).

```
my-devops-learning-journey/
├── README.md          Front page: who I am, my goal, current progress
├── ROADMAP.md         This file: the plan (Part 1) and every topic as a checkbox (Part 2)
├── .gitignore         Keeps the PDF, passwords and keys out of the public repo
├── templates/         Blank pages to copy: journal, notes, lab, retro, phase README
├── journal/
│   └── 2026/
│       └── 2026-11-20.md   One file per study day
├── cheatsheets/
│   └── linux.md       One page per tool: the commands I actually use
├── phases/
│   └── 01-linux/      Created the day the phase starts
│       ├── README.md  Goal, resources, budget, dates, tools, exit challenge
│       ├── notes/     One file per topic
│       ├── labs/      One file per lab
│       └── retro.md   End-of-phase reflection
└── scripts/
    └── learn          My progress script, built in Phase 1
```

- **Progress lives in one place.** Checkboxes appear only in Part 2 of this file, so nothing can disagree with it.
- **Notes and cheat sheets do different jobs.** Notes explain *why* things work. A cheat sheet lists the commands I actually use.
- **The repo grows as I go:**

| When | What I create |
|---|---|
| Phase 0 | README, .gitignore, templates, `phases/00-setup`, my first journal entry. ROADMAP already exists |
| Start of each phase | That phase's folder |
| Phase 1 | `scripts/learn` and my first cheat sheet |
| Phase 4 | The capstone, in its own repo |
| Phase 7 | `.github/workflows/`, the automation that refreshes my README every time I push |

- **`.gitignore` grows too:** Python virtual environments in Phase 4, Terraform state files in Phase 11.

**Naming rules:**
- Lowercase, with hyphens instead of spaces. Spaces in file names cause trouble in the terminal.
- Phase folders are numbered `00-` to `12-`, so they sort in order.
- Dates are written `YYYY-MM-DD`, so journal files sort by date.
- Inside `notes/` and `labs/`, I organise things however suits me.

### 6. What done means

**A topic is done when all three of these are true:**
1. **Learned:** I've worked through it in my main resource.
2. **Explained:** I've written notes on it in my own words.
3. **Applied:** I've done it myself in a lab. Following along with a video doesn't count; doing it again on my own, or with a small change, does.

**The flexible parts:**
- One lab can cover several topics.
- Concept topics, like the OSI model, get a small exercise instead of a big lab.
- If I've met the bar but still feel shaky, I tick the topic and add "(revisit)".
- If I've been stuck on a topic for more than a week, I do what I can, tick it with "(revisit)" and move on. Later phases often make earlier topics click.

**A phase is finished when:**
1. Every core topic is ticked. Topics marked "(revisit)" count.
2. The exit challenge is done and written up as a lab.
3. The retro is written.

Hours are never a condition for finishing, and optional topics never block me.

**How Part 2 works:**
- Core topics are plain checkbox lines. I tick one by changing [ ] to [x].
- Optional topics end with "(optional)". These are the roadmap's alternatives to its recommended tools: Azure, GCP, Puppet, Chef and CloudFormation. ELK stays a core topic, because it's the logging half of "Monitoring and Logging".
- Each phase ends with two items in bold: **Exit challenge** and **Retro**.
- Only Part 2 contains checkboxes, so scripts can count them reliably.

**A phase from start to finish:**
- **Start:** create the phase folder, write the phase README, install the phase's tools, commit.
- **During:** study sessions, where I write notes, do labs and tick topics.
- **Finish:** do the exit challenge, write the retro, update "current phase" in my README, commit. From Phase 3 onwards, I also tag each finished phase (for example `phase-01-done`) and go back to tag the earlier ones.

**Templates:**

| Template | Sections |
|---|---|
| Phase README | Goal in my own words · Resources (main, practice, docs) · Hour budget · Start and end dates · Tools installed · Exit challenge |
| Notes | What it is · Why it matters in DevOps · How to use it (commands, examples) · Mistakes I made · Links |
| Lab | Goal · What I did · What broke and how I fixed it · What I learned |
| Retro | Hours compared with the budget · Share of time spent hands-on · What went well · What was hard · Topics to revisit · One thing to change next phase |
| Journal | See [section 7](#7-journal) |

"What broke and how I fixed it" matters most. Troubleshooting is at the heart of DevOps work, and those write-ups make great examples to talk about in job interviews.

### 7. Journal

One file per study day: `journal/YYYY/YYYY-MM-DD.md`.

```markdown
---
phase: 01-linux
hours: 2.5
hands_on: 1.5
---

## What I did
- LFS101: file permissions chapter
- Lab: chmod and chown in my VM (labs/02-permissions)

## What I learned
- A folder needs "execute" permission before you can cd into it

## What confused me
- The difference between hard links and soft links

## Next time
- Finish the permissions lab, then start processes
```

**The numbers at the top** (called front matter):
- **`phase`:** which phase the time counts toward.
- **`hours`:** focused study time, rounded to the nearest quarter hour. Breaks to check my phone don't count. Noting start and end times makes this easy.
- **`hands_on`:** how much of that time was labs, exercises or the project. The retro divides this by `hours` to get my hands-on share.

**The write-up** (about 5 minutes):
- **What I did:** a record of the session.
- **What I learned:** one or two lines, written from memory.
- **What confused me:** things to look up or ask about.
- **Next time:** where to pick up. My next session starts by reading this.

**Tracking rules:**
- A study day is a file where `hours` is at least 0.5.
- If I study twice in one day, I add to the same file and update the numbers.
- Weeks run Monday to Sunday. Three or more study days keep my streak going.
- For a break week, I create a file dated any day that week:

```markdown
---
break: true
---
Work deadline this week. Back on Monday.
```

**My journal is public,** so I keep it about learning. Honest struggles are fine, but nothing about my employer or my private life.

### 8. Capstone project

**My learning tracker, grown into a web app.** It starts as my Bash `learn` script in Phase 1 and gets a new step in every phase from 4 to 12.

- **Its own repo,** created in Phase 4. I'll decide the name then.
- **This repo links to it,** and each phase's exit-challenge write-up stays here.

| Phase | Version | What I add |
|---|---|---|
| 1 Linux | — | The starting point: my Bash `learn` script |
| 4 Python | v0.4 | Rewrite it in Python. It reads my roadmap and journal from GitHub, calculates my stats, has tests (written with pytest), and shows everything on a one-page web dashboard |
| 5 AWS | v0.5 | Set it up by hand on an EC2 server. Add a daily job (Lambda) that saves a snapshot of my stats (S3 or RDS), with logs in CloudWatch |
| 6 Docker | v0.6 | Package it in a container and run it alongside a database for the snapshots, using Docker Compose |
| 7 CI/CD | v0.7 | A Jenkins pipeline that tests, builds and publishes it on every change. Plus a GitHub Action that uses it to refresh this repo's README |
| 8 Kubernetes | v0.8 | Run it on my local cluster. The daily snapshot becomes a CronJob, passwords move into Secrets, and it's packaged as a Helm chart |
| 9 Nginx | v0.9 | Put Nginx in front of it: HTTPS, load balancing across two copies, and a Redis cache to stay under GitHub's request limits |
| 10 Ansible | v0.10 | One playbook that turns a blank VM into a running copy |
| 11 Terraform | v0.11 | Build its whole AWS environment as code, then configure it with my Ansible playbook |
| 12 Monitoring | v1.0 | Prometheus and Grafana dashboards for the app *and* my study hours, an alert when my weekly streak is at risk, and logs in ELK |

**Why this app:**
- I already know what it should do, so my effort goes into the DevOps side.
- Every step has a real reason. The cache exists because GitHub limits requests; the alert exists because I want to protect my streak.
- It tells a story: "I built an app to track my DevOps learning, and deploying it *was* the learning."

### 9. The learn script

| Command | What it does |
|---|---|
| `learn help` | Lists the commands |
| `learn log` | Creates today's journal entry from the template, with the phase filled in, and opens it in nano. If today's entry already exists, it just opens it |
| `learn start 02-networking` | Creates the phase folder with `notes/`, `labs/`, a README and a retro, all from the templates |
| `learn break "Work deadline"` | Creates this week's break file |
| `learn status` | Shows topics done, topics to revisit, hours compared with the budget, and my hands-on share |

What `learn status` could show:

```
$ learn status
Phase 01-linux
  Topics    4 of 6 done (1 to revisit)
  Hours     41.5 of 63
  Hands-on  58%

All phases
  Topics    8 of 82 done
  Hours     46.5 total over 17 study days
```

**When I build it:**
- **Roughly the first 4 weeks:** I track by hand. I copy the journal template with `cp` and tick boxes in my editor.
- **During Phase 1's shell scripting chapters:** I build it in stages, in the order of the table above. Each stage is one lab and one commit. Getting all of it working together is Phase 1's exit challenge.
- **PATH:** I'll add `scripts/` to my PATH, so I can type `learn status` instead of `./scripts/learn status`.

**What it leaves out on purpose:**
- **No command for ticking topics.** I tick them by hand in this file, which keeps me looking at my roadmap.
- **No `save` command yet.** I commit and push by hand until git feels natural. After Phase 3 I can add `learn save "message"` if I want. It would run add, commit and push, and print each command so nothing is hidden.

**What waits for the Python version (Phase 4, part of the capstone):**
- My weekly streak (including break weeks), my longest streak, and a projected finish date. These need date calculations, which are much easier in Python than in Bash.
- `learn readme`, which refreshes the progress section of my README.
- If I'm enjoying Bash, the streak makes a good stretch goal.

**Two rules for the script:**
1. **It never overwrites or deletes anything.** It only reads files or creates new ones, so running `learn log` twice just opens the same entry. An action that gives the same result however many times you run it is called *idempotent*.
2. **It works out my current phase from the highest-numbered folder in `phases/`**, so there's no separate setting that could fall out of step.

I'm starting with these commands while I'm still a beginner, and I'll review them when I reach Phase 1's scripting chapters.

### 10. Git habits

**Four words I'll use every day:**
- **Commit:** a saved snapshot of my files, with a short message saying what changed.
- **Push:** uploading my commits to GitHub, so they're backed up and visible.
- **Branch:** a separate copy of my work where I can try things out, then combine them back in.
- **Tag:** a label on one commit, like a bookmark.

**The habits:**

| Habit | Why |
|---|---|
| Commit and push at the end of every session. More often is fine | My work is backed up, and my GitHub profile shows steady activity |
| Run `git status` before every commit | It lists exactly what I'm about to save, so it's my last chance to catch a password or a file that shouldn't be public |
| Write messages as `area: what changed`, phrased like an instruction | My history reads like a logbook |
| Stay on the main branch in this repo | Branches add extra steps and no benefit to a notes repo only I work on |
| If a command contains `--force` or `reset --hard`, stop and check first | These can erase work permanently |

Example messages:

```
journal: 2026-11-20
linux: add notes on file permissions
linux: add permissions lab
roadmap: tick permissions
scripts: add learn log
```

At first, one commit per session is fine, even if I did several different things.

**How the habits grow:**
- **Phases 0–2:** just the habits above.
- **Phase 3 (Git):** I learn branches, pull requests and tags properly, and start tagging finished phases.
- **Phase 4 onwards, in the capstone repo:** every change gets its own branch and goes through a pull request, the way teams work. Commit messages switch to the standard team format (`feat:`, `fix:`, `docs:`).

I'll review these habits when I reach Phase 3.

### 11. Revisit when I get there

| What | When |
|---|---|
| The `learn` script commands | When I start Phase 1's scripting chapters |
| Spending | At the month-4 checkpoint |
| Git habits | In Phase 3 |
| AWS free-plan details | At the start of Phase 5 |
| More laptop memory | Around Phase 8 (month 10) |
| Resources for Phases 5–12 | At the start of each phase |

---

## Part 2: The phases

Tick topics here and nowhere else.
- "(revisit)" after a ticked topic means it's still shaky.
- "(optional)" means the topic never blocks finishing a phase.

### Phase 0: Setup · budget 6 h

The steps:
1. Get around the terminal: `pwd`, `ls`, `cd`, `mkdir`.
2. Start the repo:
   - Run `git init`.
   - Set my full name and GitHub's private email for this repo.
   - Create `.gitignore` with the roadmap PDF in it.
   - List my private local files in `.git/info/exclude`, so they're never committed.
3. Create the templates, the README and the Phase 0 README.
4. Make my first commit and write my first journal entry.
5. Connect to GitHub:
   - Create an SSH key and add it to GitHub.
   - Create the empty repo on the GitHub website.
   - Push.
6. Write a short retro.

`ROADMAP.md` was written on 2026-11-09, before Phase 0 started.

- [✓] Terminal basics (pwd, ls, cd, mkdir, cp)
- [✓] Markdown basics (headings, lists, links, checkboxes)
- [✓] First git commands (init, status, add, commit, push)
- [✓] SSH keys and connecting to GitHub
- [✓] **Exit challenge:** first push to GitHub
- [✓] **Retro** written

### Phase 1: Linux · budget 63 h

- [ ] Basic Linux commands (ls, cp, mv, rm, etc.)
- [ ] File system hierarchy (/, /home, /etc, /var, etc.)
- [ ] Permissions and ownership (chmod, chown)
- [ ] Processes and signals (ps, top, kill)
- [ ] Package management (apt, yum)
- [ ] Shell scripting basics (variables, loops, conditionals, functions)
- [ ] **Exit challenge:** first version of my `learn` script, in Bash
- [ ] **Retro** written

### Phase 2: Networking · budget 42 h

- [ ] OSI and TCP/IP models
- [ ] IP addressing and subnetting (IPv4, IPv6)
- [ ] DNS and DHCP
- [ ] Network protocols (HTTP, HTTPS, FTP, SSH, etc.)
- [ ] Firewalls and security groups (iptables, UFW)
- [ ] Basic network troubleshooting (ping, traceroute, netstat)
- [ ] **Exit challenge:** picked at the start of the phase (for example, map and document my home network)
- [ ] **Retro** written

### Phase 3: Git · budget 42 h

- [ ] Git basics and commands (clone, commit, push, pull)
- [ ] Branching and merging
- [ ] Working with remote repositories (GitHub, GitLab)
- [ ] Pull requests and code reviews
- [ ] Git workflows (Git Flow, GitHub Flow)
- [ ] Resolving merge conflicts
- [ ] **Exit challenge:** picked at the start of the phase (for example, a full branch, pull request and merge-conflict cycle)
- [ ] **Retro** written

### Phase 4: Python · budget 126 h

- [ ] Python syntax and data structures (lists, dictionaries, sets, tuples)
- [ ] Modules and packages (importing and using libraries)
- [ ] Writing and executing Python scripts
- [ ] File handling (reading from and writing to files)
- [ ] Error handling (try, except)
- [ ] Automation scripts (subprocess, os, sys)
- [ ] Basic web scraping (requests, BeautifulSoup)
- [ ] **Exit challenge:** capstone v0.4, the Python tracker with a one-page web dashboard, in its own repo
- [ ] **Retro** written

### Phase 5: Cloud (AWS) · budget 126 h

- [ ] EC2 (virtual servers)
- [ ] S3 (object storage)
- [ ] IAM (Identity and Access Management)
- [ ] VPC (Virtual Private Cloud)
- [ ] RDS (Relational Database Service)
- [ ] Lambda (serverless compute)
- [ ] CloudWatch (monitoring and logging)
- [ ] Azure: VMs, storage accounts, networking (VNets, NSGs), Azure DevOps pipelines (optional)
- [ ] GCP: Compute Engine, Cloud Storage, networking (VPCs, firewalls), Cloud Monitoring and Logging, formerly Stackdriver (optional)
- [ ] **Exit challenge:** capstone v0.5, running on EC2 with a daily Lambda snapshot and CloudWatch logs
- [ ] **Retro** written

### Phase 6: Containers (Docker) · budget 84 h

- [ ] Docker installation and setup
- [ ] Creating and managing Docker images
- [ ] Running containers
- [ ] Dockerfile basics (writing Dockerfiles)
- [ ] Docker Compose (defining and running multi-container applications)
- [ ] Container networking
- [ ] Data persistence (volumes and bind mounts)
- [ ] **Exit challenge:** capstone v0.6, in a container with a database, using Docker Compose
- [ ] **Retro** written

### Phase 7: CI/CD (Jenkins) · budget 84 h

- [ ] CI/CD concepts and principles
- [ ] Jenkins installation and setup
- [ ] Creating and configuring Jenkins pipelines
- [ ] Jenkinsfile basics (declarative and scripted syntax)
- [ ] Automated testing (unit tests, integration tests)
- [ ] Build automation
- [ ] Deployment automation
- [ ] Monitoring and reporting
- [ ] **Exit challenge:** capstone v0.7, a Jenkins pipeline plus a GitHub Action that refreshes this repo's README
- [ ] **Retro** written

### Phase 8: Container orchestration (Kubernetes) · budget 126 h

- [ ] Kubernetes architecture (control plane, also called master, and worker nodes)
- [ ] Kubernetes components (pods, services, deployments)
- [ ] Managing resources (namespaces, ConfigMaps, Secrets)
- [ ] Scaling applications (Horizontal Pod Autoscaler)
- [ ] Helm basics (charts, repositories, releases)
- [ ] Kubernetes networking (services, ingress)
- [ ] Security in Kubernetes (RBAC, network policies)
- [ ] **Exit challenge:** capstone v0.8, on my local cluster with a CronJob, Secrets and a Helm chart
- [ ] **Retro** written

### Phase 9: Networking and infrastructure services (Nginx) · budget 84 h

- [ ] Setting up and configuring Nginx as a reverse proxy
- [ ] Setting up forward proxies
- [ ] Implementing caching with Redis or Varnish
- [ ] Configuring firewalls and security groups (iptables, UFW)
- [ ] Load balancing with HAProxy or AWS ELB
- [ ] SSL/TLS configuration for secure communications
- [ ] Troubleshooting network issues
- [ ] **Exit challenge:** capstone v0.9, behind Nginx with HTTPS, load balancing and a Redis cache
- [ ] **Retro** written

### Phase 10: Configuration management (Ansible) · budget 84 h

- [ ] Writing Ansible playbooks
- [ ] Roles and modules
- [ ] Managing variables and templates
- [ ] Puppet basics: manifests, modules, classes (optional)
- [ ] Chef basics: cookbooks, recipes, resources (optional)
- [ ] **Exit challenge:** capstone v0.10, a playbook that turns a blank VM into a running copy
- [ ] **Retro** written

### Phase 11: Infrastructure as Code (Terraform) · budget 84 h

- [ ] Terraform basics (installation, providers, resources)
- [ ] Writing Terraform configuration files
- [ ] Managing Terraform state
- [ ] Using Terraform modules
- [ ] Advanced concepts (workspaces, remote state)
- [ ] AWS CloudFormation: stacks and templates, writing templates, managing the infrastructure lifecycle (optional)
- [ ] **Exit challenge:** capstone v0.11, its AWS environment built with Terraform and configured with Ansible
- [ ] **Retro** written

### Phase 12: Monitoring and logging (Prometheus) · budget 84 h

- [ ] Prometheus basics (installation, metrics, exporters)
- [ ] Prometheus alerting
- [ ] PromQL (Prometheus Query Language)
- [ ] Grafana basics (installation, dashboards)
- [ ] Grafana visualizations (integration with Prometheus, creating visualizations)
- [ ] ELK basics (installation, data collection)
- [ ] Elasticsearch (indexing, searching)
- [ ] Logstash (data pipeline, filters)
- [ ] Kibana (visualizations, dashboards)
- [ ] **Exit challenge:** capstone v1.0, with Prometheus, Grafana, the streak alert and logs in ELK
- [ ] **Retro** written

---

> "Becoming a DevOps engineer is a journey. Be patient with yourself and stay persistent, even when things get tough." — Mosh Hamedani
