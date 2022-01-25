# [YAML](https://www.youtube.com/watch?v=IA90BTozdow) Notes

## Introduction

**Markup Language:** A computer language that consists of easily understood keywords, names, or tags that help format the overall view of a page and the data it contains

**YAML:** YAML Ain't Markup Language 
- It is basically a human readable language 
- It is data format which is used to exchange data
- It is similar to XML & JSON
- It is a data serialization language
- In YAML we can store only data, and not commands

**Serialization** is the process of converting an object into a stream of bytes to store the object or transmit it to memory, a database, or a file. 

Its main purpose is to save the state of an object in order to be able to recreate it when needed. 

The reverse process is called **Deserialization.**

**Data Serialization:** is the process of converting data objects i.e regions of storage that contain certain values present in complex data structures, into a stream of bytes for storage and transmission purposes.

**Why it is known as YAML Ain't Markup Language?** <br/>
YAML stores data as well as documents

Extension of YAML: `.yaml` `yml`

**Uses of YAML:**
- Configuration files, like Docker, Kubernetes
- Logs
- Caches

**Benefits of YAML:**
- Simple and easy to read
- It has a strict syntax; identation is important
- Easily convertible to JSON, XML
- YAML is used by most languages
- More powerful when representing complex data
- Parsing is easy and various tools are available

**NOTE:** 
- YAML is case-sensitive
- Identation is important, otherwise it will throw an error
- --- is used to represent different types of documents.
- ... is used to end a document.
- YAML doesn't support multiline comments

## Demo of YAML File

```
# Key-Value Pairs
"apple": "I am a red fruit"
  1: "this is my roll no."
---
#Lists
- apple
- mango
- banana
- Apple
---
#Block-Style
cities:
 - new delhi
 - mumbai
 - kolkata
---
cities: [new delhi, mumbai, kolkata]
---
{mango: "yellow fruit", age:56}
...
```

## Data Types in YAML

```
# String variables
myself: Sadab Halim
fruit: "apple"
job: 'student'

bio: |
My name is Sadab,
I am currently learning DevOps

# Write a single line in multiple lines
message: >
this will
all be
in one single line

# same as
message: this will all be in one single line

number: 5473
marks: 98.76
booleanValue: no # n, N, false, False, FALSE

# specify the type
zero: !!int 0
positiveNum: !!int 45
negativeNum: !!int -45
binaryNum: !!int 0b11001
octalNum: !!int 06574
hexa: !!int 0x45
commaValue: !!int +540_000 # 540,000
exponential Numbers: 6.023E56

#floating point numbers
marks: !!float 56.89
infinite: !!float .inf
not a num: .nan

#boolean
booleanValue: !!bool True

#string
message: !!str this will all be in one single line

#null
surname: !!null Null # or null NULL ~
~: this is a null key

#dates and time
date: 2022-01-25
india time: 2022-01-25T16:18:43.10 +5:30
no time zone: 2022-01-25T16:18:43.10 
```

## Advanced Data Types in YAML

```
student: !!seq
 - marks
 - name
 - roll_no
 
 # like this also
 cities: [new delhi, mumbai]
 
 # some of the keys of the seq will be empty
 # sparse seq
 sparse seq:
  - hey
  - how
  -
  - Null
  - sup
  
 # nested sequence
 -
  - mango
  - apple
  - banana
 - 
  - marks
  - roll_no
  - date
  
 # key: value pairs are called maps
 !!map
 
 #nested mappingsL map within a map
 name: Sadab Halim
 role:
  age: 21
  job: student
 
 # same as
 name: Sadab Halim
 role: (age: 21, job: student)
 
 #pairs: keys may have duplicate values
 # !!pairs
 
 pair example: !!pairs
 - job: student
 - job: developer
 
 # same as
 pair example: !!pairs [job: student, job: teacher]
 # this will be an array of hashtables
 
 # !!set will allow you to have unique values
 names: !!set
  ? Sadab
  ? Aarav
 
 # dictionary !!omap
 people: !!omap
  - Sadab:
     name: Sadab Halim
     age: 21
  - Aarav:
     name: Aarav OP
     age: 20
  
 # reusing some properties using anchors
 likings: &likes
  fav fruits: mango
  dislikes: grapes
  
 person1:
  name: Sadab Halim
  <<: *likes
  
 person2:
  name: Aarav
  <<: *likes
  dislikes: berries
  
 # this will look like
 person2:
  name: Aarav
  fav fruits: mango
  dislikes: berries
```

## Real World Example

XML Example
```
<?xml version="1.0" encoding="UTF-8"?>
<School name="DPS" principal="Someone">
  <Students>
    <Student>
      <rno>13</rno>
      <name>Sadab</name>
      <marks></marks>
    </Student>
  </Students>
</School>
```

JSON Example
```
{
  "School": [
      {
          "name": "DPS",
          "principal": "Someome",
          "Students": [
              {
                  "rno": 13,
                  "name": "Sadab Halim",
                  "marks": 93
              }
          ]
      }
  ]
}
```

YAML Example
```
---
School:
- name: DPS
  principal: Someone
  Students:
  - rno: 13
    name: Sadab Halim
    marks: 93
```

Site to check if your YAML files are correct or not: [Click here](https://itnext.io/how-to-validate-kubernetes-yaml-files-9a17b9a30f08)

## YAML DevOps Tools
- [Datree](https://datree.io/?utm_source=youtube&utm_medium=influencer&utm_campaign=kunal)
- [Monokle](https://monokle.kubeshop.io/)
- [Lens](https://k8slens.dev/?utm_source=CloudNativeHackathon&utm_medium=Youtube&utm_campaign=DevOpsBoot)
