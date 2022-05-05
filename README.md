## System Design
    
#### System Design stages
* Understanding the problem
  * set the objective, make it clear and don't deviate throughout
* Collect the requirements
  * be detailed oriented keep asking for every nook and cranny, be crystal clear.
* Scope
  * define what you will ultimately building for such as setting up resource capacity based on requirement collection
    such as volume, etc.
* Listing technical requirements
  * What all are ultimately required, ask for numbers so to design accordingly
* Limitations
* High level design
  * start desiging based on above notes taken
* Implementation
  * go into detailed design, such as which database, which service, peak hour details, consider different scenario walkthrough

#### System Design fundamentals
* Vertical scaling
  * to extend the use of available resources
* Horizontal scaling
  * to have system with more features
* Micro-services
  * losely couppled services independently mantained and indep. testable
* Distributed system
  * To serve from different network so one failure is no were imacting the other one
* Load balancing
  * once having distributed system, they can be load balanced so to effectively utilize distributed resources
* Error logging and matrix
  * to monitor and fix the alarms and issues in general such as overshooting to resource capacity
* Decoupled system
  * so change in any one would not affect the other one 
   
#### System Design Consideration
* Keep an eye on possible modularization
* Reduce resource requirements
  * reduce app install size
  * Reduce app upgrade bandwidth
  * Reduce data consumption
  * Reduce battery usage
* Reduce development effort
  * Continuous integration to run faster
  * Unit test could be performed
  * Easy to scale
  * [Easy to test](https://www.youtube.com/watch?v=PZBg5DIzNww?start=80)
  * Easy to distribute among team
* Isolate the problems
  * Interface to sandbox
  * Interface to sandbox impact
* Dependency
  * Single source of truth
  * Battery dependency
  * Other interface dependency
* Access and system requirements
  * Permissions (root permission for file access)
