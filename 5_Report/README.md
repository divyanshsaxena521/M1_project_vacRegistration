# M1_project_vacRegistration
## content
* Introduction
* workflow
* Folder structure
* Aim
* Input, process, output.
* Instruction to execute.
* Folder description.
* Refernces

## Introduction
As we all know that the covid cases are increasing day by day in India and thus the tracking became very complicated. and we all know very well the population of india is a very high and due to this vaccination is a very big deal to be executed.

## workflow 
| Codacy | Codiga | CI | Unity |
| --- | --- | --- | --- |
|[![Codacy Badge](https://app.codacy.com/project/badge/Grade/8f714b3f43564efb9d2fca62de1d50f0)](https://www.codacy.com/gh/divyanshsaxena521/M1_project_vacRegistration/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=divyanshsaxena521/M1_project_vacRegistration&amp;utm_campaign=Badge_Grade)|![codica code quality score](https://api.codiga.io/project/30942/score/svg)![codica code grade](https://api.codiga.io/project/30942/status/svg)|

## Folder structure
| 0_Certificates | 1_Requiremnts | 2_Design | 3_Implementation | 4_TestplanAndOutput | 5_Report | 6_ImagesAndVideos | 7_Others |
| --- | --- | --- | --- | --- | --- | --- | --- |
| certification details of the student | Documents detailing requirements and research | Documents related to design of model | All codes and make file | test plans with requirements | summary of all the folders | screenshots of working projects | refrences and supporting documents |

## Aim
* Easy and smooth vaccination registration process.
* Reduction of data traffic in the main server.
* Localization of operation of registration and verification.
## Input
* Pre-registered list of users for vaccination.
* New registration of users for vaccination.
## Process
* Appointment of pre registered users and verification of documents.
* Verification of pre registered users.
* New registrations addition to the vaccinated log.
* Total vaccine consumption is tracking.
## Output
* Vaccinated users data log is updated and new registrations are added to the end of the pre data list.
* printing of list of vaccinated user with total vaccine consumed.

 ## Instructions to execute
1. clone my repository "M1_PROJECT_VACREGISTRATION"
2. open terminal and select "WSL"
3. Run "make run" command in terminal for main code execution
4. Run "make run_test" command in terminal for test code execution

## Folder description
| Folder | Description |
| --- | --- |
| inc | Contains header files |
| src | Contains additional source file for compilation |
| test | Contains unit testing files 


## References
|[Getting started ](https://youtu.be/ddYg9wd4BD0)|[code support ](https://www.upgrad.com/blog/c-projects-on-github-for-programmers/)|

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

# Architecture/Design
## Flow chart
![Flowchart1 (1)](https://user-images.githubusercontent.com/89698000/132567227-09aa32d3-9fd8-46e0-ad41-43367582048a.jpg)
## UML Use case
![Untitled Workspace (5)](https://user-images.githubusercontent.com/89698000/132359625-59a60ead-ddf0-48d5-a03b-39c03fbb2a1d.jpg)

# Implementation

## Instructions to execute

1. Run "make run" command in terminal for main code execution
2. Run "make run_test" command in terminal for test code execution

| Folder | Description |
| --- | --- |
| inc | Contains header files |
| src | Contains additional source file for compilation |
| test | Contains unit testing files |

# TEST PLAN AND OUTPUT 
## High Level Test Plan
| Test ID | Description | Input | Expected output | Actual Output |
| --- | --- | --- | --- | --- |
| 01 | Check patient registration status | 123 (aadhar no) | {-1} |  (not found) |
| 02 | Check patient registration status | 123 (aadhar no) | {0,1} |  (found) |
| 03 | Check patient vaccination status | 3 (patient id) | {>0} | (vaccinated) |


## Low Level Test Plan
| Test ID | Description | Input | Expected output | Actual Output |
| --- | --- | --- | --- | --- |
| 01 | Check patient registration status | 125 (aadhar no) | 0 | 0 (registered, not vaccinated) |
| 02 | Check patient registration status | 130 (aadhar no) | 1 | 1 (registered, vaccinated) |
| 03 | Check patient vaccination status | 3 (patient id) | 1 | 1 (first dose) |
| 04 | Check patient vaccination status | 3 (patient id) | 2 | 2 (second dose) |
| 05 | Check patient vaccination status | 3 (patient id) | 3 | 3 (already vaccinated) |

# Final output AFTER RUNNING MAKE FILE
![Screenshot (109)](https://user-images.githubusercontent.com/98813747/152678646-51b2d074-3a5b-4de9-b131-2a69a3f78319.png)


## New user details saved
![Screenshot (104)](https://user-images.githubusercontent.com/98813747/152678541-4bddb345-bfcc-4f8a-8eb4-78aaeca292e3.png)

## Registered user details verifiction
![Screenshot (105)](https://user-images.githubusercontent.com/98813747/152678532-312fcc17-7c0b-4d42-b466-094413235b30.png)

### Select the vaccine type
![Screenshot (106)](https://user-images.githubusercontent.com/98813747/152678528-30c794d1-9bce-426c-b71a-8f893fca48fb.png)

## TEST CASES
![Screenshot (110)](https://user-images.githubusercontent.com/98813747/152678688-69869f69-62b6-46a0-b736-963c3c6fb12b.png)