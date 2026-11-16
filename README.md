<!--
Developer: Hamdy Abou El Anein
Contact: info@daylightlinux.ch
SPDX-License-Identifier: GPL-3.0-only
-->

<div align="center">

# Hamdy Abou El Anein

### Senior Linux Systems Engineer · Open-Source Developer · Technical Educator

**Building reliable Linux systems, practical automation, and open-source tools.**

Based in Switzerland · 15+ years in Linux and systems engineering

[![Website](https://img.shields.io/badge/Daylight_Linux-Explore-177e65?style=for-the-badge)](https://daylightlinux.ch/)
[![Training](https://img.shields.io/badge/Software--Coders-Training-225c8c?style=for-the-badge)](https://software-coders.ch/)
[![Astronomy](https://img.shields.io/badge/Astrometry-Explore-6959a6?style=for-the-badge)](https://astrometry.ch/)
[![Email](https://img.shields.io/badge/Contact-Email-334155?style=for-the-badge)](mailto:info@daylightlinux.ch)

</div>

---

## Engineering expertise for recruiters

I bring **15+ years of professional experience** operating and troubleshooting Linux systems in enterprise environments, alongside hands-on open-source development.

| Area | Relevant experience |
| --- | --- |
| **Linux & infrastructure** | Debian, Ubuntu, RHEL, SLES, enterprise operations, virtualization, system hardening and incident investigation |
| **Automation & DevOps** | Python, Bash, Ansible, Terraform, GitLab CI, GitHub Actions and reproducible operational workflows |
| **Containers & platforms** | Docker, Kubernetes, Helm, K3s and Linux service integration |
| **Observability & security** | Splunk, rsyslog, Prometheus, Grafana, TLS, networking and evidence-based diagnostics |
| **Software engineering** | Rust and Python CLI tools, testing, packaging, documentation and open-source maintenance |

### Selected engineering work

- **[WhyDown](https://github.com/hamdyaea/WhyDown)** — read-only Linux diagnostics with evidence from system state and journals; Rust CLI, terminal interface and Qt desktop GUI.
- **[ShellTrace](https://github.com/hamdyaea/ShellTrace)** — Rust-based command-behaviour investigation using filesystem comparisons and syscall tracing, with explicitly documented isolation limits.
- **[Daylight GNU/Linux](https://github.com/hamdyaea/Daylight-GNU-Linux)** — Linux distribution engineering for Raspberry Pi OS and Debian, including APT packaging, installation workflows and desktop integration.
- **[Syracuse](https://github.com/hamdyaea/Syracuse)** — Python and Rust numerical research tooling, focused on efficient computation and reproducible exploration.

**Professional focus:** Senior Linux Engineering · DevOps / Platform Engineering · Site Reliability · Linux Security / DevSecOps.

These repositories demonstrate personal open-source engineering work; enterprise experience is summarized separately above.

---

## About me

I'm a Switzerland-based **Senior Linux Systems Engineer** with over 15 years of experience in Linux administration, infrastructure operations, troubleshooting, and automation.

My work sits at the intersection of **Linux engineering, Python, Bash, Rust, open-source software, and cybersecurity**. I enjoy turning complex technical challenges into lean, maintainable systems, from Raspberry Pi distributions to monitoring and developer tooling.

I hold a **Swiss Federal Professional Certificate in ICT (Systems and Networks)**, alongside **LPIC-1 and LPIC-2** qualifications. I also teach and mentor people learning Linux and programming, and write technical books.

<!-- kernel-contributions:start -->
## Linux kernel contributions

I, **Hamdy Abou El Anein**, contribute patches to the Linux kernel's development scripts. These changes focus on preserving diagnostic text, checking Kconfig symbols, and resolving Git references.

| Contribution | Purpose | Documented milestone |
| :--- | :--- | :--- |
| [kbuild: detect module name collisions between '-' and '_'](https://git.kernel.org/kbuild/c/bc348949) | Normalize module basenames before duplicate checks because Kbuild and the module loader treat hyphens and underscores as equivalent. | Applied by Nicolas Schier to [kbuild/linux.git](https://git.kernel.org/pub/scm/linux/kernel/git/masahiroy/linux-kbuild.git), branch `kbuild-next-unstable`, with a `Fixes:` tag added. The normalization is present in [modules-check.sh in the linux-next tag `next-20261111`](https://kernel.googlesource.com/pub/scm/linux/kernel/git/next/linux-next/+/aaa2f954c21b205a0bcd0961e5b2be4e82e58455/scripts/modules-check.sh#16). On 8 November 2026, [Sasha Levin reported ARM allmodconfig failures](https://lore.kernel.org/all/20261108225808.1809266-1-sashal@kernel.org/) exposing two pre-existing module-name collisions. On 9 November, [Nathan Chancellor announced two rename patches](https://lore.kernel.org/all/20261109064930.GA829325@ax162/). For the apm-power collision, Dmitry Torokhov proposed removing the obsolete input driver. On 10 November, [Nicolas Schier confirmed applying that change](https://lore.kernel.org/all/179431695096.1779189.14927773083935970456.b4-ty@b4/) to `kbuild-next-unstable` ([commit 7f705c0a](https://git.kernel.org/kbuild/c/7f705c0a)). For the second collision, the [ARM Makefile in `next-20261112`](https://kernel.googlesource.com/pub/scm/linux/kernel/git/next/linux-next/+/6d582d78fad9d828e575ca0cdcff8ea47a77220b/arch/arm/probes/kprobes/Makefile#6) uses Nathan Chancellor’s proposed name `test-kprobes-arm`, distinct from the generic `test_kprobes` module. |
| [decode_stacktrace: preserve input while reading lines](https://lore.kernel.org/all/20261103164203.129660-1-info@daylightlinux.ch/) | Preserve whitespace, backslashes and a final line without a newline. | [Andrew Morton announced its addition to -mm / mm-nonmm-unstable](https://lore.kernel.org/mm-commits/20261103204853.F0FFB1F000C1@smtp.kernel.org/) on 3 November 2026, with Sasha Levin's Acked-by. The updated read loop is present in [decode_stacktrace.sh in the linux-next tag `next-20261111`](https://kernel.googlesource.com/pub/scm/linux/kernel/git/next/linux-next/+/aaa2f954c21b205a0bcd0961e5b2be4e82e58455/scripts/decode_stacktrace.sh#349). |
| [checkkconfigsymbols: check the complete numeric token](https://lore.kernel.org/all/20261103164203.129644-1-info@daylightlinux.ch/) | Keep names such as 64BIT_MISSING visible to the undefined-symbol check. | Reviewed-by from Nathan Chancellor received on 6 November 2026. |
| [git-resolve: check the Git object type, v2](https://lore.kernel.org/all/20261104054332.10869-1-info@daylightlinux.ch/) | Verify that an abbreviated object ID identifies a commit before using it in a Fixes reference. | Version 2 submitted on 4 November 2026 following review. |

Updated 13 November 2026. **Review approval and inclusion in a maintainer branch are distinct from a mainline merge; no mainline merge is claimed here.** AI assistance is disclosed in the patch submissions.

[Hamdy Abou El Anein's patches and review discussions on Lore](https://lore.kernel.org/all/?q=Hamdy%20Abou%20El%20Anein) · [Contribution details and status in French](https://software-coders.ch/hamdy-abou-el-anein/#contributions-linux)
<!-- kernel-contributions:end -->

## Selected projects: technical portfolio

| Project | Engineering evidence |
| :--- | :--- |
| **[Daylight GNU/Linux](https://github.com/hamdyaea/Daylight-GNU-Linux)** · [Website](https://daylightlinux.ch/) | Linux distribution integration, Debian/APT packaging, release workflows and Raspberry Pi desktop tooling. |
| **[WhyDown](https://github.com/hamdyaea/WhyDown)** | Rust-based, read-only Linux diagnostics with CLI, TUI and Qt6 GUI, evidence-driven findings and distribution packaging. |
| **[ShellTrace](https://github.com/hamdyaea/ShellTrace)** | Rust systems tooling using filesystem snapshots and `strace` to investigate command behaviour, with documented security limits. |
| **[Syracuse](https://github.com/hamdyaea/Syracuse)** | Parallel Rust computation, SQLite persistence, checkpointing, correctness tests and Python visualization. |
| **[Linux automation with Ansible](https://github.com/hamdyaea/Manjaro-Linux-ansible)** | Linux provisioning and automation workflows. |
| **[Coreutils in Rust](https://github.com/hamdyaea/coreutils-rust)** | Rust exploration of familiar Unix command-line utilities. |

Other interests include [astronomy software](https://github.com/hamdyaea/SolarSystemPercentage) and [technical education](https://software-coders.ch/).

## Engineering focus

| Systems & infrastructure | Development & automation | Security & operations |
| :--- | :--- | :--- |
| Linux · Debian · RHEL · Raspberry Pi | Python · Bash · Rust · Go | Hardening · Monitoring · Logging |
| Docker · Systemd · Networking | Git · Ansible · CLI tooling | Troubleshooting · Observability · SIEM |

I care about **performance, simplicity, reproducibility, security, and maintainability**. Good infrastructure should be understandable, observable, and efficient.

## Teaching & writing

I help learners and professionals build real-world technical skills through hands-on, individual training.

**Topics:** Linux administration, Python programming, shell scripting, Go, Rust, and cybersecurity.

- [Explore my training courses](https://software-coders.ch/)
- [Browse my published books](https://www.amazon.fr/stores/author/B0BM89T88X)

## Get in touch

I'm interested in meaningful conversations about **Linux engineering, infrastructure automation, open source, and technical collaboration**.

**Email:** [info@daylightlinux.ch](mailto:info@daylightlinux.ch)
**Projects:** [Daylight Linux](https://daylightlinux.ch/) · [Astrometry](https://astrometry.ch/) · [Software-Coders](https://software-coders.ch/)

---

<div align="center">
  <sub>Open source, practical engineering, and a lifelong curiosity for how systems work.</sub>
</div>
