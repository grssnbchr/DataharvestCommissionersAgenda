# Detailed, structured data on EU commissioners' agendas

The herein presented scraper is an enhancement to https://github.com/cguess/Fontaine - The script by [@cguess](https://twitter.com/cguess) fetches agenda data from https://ec.europa.eu/commission/2014-2019/agenda_en

Even better, i.e. **more structured data** (entities met, discussed subjects) are available on each commissioner's profile page, for example [here](http://ec.europa.eu/commission/2014-2019/timmermans_en) under the point "Agenda". Available are:

1. The meetings held by the commissioner himself/herself
2. The meetings held by his or her cabinet

For these data the scraper was written in R (what else?). It converts the HTML tables to CSV files, one for 1) (`all_meetings.csv`) and 2) (`all_meetings_by_cabinet.csv`) each. 

## How to run

```
git clone https://github.com/grssnbchr/DataharvestCommissionersAgenda.git
```

Fire up RStudio and knit `main.Rmd` (don't forget to change the working directory). The actual/current data will be written into the above presented CSV files. 

## Issues

* There are still some problems with line breaks, these are not correctly replaced in the scraper. 
* Somehow the data available under the above mentioned links are only reaching back until 2014- the data scrapable through https://github.com/cguess/Fontaine seem to be a bit more thorough - a deduplication/redundancy check would be appropriate. 
* The code is messy as hell - sorry for that. 

## Further actions:

* With the scraped data, you could search the "Entity" column for abnormally frequently met companies/NGOs/stakeholders
* You could also produce fancy word clouds or frequency tables concerning the discussed subjects using information in the "Subject" column
* ...

## Author, license

Scraper made by Timo Grossenbacher (SRF Data) as part of the Dataharvest 2015 Hackathon in Brussels, Belgium.
No license, do whatever the hell you want with the code. 
