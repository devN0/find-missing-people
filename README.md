# FINDING MISSING PEOPLE

## Introduction

An online portal for family members and friends to register a new entry for a missing child.
And on the other hand people can add information about children they find lost.
They can upload photo proofs to back their claims about the whereabouts of an abandoned child.
Missing children's data, including last seen and last appearance, are sourced from missingchildrendata.com master data.

Users can generate a report of current info about of a child: last location, last images, contact person info etc.

Users can interact with FindingMissingPeople using either a set of RESTful service endpoints, or a simple UI, or both.

## Requirements

1. As a guardian, I want to be able to register a new entry, so that I can track latest updates.

### Example 

**Given**:  A feed of missing children data are available

**When**: The user/service selects child John Doe
**When**: The user/service adds age 9 to John Doe.

**Then**: The user’s/service’s entry for a missing child with name John Doe will be saved with age 9.

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

2.	As an guardian, I want to be able to upload photos of my child at any time.

### Example 

**Given**: The user is logged in and has selected a previously-saved entry.

**When**: The user uploads a valid 640*480 photo of the child John Doe.

**Then**: The 640*480  photo of the child John Doe will be saved to the missing child's profile, and can be viewed later.

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

UI Specialist: Devendra Diwakar
Business Logic/Persitence: Devendra Diwakar
DevOps/Product Owner/Scrum Master/GitHub Admin: Devendra Diwakar

## Milestones
