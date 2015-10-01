---
layout: post
title: "Sept Standards Committee Meeting Notes"
modified:
categories: blog
excerpt:
tags: []
image:
  feature:
date: 2015-09-24T20:43:38-05:00
---

# Participants (TERRA team/Affiliation)

David LeBauer (Danforth/UIUC), Alex Thomasson (TAMU), Barnabas Poczos (TAMU/CMU), Bob Strand (LemnaTec), Carl Bernacchi (UIUC), Ed Delp (Purdue), Melba Crawford (Purdue), Matt Colgan (PNNL/Blue River), Paul Bartlett (Clemson/Near Earth), Shelley Petroy (NEON), David Lee (ARPA-E)

GitHub Team: @terraref/reference-data 

## Overview Slides

<!-- Box Version
<iframe src="https://uofi.app.box.com/embed/preview/olqdzcxyihi8mr3fgera6dc8vlrdo8y0?theme=dark&view=&sort=&direction=ASC" width="800" height="550" frameBorder="0" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>-->
<iframe src='https://onedrive.live.com/embed?cid=62A7CDC1353EF6B0&resid=62A7CDC1353EF6B0%211358&authkey=AJI5ueNcZ5qAnxA&em=2&wdAr=1.7777777777777777' width='610px' height='367px' frameborder='0'>This is an embedded <a target='_blank' href='http://office.com'>Microsoft Office</a> presentation, powered by <a target='_blank' href='http://office.com/webapps'>Office Online</a>.</iframe>


## Notes

*   The Danforth Cat5 team is responsible for generating data and making it available to the public, and the data standards committee should be responsible for defining the data products coming off their platforms.  The committee will include up to six external members in addition to the TERRA teams.
*   Would like feedback from the TERRA teams on what types of data from the Cat5 sensors they’re interested in, and what programming languages for API development are of most interest. Specifically: what data formats are researchers accustomed to using? How do they want to query the data? What meta-data do they need?
*   The Cat5 team would like to be able to provide raw data off of the LemnaTec platform in Arizona as soon as it's operational, possibly in January for some sensors. They're targeting being able to provide processed data in one year that are readily accessible and can be queried.
*   The reference team will expand the data products in years 2 and 3.
*   Example datasets can be downloaded and contributed to Box. The Danforth plantcv site already has a number of publically available data sets.
*   NEON could provide support on their data management schema, along with their pipeline description for generating a data product.  Publication workbooks and other documents could be provided.
*   UIUC/NCSA can provide access to their software platform or share it with others so that the data access and computation can be conducted on local servers instead of running it at UIUC. We are interested in knowing the scope of data storage, computational resources, and control on data access and sharing users are interested in.
*   The TERRAREF Documentation web page is where David LeBauer has been collecting all of the useful information related to data standards and products so far.  Users can provide feedback to ideas and specific documents through the website. Suggestions can be submitted via email or through github (either by opening an issue or suggesting edits through the web interface).
*   The Cat 5 platform is designed to keep intellectual property secure. For the development of data products and the design of the system itself, David LeBauer would like to make materials publicly available (e.g. sample data, meeting notes, decisions) by default while also respecting the needs of individuals with respect to their privacy and intellectual propriety. Participants therefore requested to actively identify any content that should be kept private, and to contact David directly with any requests or suggestions.

## Action Items

*   Review the documents in the Box site and TERRAREF website that David LeBauer has set up. (All)
*   Identify the different parts of the data pipeline, as described in the planning documents, that you or a member of your TERRA team can review or provide input on, and respond to Davids Lee and LeBauer.  Individuals to provide guidance on genomics and robotics would be especially welcome. (All)
*   Sign up for github and send David an email to get linked in to the discussion and access to any shared code under development for data processing. (All)
*   NEON will upload their package of information to David’s website/box site.
*   If you have any trouble accessing these resources (Github, Box, other), please contact David.
*   A physical representation of the LemnaTec system would be very useful.  Understanding the specs of the system, such as the field design, types of cameras/sensors and installation angles, calibration processes and standards, metadata, etc., will be important for data processing by the other TERRA teams.  Bob will look into providing that information. Probably I think that the files `System specification7100019_System_Specification_V11.pdf` and `VPK-USA-Field\
-Übersicht-10_Freigabe_LT.pdf` will suffice; we need to check if these can be made public. see [issue 11](https://github.com/terraref/reference-data/issues/11).
