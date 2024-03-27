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


##### Pandas 
pandas is built around DataFrame, a concept inspired by R’s Data Frame, which is column-major. A DataFrame is a two-dimensional table with rows and columns. 


#### Text vs. Binary Format
CSV and JSON are text files, whereas Parquet files are binary files. Text files are files that are in plain text, which usually means they are human-readable. 

Binary files are the catchall that refers to all nontext files. As the name suggests, binary files are typically files that contain only 0s and 1s, and are meant to be read or used by programs that know how to interpret the raw bytes. 

#### AWS Recommendation: 

AWS recommends using the Parquet format because “the Parquet format is up to 2x faster to unload and consumes up to 6x less storage in Amazon S3, compared to text formats.”

#### query optimizer
A query optimizer examines all possible ways to execute a query and finds the fastest way to do so. 

Query optimization is one of the most challenging problems in database systems, and normalization means that data is spread out on multiple relations, which makes joining it together even harder. Even though developing a query optimizer is hard, the good news is that you generally only need one query optimizer and all your applications can leverage it.

#### What is a Declarative ML System? 

With a declarative ML system, users only need to declare the features’ schema and the task, and the system will figure out the best model to perform that task with the given features. 

Users won’t have to write code to construct, train, and tune models. 

Popular frameworks for declarative ML are Ludwig, developed at Uber, and H2O AutoML. 

##### Ludwig 
In Ludwig, users can specify the model structure—such as the number of fully connected layers and the number of hidden units—on top of the features’ schema and output. 

##### H2O AutoML 
In H2O AutoML, you don’t need to specify the model structure or hyperparameters. It experiments with multiple model architectures and picks out the best model given the features and the task.

#### Structured vs. Unstructured Data

Structured data follows a predefined data model, also known as a data schema.
Even though unstructured data doesn’t adhere to a schema, it might still contain intrinsic patterns that help you extract structures. 


A data warehouse serves as a storage facility for structured data, while a data lake is designated for the storage of unstructured data.