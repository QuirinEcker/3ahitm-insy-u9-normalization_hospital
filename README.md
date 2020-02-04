# Übung 09 - Hospital Normalformen



## 1. Functional Dependencies

Station# &rarr; Station

Station &rarr; Station#

NurseName &rarr; Station#

DoctorName &rarr; Station#

Room# &rarr; NoOfBeds, PatientName, Disease, DoctorName, NurseName

Disease, Patient# &rarr; Station#, Station, Room#, NoOfBeds, Patient, DoctorName, NurseName

## 2. Normalform 1

|Station#|Station|Room#|NoOfBeds|Patient#|PatientLastName|PatientFirstName|Disease|DoctorLastName|DoctorFirstName|NurseLastName|NurseFirstName
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|1|General Medicine|1|2|1|Maier|Hans|Appendicitis|Mader|Hugo|Schober|Susi|
|1|General Medicine|1|2|2|Schmid|Peter|Broken Leg|Mader|Hugo|Schober|Susi|
|1|General Medicine|1|2|2|Schmid|Peter|Broken Arm|Mader|Hugo|Schober|Susi|
|1|General Medicine|2|1|3|Mueller|Sepp|Appendicitis|Dachs|Franz|Schober|Susi|
|2|Opthalmology|1|2|4|Stein|Berta|Grey Cateract|Weber|Karl|Holz|Fritz|
|2|Ophthalmology|1|2|5|Hein|Hanna|Detached Retina|Weber|Karl|Holz|Fritz|
|2|Ophthalmology|2|1|6|Fisch|Olga|Green cateract|Weber|Karl|Moser|Anna|
|2|Ophthalmology|2|1|6|Fisch|Olga|Conjunctivitis|Weber|Karl|Moser|Anna|

## 3. Normalform 2

### Patient

|Patient#|Room#|NoOfBeds|PatientLastName|PatientFirstName|DcotorLastName|DoctorFirstName|NurseLastName|NurseFirstName|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|

|Disease|Patient#|
|:-:|:-:|

### 4. Normalform 3

|Station#|Station|
|:-:|:-:|

|Patient#|PatientFirstName|PasientLastName|DoctorFirstName|DoctorLastName|NurseFirstName|NurseLastName|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|

|Room#|Station#|NoOfBeds|
|:-:|:-:|:-:|

