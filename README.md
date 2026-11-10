# DANDI Validations (Records)

The records of [DANDI Validations](https://github.com/dandi-validations/dandi-validations), a table of every validation capsule of every Dandiset repository of the [dandi-validations](https://github.com/dandi-validations) organization.

The records of each `dandi-validation` image are on the branch named exactly by its tag, its validator version code (e.g. `d0.82.0-s0.14.0-n0.7.2-p4.2.0-h6.2.0-b3.0.2`):

- `capsules.tsv` has one row per Dandiset validated with that image.
  Each row gives the capsule's status (pending, stalled, failed or successful), its inputs, the image's digest, the run's resource usage, and its counts of results by severity.
- `capsules.json` describes those columns, BIDS-style.

`main` holds only the **Collect records** workflow, which updates the branches every 6 hours, and on demand.
It runs `dandi-validations collect --tags` from the `main` branch of [dandi-validations/dandi-validations](https://github.com/dandi-validations/dandi-validations).
The records are kept here, apart from that code, so that their commits stay out of its history.
