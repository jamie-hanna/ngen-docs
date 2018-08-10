# SB/AD Import Instructions

## General

* Correct ordering of columns is required
* File must be saved as .xlsx
* Formatting is ignored

## Fields

### Model (Alphanumeric, 50 characters) `required`
The Model field is used to define the model applicability of the document specified in the spreadsheet row. This means that each model will require a seperate line in the case of multiple model applicability. Model applicability is the simplest form of applicability for documents.

### SerialNo (Alphanumeric, 20 characters) `required`
The SerialNo field is used to define the serial number applicability of the document specified in the spreadsheet row. This means that each specific serial number that the document is applicable to must be added as a separate row. Only serial numbers currently in the system need to be added here. When a new serial number is added to the system, you will be notified if an SB or AD is applicable.

### PartNumber (Alphanumeric, 30 characters)
The PartNumber field is used to define the part number applicability of the document specified in the spreadsheet row. This means that each specific part number that the document is applicable to must be added as a separate row. Only part numbers currently in the system need to be added here. When a new part number is added to the system, you will be notified if an SB or AD is applicable.

### Software (Alphanumeric, 50 characters)
The Software field is used to define the part number of the software which defines the applicability of the document. This means that each specific software part number must be added as a separate row. Only software part numbers currently in the system need to be added here. When a new software part number is added to the system, you will be notified if an SB or AD is applicable.

### SoftwareVersion (Alphanumeric, 50 characters)
The SoftwareVersion field is used to define the version number of the software which defines the applicability of the document. This means that each specific software version must be added as a separate row. Only software versions currently in the system need to be added here. When a new software version is added to the system, you will be notified if an SB or AD is applicable.

### DocumentType (Alphanumeric, 10 characters) `required`
The DocumentType field is used to define the type of document. The document type entered here must already exist in the system. This can be verified or updated in System & Configuration > Configuration > Master Data > Tech Records > Publication Type. The document types 'SB' and 'AD' exist by default.

### DocumentCategory (Alphanumeric, 10 characters) `required`
The DocumentCategory field is used to define the category of the document. The category entered here must already exist in the system. This can be verified and updated in System & Configuration > Configuration > Master Data > Tech Records > Publication Category. The category type 'Serial' exists by default and this default type contains the document types 'SB' and 'AD' mentioned above.

### ATA (Alphanumeric, 12 characters)
The ATA field is used to define the ATA chapter under which the document falls. ATA chapters defined here must already exist in the system. Thi can be verified and updated in Fleet Management > Maintenance Planning > ATA List

### PublicationReference (Alphanumeric, 35 characters)
The PublicationReference field is used to enter the document reference. This is the reference printed on the document, rather than the 'Library Number' which is a system generated tracking number.

### Title (Alphanumeric, 100 characters) `required`
The Title field is used to define the title of the document. This title is displayed throughout the system when a publication is referenced.

### OEM (Alphanumeric, 255 characters) `required`
The OEM field is used to define the body which issued the document. This OEM must exist in the system and can be verified and updated in Fleet Management > Tech Library > OEM Enquiry

### PublicationStatus (Alphanumeric, 10 characters) `required`
The PublicationStatus field is used to define the status of the document being imported. This status must exist in the system and can be varified and updated in System & Configuration > Configuration > Master Data > Tech Records > Publicatioin Status. The statuses of 'Active' and 'Being Checked' exist by default.

### RevisionNo (Alphanumeric, 10 characters) `required`
The RevisionNo field is used to define the latest revision number of the document being imported. This is a free-text field and (along with the 'RevisionType', 'RevisionDate' and 'RevisionDescription' fields) will be used to create the document revision within the system. This data should be available on the physical document being imported but in the case of a document not having a revision, a value must still be enterd i.e. '0' or 'Initial'.

### RevisionType (Alphanumeric, 5 characters) `required`
The RevisionType field is used to define the type of revision being added as described in 'RevisionNo'. The type must exist in the system and can be verified and updated in System & Configuration > Configuration > Master Data > Tech Records > Publication Revision Type. The types 'MR' (Master Revision) and 'TR' (Temporary Revision) exist by default.

### RevisionDate (Date/Time) `required`
The RevisionDate field is used to define the date upon which the revision being added as described in 'RevisionNo' was actioned. The date may be enterd in any conventional standard based upon the location of the system server i.e. London: 16/11/2010, New York: 11/16/2010

### RevisionDescription (Alphanumeric, 100 characters)
The RevisionDescription field is used to define the description associated with the revision itself and not the document i.e. 'Initial Revision', 'Changed applicability to include S/N 1787'

### ApplicabilityStatus (Alphanumeric, 40 characters) `required`
The field ApplicabilityStatus is used to define the applicability of the document to the specified model, part number and/or serial number specified. This applicability status must exist in the system and may be verified and updated in System & Configuration > Configuration > Master Data > Tech Records > Publication Applicability Status. The statuses of 'NA' (Not Applicable), APPLIC (Applicable) and AW (Awaiting Review) exist by default. 

### ParagraphSubpartIdentifier (Alphanumeric, 4000 characters)
The field ParagraphSubpartIdentifier is used to define the paragraph which has been split out from the overarching document (if required) i.e. 'Para 1', '(1.2.1)'. This field is free-text. Each paragraph must be included on a seperate row in the spreadsheet.

### ComplianceTaskType (Alphanumeric, 4000 characters)
The field ComplianceaskType is used to define the type of task that is detailed to be carried out by the document i.e. 'Imspection', 'Modification'. The type must exist in the system and may be verified and updated in System & Configuration > Configuration > Master Data > Tech Records > Compliance Task Type. 

### ParagraphSubpartDescription (Alphanumeric, 4000 characters)
The field ParagraphSubPartDescription is used to define the description of the paragraph identified in ParagraphSubpartIdentifier. This is a free-text field and is most commonly used to list out the exact wording of the paragraph.

### EffectiveDate (Date/Time)
The field EffectiveDate is used to define the effactive date listed on the document. The date entered here is then available to be be selected when defining the EO Task Card associated with the document for scheduling purposes. The date may be enterd in any conventional standard based upon the location of the system server i.e. London: 16/11/2010, New York: 11/16/2010

### EOTaskNumber (Alphanumeric, 40 characters)
The field EOTaskNumber is used to define the EO task cards that are linked to the document. These EO task cards must exist in the system and may be verified and updated in Fleet Management > Mantenance Planning > Card Enquiry. Multiple cards may be listed in a comma-seperated list.