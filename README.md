# FINDING MISSING PEOPLE

## Introduction

An online portal for family members and friends to register a new missing child.
And on the other hand people can add information about children they find lost.
They can upload photo proofs to back their claims about the whereabouts of a missing child.
Missing children's data, including last seen and last appearance, are sourced from C.com master data.

Users can generate a report to show several attributes of their yard: sustainability, edibility, native, etc.  This report can be used to help sell the positive attributes of the house.

Users can interact with FindingMissingPeople using either a set of RESTful service endpoints, or a simple UI, or both.

## Storyboard

[Storyboard in Invision](https://projects.invisionapp.com/prototype/Plant-Diary-ck0bict0n005bqh01aaeu8tuu)

## Requirements

1. As a homeowner, I want to be able to catalog my specimens, so that I will remember what I planted.

### Example 

**Given**:  A feed of plant data are available

**When**: The user/service selects plant Eastern Redbud

**When**: The user/service adds latitude 39.74 to an Eastern Redbud specimen

**Then**: The user’s/service’s Eastern Redbud will be saved with 39.74 latitude.

### Example 

**Given**: Specimen data are available

**When**: The user/service searches for “kajsd;luaopuidfjo;aj;sd”

**Then**: My Plant Diary will not return any results, and the user will not be able to save the specimen.

### Example 

**Given**: Specimen data are available, and specimen 83 is Eastern Redbud.

**When**: The user/service searches for the specimen with ID “83”

**Then**: My Plant Diary will return exactly one specimen record for "Eastern Redbud".

### Example 

**Given**: Specimen data are available

**When**: The user/service posts a new Specimen object with valid attributes "latitude=39.74, longitude=-84.51"

**Then**: MyPlantDiary will create a new specimen for this record, and will return this new specimen object.

2.	As a homeowner, I want to be able to upload photos of my plant at any time.

### Example 

**Given**: The user is logged in and has selected a previously-saved Eastern Redbud specimen

**When**: The user uploads a valid 640*480 photo of an Eastern Redbud Flower

**Then**: The 640*480  photo of an Eastern Redbud flower will be saved to the specimen profile, and can be viewed later.

### Example 

**Given**: The user is logged in and has selected a previously-saved Eastern Redbud specimen

**When**: The user uploads a 100GB photo

**Then**: The photo will be rejected as too large.

### Example 

**Given**: The user is logged in and has selected a previously-saved Eastern Redbud specimen

**When**: The user uploads a 1600*1200 photo

**Then**: The photo will be resized automatically to 640*480

**Then**: The 640*480 photo will be shown to the user.

3)	As a homeowner, I want to generate a report of the sustainability of my yard.
### Example 

**Given**: The user has a valid account and specimens associated to that account.

**When**: The user runs a report.

**Then**: The user will see a report of plants, dates, native, edible, and sustainability rating.

### Example 

**Given**: The user has a valid account and no specimens associated to that account.

**When**: The user runs a report.

**Then**: The user will see an error, indicating no data available for report.

## Class Diagram

![My Plant Diary Class Diagram](https://github.com/discospiff/SpringBootMicroservicesWithIntelliJIDEA/blob/master/PlantDiaryClassDiagram.drawio.png)

### Class Diagram Description 

## JSON Schema

This is what we plan to export to another app.


> {
>  "type" : "object",
>  "properties" : {
>    "name" : {
>      "type" : "string"
>    },
>    "age" : {
>      "type" : "integer"
>    }
>  }
> }
## Team Memebers and Roles

UI Specialist: Brandan Jones
Business Logic/Persitence: Brandan Jones
DevOps/Product Owner/Scrum Master/GitHub Admin: Brandan Jones

## Milestones

[Milestone 1](https://github.com/discospiff/SpringBootMicroservicesWithIntelliJIDEA/milestone/1)
