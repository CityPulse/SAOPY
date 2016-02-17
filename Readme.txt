{\rtf1\ansi\ansicpg1252\cocoartf1348\cocoasubrtf170
{\fonttbl\f0\froman\fcharset0 Times-Roman;\f1\fswiss\fcharset0 Helvetica;\f2\fmodern\fcharset0 Courier;
}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red0\green0\blue233;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid1\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural

\f0\b\fs36 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 How to use saopy (
\f1\b0\fs24 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 source: http://iot.ee.surrey.ac.uk/citypulse/ontologies/sao/saopy.html
\f0\b\fs36 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 )\
\pard\pardeftab720\sa240

\b0\fs24 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 saopy depends on:\
\pard\tx220\tx720\pardeftab720\li720\fi-720
\ls1\ilvl0\cf2 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	1.	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 rdflib ({\field{\*\fldinst{HYPERLINK "http://rdflib.org/"}}{\fldrslt \cf3 \expnd0\expndtw0\kerning0
\ul \ulc3 \outl0\strokewidth0 \strokec3 http://rdflib.org/}}) v2.4.0 (easy_install) \
\pard\pardeftab720\sa240
\cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 saopy can be downloded from the following link: {\field{\*\fldinst{HYPERLINK "file:///Users/sefki/Documents/SVN/ICS/Webpage/citypulse/web/ontologies/sao/saopy-1.0.0-py2.py3-none-any.whl.zip"}}{\fldrslt \cf3 \expnd0\expndtw0\kerning0
\ul \ulc3 \outl0\strokewidth0 \strokec3 SAOPY}} (v1.0.0). Since it is an ongoing work, please make sure that you are using the latest version. In order to install SAOPY library, you have to use the following command in the directory that you have downloaded the SAOPY python wheels. \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 $ pip install ./saopy-1.0.0-py2.py3-none-any.whl
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0  \
then start python using\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 $ python
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Now let's open the python interpreter and give it a go...\
\pard\pardeftab720\sa240

\f2 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 [GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.56)] on darwin\uc0\u8232 Type "help", "copyright", "credits" or "license" for more information.\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Start by importing the saopy package : \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> import saopy\uc0\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
To view all "saopy" classes:\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> dir(saopy)\uc0\u8232 ['DUL', 'PropertySet', 'RDFInterface', 'SaoInfo', '__builtins__', '__doc__', '__file__', '__name__', '__package__', '__path__', 'ces', 'ct', 'exportRDFFile', 'exportRDFGraph', 'foaf', 'geo', 'importRDFFile', 'importRDFGraph', 'model', 'muo', 'owl', 'owlsg', 'owlss', 'owlssc', 'owlssp', 'owlssrp', 'prov', 'qoi', 'rdfs', 'sao', 'ssn', 'tl', 'tm', 'tzont'] 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
To view all classes of sao ontology from saopy library:\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> dir(saopy.sao)\uc0\u8232 ['DiscreteCosineTransform', 'DiscreteFourierTransform', 'Mean', 'Median', 'PiecewiseAggregateApproximation', 'Point', 'Segment', 'StreamAnalysis', 'StreamData', 'StreamEvent', 'SymbolicAggregateApproximation', '__builtins__', '__doc__', '__file__', '__name__', '__package__', '__path__', 'saopy'] 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Creating a sensor object:\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> sensor124 = saopy.ssn.Sensor("http://example.org/x")\uc0\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Why shall we use saopy for annotation of IoT data? Saopy enables a user to avoid various common problems including use of undefined properties and classes, poorly formed namespaces, problematic prefixes, literal syntax and other optional heuristics.\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> sensor124 = saopy.ssn.Senzor("http://example.org/x")\uc0\u8232 Traceback (most recent call last):\u8232 File "", line 1, in \u8232 AttributeError: 'module' object has no attribute 'Senzor'\u8232 >>> cityofaarhus = saopy.foaf.Organisation("http://example.org/cityofaarhus") \u8232 Traceback (most recent call last):\u8232 File "", line 1, in \u8232 AttributeError: 'module' object has no attribute 'Organisation'\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
To mash up multiple sensory objects for serialisation, you can use the ``SaoInfo" class. The following example shows how to create and export a sensor observation object with a value:\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> trafficData124 = saopy.sao.StreamData("http://example.org/data1")\uc0\u8232 >>> trafficData124.value = "1234"\u8232 >>> saoOut = saopy.SaoInfo()\u8232 >>> saoOut.add(trafficData124)\u8232 >>> saopy.RDFInterface.exportRDFFile(saoOut,\'94example1.rdf\'94, "n3") \u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Now that we know how to describe a simple observation, let's start annotating more detailed sensory observation. First create provenance information for sensory data: \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> cityofaarhus = saopy.foaf.Organization("http://example.org/cityofaarhus")\uc0\u8232 >>> cityofaarhus = saopy.prov.Agent("http://example.org/cityofaarhus")\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \

\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> trafficsensor158324 = saopy.ssn.Sensor("http://example.org/data158324") \uc0\u8232 >>> trafficsensor158324.actedOnBehalfOf = cityofaarhus \u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
creating properties of sensory data: \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> measuredTime = saopy.ssn.Property("http://unis/ics/property003")\uc0\u8232 >>> measuredTime.description = "Measured Time"\u8232 >>> estimatedTime = saopy.ssn.Property("http://unis/ics/property004")\u8232 >>> estimatedTime.description = "Estimated Time"\u8232 >>> avgSpeed = saopy.ssn.Property("http://unis/ics/property001")\u8232 >>> avgSpeed.description = "Average Speed"\u8232 >>> vcCount = saopy.ssn.Property("http://unis/ics/property002")\u8232 >>> vcCount.description = "Vehicle Count"\u8232 >>> trafficsensor158324.observes.add(vcCount)\u8232 >>> trafficsensor158324.observes.add(avgSpeed)\u8232 >>> trafficsensor158324.observes.add(estimatedTime)\u8232 >>> trafficsensor158324.observes.add(measuredTime)\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
SAOPY allows to describe time 
\b \expnd0\expndtw0\kerning0
\outl0\strokewidth0 instants
\b0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0  and 
\b \expnd0\expndtw0\kerning0
\outl0\strokewidth0 intervals
\b0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 . Time instants should only be used with 
\b \expnd0\expndtw0\kerning0
\outl0\strokewidth0 tl:at
\b0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0  to describe the time instance that data has been collected, whereas time interval should specify both the beginning time of the interval and duration. Here we provide both of the examples. \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> universaltimeline = saopy.tl.PhysicalTimeLine("http://purl.org/NET/c4dm/timeline.owl#universaltimeline")\uc0\u8232 >>> instant = saopy.tl.Instant("http://unis/ics/timeinstant")\u8232 >>> interval = saopy.tl.Interval("http://unis/ics/timeinterval")\u8232 >>> instant.at = "2014-09-30T06:00:00"\u8232 >>> instant.onTimeLine = universaltimeline\u8232 >>> interval.beginsAtDateTime = "2014-09-30T06:00:00"\u8232 >>> interval.durationXSD = "PT5M"\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
SAO ontology subsumes the measurement unit descriptions from Measurement Unit Ontology (muo). Therefore, it enables to describe measurement unit of an observation as follows: \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> unitseconds = saopy.muo.UnitOfMeasurement("http://unis/ics/unit1:seconds")\uc0\u8232 >>> unitkilometer = saopy.muo.UnitOfMeasurement("http://unis/ics/unit2:km-per-hour")\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
Now, we can annotate sensor observations for two sensor features, namely average speed and measure time:\uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> trafficData001 = saopy.sao.StreamData("http://unis/ics/trafficdataavgspeed001")\uc0\u8232 >>> trafficData001.value = "60"\u8232 >>> trafficData001.hasUnitOfMeasurement=unitkilometer\u8232 >>> trafficData001.observedProperty = avgSpeed\u8232 >>> trafficData001.observedBy = trafficsensor158324\u8232 >>> trafficData001.time = instant\u8232 \u8232 >>> trafficData003 = saopy.sao.StreamData("http://unis/ics/trafficdataMeasuredTime001")\u8232 >>> trafficData003.value = "30"\u8232 >>> trafficData003.hasUnitOfMeasurement=unitseconds\u8232 >>> trafficData003.observedProperty = measuredTime\u8232 >>> trafficData003.observedBy = trafficsensor158324\u8232 >>> trafficData003.time = interval
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0  \
exporting sensor data in N3 format: \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> saoOut.add(trafficData001)\uc0\u8232 >>> saoOut.add(trafficData003)\u8232 >>> saoOut.add(cityofaarhus)\u8232 >>> saoOut.add(trafficsensor158324)\u8232 >>> saoOut.add(estimatedTime)\u8232 >>> saoOut.add(measuredTime)\u8232 >>> saoOut.add(avgSpeed)\u8232 >>> saoOut.add(vcCount)\u8232 >>> saoOut.add(unitkilometer)\u8232 >>> saoOut.add(unitseconds)\u8232 >>> saoOut.add(universaltimeline)\u8232 >>> saoOut.add(instant)\u8232 >>> saoOut.add(interval)\u8232 >>> saopy.RDFInterface.exportRDFFile(saoOut, "example2.rdf", "n3")\u8232 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
saopy also allows to annotate quality values, such as correctness, frequency, age and completeness. The following example illustrates how to annotate quality features for a data segment of the traffic data stream. The correctness has been obtained based on an algorithm by examining the difference between two successful submitted traffic streams to validate the correctness quality value. \uc0\u8232 
\f2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 >>> segmentSample1 = saopy.sao.Segment("segment-sample-1") \uc0\u8232 >>> age = saopy.qoi.Age("age-sample-1")\u8232 >>> age.hasAge = "10" \u8232 >>> completeness = saopy.qoi.Completeness("completeness-sample-1") \u8232 >>> completeness.hasCompleteness = "1" \u8232 >>> correctness = saopy.qoi.Correctness("correctness-sample-1") \u8232 >>> correctness.hasCorrectness = "1" \u8232 >>> frequency = saopy.qoi.Frequency("frequency-sample-1") \u8232 >>> frequency.hasFrequency = "10" \u8232 >>> segmentSample1.hasQuality.add(frequency) \u8232 >>> segmentSample1.hasQuality.add(correctness) \u8232 >>> segmentSample1.hasQuality.add(completeness) \u8232 >>> segmentSample1.hasQuality.add(age) \u8232 >>> owner = saopy.prov.Person("MisterX") \u8232 >>> segmentSample1.hasProvenance = owner \u8232 >>> saoOut = saopy.SaoInfo() \u8232 >>> saoOut.add(segmentSample1) \u8232 >>> saoOut.add(age) \u8232 >>> saoOut.add(completeness) \u8232 >>> saoOut.add(correctness) \u8232 >>> saoOut.add(frequency) \u8232 >>> saoOut.add(owner) \u8232 >>> saopy.RDFInterface.exportRDFFile(saoOut, "example3.rdf", "n3") 
\f0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
\
\pard\pardeftab720
\cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
\pard\pardeftab720\sa298

\b\fs36 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \
}