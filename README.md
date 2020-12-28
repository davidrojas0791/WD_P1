# Web-Datos-Proy1-T10

## Prefixes
```
@prefix rdf:      <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs:     <http://www.w3.org/2000/01/rdf-schema#> .
@prefix owl:      <http://www.w3.org/2002/07/owl#> .
@prefix xsd:      <http://www.w3.org/2001/XMLSchema#> .
@prefix skos:     <http://www.w3.org/2004/02/skos/core#> .
@prefix void:     <http://rdfs.org/ns/void#> .
@prefix dct:      <http://purl.org/dc/terms/> .
@prefix foaf:     <http://xmlns.com/foaf/0.1/> .
@prefix org:      <http://www.w3.org/ns/org#> .
@prefix admingeo: <http://data.ordnancesurvey.co.uk/ontology/admingeo/> .
@prefix interval: <http://reference.data.gov.uk/def/intervals/> .
@prefix time: <http://www.w3.org/2006/time#> .
@prefix wd:  <http://www.wikidata.org/entity/> .

@prefix qb:  <http://purl.org/linked-data/cube#> .
@prefix ex:  <http://ex.org/a#> .

@prefix sdmx-concept:    <http://purl.org/linked-data/sdmx/2009/concept#> .
@prefix sdmx-dimension:  <http://purl.org/linked-data/sdmx/2009/dimension#> .
@prefix sdmx-attribute:  <http://purl.org/linked-data/sdmx/2009/attribute#> .
@prefix sdmx-measure:    <http://purl.org/linked-data/sdmx/2009/measure#> .
@prefix sdmx-metadata:   <http://purl.org/linked-data/sdmx/2009/metadata#> .
@prefix sdmx-code:       <http://purl.org/linked-data/sdmx/2009/code#> .
@prefix sdmx-subject:    <http://purl.org/linked-data/sdmx/2009/subject#> .


@prefix c19:  <http://example.org/ns#> .
@prefix c19-measure:  <http://example.org/measure#> .
@prefix c19-dimension:  <http://example.org/dimension#> .
@prefix c19-unit:  <http://example.org/unit#> .
@prefix c19-structure:  <http://example.org/structure#> .
@prefix c19-interval:  <http://example.org/interval#> .
```

## Metadata: Health systems

### Completeness birth registration

```
# -- Data Set ---------------------------------------------

c19:dataset-completeness_birth_registration a qb:Dataset ; 
	dct:title "Completeness of birth registration"@en ; 
	rdfs:label "completeness_birth_registration"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Completeness of birth registration is the percentage of children under age 5 whose births were registered at the time of the survey. The numerator of completeness of birth registration includes children whose birth certificate was seen by the interviewer or whose mother or caretaker says the birth has been registered."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ; 
	qb:structure c19-structure:dsd-completeness_birth_registration ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-completeness_birth_registration a qb:DataStructureDefinition ;
	qb:component
		[ qb:dimension c19-dimension:refArea; qb:order 2 ] ,
		[ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ;
	qb:component 
		[ qb:measure c19-measure:completenessOfBirthRegistrations ] ; 
	qb:component
		[ qb:attribute sdmx-attribute:decimals ; qb:attribute sdmx-attribute:unitMultiplier ;] ; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2013-18 a time:Interval ;
    time:hasBeginning "2013"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2013-18" .

# -- Dimensions and measures ------------------------------

c19-measure:completenessOfBirthRegistrations a rdf:Property, qb:MeasureProperty ; 
	rdfs:label "Percent of Completed Birth Registrations"@en ; 
	rdfs:subPropertyOf sdmx-measure:obsValue ; 
	rdfs:range xsd:decimal ; .
```

### Completeness death registration

```
# -- Data Set ---------------------------------------------

c19:dataset-completeness_death_registration a qb:Dataset ; 
	dct:title "Completeness of death registration"@en ; 
	rdfs:label "completeness_death_registration"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Completeness of death registration is the estimated percentage of deaths that are registered with their cause of death information in the vital registration system of a country."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ; 
	qb:structure c19-structure:dsd-completeness_death_registration ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-completeness_death_registration a qb:DataStructureDefinition;
        qb:component
                [ qb:dimension c19-dimension:refArea; qb:order 2 ] ,
                [ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ;
        qb:component
                [ qb:measure c19-measure:completenessOfDeathRegistrations ] ;
        qb:component
                [ qb:attribute sdmx-attribute:decimals ;
                qb:attribute sdmx-attribute:unitMultiplier ;] ;
.

# -- Intervals --------------------------------------------

c19-interval:Year2008-16 a time:Interval ;
    time:hasBeginning "2008"^^xsd:gYear ;
    time:hasEnd "2016"^^xsd:gYear ;
    rdfs:label "2008-16" .

# -- Dimensions and measures ------------------------------

c19-measure:completenessOfDeathRegistrations a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of Completed Death Registrations"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .
```

