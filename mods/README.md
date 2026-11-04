# Personal mods

Patches applied on top of an upstream AndroidAPS tag by the "AAPS CI + mods" workflow
(`.github/workflows/aaps-ci-mods.yml`). The stock "AAPS CI" workflow ignores this folder.

- `dash-auto-deactivate-expired.patch`: Omnipod Dash. When the pod itself reports it has expired
  (status ALARM, fault 0x1C, pod's own counter >= 79 h), deactivate it and leave a silent
  notification. Setting "Auto-deactivate pod when it expires" (Dash > Advanced), off by default.
  Made against tag 4.0.0.

If a patch no longer applies to a new tag, the run fails before building. Refresh the patch
against the new tag and commit it here.
