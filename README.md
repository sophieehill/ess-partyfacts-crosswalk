## Description

A crosswalk linking the party codes used for the vote intention variables in the [European Social Survey](https://www.europeansocialsurvey.org/) to their corresponding [Partyfacts](https://partyfacts.herokuapp.com/) ID. This allows you to merge in information on these parties from other datasets, such as [ParlGov](http://www.parlgov.org/), the [Manifesto Project](https://manifesto-project.wzb.eu/), and the [Chapel Hill experty surveys](https://www.chesdata.eu/).

This crosswalk is based on the original [ESS-Partyfacts dataset](https://github.com/hdigital/partyfactsdata/blob/master/import/ess/ess-partyfacts.csv), but has been updated to include the codes from ESS Round 8 (2016) and Round 9 (2018). 

If you find any errors in the crosswalk, please let me know via [email](mailto:sophie.eva.hill@gmail.com) or submit a PR.


## Codebook

| Variable            | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| `cntry`               | 2 letter country abbreviation                                                                   |
| `essround`            | ESS Round (1-9)                                                                                 |
| `variable`            | Name of the ESS vote intention variable (country-round specific)                                |
| `ess_id`              | ESS numeric party codes (country-round specific)                                                |
| `party`               | Party name                                                                                      |
| `partyfacts_id`       | Partyfacts numeric party code                                                                   |
| `partyfacts_name`     | Partyfacts abbreviated party name                                                               |
| `original_partyfacts` | Indicator for whether data comes from original Partyfacts dataset (=1) or was added by me (=0). |

## Notes

- Germany is not included here because it was not included in the original ESS-Partyfacts crosswalk. In principal it should be straightforward to add the mappings for German parties by hand, since the major parties do already have Partyfacts IDs. This is on my to-do list but if you've already done it please submit a PR and I'd be happy to credit you!
