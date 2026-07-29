# debian12_cis — Ansible role (debian12-cis)

**Ansible hardening role** for **Debian 12** (CIS Benchmark). Suitable for playbooks, Packer/Ansible provisioners, and golden-image pipelines. Search keywords: `ansible`, `ansible-role`, `bookworm`, `cis`, `cis-benchmark`, `cis-hardening`, `compliance`, `debian`, `debian12`, `devsecops`, `hardening`, `infrastructure`, `openscap`, `security`.

StigForge-exported Ansible role **`debian12_cis`** · release **`0.2.3-private-review`**.
Matrix cell status: **`green`**.

## Install (Ansible Galaxy)

This repository root **is** the Ansible role (Galaxy-style layout). OpenSCAP evidence
lives under `compliance/` and is not loaded when the role runs.

From **Ansible Galaxy** (after import; namespace `stigready`):

```bash
ansible-galaxy role install stigready.debian12_cis,0.2.3-private-review
```

From **GitHub** (public):

```yaml
# requirements.yml
roles:
  - src: https://github.com/stigready/debian12-cis
    scm: git
    version: v0.2.3-private-review   # or an immutable commit SHA
    name: debian12_cis
```

```bash
ansible-galaxy role install -r requirements.yml -p ./roles
ansible-playbook -i inventory site.yml   # role: debian12_cis
```

## Verification status (this release)

Evidence was produced by **docker verify + OpenSCAP** on the factory CI run cited below.

| Profile | Score | Floor | Gate | Ansible | Evidence tested (UTC) |
|---|---:|---:|---|---|---|
| `cis-l1` | **92.09%** ✓ | 90.0% | PASS ✓ | rc 0 | 20260729T082623Z |
| `cis-l2` | **91.21%** ✓ | 90.0% | PASS ✓ | rc 0 | 20260729T082846Z |

Full artifacts per profile: `compliance/releases/0.2.3-private-review/<profile>/` (`score.json`, `results.xml`, `report.html`, `evidence.json`, `evidence-report.html`, `poam.md`).

## Reports & review

- **[REVIEW.md](REVIEW.md)** — linked evidence index for product owner review
- **[reports/index.html](reports/index.html)** — HTML report index
- **[CHANGELOG.md](CHANGELOG.md)** — release notes and verify summary

## Verify the score (customer)

Re-run OpenSCAP in Docker and compare to this release's evidence:

```bash
make prove RELEASE=0.2.3-private-review
```

Or score your own `results.xml`: see **[compliance/README.md](compliance/README.md)**.

## License

- **[LICENSE](LICENSE)** (MIT) — StigForge export packaging
- **[NOTICE](NOTICE)** — ComplianceAsCode / BSD-3-Clause task body attribution

## Factory

- Monorepo: [stigready/stigforge](https://github.com/stigready/stigforge) @ `e8e323a3af3258bee63ebc1a873ba26c0cc12049`
- CI run: https://github.com/stigready/stigforge/actions/runs/30435216810
- Catalog: [https://stigready.com/#stigforge](https://stigready.com/#stigforge)

