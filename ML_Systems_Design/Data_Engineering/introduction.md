#### Data Engineering 

If data models describe the data in the real world, databases specify how the data should be stored on machines. 

two major types of processing: 
###### Transactional 
###### Analytical

#### Data Sources 
An ML system can work with data from many different sources. 


###### Note: 
Debugging ML systems is hard, it’s a common practice to log everything you can!!! 
This means that your volume of logs can grow very, very quickly. 

###### Log Analysis Tools
Splunk, Elasticsearch - Logstash, Datadog, Logz.io, etc

also note, Even though this is system-generated data, it’s still considered part of user data and might be subject to privacy regulations. 

#### First-party data
is the data that your company already collects about your users or customers. 

#### Second-party data  
is the data collected by another company on their own customers that they make available to you, though you’ll probably have to pay for it. 

#### Third-party data
companies collect data on the public who aren’t their direct customers.



#### Smart Phone Data - Now, its a opted service on most smartphones. 
Each phone used to have a unique advertiser ID. iPhones with Apple’s Identifier for Advertisers (IDFA) and Android phones with their Android Advertising ID (AAID)—which acted as a unique ID to aggregate all activities on a phone. 


#### Data Formats 

How do I store multimodal data, e.g., a sample that might contain both images and texts?

#### Data Serialization 
The process of converting a data structure or object state into a format that can be stored or transmitted and reconstructed later is data serialization. 

#### Data Formats 
Format	Binary/Text	Human-readable	Example use cases
JSON	Text	Yes	Everywhere
CSV	Text	Yes	Everywhere
Parquet	Binary	No	Hadoop, Amazon Redshift
Avro	Binary primary	No	Hadoop
Protobuf	Binary primary	No	Google, TensorFlow (TFRecord)
Pickle	Binary	No	Python, PyTorch serialization


#### JSON 
JSON, JavaScript Object Notation, is everywhere. Even though it was derived from JavaScript, it’s language-independent—most modern programming languages can generate and parse JSON. It’s human-readable. Its key-value pair paradigm is simple but powerful, capable of handling data of different levels of structuredness.

{
  "firstName": "Sandeep",
  "lastName": "Seeram",
  "isVibing": true,
  "age": 37,
  "address": {
    "streetAddress": "12 Ocean Drive",
    "city": "Visakhapatnam",
    "postalCode": "530022"
  }
}

#### Row-Major Versus Column-Major Format 

- CSV (comma-separated values) is row-major, which means consecutive elements in a row are stored next to each other in memory. 
- Parquet is column-major, which means consecutive elements in a column are stored next to each other. 

 Column-major formats like Parquet are better for accessing features, e.g., accessing the timestamps of all your examples.

##### Use Cases: 
 Row-major formats are better when you have to do a lot of writes, whereas column-major ones are better when you have to do a lot of column-based reads. 

