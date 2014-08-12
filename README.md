
BackEnd
================== 

http://es.seedfinder.eu/api/
Output: JSON

Serivce Proxy (django possible)  

Frontend
================== 

Android App WebContainer +  Ember JS + Ember Data

seriveces list
================== 

```
api/v
     /strains  	          	GET		List all strains		
     /strains/{id}	      	GET		Get strain by id
     /breeders	          	GET     List all breeders
     /breeders/{id}	      	GET		Get breeder by id
     /plants		        GET     List all plants
     /plants		        POST	Create a new plant
     /plants/{id}	        GET		Get plant by id
     /plants/{id}/images  	GET		Get all images for a plant by id
     /plants/{id}	        PUT		Edit a plant by id
     /plants/{id}	        DELETE  Delete a plant
     /rooms		            GET     List all rooms
     /rooms		            POST	Create a new room
	 /rooms/{id}	        GET		Get room by id
     /rooms/{id}	        PUT		Edit a room by id
     /rooms/{id}	        DELETE  Delete a room
     /conteiners          	GET     List all conteiners
     /conteiners		    POST	Create a new conteiner
	 /conteiners/{id}	    GET		Get conteiner by id
     /conteiners/{id}	    PUT		Edit a conteiner by id
     /conteiners/{id}	    DELETE  Delete a conteiner 
```

Entities
==================

```
Strain
    id: Number
    name: String
    breeder: Breeder
    floweringDays: Number

    
Breeder
  id: Number
  name: String
  locate: Locate
  
Locate
  id: Number
  address: String
  geoLoc: { latitude: Double, Latitude: Double }
  
  
Image
  id: Number
  url: String
  label: String
  date: Date

Plant
  id: Number
  strain: Strain 
  tags: [String]
  container: Container
  room: Room
  floweringDate: Date
  label: String
  images: [Image]
  
Container
  id: Number
  name: String
  size: Number

Room
  id: Number
  name: String
  plants: [Plant]
```  



          
