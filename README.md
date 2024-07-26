# Primary-Health-Care-Services-Application
 The application includes modules for Maternal and Child Health, General Medical Care, and Trainings and Workshops for healthcare providers and the community. It aims to streamline the delivery of essential health services in resource-limited settings and enhance data collection timeliness through mobile devices.


Objectives:
Improve the efficiency and effectiveness of primary health care delivery.
Enhance primary health care services through systematic tracking and management.
Provide ongoing training and support for healthcare providers to ensure high-quality care.

Features:
Maternal and Child Health:
Antenatal care tracking
Delivery
Postnatal care management
Reproductive Health
Family Planning
Nutrition

Medical Care:
Patient registration and history
Diagnostic tools and treatment plans
Medication tracking

Training:
Training modules for healthcare workers
Assessments
Workshops - Reproductive health awareness, healthcare worker meetings, school health, water, sanitation and hygiene, disease prevention procedures... 

Technology Used:
CommCare: A powerful, open-source mobile data collection platform 
XML: For form structure and logic.
APIs: For data integration and interoperability with other health information systems.

Example functions in Commcare XML:
Lookup Table Value References 
join(", ", instance("area")/area_list/area[area_id = #form/area_name]/name)
join(", ", instance("tsp")/tsp_list/tsp[id = #form/township_name]/name)
join(", ", instance("clinic")/clinic_list/clinic[id = #form/clinic_name]/name)
join(", ", instance("village")/village_list/village[village_id = #form/village_name]/name)
Group
jr:itext(concat('investigation_group_gm/malaria_gm-', #form/investigation_group_gm/malaria_gm, '-label'))
Duplication
count(instance('casedb')/casedb/case[@case_type = 'phc'][registration_number = #form/registration_list/registration_number])
if(#form/registration_list/duplication_regno >= 1, 'Duplicate Number', '')

