monkey
======

### Ii is a plug-in for convenient to mongodb.

you can find method insert_collection, update_collection, find_collection, delete_collection, auto_dereference and other,
I hope someone can help to perfect it.

### introduction
  mongo is a no sql database, we can operate the data without the shackles of the structure,that means you can insert
data with different structure(of course it should be json-format), but it is a good thing for that? If it is true ,doesn't
it means the structure design of the database can be wiped out from the developping process ? what a damn thing?right?
so here, I choose to maintain the integrity of the database structure. that's why the plugin is developped.
 
   when you insert a collection which structure is not the same as the document, it will throw the exception of different
.so before developping, the structure of db should be defined in mon_config.py.just like:
 
 '''java
  
  COLLECTION_NAME = {
   
   'name':
    
        {'length': 0,
         
          'country' : ''
           
        }
         
   
  }
  '''
   
  Above, we defined a document name, which has a colletion with two keys:length and country, if you do the following operation
  db.insert_collection('name', {'length' : 0}), it will throw the exception, maybe you think it should be work, because 
  when the collection's keys' number are too many,it will be comlex to write the insert data format.It's my fault, ok.
