# kkmnow-data

This is the data repo for KKMNOW. Note that this contains highly processed data intended for use by [`kkmnow-back`](https://github.com/MoH-Malaysia/kkmnow-back) rather than for members of the public to download and play with. Consequently, although this repo is open, we do not accept contributions (but are happy to fix any issues). 

Note that you do not need to clone the repo locally in order to serve your API - the backend code pulls directly from the latest version of this repo.

---

## Why do we use parquet files?

For two reasons. First, Parquet files are compressed to a much smaller size (usually ~10x smaller than the corresponding CSV for our datasets), making them faster to read and cheaper to store. Second, Parquet files have an embedded schema, which means that the data types are clearly defined.

We **do not** intend for these files to be what the community at large leverages on (although you may if you wish). They only contain precisely what is needed for the site's API. If you want to work with the full datasets in (for example) CSV format in Excel, you should go to one of the open-data repos below and take the files you need - they are all maintained with the complete datasets underlying what is displayed on the site.

## Download to work locally

In a git-supported terminal:

```bash
git clone git@github.com:moh-malaysia/kkmnow-data.git
```

## Open Data repos maintained by MoH Malaysia
- [COVID-19](https://github.com/MoH-Malaysia/covid19-public/)
- [Blood donation](https://github.com/MoH-Malaysia/data-darah-public)
- [Organ donation](https://github.com/MoH-Malaysia/data-organ-public)
- [PeKa B40 screening](https://github.com/MoH-Malaysia/data-peka40-public)
- [Healthcare resources](https://github.com/MoH-Malaysia/data-resources-public)

## Larger datasets made available via Google Cloud
- [Anonymised individual-level COVID-19 cases](https://storage.googleapis.com/moh-malaysia-covid19/linelist_cases.parquet)
- [Anonymised individual-level COVID-19 deaths](https://storage.googleapis.com/moh-malaysia-covid19/linelist_deaths.parquet)

