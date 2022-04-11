# PUMA-descriptors

## Contact

For all questions and errata associated with PUMA Descriptors, please email cmurray@aei.org. 

## Source Datafiles

* _ACS 2015-19_: The five year aggregation of the American Community Survey for 2015 through 2019. Downloaded from [IPUMS USA](usa.ipums.org)
* _2020 population data_: [2020 Decennial Census](https://www.census.gov/programs-surveys/decennial-census/about/rdo/summary-files.html). The data were downloaded from [Social Explorer](socialexplorer.com).
* _Summary data by PUMA_: Downloaded from [Social Explorer](socialexplorer.com), which has a $100/month subscription fee. The data are also available without cost at [IPUMS NHGIS](www.nhgis.org).
* _Individual PUMA maps and their descriptive titles_: Accessed at [Census.gov/Census Reference Maps/2010 Census Public Use Microdata Area (PUMA) Reference Maps](census.gov/geographies/reference-mxaps/2010/geo/2010-PUMAs.html). These maps consist of a single PUMA showing towns and cities within the PUMA.
* _PUMA maps in national context_: Both Social Explorer and NHGIS use the PUMA as a geography for national maps, enabling comparison of PUMA borders and CBSA borders.
* _Google Maps_: [Google Maps](google.com/maps) was used to assess the relationship of the towns in a PUMA to nearby urban areas. 

## Nomenclature

* _Public Use Microdata Area (PUMA)_: In the words of the Census Bureau, PUMAs “are non-overlapping, statistical geographic areas that partition each state or equivalent entity into geographic areas containing no fewer than 100,000 people each.” Borders of the PUMAs are revised every ten years by an agency or commission in each state.
* _Core-Based Statistical Area (CBSA)_: The Census Bureau defines urban areas in terms of a core city and adjacent territory that has “a high degree of social and economic integration with the core as measured by commuting ties.” 
* _Metropolitan or Micropolitan Area (MSA)_: A metropolitan area has at least one urbanized area with a population of 50,000 or more. A micropolitan area has at least one urban cluster of at least 10,000 but fewer than 50,000 total population. The current configuration has 707 MSAs. A single CBSA may contain several MSAs. The record is 18, in the CBSA labeled “Los Angeles-Long Beach-Anaheim.” 
* _Principal City_: The Census Bureau assigns one Principal City to each MSA. The Principal City is supposed to represent the focal point for social and economic integration in the immediate area.  

## Codebook

The datafile is named [Puma_descriptors.csv](). It is in fixed comma-separated format with variable names in the first line. The file has 17 variables. The universe for the variables consists of the 2,351 PUMAs in the 50 states.

* **state**: Two-letter postal code for states. 
* **statefip**: FIPS numeric code for states. 
* **cbsa**: The Census Bureau’s official label of the CBSA of which the PUMA is a part. If a PUMA is not associated with any CBSA, _cbsa_ is coded “Not in a CBSA.”
* **cbsacity**: The largest Principal City in the CBSA associated with the PUMA. If a PUMA is not associated with any CBSA, _cbsacity_ is coded “Not in a CBSA.” 
* **cbsacitypop**: The 2020 population of _cbsacity_. 
* **cbsacode**: The Census Bureau’s official numerical code for the CBSA containing _cbsacity_.
* **metpop10**: The population-weighted geometric mean of the populations of the CBSA associated with the PUMA.
* **pumaname**: The Census Bureau’s descriptive label for the PUMA.
* **pumanum**: Numeric code for the PUMA, which may be the same across states. _state_ and _pumanum_ must be used in combination to uniquely identify a PUMA. 
* **pumapop**: The 2020 population of the PUMA.
* **pumacity**: Name of the most populous town or city located wholly or almost wholly within the boundaries of the PUMA. If that city contains more than one puma, _pumacity_ is the name of the of the part of the city covered by the PUMA.  
* **pumacitypop**: The 2020 total population of _pumacity_. 
* **geodensity**: Population-weighted geometric mean of census tract population densities in the PUMA.
* **simpledensity**: The PUMA’s population divided by the PUMA’s square miles of land area. 
* **princity**: The Census Bureau’s officially designated Principal City associated with the PUMA. If a PUMA is not associated with any Principal City, _princity_ is coded “No Principal City.” 
* **princitypop**: The 2020 population of _princity_. 
* **altmetro**: A categorical variable characterizing the PUMAs with the following codes
  1.	“Rural”: An agricultural or otherwise sparsely populated PUMA with a largest place of fewer than 20,000 people that is not contiguous with another place.
  2.	“Town”: PUMAs with a largest place of fewer than 50,000 people that is not contiguous with another place.
  3.	“Small City”: PUMAs with a largest place consisting of a town of 50,000–149,999 people that is not contiguous with a larger place.
  4.	“Satellite”: PUMAs with a largest place that is a suburb or satellite to a larger place.
  5.	“Core City”: PUMAS with a city of 150,000 or more that is either the largest place in the CBSA or larger than any other contiguous place.

See [variable_details]() for a description of the variables, their coding, and their uses.
