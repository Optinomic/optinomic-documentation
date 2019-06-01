# Optinomic | HL7 - Interface

Health Level 7 is a group of international standards for the exchange of data between healthcare organizations and their computer systems.

## Data-Import

All `*.hl7` files of the [specified](https://github.com/ottigerb/therapy-server/blob/master/api/clinics/config-suedhang.json#L193-L196) directory are processed and moved to a [specified](https://github.com/ottigerb/therapy-server/blob/master/api/clinics/config-suedhang.json#L193-L196) subdirectory `SAVE` (example) after processing. Both successful and incorrect processing will be moved to this `SAVE` subdirectory.

Administrators can check the status (what's imported; any errors?) at any time using the following query:

```SQL
SELECT * 
FROM patient_events
ORDER BY created_at DESC
```

In the case of an error, detailed information is displayed in the field `error`. Otherwise `error` remains empty.
Administrators thus have the option of correcting the error and, if necessary, importing the corresponding `*.hl7` file again.

## HL7 Ressources & Documentation

1. http://www.hl7.org/participate/toolsandresources.cfm
2. https://www.hl7.ch/hl7-standard/hl7-tools/
