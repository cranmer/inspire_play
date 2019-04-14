# IRIS-HEP publications using INSPIRE API

Prototyping a simple script to take a list of INSPIRE recid's, that hits the new INSPIRE labs API, and summarizes json and converts it to yaml for the IRIS-HEP webpage.

The recid are at the end of the INSPIRE labs URLS. two example 
  * https://labs.inspirehep.net/literature/1705857
  * https://labs.inspirehep.net/literature/1726790


See the notebook

## Usage

```
recid_unpublished = 1726790 #notpublished
recid_published = 1705857 #published
list_of_recids = [recid_published, recid_unpublished]
yaml.dump(summarize_records(list_of_recids),default_flow_style=False)
```

yields

```
publications:
- arxiv_eprint: '1811.12113'
  authors: Aaboud, Morad; Aad, Georges; Abbott, Brad; Abdinov, Ovsat; Abeloos, Baptiste;
    et. al.
  collaboration: ATLAS
  creation_date: '2018-11-30'
  doi: 10.1007/JHEP04(2019)046
  journal_title: JHEP
  journal_volume: '04'
  journal_year: 2019
  page_start: '046'
  recid: 1705857
  title: Measurements of fiducial and differential cross-sections of $t\bar{t}$ production
    with additional heavy-flavour jets in proton-proton collisions at $\sqrt{s}$ =
    13 TeV with the ATLAS detector
  url: https://arxiv.org/abs/1811.12113
- arxiv_eprint: '1903.10563'
  authors: Carleo, Giuseppe; Cirac, Ignacio; Cranmer, Kyle; Daudet, Laurent; Schuld,
    Maria; et. al.
  creation_date: '2019-03-27'
  recid: 1726790
  title: Machine learning and the physical sciences
  url: https://arxiv.org/abs/1903.10563
```