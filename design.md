### Scenarios

[System Design](https://medium.com/@systemdesign)
* ```Messaging``` : Facebook messanger or Whatsapp
* ```Media Streaming``` : [Youtube or Netflix](https://medium.com/double-pointer/system-design-interview-video-streaming-service-e-g-netflix-or-youtube-design-adc2402e54a1)
* ```File Sharing```:[png diagram](https://systemdesignprimer.com/assets/images/dropbox-system-design.png):
  * [Dropbox](https://www.youtube.com/watch?v=PE4gwstWhmc) :
      * [ACID](https://www.ibm.com/docs/en/cics-ts/5.4?topic=processing-acid-properties-transactions): Accuracy, consistancy, isolation, durablity
      * microservices: blocksyncService(rsync), metadataService(https/REST)+sql-db, notificationService(websocket), chunkService(rsync)
      * LoadBalancer
      * Availiblity
      * security
      * DB Cache
      * Analytics Service: service load, no. of requests from channels/sec, bandwidth at user end, 
      * Alarm service
      * Authentication policy
      * Not necessary to be very real time, so we can save some infrastructure cost here
  * google drive or google photos
* ```Social Networking``` : Facebook, twitter or instagram
* Others: Uber

### common things
* Design to interface for smoke test automations and mock server interation in labs
* Stress test simulation system
### How to crack
* [Interview questions](https://www.geeksforgeeks.org/top-10-system-design-interview-questions-and-answers/)
* [how to do](https://www.geeksforgeeks.org/how-to-crack-system-design-round-in-interviews/?ref=lbp)
* [Interview day prepration](https://www.geeksforgeeks.org/5-common-system-design-concepts-for-interview-preparation/?ref=lbp)

### Design backend nosql DB:
To work with backend analytics, we might use the services from AWS or we can have inhouse servers as this is not for the end user but for organization to use data for development and business decisions. So, in that case, the domain could be taken from AWS, and ultimately data could be routed to in campus servers. Or if we want to keep it simple, let it be hosted in AWS server itself. We would need fluentd sitting in parlal with web microservice, and listening the clickstream, event data and logs and building buffer and writing to nosql db. This is for performance improvements.    

* Use [fluentd](https://stackoverflow.com/a/13428282/6146338) for:
  * Event data
  * clickstream
  * application logging
* Save the data in MongoDB kind of NoSQL db
* Use user onboarding services with https protocol based on REST API
  * Save into SQL DB

* For social media interaction
  * Implement relational DB schema, high performance for related DB in social media
* Using S3 like simple storage for media contents
  * Video
  * Image
  * Files
* Look for availiblity zone
  * Data cache
  * DB cache
  * User onboarding
  * Search
