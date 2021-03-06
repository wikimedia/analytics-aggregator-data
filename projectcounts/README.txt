Projectcounts aggregates
========================

This directory holds aggregates of pageviews per wiki.



Sources
-------

The per wiki files underneath this directory take Webstatscollector's
projectfiles as input. The data for 2008-01-01 up to 2014-09-22 is
obtained from

  http://dumps.wikimedia.org/other/pagecounts-ez/projectcounts/

(and only contains numbers for the desktop site). The data from
2014-09-23 onwards is obtained from

  http://dumps.wikimedia.org/other/pagecounts-all-sites/

(and contains numbers for the desktop, mobile, and zero site).



Available aggregations
----------------------

The following aggregations are available

* `daily_raw`: Per wiki CSVs containing daily aggregates of the
  projectcounts numbers. Those files are not sanitized in any way. So
  it contains data for days that are known to be wrong. The `daily`
  filters those bad dates out.

* `daily`: Per wiki CSVs containing daily aggregates of the
  projectcounts numbers. Those files only contain data for which no
  further issues are known.

* `weekly_rescaled`: Per wiki CSVs containing `daily` data summed up
  per week and each week rescaled to 7 good days.

* `monthly_rescaled`: Per wiki CSVs containing `daily` data summed up
  per month and each month rescaled to 30 good days.

* `yearly_rescaled`: Per wiki CSVs containing `daily` data summed up
  per year and each year rescaled to 365 good days.

For aggregations that filter away bad dates, `BAD_DATES.csv` contains
the bad dates in a machine readable format.