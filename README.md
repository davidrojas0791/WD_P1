# Web-Datos-Proy1-T10




## temp notes

#################### intervals ####################

c19-interval:Year2008-16 a time:Interval ;
    time:hasBeginning "2008"^^xsd:gYear ;
    time:hasEnd "2016"^^xsd:gYear ;
    rdfs:label "2008-16" .

c19-interval:Year2008-18 a time:Interval ;
    time:hasBeginning "2008"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2008-18" .

c19-interval:Year2013-18 a time:Interval ;
    time:hasBeginning "2013"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2013-18" .




c19-interval:Year1990-18 a time:Interval ;
    time:hasBeginning "1990"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "1990-18" .

c19-interval:Year1990-19 a time:Interval ;
    time:hasBeginning "1990"^^xsd:gYear ;
    time:hasEnd "2019"^^xsd:gYear ;
    rdfs:label "1990-19" .

#################### dimension_measure ####################


c19-measure:completenessOfBirthRegistrations  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of Completed Birth Registrations"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:completenessOfDeathRegistrations  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of Completed Death Registrations"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:externalHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of current external health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:currentHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of current health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:publicHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of public health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:outOfPocketHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of public health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:percapitaHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of public health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:percapitaPPPHealthExpenditure  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Percent of public health expenditure"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:healthWorkersPhysicians  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Physicians per 1000 people"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:healthWorkersNursesAndMidwives  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Nurses and midwives per 1000 people"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:specialistSurgicalWorkforce  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Specialist Surgical Workforce per 100000 population"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .








c19-measure:adultMortalityRateMale  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Adult male mortality per 1000 population"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:adultMortalityRateFemale  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Adult female mortality per 1000 population"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .


c19-measure:infantMortalityRate1990  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Infant mortality per 1000 live births in 1990"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .

c19-measure:infantMortalityRate2019  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Infant mortality per 1000 live births in 2019"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .


c19-measure:lifeExpectancyBirthTotal1990  a rdf:Property, qb:MeasureProperty;
    rdfs:label "Infant mortality per 1000 live births in 2019"@en;
    rdfs:subPropertyOf sdmx-measure:obsValue;
    rdfs:range xsd:decimal ;
    .



#################### structure ####################
 # c19-structure:dsd-completeness_birth_registration
c19-structure:dsd-completeness_birth_registration a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:completenessOfBirthRegistrations ];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.

 # c19-structure:dsd-completeness_death_registration
c19-structure:dsd-completeness_death_registration a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:completenessOfDeathRegistrations ];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.

 # c19-structure:dsd-external_health_expenditure
c19-structure:dsd-external_health_expenditure a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:externalHealthExpenditure ];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.

 # c19-structure:dsd-health_expenditure
c19-structure:dsd-health_expenditure a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:currentHealthExpenditure ; 
     qb:measure c19-measure:publicHealthExpenditure ;
     qb:measure c19-measure:outOfPocketHealthExpenditure ;
     qb:measure c19-measure:percapitaHealthExpenditure ;
     qb:measure c19-measure:percapitaPPPHealthExpenditure ;];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.

 # c19-structure:dsd-health_workers
c19-structure:dsd-health_workers a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:healthWorkersPhysicians ; 
     qb:measure c19-measure:healthWorkersNursesAndMidwives ;];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.

 # c19-structure:dsd-specialist_surgical_workforce
c19-structure:dsd-specialist_surgical_workforce a qb:DataStructureDefinition;
    qb:component
    [ qb:dimension c19-dimension:refArea;               qb:order 2 ],
    [ qb:dimension c19-dimension:refPeriod;               qb:order 1 ];
    qb:component
    [ qb:measure c19-measure:specialistSurgicalWorkforce ];
    qb:component
    [ qb:attribute sdmx-attribute:decimals ;
    qb:attribute sdmx-attribute:unitMultiplier ;];
.