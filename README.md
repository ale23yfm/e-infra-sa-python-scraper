[![Oportunitati SI Cariere](https://github.com/ale23yfm/e-infra-sa-python-scraper/actions/workflows/job-seeker-ro-spider.yml/badge.svg)](https://github.com/ale23yfm/e-infra-sa-python-scraper/actions/workflows/job-seeker-ro-spider.yml)
[![Automation Tests](https://github.com/ale23yfm/e-infra-sa-python-scraper/actions/workflows/automation-testing.yml/badge.svg)](https://github.com/ale23yfm/e-infra-sa-python-scraper/actions/workflows/automation-testing.yml)
[![Version](https://img.shields.io/badge/version-1.0.0-blue)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.12-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Website](https://img.shields.io/website?url=https%3A%2F%2Fpeviitor.ro&label=peviitor.ro)](https://peviitor.ro)
[![API](https://img.shields.io/website?url=https%3A%2F%2Fapi.peviitor.ro%2F&label=api.peviitor.ro)](https://api.peviitor.ro/)
[![GitHub Pages](https://img.shields.io/github/deployments/ale23yfm/e-infra-sa-python-scraper/github-pages?label=GitHub%20Pages)](https://ale23yfm.github.io/e-infra-sa-python-scraper/)

# job_seeker_ro_spider — E-INFRA S.A. Scraper

**job_seeker_ro_spider** — un scraper pentru job-urile E-INFRA S.A. din România. Extrage anunțurile publicate de departamentul [E-INFRA](https://electrogrup.applytojob.com/apply/jobs/?department=E-INFRA) pe board-ul applytojob al grupului și le publică în [peviitor.ro](https://peviitor.ro) prin API-ul Peviitor.

> **🌱 Derived scraper.** Acest repo este derivat din [electrogrup-sa-python-scraper](https://github.com/peviitor-scrapers/electrogrup-sa-python-scraper), implementarea de referință pentru scraper-ele Python din ecosistemul peviitor.ro.

## Overview

Proiectul automatizează colectarea zilnică a job-urilor E-INFRA din România, menținând board-ul peviitor.ro la zi cu cele mai recente oportunități de carieră.

## Features

- Extrage job-uri din board-ul applytojob al grupului E-INFRA (filtru `?department=E-INFRA`)
- Job-uri ANOFM suplimentare prin CIF
- Validează compania via ANAF (CUI, status activ/inactiv, adresă completă) cu fallback CUIScan
- **Cache ANAF** — nu lovește API-urile la fiecare scrape
- **Fallback la cache stale / config** dacă ANAF e indisponibil
- Cross-validează cu Peviitor API
- Șterge job-urile stale (de pe site dar nu și în Peviitor)
- Stochează în Peviitor API (job core + company core)
- Generează `docs/jobs.md` automat — accesibil pe GitHub Pages
- **Identitate companie într-un singur fișier** (`scraper/config/company.json`)
- GitHub Actions: scrape zilnic + testare automată (unit, integration, e2e, consistency)
- Se identifică prin User-Agent: `job_seeker_ro_spider`

## License

Copyright (c) 2026 Alexandra Ifrim

Licensed under the [MIT License](LICENSE).

## Managed By

This project is managed by [ASOCIATIA OPORTUNITATI SI CARIERE](https://oportunitatisicariere.ro) and used as a web scraper for the [peviitor.ro](https://peviitor.ro) job board project.

## Disclaimer

This scraper is designed for educational purposes and legitimate job data aggregation for the Romanian job market.
