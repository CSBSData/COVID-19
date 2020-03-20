# COVID-19 Structured Data  
Thank you for visiting the CSBSData Github, the official Github of the
Conference of State Bank Supervisors (CSBS). This Github is maintained
by the CSBS Analytics and Research team and was designed to give CSBS
members, state financial regulators, members of the public,
reporters/media, and other government agencies with easy access to
structured county-level COVID-19 reporting information. The file on this
site is updated once an hour. If you have questions, please direct them
to:

**Data Questions**: Brennan Zubrick, Senior Director of Analytics and
Research, <bzubrick@csbs.org>**Media/Communications Inquiries**: Matt
Longacre, Director of Communications, <mlongacres@csbs.org>. When using
the CSBS Structured dataset made available on this site, please provide
some form of attribution to CSBS

The CSBS Structured COVID-19 file contains the following fields:

1.  County Name
    
    1.  In cases where cases are reported at the county level but also
        at the independent city level, CSBS takes steps during the
        transformation process to remove any city level reporting that
        is already included in the county level counts (e.g. Baltimore
        city reports counts but is removed because their counts are
        included in Baltimore county).

2.  State Name

3.  Confirmed
    
    1.  Total number of confirmed cases of COVID-19 in the jurisdiction.

4.  New
    
    1.  Reports new cases since midnight of the previous day

5.  Death
    
    1.  Total number of COVID-19 deaths

6.  Fatality Rate
    
    1.  Calculated as number of deaths over number of confirmed cases

7.  Latitude

8.  Longitude

9.  State FIPS Code

10. County FIPS Code  
    Note: please read notes below on steps CSBS is taking to accurately
    geocode this dataset.

11. New cases this week
    
    1.  A metric calculated by CSBS which shows a cumulative total of
        new cases in a given week – resets to 0 every Sunday at
        midnight. This metric is added by CSBS to supplement the new
        cases since midnight, since it resets everyday at midnight

12. Last Update
    
    1.  Date and time of last update to the data. Currently

When using the CSBS Structured dataset made available on this site,
please provide some form of attribution to CSBS. The source\[s\],
validations, transformations, and calculations CSBS provides on this
dataset are outlined below.

  - COVID-19 confirmed cases, new cases since midnight, and deaths are
    obtained through a private organization named 1Point3Acres – which
    sources its information from several sources, mainly state and
    county government run health agencies.

  - Some data points, especially those in the “Unassigned” category come
    from contemporaneous and credible sources (such as news reports and
    press releases) which may provide more updated numbers. As hourly
    updates continue to run, and information from these contemporaneous
    sources becomes available through the official government
    state/county/city health agencies, the counts in the “Unassigned”
    category generally go down over time.

  - After obtaining the raw counts from the 1Point3Acres site and other
    contemporaneous sources, CSBS takes a number of additional steps to
    verify, validate, and transform the data including:
    
      - A weekly validation confirms the data on the 1Point3Acres site
        matches the data listed on the individual, government-run,
        state/county/city health agencies sites. So far these
        validations have proved 1Point3Acres to be a reliable source.
    
      - Validations with other organizations using and relying upon this
        data.

  - Once CSBS ingests information from the 1Point3Acres site, it runs a
    geospatial matching algorithm to translate county names into
    latitude and longitude coordinates, as well as assigning State FIPS
    and County FIPS code to make it clear for which jurisdictions this
    information’s being reported.
    
      - This matching process involves a substantial amount of manual
        reconciliation to ensure that the latitude and longitude
        coordinates, and the county/state codes accurately represent the
        area for which information was originally intended to repot on.
        CSBS has integrated more than 150 individual adjustments into
        its data updating process to make sure this information is as
        accurate as possible.
    
      - This process also involves processes to remove duplicative
        information in instances where a city may be reporting the
        counts already included in the county totals.

  - In addition to providing raw counts of confirmed, new cases since
    midnight, and deaths, CSBS also calculates its own metrics which may
    aid individuals in their analysis of this information. The manually
    calculated metrics CSBS calculates internally are:
    
      - Number of new cases this week (resets Sunday at midnight of each
        week)

The Conference of State Bank Supervisors (CSBS) is providing the data in
the CSBSData Github “as is” with no warranties of any kind and CSBS
assumes no responsibilities for any errors or omissions. The user
assumes all risk associated with the user of the data provided in the
CSBSData Github. In no event will CSBS be liable for any damages
whatsoever arising out of or related to the data, including, but not
limited to direct, indirect, incidental, special, consequential or
punitive damages, whether under a contract, tort or any other theory of
liability, even if CSBS is aware of the possibility of such damages. The
structure, format, and availability of this data is subject to change at
any time, and for any reason, at CSBS’ sole discretion.
