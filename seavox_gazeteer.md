#SeaVoX Gazetteer as a SKOS Concept Scheme#

##2013-06-17##
###@adamml###
Dear all

The SeaVoX Gazetteer as mentioned by Yassine and Roy during the Technical Committee meeting is available from the NERC Vocabulary Server at

http://vocab.nerc.ac.uk/scheme/SVX_GAZTR/

Cheers

Adam
##2013-06-18##
###@tchaddad###
And Yassine just demo-ed in David's CoastGIS workshop that he has added the full globe Gazetteer to the portal, along with the Wisconsin Coastal Atlas - check it out!

very exciting...

Tanya
##2013-06-18##
###Yassine Lassoued###
The ontology mappings are incorrect though. So WCA search using ICAN terms does not work currently. Will fix this with Adam.
##2013-06-19##
###@adamml###
That's great news - I'll check it out in the portal in a minute.

Yassine - can you try ingesting http://vocab.nerc.ac.uk/scheme/WCATHES/ and let me know how you get on?

There's currently an issue with displaying some of the schemes, which I'll try and get fixed soon. It's to do with the stylesheet and its response to concepts which use the NAR & BRD to specify equivalence, instead of sameAs.

Cheers

Adam
##2013-06-19##
###Simon Claus###
Hi guys,
 
You might want to have a look at marineregions, to include some marine geographic boundaries into the prototype. All resources are available (including the Seavox boundaries) through OGC services at http://www.marineregions.org/webservices.php We are also in the process of developing soap and rest services on top of the gazetteer to retrieve the names, coordinates and classifications. I believe it would be nice if we could include the Marine Regions into the prototype, which is an intersection of the global seas and the EEZ:
http://www.marineregions.org/sources.php#ihoeez
http://www.marineregions.org/gazetteer.php?p=list&placetype=266
http://geo.vliz.be/geoserver/MarineRegions/wms?service=WMS&version=1.1.0&request=GetMap&layers=MarineRegions:eez_iho_union_v2&styles=&bbox=-180.0,-85.4702911376953,180.000015258789,90.0000076293945&width=677&height=330&srs=EPSG:4326&format=application/openlayers 
http://geo.vliz.be/geoserver/MarineRegions/ows?service=WFS&version=1.0.0&request=GetFeature&typeName=MarineRegions:eez_iho_union_v2&maxFeatures=50
 
Cheers,
 
Simon
##2013-06-19##
###Roy Lowry###
Dear All,

The metadata we have in ICAN at the moment is tagged using the SeaVoX C19 references. Pauline and I have been doing some work trying to link C19 to the OGC services provided by Marine Regions using the ShapeFile that underpins C19.  Whilst this works fine for the 'leaf nodes' in the C19 hierarchy, anything higher up in the hierarchy returns a geometry from the service that excludes the areas covered by its children.  For example, Liverpool Bay is not included in the Irish Sea geometry.  To get a complete polygon service calls need to be made for the target area plus all of its children and the display built  by aggregating the service returns.  Pauline is looking into ways of circumventing the problem.  When fixed, Marine Regions will be provided with an updated SeaVoX Sea Areas file and I'll build linkages  from C19 to the Marine Regions services.

In the mean time, if Yassine fancies demonstrating some geometries from Marine Regions then let me know the preferred service type (WMS or WFS) and the  desired example leaf nodes and I will add  Marine Regions service URLs to the appropriate C19 concept definitions  in addition to the bounding boxes currently served.

Cheers, Roy.