# DANDI Validations (Records)

The records of [DANDI Validations](https://github.com/dandi-validations/dandi-validations), a table of every validation capsule of every Dandiset repository of the [dandi-validations](https://github.com/dandi-validations) organization.

- `records/capsules.tsv` has one row per Dandiset and `dandi-validation` image.
  Each row gives the capsule's status (pending, stalled, failed or successful), its inputs, the image's digest, the run's resource usage, and its counts of results by severity.
- `records/capsules.json` describes those columns, BIDS-style.

The **Collect records** workflow rebuilds them every 6 hours, and on demand, with `dandi-validations collect` from the `main` branch of [dandi-validations/dandi-validations](https://github.com/dandi-validations/dandi-validations).
The records are kept here, apart from that code, so that their commits stay out of its history.
