# Medical Equipment Section (V2)

OID: 2.16.840.1.113883.10.20.22.2.23

LOINCs: #{"46264-8"}

Alias: medical-equipment

Entries Required: N/A

Internal ID: MedicalEquipmentSectionV2

[IG Link](https://www.hl7.org/ccdasearch/templates/2.16.840.1.113883.10.20.22.2.23.html)

## sample2

```json
{
  "resourceType" : "Procedure",
  "id" : "SOME-STRING",
  "code" : {
    "text" : "Biliary Stent, May 5, 2013",
    "coding" : [ {
      "code" : "103716009",
      "display" : "Stent Placement",
      "system" : "http://snomed.info/sct"
    } ]
  },
  "performed" : {
    "dateTime" : "2013-05-12"
  },
  "status" : "completed",
  "bodySite" : [ {
    "text" : "bile duct",
    "coding" : [ {
      "code" : "28273000",
      "display" : "bile duct",
      "system" : "http://snomed.info/sct"
    } ]
  } ],
  "subject" : {
    "id" : "patient",
    "resourceType" : "Patient"
  }
}
```

C-CDA Equivalent:
```xml
<section>
   <templateId root="2.16.840.1.113883.10.20.22.2.23" extension="2014-06-09"/>
   <templateId root="2.16.840.1.113883.10.20.22.2.23"/>
   <code codeSystem="2.16.840.1.113883.6.1"
          codeSystemName="http://loinc.org"
          displayName="display string"
          code="46264-8"/>
   <title>Medical Equipment Section (V2)</title>
   <text>
      <table border="1" width="100%">
         <thead>
            <tr>
               <td>ID</td>
               <td>Assigning Auth</td>
               <td>Code</td>
               <td>Date</td>
            </tr>
         </thead>
         <tbody>
            <tr>
               <td>No information</td>
               <td>2013-05-12</td>
            </tr>
         </tbody>
      </table>
   </text>
   <entry>
      <procedure classCode="PROC" moodCode="EVN">
         <templateId root="2.16.840.1.113883.10.20.22.4.14" extension="2014-06-09"/>
         <templateId root="2.16.840.1.113883.10.20.22.4.14"/>
         <id root="7df888b6-0268-1e62-ff60-ceb2f2f88630"/>
         <code codeSystem="2.16.840.1.113883.6.96"
                codeSystemName="http://snomed.info/sct"
                displayName="Stent Placement"
                code="103716009">
            <originalText>Biliary Stent, May 5, 2013</originalText>
         </code>
         <statusCode code="completed"/>
         <effectiveTime value="20130512"/>
         <targetSiteCode codeSystem="2.16.840.1.113883.6.96"
                          codeSystemName="http://snomed.info/sct"
                          displayName="bile duct"
                          code="28273000">
            <originalText>bile duct</originalText>
         </targetSiteCode>
      </procedure>
   </entry>
</section>
```

## sample1

```json
{
  "resourceType" : "List",
  "entry" : [ {
    "item" : {
      "focalDevice" : [ {
        "manipulated" : {
          "uri" : "#device"
        },
        "action" : {
          "text" : "Cardiac Pacemaker",
          "coding" : [ {
            "code" : "14106009",
            "display" : "cardiac pacemaker, device (physical object)",
            "system" : "http://snomed.info/sct"
          } ]
        }
      } ],
      "performed" : {
        "dateTime" : "2013-05-12"
      },
      "resourceType" : "Procedure",
      "contained" : [ {
        "udiCarrier" : [ {
          "deviceIdentifier" : "(01)51022222233336(11)141231(17)150707(10)A213B1(21)1234",
          "issuer" : "https://www.fda.gov/"
        } ],
        "patient" : {
          "resourceType" : "Patient",
          "id" : "patient"
        },
        "id" : "device",
        "resourceType" : "Device"
      } ],
      "status" : "completed",
      "id" : "SOME-STRING",
      "code" : {
        "text" : "Biliary Stent, May 5, 2013",
        "coding" : [ {
          "code" : "103716009",
          "display" : "Stent Placement",
          "system" : "http://snomed.info/sct"
        } ]
      },
      "bodySite" : [ {
        "text" : "bile duct",
        "coding" : [ {
          "code" : "28273000",
          "display" : "bile duct",
          "system" : "http://snomed.info/sct"
        } ]
      } ],
      "subject" : {
        "id" : "patient",
        "resourceType" : "Patient"
      }
    }
  } ],
  "id" : "SOME-STRING",
  "status" : "current",
  "mode" : "snapshot"
}
```

C-CDA Equivalent:
```xml
<section>
   <templateId root="2.16.840.1.113883.10.20.22.2.23" extension="2014-06-09"/>
   <templateId root="2.16.840.1.113883.10.20.22.2.23"/>
   <code codeSystem="2.16.840.1.113883.6.1"
          codeSystemName="http://loinc.org"
          displayName="display string"
          code="46264-8"/>
   <title>Medical Equipment Section (V2)</title>
   <text>
      <table border="1" width="100%">
         <thead>
            <tr>
               <td>ID</td>
               <td>Assigning Auth</td>
               <td>Code</td>
               <td>Date</td>
            </tr>
         </thead>
         <tbody>
            <tr>
               <td>No information</td>
               <td>No information</td>
            </tr>
         </tbody>
      </table>
   </text>
   <entry>
      <organizer classCode="CLUSTER" moodCode="EVN">
         <templateId root="2.16.840.1.113883.10.20.22.4.135"/>
         <id root="7df888b6-0268-1e62-ff60-ceb2f2f88630"/>
         <component>
            <procedure moodCode="EVN" classCode="PROC">
               <templateId root="2.16.840.1.113883.10.20.22.4.14" extension="2014-06-09"/>
               <templateId root="2.16.840.1.113883.10.20.22.4.14"/>
               <id root="7df888b6-0268-1e62-ff60-ceb2f2f88630"/>
               <code codeSystem="2.16.840.1.113883.6.96"
                      codeSystemName="http://snomed.info/sct"
                      displayName="Stent Placement"
                      code="103716009">
                  <originalText>Biliary Stent, May 5, 2013</originalText>
               </code>
               <statusCode code="completed"/>
               <effectiveTime value="20130512"/>
               <targetSiteCode codeSystem="2.16.840.1.113883.6.96"
                                codeSystemName="http://snomed.info/sct"
                                displayName="bile duct"
                                code="28273000">
                  <originalText>bile duct</originalText>
               </targetSiteCode>
               <participant typeCode="DEV">
                  <participantRole classCode="MANU">
                     <templateId root="2.16.840.1.113883.10.20.22.4.37"/>
                     <id root="913f9c49-dcb5-44e2-087c-ee284f4a00b7"/>
                     <id root="2.16.840.1.113883.3.3719"
                          extension="(01)51022222233336(11)141231(17)150707(10)A213B1(21)1234"
                          assigningAuthorityName="https://www.fda.gov/"/>
                     <playingDevice>
                        <code codeSystem="2.16.840.1.113883.6.96"
                               codeSystemName="http://snomed.info/sct"
                               displayName="cardiac pacemaker, device (physical object)"
                               code="14106009">
                           <originalText>Cardiac Pacemaker</originalText>
                        </code>
                     </playingDevice>
                     <scopingEntity>
                        <id root="2.16.840.1.113883.3.3719"/>
                     </scopingEntity>
                  </participantRole>
               </participant>
            </procedure>
         </component>
      </organizer>
   </entry>
</section>
```