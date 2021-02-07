# cps-data-cleaning
For extracting, converting, and merging the Current Population Survey data. Datasets include the basic monthly survey, the March supplements, and other supplemental modules.

Initial setup
Change the extension of the datasets from .dat to .raw
For basic monthly data, rename the datasets to cpsbxxxxxx, where the last 6 digits indicate year and month (e.g. cpsb201911, cpsb202005)

CPS statistical weights: all weight variables have an implied four decimals, though the decimal itself is not included. Hence, each weight must be divided by 10000 when used.
Weight variables:
Weight name	Definition 	Description 
PWFMWGT	Family weight	Used for estimates of families
PWORWGT	Outgoing rotation weight	Used only for the outgoing rotation groups (people who have been the sample for either their 4th or their 8th month)
PWSSWGT	Second stage weight	The final step before creating the composited final weight for major labor force statistics. Also used in creating other weights, including the veterans weight and the household weight. It is the most demographically correct weight 
PWVETWGT	Veterans weight	Used when computing estimates of veterans and nonveterans. Controlled to population estimates maintained by the Department of Veterans Affairs. 
PWCMPWGT	Composite final weight	Used to create BLS published labor force statistics. Only created for the civilian noninstitutional population 16 and over. 
HWHHWGT	Household weight	Used when estimating household characteristics

Link the CPS public use files
In order to link the same individuals across months, three variables must be used: hrhhid, hrhhid2, and pulineno
