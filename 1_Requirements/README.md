# Requirements
## Introduction
As we all know that the covid cases are increasing day by day in India and thus the tracking became very complicated. and we all know very well the population of india is a very high and due to this vaccination is a very big deal to be executed.
Due to multiple input and output commands on the server, it resulted in several slow running issues and crashes. 
The Aadhar details were used to allot the vaccines and hence it operated on a central server.
To avoid the use of central server for all commmands, a local server will be loaded with the vaccine-registered data. 
Local verification and completion of vaccination data will be processed locally and will be loaded back to the main server by the end of day.

The local server must store the data of around 100 people where the allocated online registration data will be loaded onto the local server of that local centre. 
Verification of the data is done based on the details provided by the patient. Once completed, the data of the vaccinated will be sent back for future use and reference.
### Advantages
* Smoother data handling.
* Pre data readily available for verification.
* Flexibility to add new registrations limited with server alloted memory.
### Disadvantages
* Cannot add large number of new registrations due to local server limitations.
* Encryption is not enabled to protect the data.
* OTP verification is not activated for new registrations.

## 4 W's and 1 H
### Who
* Patient who needs to be vaccinated.
### What
* Verify the details of the patient using the alloted data.
### When
* During the time alloted for vaccination.
### Where
* Local vaccination centre.
### How
* Online registration and on field verification using local server.
* 
## SWOT Analysis 
![SWOT analysis vaccine](https://user-images.githubusercontent.com/98813747/152639216-8898b23c-f447-45b3-9178-5063b4e7a349.png)
after SWOT analysis we concluded the following requirements. which are mentioned below:

## High Level Requirements
| ID | Description | 
| --- | --- |
| HL01 | System should be able to access pre loaded registration data for verification | 
| HL02 | User should be able to add new registrations |
| HL03 | System should recognize vaccinated patients| 
| HL04 | OTP generated verification for secure registration |
| HL05 | System should recognize invalid credentials| 
| HL06 | System should be updated with the time interval between two doses | 

## Low Level Requirement
| ID | Description |
| --- | --- |
| LL01 | Only new user must be given an option to select vaccine type | 
| LL02 | Total quantity of vaccines used must be shown by EOD | 
| LL03 | Full list of patients vaccinated must be set as output | 
| LL04 | Remaining and present stock of vaccines must be tracked |
| LL05 | Vaccine vials must be tracked for its use within a day | 