### External health expenditure

```
# -- Data Set ---------------------------------------------

c19:dataset-external_health_expenditure a qb:Dataset ; 
	dct:title "External health expenditure"@en ; 
	rdfs:label "external_health_expenditure"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Share of current health expenditures funded from external sources. External sources compose of direct foreign transfers and foreign transfers distributed by government encompassing all financial inflows into the national health system from outside the country. External sources either flow through the government scheme or are channeled through non-governmental organizations or other schemes."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ; 
	qb:structure c19-structure:dsd-external_health_expenditure ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-external_health_expenditure a qb:DataStructureDefinition; 
        qb:component 
                [ qb:dimension c19-dimension:refArea; qb:order 2 ] , 
                [ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ; 
        qb:component 
                [ qb:measure c19-measure:externalHealthExpenditure ] ; 
        qb:component 
                [ qb:attribute sdmx-attribute:decimals ; 
                qb:attribute sdmx-attribute:unitMultiplier ;] ; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2017 a time:Interval ;
    time:hasBeginning "2017"^^xsd:gYear ;
    time:hasEnd "2017"^^xsd:gYear ;
    rdfs:label "2017" .

# -- Dimensions and measures ------------------------------

c19-measure:externalHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of current external health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .
```

### Health expenditure

```
# -- Data Set ---------------------------------------------

c19:dataset-health_expenditure a qb:Dataset ; 
	dct:title "Health expenditure"@en ; 
	rdfs:label "health_expenditure"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Level of current health expenditure expressed as a percentage of GDP. Estimates of current health expenditures include healthcare goods and services consumed during each year. This indicator does not include capital health expenditures such as buildings, machinery, IT and stocks of vaccines for emergency or outbreaks."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ;
	qb:structure c19-structure:dsd-health_expenditure ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-health_expenditure a qb:DataStructureDefinition; 
        qb:component 
                [ qb:dimension c19-dimension:refArea; qb:order 2 ] , 
                [ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ; 
        qb:component 
                [ qb:measure c19-measure:currentHealthExpenditure ; 
                qb:measure c19-measure:publicHealthExpenditure ; 
                qb:measure c19-measure:outOfPocketHealthExpenditure ; 
                qb:measure c19-measure:percapitaHealthExpenditure ; 
                qb:measure c19-measure:percapitaPPPHealthExpenditure ;] ; 
        qb:component 
                [ qb:attribute sdmx-attribute:decimals ; 
                qb:attribute sdmx-attribute:unitMultiplier ;] ; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2017 a time:Interval ;
    time:hasBeginning "2017"^^xsd:gYear ;
    time:hasEnd "2017"^^xsd:gYear ;
    rdfs:label "2017" .

# -- Dimensions and measures ------------------------------

c19-measure:currentHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of current health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .

c19-measure:publicHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of public health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .

c19-measure:outOfPocketHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of public health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .

c19-measure:percapitaHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of public health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .

c19-measure:percapitaPPPHealthExpenditure a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Percent of public health expenditure"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .
```

### Health workers

```
# -- Data Set ---------------------------------------------

c19:dataset-health_workers a qb:Dataset ; 
	dct:title "Health workers"@en ; 
	rdfs:label "health_workers"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Physicians include generalist and specialist medical practitioners. Nurses and midwives include professional nurses, professional midwives, auxiliary nurses, auxiliary midwives, enrolled nurses, enrolled midwives and other associated personnel, such as dental nurses and primary care nurses."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ; 
	qb:structure c19-structure:dsd-health_workers ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-health_workers a qb:DataStructureDefinition; 
        qb:component 
                [ qb:dimension c19-dimension:refArea; qb:order 2 ] , 
                [ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ; 
        qb:component 
                [ qb:measure c19-measure:healthWorkersPhysicians ; 
                qb:measure c19-measure:healthWorkersNursesAndMidwives ;] ; 
        qb:component 
                [ qb:attribute sdmx-attribute:decimals ; 
                qb:attribute sdmx-attribute:unitMultiplier ;] ; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2013-18 a time:Interval ;
    time:hasBeginning "2013"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2013-18" .

# -- Dimensions and measures ------------------------------

c19-measure:healthWorkersPhysicians a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Physicians per 1000 people"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .

c19-measure:healthWorkersNursesAndMidwives a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Nurses and midwives per 1000 people"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .
```

