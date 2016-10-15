# Hillary Clinton's Emails

On Monday, August 31, the State Department released nearly 7,000 pages of Clinton's heavily redacted emails (its biggest release of emails to date).

The documents were released by the State Department as PDFs. Kaggle cleaned and normalized the released documents and are hosting them for public analysis. 

Data source: [Kaggle](https://www.kaggle.com/kaggle/hillary-clinton-emails)

## Files 

Aliases.csv (20.01 KB)

    Id - unique identifier for internal reference
    Alias - text in the From/To email fields that refers to the person
    PersonId - person that the alias refers to

database.sqlite (7.05 MB)

This SQLite database contains all of the tables (Emails, Persons, Aliases, and EmailReceivers) with their corresponding fields. You can see the schema and ingest code under scripts/sqlImport.sql

EmailReceivers.csv (117.42 KB)

    Id - unique identifier for internal reference
    EmailId - Id of the email
    PersonId - Id of the person that received the email

Emails.csv (25.6 MB)

    Id - unique identifier for internal reference
    DocNumber - FOIA document number
    MetadataSubject - Email SUBJECT field (from the FOIA metadata)
    MetadataTo - Email TO field (from the FOIA metadata)
    MetadataFrom - Email FROM field (from the FOIA metadata)
    SenderPersonId - PersonId of the email sender (linking to Persons table)
    MetadataDateSent - Date the email was sent (from the FOIA metadata)
    MetadataDateReleased - Date the email was released (from the FOIA metadata)
    MetadataPdfLink - Link to the original PDF document (from the FOIA metadata)
    MetadataCaseNumber - Case number (from the FOIA metadata)
    MetadataDocumentClass - Document class (from the FOIA metadata)
    ExtractedSubject - Email SUBJECT field (extracted from the PDF)
    ExtractedTo - Email TO field (extracted from the PDF)
    ExtractedFrom - Email FROM field (extracted from the PDF)
    ExtractedCc - Email CC field (extracted from the PDF)
    ExtractedDateSent - Date the email was sent (extracted from the PDF)
    ExtractedCaseNumber - Case number (extracted from the PDF)
    ExtractedDocNumber - Doc number (extracted from the PDF)
    ExtractedDateReleased - Date the email was released (extracted from the PDF)
    ExtractedReleaseInPartOrFull - Whether the email was partially censored (extracted from the PDF)
    ExtractedBodyText - Attempt to only pull out the text in the body that the email sender wrote (extracted from the PDF)
    RawText - Raw email text (extracted from the PDF)

Persons.csv (9.94 KB)

    Id - unique identifier for internal reference
    Name - person's name
