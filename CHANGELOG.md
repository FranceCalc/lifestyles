# Changelog

## unreleased
### Added
- Nothing
### Changed
- Input lever file for pkm reflecting feedback from call for evidence
- Calibration period of transport pkm
### Removed
- Old and not working metanode "EUcalc detailed lever export".
### Fixes
- Nothing

## 3.6
### Added
- New calibration data for passenger travel.
### Changed
- Correction of the double aggregation issue on node #901
- Update of ll trajectories for product replacement rate.
- Clean-up of Regex for GTAP outputs.
- Aluminium demand from packaging modified to match Manufacturing needs
- Correction of the floor area stagnation between 2015 and 2020
- Changes to input data on appliance use OTS, fridges and freezers
- Population data inputs changed to reflect EUROSTAT scenario update in 2018
- Logic to supply Minerals module with population
- Removed population from the interfaces with Storage
- Changed interfaced to Minerals.
- Simplification of the flow to determine calorie aggregation to Employment module.
- A number of small corrections in some input files.
- Interfaces to employment.
- Input files on appliance use (ll_lfs_appliance-use.xlsx) fixing the discrepancy of computer user between ots and fts
- Updated inputs files for diets, waste and RoGF
### Removed
- A bunch of nodes in the Employment flow
### Fixes
- Slight improvements on calibration from 108 to 105%
- Drop in pigs and milk from 2015 to 2020 in the Agricultural graphics
- Break of the m2 of cooled floor space in the projections.
- Calories of milk wasted where a factor of 3 too low on the scenarios when compared with 2015
- Input data for fraction of area cooled and appliances owned

##2.1
### Added
- Interfaces to Air pollution module.
- Experimental workflow to determine health benefits of diets in diabetes (no outputs to no module/TPE).
- Slight change of logic in determining non-shiftable transport demand. 
### Changed
- Names of outputs to GTAP following Francesco's recommendations.
- New xlsx files for population and  floor use intensity.
- Updated transport split factors in file "tra_demand_split_factors.xlsx"
- Updated metadata of product substitution rate, ots and ll
### Removed
- Nodes generating EU values for GTAP. Only individual countries are now provided.
### Fixes
- Fixed 1992-1994 peak sanitary paper demand on ots_lfs_paperpack.xlsx.
- Fixed unit name of product substitution rate for Buildings, form [%] to [factor]
- Fixed interfaces with storage module.

##2.0
### Added
- Updated lever trajectories to start in 2020. Please, UPDATE the input excel sheets of Lifestyles.
- Established interfaces with storage (5.3) but NOT appearing in the L2 interfaces yet but outputs are stored as str.xlsx
- Added temperature set points as output to storage.
- Interface to GTAP (outputs stored as GTAP.xlsx
- Interfaces to employment module.
### Changed
- Minor changes in layout
- Visualization plot to check on calibration on agriculture.
- New xlsx files, cal_lfs_diet, cal_lfs_fwaste, and ots_lfs_diet, years 2014 and 15 aligned with Agriculture module.
- New bld_factors.xlsx with set-point information for storage.
- After the last push I now get error on node 5.
### Removed
- Nothing
### Fixes
- Excessive milk demand for agriculture.
- Czech Republic naming issues.

##1.8
### Added
- New interface to Agriculture output, lfs_diet_rice and lfs_fwaste_rice
- More detail description of work-flow in Employment
- Interface to minerals passing on 3 types of population data and new interface to employment. Added new output ports in the 1.1 lifestyles metanode and linked them to Update L2 google node with names 4.2 Minerals and 6.1 Employment. Node runs but the interface with Employment does not show up in the google sheet. Vincent is aware of it.
### Changed
- Some of the input data has been refined (see below some). I advise that for NEXt release to UPDATE ALL of the input data.
- Updates to ots_lfs_diet.xlsx, ots_lfs_fwaste.xlsx, ll_lfs_fwaste.xlsx and RoFG_shares.xlsx to include rice calories.
- Updates to tra_demand_split_factors.xlsx, ll_lfs_paperpack.xlsx.... etc (see above request to update all inputs).
### Removed
- Nothing
### Fixes
- Abnormal values to transport.

##1.7
### Added
- Final calculation flow for employment with several aggregations of intermediate outputs.
- Glass and aluminium packaging demand
- Two new interfaces with the industry module
### Changed
- ots_lfs_paperpack and ll_lfs_paperpack input data
- Calibration data for transport cal_lfs_travel
### Removed
- Nothing
### Fixes
-  Bug preventing ots values for Czech Republic in output

##1.6
### Added
- Visuals of outputs aggregated to EU (outside main metanode)
### Changed
- Updates to the calculation flows to be connected with transboudary
- Updates to the calculation flows to be connected with employment
- Revisions of several input data
### Removed
### Fixes

## 1.5
### Added
- Inclusion of calculation flows for employment and transboundary (mostly aggregation of results calculated in other flows), no interface established yet.
- Lever on product life-time albeit only with constant figures for countries. 

### Changed
- Input data on heat-cool behaviour (in the future this interface will be done with the climate module)
- Calculation of charge time rather than time use of phone.
- Constant factors for cooling space imported as excel in LFS_building_use node
- Calculation of area of buildings of residential buildings cooled
- Interface lfs_floor-space_cool[1000m2] added
- Input data ots_lfs_floor-intensity.xlsx and ll_lfs_floor-intensity.xlsx refined
- Input data ots_lfs_pop.xlsx and ll_lfs_pop.xlsx refined
- Input data ll_lfs_kcal-req.xlsx refined
- Input data ll_lfs_pkm.xlsx refined
### Removed
- interfaces lfs_appliance-own_ac[num] and lfs_appliance-own_ac[h] removed 


## 1.4
### Added
- Nothing so far
### Changes
- Input data file ll_lfs_urbpop.xlsx to correct bad lever 4 and 2
### Removes
### Fixes
- Aggregation on setpoint temperature changed from sum to mean after bug detected by Benoît. 
- Aggregation of hours of appliance used also changed.

## 1.2
### Added
- Calibration of waste

### Changes
- "Some decompression"
- More documentation of the formulas in the node description
- Simplified flow on determining calorie demand

### Removes
- Nothing

### Fixes
- Nothing


## 1.0
### Added
- better travel split methodology for transport output.
- details on the inputs and outputs of the calculation trees for calorie, waste, travel and building demand.
- interaction of lever urban population with urban transport.
- inclusion of appliances use and number in the work-flow and has inputs
- calculation of household number for buildings (past value ok, future values dummy)
- inclusion of heat and lighting requirements in the work-flow and as inputs (very very crude, will probably require an interaction with climate)

### Changes
- calculation tree for calorie demand after interaction with land module.
- manual selection of columns to regex.

### Removes
- nothing

### Fixed 
- naming of Czech republic in input OTS data of diets.
- double counting of OTS and FTS for the year 2015.
- input data of food waste after exchange with land module.
- aggregation by country of electricity from servers.

## 0.9
- Initial version, integrating all modules.