# Changelog

Format based on [Keep a Changelog](https://keepachangelog.com/).

## [0.3.0] - 2026-09-12

### Changed
- StigForge export refresh for `debian12_cis` at `0.3.0`.

### Verified (OpenSCAP)

- **`cis-l1`** — score **99.26%** (floor 90.0%) · gate **PASS** · evidence `20260912T140647Z`
  - Remaining counted failures: `use_pam_wheel_group_for_su`
- **`cis-l2`** — score **99.28%** (floor 90.0%) · gate **PASS** · evidence `20260912T140842Z`
  - Remaining counted failures: `use_pam_wheel_group_for_su`
- **`cis-ws-l1`** — score **98.5%** (floor 90.0%) · gate **PASS** · evidence `20260912T141003Z`
  - Remaining counted failures: `file_permissions_ungroupowned, use_pam_wheel_group_for_su`
- **`cis-ws-l2`** — score **98.54%** (floor 90.0%) · gate **PASS** · evidence `20260912T141209Z`
  - Remaining counted failures: `file_permissions_ungroupowned, use_pam_wheel_group_for_su`

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/34693316989
- Factory commit: `562a1f7c1a8e19235ee26e972174d1be6c88998c`

## [0.2.4] - 2026-07-30

### Changed
- StigForge export refresh for `debian12_cis` at `0.2.4`.

### Verified (OpenSCAP)

- **`cis-l1`** — score **94.92%** (floor 90.0%) · gate **PASS** · evidence `20260729T223616Z`
  - Remaining counted failures: `accounts_password_pam_pwhistory_remember, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled, accounts_passwords_pam_faillock_unlock_time, ensure_pam_wheel_group_empty, package_pam_modules_installed, package_pam_runtime_installed, set_password_hashing_algorithm_logindefs`
  - _(+1 more — see `score.json`)_
- **`cis-l2`** — score **94.51%** (floor 90.0%) · gate **PASS** · evidence `20260729T223833Z`
  - Remaining counted failures: `accounts_password_pam_pwhistory_remember, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled, accounts_passwords_pam_faillock_root_unlock_time, accounts_passwords_pam_faillock_unlock_time, ensure_pam_wheel_group_empty, package_pam_modules_installed, package_pam_runtime_installed`
  - _(+2 more — see `score.json`)_

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30496236357
- Factory commit: `7f7cafc85a392bf2a7eb04f1b979185dbcdf5530`

## [0.2.4-private-review] - 2026-07-29

### Changed
- StigForge export refresh for `debian12_cis` at `0.2.4-private-review`.

### Verified (OpenSCAP)

- **`cis-l1`** — score **92.09%** (floor 90.0%) · gate **PASS** · evidence `20260729T100609Z`
  - Remaining counted failures: `account_disable_post_pw_expiration, accounts_password_pam_pwhistory_enabled, accounts_password_pam_pwhistory_enforce_root, accounts_password_pam_pwhistory_remember, accounts_password_pam_pwhistory_use_authtok, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled, accounts_passwords_pam_faillock_unlock_time`
  - _(+6 more — see `score.json`)_
- **`cis-l2`** — score **91.21%** (floor 90.0%) · gate **PASS** · evidence `20260729T100830Z`
  - Remaining counted failures: `account_disable_post_pw_expiration, accounts_minimum_age_login_defs, accounts_password_pam_pwhistory_enabled, accounts_password_pam_pwhistory_enforce_root, accounts_password_pam_pwhistory_remember, accounts_password_pam_pwhistory_use_authtok, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled`
  - _(+8 more — see `score.json`)_

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30440754045
- Factory commit: `c481b47d629f5bc2357a86a933aa6f94f5245fce`

## [0.2.3-private-review] - 2026-07-29

### Added
- Initial StigForge export of matrix role `debian12_cis`.
- OpenSCAP verify evidence bundles per profile under `compliance/releases/`.

### Verified (OpenSCAP)

- **`cis-l1`** — score **92.09%** (floor 90.0%) · gate **PASS** · evidence `20260729T082623Z`
  - Remaining counted failures: `account_disable_post_pw_expiration, accounts_password_pam_pwhistory_enabled, accounts_password_pam_pwhistory_enforce_root, accounts_password_pam_pwhistory_remember, accounts_password_pam_pwhistory_use_authtok, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled, accounts_passwords_pam_faillock_unlock_time`
  - _(+6 more — see `score.json`)_
- **`cis-l2`** — score **91.21%** (floor 90.0%) · gate **PASS** · evidence `20260729T082846Z`
  - Remaining counted failures: `account_disable_post_pw_expiration, accounts_minimum_age_login_defs, accounts_password_pam_pwhistory_enabled, accounts_password_pam_pwhistory_enforce_root, accounts_password_pam_pwhistory_remember, accounts_password_pam_pwhistory_use_authtok, accounts_passwords_pam_faillock_deny, accounts_passwords_pam_faillock_enabled`
  - _(+8 more — see `score.json`)_

### Provenance

- Factory pipeline: https://github.com/stigready/stigforge/actions/runs/30435216810
- Factory commit: `e8e323a3af3258bee63ebc1a873ba26c0cc12049`

## [0.2.1-private-review] - 2026-07-28

### Changed
- Galaxy-style layout: Ansible role at repository root; evidence under `compliance/`.
- Private review tag `v0.2.1-private-review` (supersedes nested `roles/<role>/` export).

## [0.2.0-private-review] - 2026-07-26

### Added
- First private StigForge export to `stigready/*` (factory review; nested role path).
