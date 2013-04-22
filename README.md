monkey
======

### Ii is a plugin for convenient use of mongodb.

you can find methods just like: insert_collection, update_collection, find_collection, delete_collection, auto_dereference and other,
I hope someone can do me a favor to perfect it.

### introduction
  mongo is a no sql database, we can operate the data without the shackles of the structure,which means you can insert
data with different structure(of course it should be json-format), but is it a resonable thing for that? If it is ,doesn't
it mean the structural design of the database should be removed from the development process ? What a damn thing? right?
so here, I choose to maintain the integrity of the database structure. That's why the plugin was developped.
 
   when you insert a collection which structure is not the same as the document, it will throw the exception of difference
.so before developping, the structure of database should be defined in mon_config.py. just like:
 
  
    COLLECTION_NAME = {
    'name':
        {'length': 0,
         
          'country' : ''
           
        }
      }
   
   
  Above, we defined a document "name", which has a colletion with two keys: "length" and "country", if you do the following operation:
  db.insert_collection('name', {'length' : 0}), it will throw the exception.

        the mon_config.py contains the defenition of one of my project.
