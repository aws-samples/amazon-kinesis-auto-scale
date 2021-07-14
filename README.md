## Build and optimize real-time stream processing pipeline with Amazon Kinesis Data Analytics for Apache Flink


In real-time stream processing, it becomes critical to collect, process, and analyze high-velocity real-time data to provide timely insights and react quickly to new information. Streaming data velocity could be unpredictable, and volume could spike based on user demand at a given time of day. Real-time analysis needs to handle the data spike, because any delay in processing streaming data can cause a significant impact on the desired outcome. The value of insights and actions reduces over time, whereas real-time analysis can substantially improve the effectiveness of the analytics application.

A widespread use case is fleet management for vehicles, especially in the autonomous car industry. It’s essential to collect, process, and analyze high-velocity traffic data and react in real time to control and reroute traffic. Real-time stream processing is crucial in many other use cases, such as manufacturing production lines, robotics automation, analyzing high-volume web and application logs, website clickstreams or database event streams, aggregating social media feeds, and tracking financial transactions.

[Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/) reduces the complexity of building, managing, and integrating [Apache Flink](https://flink.apache.org/) applications with other AWS services. [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/) takes care of everything required to run streaming applications continuously and scales automatically to match your incoming data volume and throughput in a serverless manner.

In this post, you learn the required concepts to implement robust, scalable, and flexible real-time streaming extract, transform, and load (ETL) pipelines with [Apache Flink](https://flink.apache.org/) and [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/). We demonstrate how to calibrate the Kinesis streaming analytics pipeline to achieve higher performance efficiency and better cost optimization with the right amount of [Kinesis Processing Units (KPUs)](https://docs.aws.amazon.com/kinesisanalytics/latest/java/how-scaling.html). Estimating the optimal number of KPUs to handle your streaming workload depends on several factors, including the type of stream processing involved. For instance, if you’re performing CPU-intensive statistical calculations, your application might need more CPU or memory. On the other hand, if your application is simply enriching records via external API calls as they flow through, you might be I/O bound. In [Part 1](https://aws.amazon.com/blogs/big-data/part2-build-and-optimize-real-time-stream-processing-pipeline-with-amazon-kinesis-data-analytics-for-apache-flink/) of this series, you learn various parameters such as Parallelism and ParallelismPerKPU for KPU calibration. In [Part 2](https://aws.amazon.com/blogs/big-data/part2-build-and-optimize-real-time-stream-processing-pipeline-with-amazon-kinesis-data-analytics-for-apache-flink/), you learn about applying auto scaling to add the right amount of KPUs based streaming data spike.

You will not only build a reliable, scalable, and highly available streaming application based on [Apache Flink](https://flink.apache.org/) and [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/), but also scale the different components while ingesting and analyzing thousands of events per second in near-real-time. Auto scale both [Amazon Kinesis Data Streams](https://aws.amazon.com/kinesis/data-streams/) and [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/) to accommodate the throughput of data stream. The scenario utilizes managed services without having to provision and configure underlying infrastructure.

For this post, we analyze the telemetry data of a taxi fleet in New York City in real time to optimize fleet operation using [Amazon Kinesis Data Analytics](https://aws.amazon.com/kinesis/data-analytics/) for Apache Flink. Kinesis Data Analytics helps process and analyze the data in real time to identify areas currently requesting high number of taxi rides. The derived insights are visualized on a dashboard for operational teams to inspect.

Read more in AWS Channel:

[Build and optimize a real-time stream processing pipeline with Amazon Kinesis Data Analytics for Apache Flink,Part 1](https://aws.amazon.com/blogs/big-data/part1-build-and-optimize-a-real-time-stream-processing-pipeline-with-amazon-kinesis-data-analytics-for-apache-flink/)

[Build and optimize real-time stream processing pipeline with Amazon Kinesis Data Analytics for Apache Flink, Part 2](https://aws.amazon.com/blogs/big-data/part2-build-and-optimize-real-time-stream-processing-pipeline-with-amazon-kinesis-data-analytics-for-apache-flink/)

## License Summary

This sample code is made available under a modified MIT license. See the LICENSE file.
