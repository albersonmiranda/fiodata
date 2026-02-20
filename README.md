
<!-- README.md is generated from README.Rmd. Please edit that file -->

# fiodata

<!-- badges: start -->

[![R-CMD-check](https://github.com/albersonmiranda/fiodata/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/albersonmiranda/fiodata/actions/workflows/R-CMD-check.yaml)
[![CRAN
status](https://www.r-pkg.org/badges/version/fiodata)](https://CRAN.R-project.org/package=fiodata)
<!-- badges: end -->

{fiodata} is a data-only package containing input-output matrices for R.
It serves as a companion to the
[{fio}](https://github.com/albersonmiranda/fio) package, providing the
necessary data for input-output analysis while keeping the main package
size manageable.

## Datasets

The package currently includes two major datasets provided by the Center
for Computational Studies in General Equilibrium (CECEG) at the Federal
University of Espírito Santo (UFES):

- `br_2020`: Brazilian input-output matrix for the year 2020, featuring
  51 sectors.
- `world_2000`: World input-output matrix for the year 2000, covering 26
  countries and 23 sectors.

Both datasets are provided as R6 objects, allowing for easy access to
various components such as intermediate transactions, total production,
final demand, and more.

## Installation

You can install {fiodata} from CRAN with:

``` r
install.packages("fiodata")
```

## Example

Here is how you can load the data and explore its structure:

``` r
library(fiodata)

# Accessing the Brazilian 2020 matrix
br_2020
#> <iom>
#>   Public:
#>     add: function (matrix_name, matrix) 
#>     allocation_coefficients_matrix: NULL
#>     clone: function (deep = FALSE) 
#>     close_model: function (sectors) 
#>     compute_allocation_coeff: function () 
#>     compute_field_influence: function (epsilon) 
#>     compute_ghosh_inverse: function () 
#>     compute_hypothetical_extraction: function (matrix = "ghosh") 
#>     compute_key_sectors: function (matrix = "leontief") 
#>     compute_leontief_inverse: function () 
#>     compute_multiplier_employment: function () 
#>     compute_multiplier_output: function () 
#>     compute_multiplier_taxes: function () 
#>     compute_multiplier_wages: function () 
#>     compute_tech_coeff: function () 
#>     exports: 211701.585303601 9020.59508776331 90378.1074784573 11930 ...
#>     field_influence: NULL
#>     final_demand_matrix: 104928.069246247 46278.8893081818 2383.173159778 26.5479 ...
#>     final_demand_others: 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0  ...
#>     ghosh_inverse_matrix: NULL
#>     government_consumption: 136.113573476333 11.54067682294 0 0 0.0811353071766701 1 ...
#>     household_consumption: 104928.069246247 46278.8893081818 2383.173159778 26.5479 ...
#>     hypothetical_extraction: NULL
#>     id: br_2020
#>     imports: 49458.409248264 9116.64269499715 20717.254037798 8093.11 ...
#>     initialize: function (id, intermediate_transactions, total_production, household_consumption = NULL, 
#>     intermediate_transactions: 15729.0261267023 1642.35644867239 70.8986993216234 1.210 ...
#>     key_sectors: NULL
#>     leontief_inverse_matrix: NULL
#>     multiplier_employment: NULL
#>     multiplier_output: NULL
#>     multiplier_taxes: NULL
#>     multiplier_wages: NULL
#>     occupation: 6535675 6024724 51889 27455 132930 2360997 16862 584268  ...
#>     operating_income: 291773 88969 69857 79996 10107 67188 1869 1932 6915 3751 ...
#>     remove: function (matrix_name) 
#>     set_max_threads: function (max_threads) 
#>     taxes: 17488.6298516185 7403.92703803047 8173.68392418209 4301. ...
#>     technical_coefficients_matrix: NULL
#>     total_production: 574694 221067 238713 156454 46864 960384 17271 56657 639 ...
#>     update_final_demand_matrix: function () 
#>     update_value_added_matrix: function () 
#>     value_added_matrix: 49458.409248264 17488.6298516185 33816 291773 1.41464617 ...
#>     value_added_others: 1.41464617797737e-12 -1.31712349360491e-13 2261 -5534 3. ...
#>     wages: 33816 22610 19400 4870 6760 89172 1839 10391 16634 9448  ...
#>   Private:
#>     iom_elements: function ()

# Viewing the names of the available matrices within the object
names(br_2020)
#>  [1] "final_demand_matrix"             "compute_hypothetical_extraction"
#>  [3] "compute_allocation_coeff"        "compute_leontief_inverse"       
#>  [5] "compute_tech_coeff"              "leontief_inverse_matrix"        
#>  [7] "exports"                         "value_added_others"             
#>  [9] ".__enclos_env__"                 "id"                             
#> [11] "add"                             "household_consumption"          
#> [13] "occupation"                      "multiplier_output"              
#> [15] "update_final_demand_matrix"      "operating_income"               
#> [17] "taxes"                           "technical_coefficients_matrix"  
#> [19] "compute_multiplier_employment"   "compute_ghosh_inverse"          
#> [21] "compute_multiplier_taxes"        "compute_multiplier_output"      
#> [23] "multiplier_employment"           "imports"                        
#> [25] "value_added_matrix"              "hypothetical_extraction"        
#> [27] "wages"                           "field_influence"                
#> [29] "intermediate_transactions"       "update_value_added_matrix"      
#> [31] "compute_key_sectors"             "multiplier_taxes"               
#> [33] "key_sectors"                     "close_model"                    
#> [35] "clone"                           "initialize"                     
#> [37] "multiplier_wages"                "final_demand_others"            
#> [39] "ghosh_inverse_matrix"            "allocation_coefficients_matrix" 
#> [41] "remove"                          "government_consumption"         
#> [43] "total_production"                "compute_multiplier_wages"       
#> [45] "compute_field_influence"         "set_max_threads"
```

For performing analysis on these matrices, please refer to the
[{fio}](https://github.com/albersonmiranda/fio) package.
