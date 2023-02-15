# Event Planning System
> Purpose: To Track events, manage Guest Lists and Invitations, Budget Planning


### Event Requiremtns
1. Event Date
2. Event Name
3. Event Location
4. Guest List
5. Budget 
6. Notes


### Events Data in Tablur Format
|   Event Date  |   Event Name      |  Event Location    |   Guest List  |   Budget  |   Notes  |
|  ------------ | --------------    | ----------------   | ------------- | --------- | -------- |
|  28-02-2023   | Marriage Function | Gachibowli Gardens |      600      |   1500000 |          |
|  01-05-2023   | May Day           | Comrad Buildings   |      150      |   200000  |  Organize comrad songs        |


### Storing Data in MySql DB

#### Steps
1. Create a Database
2. Create a table with column defination
  ```sql
  CREATE TABLE events (
   event_date DATE,
   event_name VARCHAR(100),
   event_location VARCHAR(150),
   guest_list INT,
   budget FLOAT,
   notes TEXT
  )
  ```

3. **C**reate a event record in table
  ```sql
  INSERT INTO events (
    event_date,
    event_name,
    event_location,
    guest_list,
    budget
  ) VALUES (
    "28-02-2023",
    "Marriage Function",
    "Gacchibowli Garders",
    600,
    1500000
  )
  ```
4. **R**ead events record from the table
  ```sql
  SELECT * from events
  ```
  
  ```sql
  SELECT * from events WHERE event_name="Marriage Function"
  ```
5. **U**pdate event record 
  ```sql
  UPDATE events
  SET
    guest_list=800,
    budget=1800000
   WHERE
    event_name="Marriage Function"
  ```
6. **D**elete completed event
  ```sql
  DELETE FROM events WHERE event_name="Marriage Function"
  ```



### Events data in label wise (key: value)
-------------------------------------------
Event Date      : 28-02-2023

Event Name      : Marriage Function

Event Location  : Gachibowli Gardens

Guest List      : 600

Budget          : 1500000

Notes           : 

-------------------------------------------
Event Date      : 01-05-2023

Event Name      : May Day 

Event Location  : Comrad Buildings

Guest List      : 150

Budget          : 200000

Notes           : Organize comrad songs


### Sample Label and Values for a Person
Name: Syed Zakeer Hussain

City: Guntur

Job: Developer

Married: Yes

Kids: 2



## JSON (**J**ava**S**cript **O**bject **N**otation)
> Popular format for storing and exchanging data. 

#### JSON Syntax
```json
  {
    "key": "value",
    "key2": "value2"
  }
```

#### Sample JSON Data
```json
{
  "Name" : "Syed Zakeer Hussain",
  "Location" : "Guntur",
  "Kids": 2
}
```


#### Event Data in JSON Format
```json
{
  "EventDate": "28-02-2023",
  "EventName": "Marriage Function",
  "EventLocation": "Gacchibowli Gardens",
  "GuestList": 600,
  "Budget": 1500000,
  "Notes": ""
}
```