### Specialist surgical workforce

```
# -- Data Set ---------------------------------------------

c19:dataset-specialist_surgical_workforce a qb:Dataset ; 
	dct:title "Specialist surgical workforce"@en ; 
	rdfs:label "specialist_surgical_workforce"@en ; 
	rdfs:comment "2.12 | World Development Indicators: Health systems"@en ; 
	dct:description "Specialist surgical workforce is the number of specialist surgical, anaesthetic, and obstetric (SAO) providers who are working in each country per 100,000 population."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.12> ; 
	qb:structure c19-structure:dsd-specialist_surgical_workforce ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-specialist_surgical_workforce a qb:DataStructureDefinition; 
        qb:component 
                [ qb:dimension c19-dimension:refArea; qb:order 2 ] , 
                [ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ; 
        qb:component 
                [ qb:measure c19-measure:specialistSurgicalWorkforce ] ; 
        qb:component 
                [ qb:attribute sdmx-attribute:decimals ; 
                qb:attribute sdmx-attribute:unitMultiplier ;]; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2008-18 a time:Interval ;
    time:hasBeginning "2008"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2008-18" .

# -- Dimensions and measures ------------------------------

c19-measure:specialistSurgicalWorkforce a rdf:Property, qb:MeasureProperty; 
        rdfs:label "Specialist Surgical Workforce per 100000 population"@en; 
        rdfs:subPropertyOf sdmx-measure:obsValue; 
        rdfs:range xsd:decimal ; .
```

## Metadata: Mortality

### Adult mortality rate

```
# -- Data Set ---------------------------------------------

c19:dataset-adult_mortality_rate a qb:Dataset ; 
	dct:title "Adult mortality rate"@en ; 
	rdfs:label "adult_mortality_rate"@en ; 
	rdfs:comment "2.18 | World Development Indicators: Mortality"@en ; 
	dct:description "Adult mortality rate, male, is the probability of dying between the ages of 15 and 60--that is, the probability of a 15-year-old male dying before reaching age 60, if subject to age-specific mortality rates of the specified year between those ages. Adult mortality rate, female, is the probability of dying between the ages of 15 and 60--that is, the probability of a 15-year-old female dying before reaching age 60, if subject to age-specific mortality rates of the specified year between those ages."@en ; 
	dct:publisher wd:Q7164 ; 
	dct:issued "2020-09-22"^^xsd:date ; 
	dct:source <http://wdi.worldbank.org/table/2.18> ; 
	qb:structure c19-structure:dsd-adult_mortality_rate ; 
. 

# -- Data structure definition ----------------------------

c19-structure:dsd-adult_mortality_rate a qb:DataStructureDefinition ;
	qb:component
		[ qb:dimension c19-dimension:refArea; qb:order 2 ] ,
		[ qb:dimension c19-dimension:refPeriod; qb:order 1 ] ;
	qb:component 
		[ qb:measure c19-measure:adultMortalityRate ] ; 
	qb:component
		[ qb:attribute sdmx-attribute:decimals ; qb:attribute sdmx-attribute:unitMultiplier ;] ; 
.

# -- Intervals --------------------------------------------

c19-interval:Year2013-18 a time:Interval ;
    time:hasBeginning "2013"^^xsd:gYear ;
    time:hasEnd "2018"^^xsd:gYear ;
    rdfs:label "2013-18" .

# -- Dimensions and measures ------------------------------

c19-measure:adultMortalityRate a rdf:Property, qb:MeasureProperty ; 
	rdfs:label ""@en ; 
	rdfs:subPropertyOf sdmx-measure:obsValue ; 
	rdfs:range xsd:decimal ; .
```

### Infant mortality rate

### Life expectancy birth total

### Neonatal mortality rate

### Under-five mortality rate complete