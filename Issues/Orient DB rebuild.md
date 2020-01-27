
     *Connect Orient DB*

/usr/bin/java -jar  -Xms1g -Xmx4g -jar  /opt/nexus/lib/support/nexus-orient-console.jar

       Connect to local DB component
       
CONNECT plocal:/opt/sonatype-work/nexus3/db/component admin admin
 
     * Delete current database*
     
drop database
      
      * Create a new database*

create database plocal:/opt/sonatype-work/nexus3/db/component

      *Import the exported component DB*
      
import database component-export.json.gz

     *Rebuild the Database*
     
REBUILD INDEX * 
