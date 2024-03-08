#### ML Systems Design  

1. ML is a data-driven system design 

#### ML objectives: 
the metrics they can measure about the performance of their ML models such as accuracy, F1 score, inference latency, etc.

#### System Design Considerations 

1. Reliability 
2. Scalability
3. Maintainability
4. Adaptability
5. Iterative Process

#### Model Training & Deployment Process 

1. Choose a metric to optimize. For example, you might want to optimize for impressions—the number of times an ad is shown.

2. Collect data and obtain labels.

3. Engineer features.

Train models.

During error analysis, you realize that errors are caused by the wrong labels, so you relabel the data.

Train the model again.

During error analysis, you realize that your model always predicts that an ad shouldn’t be shown, and the reason is because 99.99% of the data you have have NEGATIVE labels (ads that shouldn’t be shown). So you have to collect more data of ads that should be shown.

Train the model again.

The model performs well on your existing test data, which is by now two months old. However, it performs poorly on the data from yesterday. Your model is now stale, so you need to update it on more recent data.

Train the model again.

Deploy the model.

The model seems to be performing well, but then the businesspeople come knocking on your door asking why the revenue is decreasing. It turns out the ads are being shown, but few people click on them. So you want to change your model to optimize for ad click-through rate instead.